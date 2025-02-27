1. [Besu](index.html)
2. [Besu](Besu_22151173.html)
3. [Besu Roadmap &amp; Planning](22154278.html)

# Besu : Prague Planning

Created by Matt Nelson (Deactivated), last modified by gabriel.trintinalia@gmail.com on Apr 11, 2024

[Prague Meta Thread](https://ethereum-magicians.org/t/prague-electra-network-upgrade-meta-thread/16809)

EIP

Status

T-shirt Size

PR

Besu POC or Champion? 

Notes

Driver? EOF

[EIP-3540](https://eips.ethereum.org/EIPS/eip-3540)

[EIP-3670](https://eips.ethereum.org/EIPS/eip-3670)

[EIP-4200](https://eips.ethereum.org/EIPS/eip-4200)

[EIP-4750](https://eips.ethereum.org/EIPS/eip-4750)

CFIXL  
Danno Ferrin

Let's us ship faster and include more EIPs while giving Verkle more time to build and test.

Shippable state in Besu right now. Mega EOF branch is nearly up to date. Engineering work mostly worked out. 

Validation rules to be updated. Tests to be updated. 

Testnets need implementations from Vyper/Solidity → needs spec freeze. Need compiler support.

Timing → Q3 for testnet rollout 

Fork gated on time for fuzzing finding nothing. Running week(s) without issue. 

Driver? [Verkle Tries](https://eips.ethereum.org/EIPS/eip-6800)CFI

XXL

Karim Taam, Stefan Pingel, Gabriel FukushimaThe longer we delay the transition, the bigger the headache. Tons of value to users and devs, but more complexity. [EIP-2537](https://ethereum-magicians.org/t/eip-2537-bls12-precompile-discussion-thread/4187/48) - BLS PrecompileCFIS  
Justin FlorentineShip - updated to use Gnark? Signature aggregation for smart contract wallets[EIP-3068](https://eips.ethereum.org/EIPS/eip-3068) - BN-256 HashToCurveCFIS  
Justin FlorentineShip - updated to use Gnark? [EIP-3074](https://eips.ethereum.org/EIPS/eip-3074) - AUTH and AUTHCALLCFIM/L  
TBD

Should talk to wallet providers 

Danno - View unsafe as no revocation. No inclusion without it.

Justin - Hesitations from MM team and Consensys

[EIP-4444](https://eips.ethereum.org/EIPS/eip-4444) - History ExpiryCFIS/M  
Matt Nelson, Gary Schulte

Need to implement Portal proxy in Besu. Entirely optional! 

[https://notes.ethereum.org/@Kolby-ML/HJ-9D5aYp](https://notes.ethereum.org/@Kolby-ML/HJ-9D5aYp)

[EIP-6110](https://eips.ethereum.org/EIPS/eip-6110) - In-Protocol DepositsCFIS

5055

5295

5752

Fabio Di Fabio, Simon DudleyShip - reference implementation ready[EIP-6913](https://eips.ethereum.org/EIPS/eip-6913) - SETCODE OpCodeCFIS  
Daniel LehrnerLukewarm - small improvement on status quo  

[EIP-7002](https://ethereum-magicians.org/t/eip-7002-execution-layer-triggerable-exits/14195) - Execution layer triggerable exits

CFIM

6783, 6801,

6883

Lucas SaldanhaShould talk to some staking providers first

[EIP-7212](https://eips.ethereum.org/EIPS/eip-7212) - Precompile for Secp256R1 

CFIS  
Matt Nelson

[EIP-7251](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-7251.md) - Maximum Effective Balance Increase

CFINA  
\-CL only

[EIP-7377](https://eips.ethereum.org/EIPS/eip-7377) - EOA Upgrade / Migration Transactions

CFI??  
Gary Schulte

[EIP-7547](https://eips.ethereum.org/EIPS/eip-7547) - Inclusion lists 

CFIL or XL  
Justin Florentine

[EIP-7549](https://eips.ethereum.org/EIPS/eip-7549) - Move committee index outside Attestation

CFINA  
\-CL only 

# Verkle vs. EOF

## EOF First, Verkle Second (Pros &amp; Cons)

**Pros**

- Ready to ship this year. Verkle is not
- Necessary step to safely increase the code limit sizes
- EOF can be safely codesize uncapped 
  
  - EOF storage and verkle tree → Compatible by chunking into 32bytes and storing in sequence
  - Jumpdest validation is what causes issues
  - 31 byte in verkle may be overfitting to legacy EVM impl.
- Good for zk 
  
  - Dynamic jumps
  - Only have static jumps in EOF
  - Static register reallocation
  - Stack height validation requirements
  - Cross-compilation
  - No-code introspection in EOF
- More time to work on Verkle

**Cons**

- "Small feature fork scope" might not allow for EOF
- Consensus risk (long period of testing?)
- Layer 2 zk development will take time to adopt

## Verkle First, EOF second

**Pros**

- Shorter migration and less state to migrate !!!
- Less complexity of adding EOF EVM and adding risk
- Verkle functionality improvements (getting the stuff faster)
- More time for L2s to adopt EOF
  
  - Verkle not mandatory for immediate fork coverage

**Cons**

- More time to work on Verkle if we ship second

Document generated by Confluence on Nov 26, 2024 13:01

[Atlassian](http://www.atlassian.com/)
