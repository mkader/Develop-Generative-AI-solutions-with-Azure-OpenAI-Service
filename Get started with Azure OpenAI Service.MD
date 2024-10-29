## Access Azure OpenAI Service
  * Provision an Azure OpenAI resource in your Azure subscription.
  * Create an Azure OpenAI Service resource in the Azure portal.
  * Create an Azure OpenAI Service resource in Azure CLI.
	  1. az cognitiveservices account create -n MyOpenAIResource -g OAIResourceGroup -l eastus --kind OpenAI --sku s0 --subscription subscriptionID
  
## Use Azure AI Studio -  https://ai.azure.com/
  * Azure AI Studio provides access to model management, deployment, experimentation, customization, and learning resources.
	* Select your resource, deploy your first model through the Deployments page
	* ![](https://learn.microsoft.com/en-us/training/wwl-data-ai/get-started-openai/media/studio-deployment.png)

## Explore types of generative AI models
	* MS provides base models and the option to create customized base models. This module covers the currently available base models.
		1. GPT-4 models - Latest generation of generative pretrained (GPT) models that can generate NL and code completions based on NL prompts.
		1. GPT 3.5 models  - Generate NL and code completions based on NL prompts. 
			1. GPT-35-turbo models - Optimized for chat-based interactions and work well in most generative AI scenarios.
		1. Embeddings models - Convert text into numeric vectors, and are useful in language analytics scenarios such as comparing text sources for similarities.
		1. DALL-E models - Used to generate images based on NL prompts. 
	* ![Pricing Options](https://azure.microsoft.com/en-us/pricing/details/cognitive-services/openai-service/)

## Deploy generative AI models
	* Deploy a model to chat with or make API calls to receive responses to prompts.
	* Depoy using Azure AI Studio
	* ![](https://learn.microsoft.com/en-us/training/wwl-data-ai/get-started-openai/media/studio-deploy-model.png)
	* Deploy using Azure CLI
		1. az cognitiveservices account deployment create -g OAIResourceGroup -n MyOpenAIResource --deployment-name MyModel --model-name gpt-35-turbo --model-version "0301"  --model-format OpenAI --sku-name "Standard" --sku-capacity 1
	* ![Deploy using the REST API](https://learn.microsoft.com/en-us/azure/ai-services/openai/)
