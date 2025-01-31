# Azure AI Starter Kit

## Overview

### AI Building Blocks

This folder contains a collection of easy-to-consume samples and is designed to elucidate the fundamental building blocks of AI applications. Inside this folder, you'll find a set of Notebooks that provide explanations and hands-on demonstrations. The notebooks are grouped into building blocks explaining various aspects of the specific area.

Each notebook is crafted to be easily executed, making it accessible for both beginners and experienced practitioners.

### Folder Contents

Below is a detailed breakdown of each folder in this repository. Each section contains a descriptive overview and an architecture diagram explaining the interaction between various components and the flow of data.

| Section | Notebook  |  Description | Details |
| --------  | --------  |  ----------- | ------- |
| [01](./01_DemoEnvironment/)  | [Environment Setup](./docs/01_DemoEnvironment/01_Environment.ipynb)  |  Detailed instructions for deploying Azure Services like Azure OpenAI and Cognitive Search | Includes a `application.env` file within the [conf](./docs/01_DemoEnvironment/conf) folder containing essential configuration details |
| [02](./02_REST_API/)  | [Basic Chat](./docs/02_REST_API/01_BasicChat.ipynb)  |  Examples of HTTP calls to the deployed Chat Completion LLM (gpt-3.5-turbo)  | .NET code is used to perform HTTP calls, Another option could be utilizes the [REST Client extension](https://marketplace.visualstudio.com/items?itemName=humao.rest-client) for Visual Studio Code to execute the calls |
| [02](./02_REST_API/)  | [Other Models](./docs/02_REST_API/02_OtherModels.ipynb)  |  Examples of HTTP calls to various LLMs like Embedding, Whisper  | Also uses .NET to perform HTTP calls. |
| [02](./02_REST_API/)  | [JSON Mode](./docs/02_REST_API/03_JsonMode.ipynb)  |  Example of HTTP calls instructing the model to respond in valid JSON format  | Also uses .NET to perform HTTP calls. |
| [02](./02_REST_API/)  | [GPT-4 Vision](./docs/02_REST_API/04_MultiModalVision.ipynb)  |  Sample using text and image data as model input | gpt-4 vision is one of the first multi-modal models being able to process text and image data as input. Image data is provided as base64-encoded string
| [03](./03_SDK/)  | [Chat Completion](./docs/03_SDK/01_-_ChatCompletion.ipynb)  | C# sample code to interact with the ChatCompletion LLM using the `Azure.AI.OpenAI` NuGet package |
| [03](./03_SDK/)  | [Chat Completion Streaming](./docs/03_SDK/02_ChatCompletionStreaming.ipynb)  | Advanced C# sample code for streaming interactions with the ChatCompletion LLM |
| [03](./03_SDK/)  | [JSON Mode](./docs/03_SDK/03_JSONMode.ipynb)  | C# sample instructing the model to respond in valid JSON format |
| [03](./03_SDK/)  | [GPT-4 Vision](./docs/03_SDK/04_MultiModalVision.ipynb)  | C# sample using text and image data as model input | gpt-4 vision is one of the first multi-modal models being able to process text and image data as input. Image data is provided as URI
| [03](./03_SDK/)  | [Function Calling](./03_SDK/05_ChatTools.ipynb)  | C# sample demonstrating the use of tools | LLMs provide functionality to accept descriptions of available functions and suggest calling on of them if expected results are beneficial in fulfilling a chat completion request.
| [04](./04_Embeddings/)  | [Basic Embeddings](./docs/04_Embeddings/01_BasicEmbeddings.ipynb)  | C# code to create embeddings with the `Azure.AI.OpenAI` NuGet package | Embeddings are numerical text representations in a 1536-dimension vector |
| [04](./04_Embeddings/)  | [Cosine Similarity](./docs/04_Embeddings/02_CosineSimilarity.ipynb)  | C# examples using `MathNet.Numerics` to calculate the cosine distance between vectors | The closer the distance, the more similar the semantic meanings |
| [05](./05_VectorDB/)  | [Vector Database](./docs/05_VectorDB/01_CognitiveSearch.ipynb)  | C# code for using Azure Cognitive Search as a vector database | Involves storing and querying embeddings with a created Search Index |
| [06](./06_SemanticKernel/)  | [Semantic Function Inline](./docs/06_SemanticKernel/01_PlugIn_SemanticFunction_Inline.ipynb)  | Demonstrates inline definition of a Microsoft Semantic Kernel function |
| [06](./06_SemanticKernel/)  | [Semantic Function File](./docs/06_SemanticKernel/02_PlugIn_SemanticFunction_File.ipynb)  | Illustrates importing a Semantic Kernel function from an external file |
| [06](./06_SemanticKernel/)  | [Native Function](./docs/06_SemanticKernel/03_PlugIn_NativeFunction.ipynb)  | Example of importing a native C# function to the Semantic Kernel |
| [06](./06_SemanticKernel/)  | [Memory](./docs/06_SemanticKernel/04_Memory.ipynb)  | Explanation of the Semantic Kernel Memory concept and usage |
| [06](./06_SemanticKernel/)  | [Planner](./docs/06_SemanticKernel/05_Planner.ipynb)  | Overview of the Semantic Kernel planner which sequences function calls for a task |
| [06](./06_SemanticKernel/)  | [Logging](./docs/06_SemanticKernel/06_Logs.ipynb)  | How to utilize the default .NET logger with the Semantic Kernel |