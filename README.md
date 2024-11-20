# OpenAI o1 Model Analysis
An exploration of the OpenAI o1 model capabilities

## Overview
This repo shows a few examples for capability testing the OpenAI o1 model on Azure.  It was demonstrated during the Ignite 2024 BRK 110 session.  

## Setup
This project requires access to an Azure OpenAI resource to run the o1-preview model.  At the [model catalog](https://ai.azure.com/explore/models), you will need to deploy the **o1-preview** model.  Then update the .env file with the endpoint (and the deployment name if you change from the default).  You will also need to supply either an API key or use Microsoft Entra ID (formerly called Azure Active Directory) authentication.  We strongly recommend Microsoft Entra ID authentication for greater security.  To set it up, see https://learn.microsoft.com/azure/ai-services/openai/how-to/managed-identity.  Don't forget that you may need to run "az login" to refresh your credentials.  

Finally, use the following commands in a python environment (such as an Anaconda prompt window) to set up your environment.  This creates and activates an environment and installs the required packages.  For subsequent runs after the initial install, you will only need to activate the environment and then run the python script.  

### First run
```
conda create --name o1Analysis -y
conda activate o1Analysis

pip install -r requirements.txt
jupyter notebook o1Analysis.ipynb
```

### Subsequent runs
```
conda activate o1Analysis
jupyter notebook o1Analysis.ipynb
```