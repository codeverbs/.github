
# Welcome to CodeVerb

CodeVerb took the initiative to revolutionize the development like never before. CodeVerb generates Python Language Code from English Language Text.


![new-logo-transparent](https://user-images.githubusercontent.com/75477054/211206431-6ac57b57-39dd-47be-acd3-65f6893ab026.png)



# CodeVerb Architecture

There are three repositories, each with their own purpose.

1. **transformer-pytorch**: Contains the code for transformer based model. The model is developed using PyTorch.

2. **web-portal**: Contains the code for Frontend Portal. The portal is made using ReactJS, TailwindCSS.

3. **model-api**: Contains the code for Backend Server of the portal. The server is made using Flask.


# Dataset Collection

> Scraped Dataset from GitHub Public Repositories, StackExchange, GeeksForGeeks

> 100 of Millions of Python Code Lines

> Approx. 7.2 million files of Python are scraped

> Assuming 5 files take 1 second to scrape 7.2million/432000 secs ~ 15 Days 

> Parallel Processing helped us scrape this dataset in just ~ 7 Days


# State Diagram

![image](https://user-images.githubusercontent.com/75477054/211206894-f8cff537-53a4-4a1d-8796-6a395ed27b78.png)


# Project Workflow

![image](https://user-images.githubusercontent.com/75477054/211206954-ee6a99eb-2974-4e13-bdb0-5dffab517f8d.png)


# Iteration 01

## Data Scraping & Collection Flow

We are scraping our dataset from StackExchange (StackOverflow, CodeReview, etc.) and GitHub. To achieve this, we have made our custom scrappers from scratch for the both platforms. 
For GitHub, as the dataset was massive, we had to use a cluster setup to perform multithreading to execute the processes in parallel in order to achieve faster and efficient execution. 
We stored the dataset in separate files as it is more convenient to transfer over the network as well as load while training or viewing the dataset.

![image](https://user-images.githubusercontent.com/75477054/211207033-64780063-e11f-4b30-a9f8-14dffa69de32.png)


# Iteration 02

CodeVerb uses state of the art deep learning model to achieve its target of code generation from natural language input. In 2017, research named “Attention is all you Need” was published which helped pave the way for the advent of large language models making breakthroughs in the field of Natural Language Processing (NLP). Our system was designed using the idea behind that research as its basis. 

## Model Architecture

CodeVerb uses Transformer based model to achieve its goal. The Encode-Decoder model serves the purpose really well according the use case.

![image](https://user-images.githubusercontent.com/75477054/211207153-40a2e0dd-b143-4abc-8491-fd5944a7a8a8.png)


## Web Portal

### Landing Page

![image](https://user-images.githubusercontent.com/75477054/211207269-3ab03624-5c27-49ff-bf24-fca830267bdd.png)



### Playground Page

![image](https://user-images.githubusercontent.com/75477054/211207252-0ccc34a2-9ea2-4624-9370-cd4e82385c5e.png)


# Iteration 03

> Set up Distributed Training Environment

> Neural Network Based Large Language Model Training [Currently Ongoing]

## Training Environment 

1. Implemented PyTorch Data Distributed Pipeline
2. Used Nvidia Nickel (NCCL) backend to communicate with distributed machine setup
3. Total Machines = 3
4. Total GPUs = 3 (Nvidia 3060)

## Training Time 
> EPOCHS: 50000

> Single Epoch Training Time: ~ 0.7 secs

> Total Training Time: 0.7*EPOCHS = ~ 24 days

> Current Model Epochs: ~ 5000

> Training Time: 0.7*5000 = ~ 3 Days








