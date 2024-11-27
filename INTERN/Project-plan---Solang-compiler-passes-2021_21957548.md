1. [Hyperledger Mentorship Program](index.html)
2. [Hyperledger Mentorship Program](Hyperledger-Mentorship-Program_21954571.html)
3. [Mentorship Projects](Mentorship-Projects_21954604.html)
4. [2021 Projects](2021-Projects_21964295.html)
5. [Implement two compiler passes for the Solang Solidity Compiler](Implement-two-compiler-passes-for-the-Solang-Solidity-Compiler_21956641.html)

# Hyperledger Mentorship Program : Project plan - Solang compiler passes 2021

Created by Lucas Steuernagel, last modified by salaheldin\_sameh on Jun 18, 2022

## **Abstract**

Solang is a compiler for the Solidity language, targeting Substrate, Solana, Sawtooth and ewasm. It is written in Rust and is currently under development. The purpose of this project is to implement two compiler passes for improving the LLVM IR Solang generates. We can split the work into three main milestones: unused variable elimination, undefined variable warning and common subexpression elimination.

## **Mentor and Mentee**

Mentor: Sean Young

Timezone: BST

Rocketchat (hyperledger): seanyoung

Mentee: Lucas Steuernagel

Timezone: BRT

Fork of official repository for this project: [https://github.com/LucasSte/solang](https://github.com/LucasSte/solang)

## **Deliverables**

- Warnings for unused variables
- Warnings for undefined variables
- Unused variable elimination
- Common subexpression elimination

## **Milestones**

### **Evaluation 1:**

- Leverage the symbol table to detect unused variables.
- Generate warnings for them.

### **Evaluation 2:**

- Eliminate the detected unused variables when generating the intermediate representation.
- Utilize the reaching definitions implementation of Solang to detect undefined variables.

### **Evaluation 3:**

- Generate complete warnings for the detected issue.
- Implement an available expression analysis algorithm

### **Evaluation 4:**

- Eliminate common subexpression when generating the intermediate representation.
- Write a complete documentation for the project

## **Timeline**

**Week #**

**Week**

**Activity**

**Status**

0

May 24 - May 30

First contact with mentor and discussion of solutions.

✅

1-2

May 31 - June 13

Modify the symbol table and the parsing to detect unused variables.

✅

3-4

June 14 - June 27

Generate warnings on the code.✅

5-6

June 28 - July 11

Evaluation 1

Provide tests and documentation.

✅

7-8

July 12 - July 25

Eliminate unused variables from generated code.

✅

9-10

July 26 - August 8

Provide tests and documentation.

✅

11-12

August 9 - August 22

Evaluation 2

Utilize the reaching definitions to detect undefined variables.

✅

13-14

August 23 - September 5

Reutilize the solutions for warnings from the last problem to generate warnings.

✅

15-16

September 6 - September 19

Provide tests and documentation.

✅

17-18

September 20 - October 3

Evaluation 3

Implement available expressions analysis algorithm (part 1)

✅

19-20

October 4 - October 17

Implement available expressions analysis algorithm (part 2)

✅

21-22

October 18 - October 31

Eliminate common subexpressions.

✅

23-24

November 1 - November 14

Evaluation 4

Provide tests and documentation.

✅

## **Methodology**

After I start coding each milestone, my mentor and I will have a planning session to define the best way to tackle the challenges. Then, I will execute the planning and schedule a review session with my mentor. If everything is working and we agree upon the implemented solution, I am going to write tests and update the Solang documentation website with the most recent features. In addition to those meetings, we are doing weekly calls to review the progress of the project.

Following this methodology, I intend to maintain the transparency of my work and keep the Solang users updated with the most recent features and documentation.

## **Documentation**

### **Unused variable detection**

A variable in solidity can have three scopes: a global scope, a contract scope (state variables) and a function scope. Global variables can only be constant variables. State variables reside inside a contract. After solang parses a solidity file and builds the AST (abstract syntax tree), all data is saved inside the *struct Namespace*, which contains a vector of contracts. Inside *Contracts* there is a vector of variables (struct *Variable*) that saves state variables. Global constant variables reside in a vector of constants inside *Namespace* and local variables are saved in a each function's symbol table.

We added a boolean variable *read* inside *struct variable* to signal that a variable has been used in the code. At first, *used* is initialized to false. Once we parse an expression that uses the variable, we set it to true. In addition, we included a boolean variable *assigned* to signal that a variable has been assigned. Once we parse an assignment expression, we set this variable to true. The aforementioned modification will allow us to emit warnings for unused variables and unassigned ones.

For example, in the following contract, we should expect three warnings. The variables *a* and *b* have been assigned, but never read and variable *c* has never been read nor assigned.

**Example contract 1**

```
contract Test {
    function get() public pure {
        uint32 a = 1;
        uint32 b;
        b = 1;
        uint32 c;

        uint32 d;
        d = 1;
        uint32 e;
        e = d*5;
        d = e/5;
   }
}
```

When running solidity, we got the following warnings as expected:

**Warnings for Example 1**

```
test.sol:4:16-17: warning: local variable 'a' has been assigned, but never read
test.sol:5:16-17: warning: local variable 'b' has been assigned, but never read
test.sol:7:16-17: warning: local variable 'c' has never been read nor assigned
```

Likewise, in the next contract, we expect to see warnings because local variable *b32* has never been assigned a values, but has been read and storage variable *byteArr* has been assigned, but never read.

**Example contract 2**

```
contract Test {
    bytes byteArr;
    bytes32 baRR;

    function get() public  {
        string memory s = "Test";
        byteArr = bytes(s);
        uint16 a = 1;
        uint8 b;
        b = uint8(a);

        uint256 c;
        c = b;
        bytes32 b32;
        bytes memory char = bytes(bytes32(uint(a) * 2 ** (8 * b)));
        baRR = bytes32(c);
        bytes32 cdr = bytes32(char);
        assert(b32 == baRR);
        if(b32 != cdr) {

        }
    }
}
```

After running solidity, we got the following warnings:

**Warnings for Example 2**

```
test.sol:15:17-20: warning: local variable 'b32' has never been assigned a value, but has been read
test.sol:3:5-18: warning: storage variable 'byteArr' has been assigned, but never read
```

### Unused variable elimination

Before creating the Control Flow Graph (CFG), Solang generates a variable table from the AST. During that phase, we can raise a warning when we see an unused variable and leave it out of the CFG. Using the *id* variable inside the *Variable* struct, we can backtrack the position where the variable appeared in the file and print a meaningful warning, containing the file name and line position. If the variable has only been assigned within a function, but has never been read, in addition to eliminating the variable declaration, we remove all the assignments from the intermediate representation.

### **Warning for undefined variables**

During the codegen phase,  we use the reaching definitions implementation to check if an undefined definition reaches the variable we are parsing. If so, we will raise an error. Using the *id* variable inside the *Variable* struct, we backtrack the variable’s location in the source file and emit a complete warning. All warnings will be saved into the *diagnostic* vector, which is a vector of *struct Diagnostics*, containing the error type, error message and error position.

### **Common subexpression elimination**

We perform common subexpression elimination using two passes over the Control Flow Graph (CFG). During the first on, we build a graph to track existing expressions and detect repeated ones. During the second pass, we replace the repeated expressions by a temporary variable, which assumes the value of the expression. The example below contains multiple repeated expressions:

**Common subexpression elimination**

```
contract {

    function csePass(int a, int b) {
        int x = a*b-5;
        if (x > 0) {
            x = a*b-19;
        } else {
            x = a*b*a;
        }

        return x+a*b;
    }
}
```

The expression \`a\*b\` is repeated throughout the code and will be saved to a temporary variable, which will be placed wherever there is a \`a\*b\` expression.

Document generated by Confluence on Nov 26, 2024 14:57

[Atlassian](http://www.atlassian.com/)
