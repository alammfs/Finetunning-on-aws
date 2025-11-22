https://docs.google.com/document/d/1NfLe1jQUGpeX0qOQnoggl5kZroKoM9m5YLOAyhL-huA/edit?tab=t.0
project link -  https://github.com/sunnysavita10/Finetuning-on-aws
Udemy free course - https://www.udemy.com/course/complete-mcp-bootcamp-build-next-gen-ai-agents-with-mcp/?couponCode=FREEMCP

Serverless finetunning using sagemaker
then access app lambda and API gateway
for this project we will use
1. I am roles
2. s3 buckets
3. sagemaker instance
4. training script for finetunning
5. Model train and deploy and get endpoint url to interact with model
6. create dynamo db to keep request log and etc
7. Lambda function
8. API gateway configuration.
9. Cloud watch
10 end to end testing vai UI
11 Added a model into model registry
Sunny sir github repo - https://github.com/sunnysavita10?tab=projects
Sunny sir youtube channel - https://www.youtube.com/@sunnysavita10/videos
Krish naik youtube channel - https://www.youtube.com/@krishnaik06/videos
In this project we gonna use complete AWS
Pretraining - can be done using self supervised technique 
second supervised fine tunning - can be done by using instruction fine tunning techqiue, through which model is able to understand instruction and generate output
Preference based learning - Collected the user feedback and retrained model.
instructions to every LLM is given in terms of prompt so prompt engg plays an important role.

To create a domain specific LLM you have 2 ways
1 Create your own LLM from scratch with domain data which is very time consuming and costly
22 Use any pretrain/existing model, finetune it it on your domain dataset
so that model can understand your business queries/domain specific queries.
on top of that finetune model you can create RAG or agentic flow to expose BE logic through API.
Question - why we do finetune a model.
Answer if we wants to teach model our domain specific knowledge then we need to finetune it. it is like that we have to train our model again.
steps to finetune a model.
step 1 - take a pretrain model/base model and perform supervised fine tunning or can take any model which is already gone through instructions tunning, preference alignment training
instruction tunning - prepare your data in such a way that in one column you have input and in other column you have output
you can train your model on non instruction data, (non instruction data means plain text which is available in docs, pdfs, texts)
LLMS may have many params size of params can be billion or trillion, we can not train all the parameters- retrainnning of all params are impossible we do partial traiinng
partial traiining means we take subset of params there is a very famous technique PEFT (parameter efficient fine technique. examples are LORA, DORA, Adapter)

As a gen AI developer you need to focus on
instructions tunning or non instruction tunning
and PEFT technique - LORA, DORA
Preference based techniques - DPO

To implement all these we required a frameworks - most famous is huggingface, LLAma factory, Axolotal
main aim of finetunning is to teach our model domain specific knowledge.
Finetune vs RAG
Finetunning - retrain the model on our own data
RAG - Give the context and use the model, in RAG we are not doing any training
Bedrock - already given a trained model similar to Open AI API - similar to Grok API
AWS hosted the model on his server 
We can use this model only throghh api for RAG and agent and not for finetunning
if u have data concern GPT said
I hosted model the data will be available on my infra use this through bedrock and give you that particular model as a service and use it through bedrock - AZure AI foundry is also similar to amazon bedrock
RAG we also do it on top of data - as complex data we have like image data, table data, complex table called complex RAG.
in RAG need to focus on 2 things parsing and retrival and prompt
SageMaker is a platform using which we used huggingface framework to finetune a model
finetunning_of_gptModel ipynb file - https://drive.google.com/file/d/1fyKk6v7pfYJGxzmFwgpadYiZ7GITSUha/view



Service that we use in this project
S3 - to keep data and others
Sage Maker/colab
Lambda
API Gateway
Dynamo DB (optional)
cloud watch
Hugging face is a framework provide tools/modules to finetune models (in backend they write code using pytorch and tensorflow) just needs to call high legel api.
infrencing means - prediction
model has 2 phase
train and infrencing
TinyLlama for small model for learning purpose
MetaLlama - big model
misteral repo

tokenizer - data is converted into words, each word is assign a number called token that pass to transformer 
AWS sagemkaer does not allow to load a model from notebook file ipynb
Laura config
we load model using LORA - Model is transformer enabled model
params are nothing but they are weight and baises value
Behind architecture of every LLM with one example say
what is capital of USA
Autoregresive training means next token prediction
Service - Service quota
in left side AWS services
search sageMaker
and ask increase the quota
google adk instead of langraph

Causal_LM - predict next token



I AM user/I am Role
LLM is build on transformer architecture
encoder/decoer architecture
next token prediction technique

finetune a model is very costly
in most cases like 95% we use pre train model and use the reasoning capability of model and build the RAG on top of it.
we will do the instruction fine tunning



