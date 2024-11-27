1. [Hyperledger Labs](index.html)
2. [Hyperledger Labs Home](Hyperledger-Labs-Home_20283400.html)
3. [AI FAQ](AI-FAQ_20290949.html)
4. [2024 Mentorship Program](2024-Mentorship-Program_20291094.html)

# Hyperledger Labs : Peter Atef

Created by Peter Atef, last modified on May 22, 2024

**Project Name: AI-faq**

**Contributor Name: Peter Atef**

Hello there, I’m Peter Atef, a senior student in the Computer Department, at the faculty of Engineering, at Cairo University.

I expect to graduate in fall 2024. My current GPA is 3.7 out of 4. Here is my website where you can find all the details about my career: skills, courses, past experiences…etc: [Peter Atef (engpeteratef.github.io)](https://engpeteratef.github.io/)

Contacts:

- Email: [peter.atef2000@gmail.com](mailto:peter.atef2000@gmail.com)
- Phone number: +201212773495

I am super interested in this program because I know how much experience anyone in the tech industry can gain from participating in open-source projects, regardless of the technical experience, a lot of soft skills are gained and developed which are so important for a senior student who is graduating in a couple of months. Also, once I learned about the program and AI-FAQ, I got very excited because I was very interested in the field of NLP and building apps that provide the user with the power of AI.

Due to the projects I participated in, previously, I had experience in almost all the technologies recommended to build this project.

For example, I had a three-month internship at VNCR where I was working on a Blog Writer website which was a website that takes input from the user and then creates a prompt that will be given to LLM to generate the blog for the user based on the user preferences like topic, number of words, and sources to collect the information from.

# Project Summary and Proposed Plan

We can break down the problem into multiple stages:

1. Load the data
   
   1. Load the data from websites, GitHub Repo, or maybe search for answers on Google and use the results as verbs.
2. Data processing
   
   1. Text tokenization
3. Create embeddings
   
   1. Using any embedding algorithm provided by HuggingFace or OpenAI, however, choosing the algorithm is critical in terms of time because the process of creating embeddings takes a lot of time.
4. Create a vector database
   
   1. Using a cloud vector database to keep the history of the chat and also keep any data we got from the previous search process. We may use Qdrant to achieve this goal or deploy any vector database like chromaDB, Pgvector, or Faiss.
   2. I have a great experience with vector databases because I've participated in implementing a vector database indexer project so I know they work and the algorithms used to implement them.
5. LLM
   
   1. I want to talk about this point specifically because it’s critical, we want to use LLM cheap, efficient, and fast.
   2. There are multiple greater models on Huggingface with an Apache 2.0 License and they are created for question-answering tasks like Intel/dynamic\_tinybert, distilbert/distilbert-base-cased-distilled-squad, FlagAlpha/Llama2-Chinese-13b-Chat,
6. Create back-end APIs
   
   1. I recommend using Python frameworks like Django to build our back-end and endpoints because the part that deals with LLM and gets its response will be implemented in Python, and to make the interface between them easy it’s a good idea to build the back-end using Python.
7. Create front-end
   
   1. There is no doubt that React is a great front-end framework in terms of performance.
   2. I think the website has the following features:
      
      1. Create an account: Sign in/ Sign-up
      2. Chat with LLM
      3. Show search history
      4. Clear History
      5. Continue as a guest (without memory)
8. Integrate the front end with the back end
9. Deploy the website

# Block Diagram:

![](attachments/20283453/20294613.jpg?height=400)

## Data workflow:

1. Loading data from documentation, websites, GitHub,...etc
2. Processing the data using Langchain tools like tokenization and splitting.
3. Send the documents to create embeddings for the collected data
4. Return to Langchain vectors of fixed size that represent the documents
5. Send the embeddings to Qdrant to be stored

## Chat workflow

01. The user enters the query and the website sends an API call to the server
02. The server calls Langchain functions on the user's query and the chat history
03. Converting the user query and chat history to embeddings using HuggingFace.
04. Getting the vectorized data from hugging face
05. Making API calls to send the embeddings to Qdrant.
06. Get the result of querying Qdrant to get the top-k relevant documents
07. Construct a well-defined prompt that contains the relevant data to LLM.
08. Get the generated response from the LLM.
09. Further processing on the generated output to be in a user-friendly format and have the result on the back-end side.
10. Returning the response to the client side.

# Suggestions

- Instead of using React to build the website, we can use Flutter to take our service to the next level to have a single code base and our application will work on mobile phones (android or IOS), websites, and desktops.
- Fine-tuning a pre-trained model.

### Fine-tuning process:

1. Initialize with a pre-trained model.
2. Prepare a labeled dataset for the question-answering task
3. Train the model using this dataset, adjusting all layers.
4. Try different learning rates to avoid catastrophic forgetting and also to avoid over-fitting.

### Types of Fine-tuning:

1. Standard Fine-tuning as I mentioned its steps previously.
2. Feature-Based Fine-Tuning: This involves using a pre-trained model as a feature extractor and then using a smaller model as a classifier. The advantage of this approach is  it's computationally efficient and less prone to overfitting but also it might be weak in classification.
3. There are other types of fine-tuning but they may not be suitable for your project

# Learning Progress

1. Natural Language Processing (NLP) course.
2. Studying more about the Langchain framework
3. Study React.js and Nest.js
4. Learn more about Blockchain and
5. Learn more about RAG and fine-tuning

## Attachments:

![](images/icons/bullet_blue.gif) [Untitled.jpg](attachments/20283453/20294613.jpg) (image/jpeg)

Document generated by Confluence on Nov 26, 2024 15:08

[Atlassian](http://www.atlassian.com/)
