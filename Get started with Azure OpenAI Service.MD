# Access Azure OpenAI Service
  <ui><li>Provision an Azure OpenAI resource in your Azure subscription.</li>
  <li>Create an Azure OpenAI Service resource in the Azure portal</li>
  <li>Create an Azure OpenAI Service resource in Azure CLI</li>
    az cognitiveservices account create \
        -n MyOpenAIResource \
        -g OAIResourceGroup \
        -l eastus \
        --kind OpenAI \
        --sku s0 \
        --subscription subscriptionID

# Use Azure AI Studio
