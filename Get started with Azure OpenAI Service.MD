## Access Azure OpenAI Service
  * Provision an Azure OpenAI resource in your Azure subscription.
  * Create an Azure OpenAI Service resource in the Azure portal.
  * Create an Azure OpenAI Service resource in Azure CLI.
	  1. az cognitiveservices account create -n MyOpenAIResource -g OAIResourceGroup -l eastus --kind OpenAI --sku s0 --subscription subscriptionID
  
## Use Azure AI Studio -  https://ai.azure.com/
  * Azure AI Studio provides access to model management, deployment, experimentation, customization, and learning resources.
	* Select your resource, deploy your first model through the Deployments page
	* <img src="https://learn.microsoft.com/en-us/training/wwl-data-ai/get-started-openai/media/studio-deployment.png" width=500 height=500>

## Explore types of generative AI models
	* MS provides base models and the option to create customized base models. This module covers the currently available base models.
		1. GPT-4 models - Latest generation of generative pretrained (GPT) models that can generate NL and code completions based on NL prompts.
		1. GPT 3.5 models  - Generate NL and code completions based on NL prompts. 
			1. GPT-35-turbo models - Optimized for chat-based interactions and work well in most generative AI scenarios.
		1. Embeddings models - Convert text into numeric vectors, and are useful in language analytics scenarios such as comparing text sources for similarities.
		1. DALL-E models - Used to generate images based on NL prompts. 
	* Pricing Options - https://azure.microsoft.com/en-us/pricing/details/cognitive-services/openai-service/

## Deploy generative AI models
	* Deploy a model to chat with or make API calls to receive responses to prompts.
	* Depoy using Azure AI Studio
	* <img src="https://learn.microsoft.com/en-us/training/wwl-data-ai/get-started-openai/media/studio-deploy-model.png" width=500 height=500>
	* Deploy using Azure CLI
		1. az cognitiveservices account deployment create -g OAIResourceGroup -n MyOpenAIResource --deployment-name MyModel --model-name gpt-35-turbo --model-version "0301"  --model-format OpenAI --sku-name "Standard" --sku-capacity 1
	* Deploy using the REST API - https://learn.microsoft.com/en-us/azure/ai-services/openai/

## Use prompts to get completions from models
  * Test, A prompt is the text portion of a request that is sent to the deployed model's completions endpoint. 
  * Responses are referred to as completions, which can come in form of text, code, or other formats.
  * Prompt types, Prompts can be grouped into types of requests based on task.
  
| Task type | Prompt example | Completion example |
|-- |-- |--|  
| Classifying content | Tweet: I enjoyed the trip. Sentiment: | Positive |
| Generating new content | List ways of traveling | 1. Bike 2. Car ... |
| Holding a conversation | A friendly AI assistant | <a href="https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/completions#conversation?portal=true">See examples</a> |
| Transformation (translation and symbol conversion) English: Hello French: | bonjour |
| Summarizing content | Provide a summary of the content {text} | The content shares methods of machine learning. |
| Picking up where you left off | One way to grow tomatoes | is to plant seeds. |
| Giving factual responses | How many moons does Earth have? | One |

Completion quality
Several factors affect the quality of completions you'll get from a generative AI solution.

The way a prompt is engineered. Learn more about prompt engineering here.
The model parameters (covered next)
The data the model is trained on, which can be adapted through model fine-tuning with customization
You have more control over the completions returned by training a custom model than through prompt engineering and parameter adjustment.

Making calls
You can start making calls to your deployed model via the REST API, Python, C#, or from the Studio. If your deployed model has a GPT-3.5 or GPT-4 model base, use the Chat completions documentation, which has different request endpoints and variables required than for other base models.
