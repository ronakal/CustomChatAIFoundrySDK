1: Create an Azure AI Hub resource and project

<img width="914" height="462" alt="image" src="https://github.com/user-attachments/assets/194a1eac-ad37-4c83-87de-ed82188e4674" />
<img width="935" height="505" alt="image" src="https://github.com/user-attachments/assets/735f7abf-f809-4c1c-a061-2f4e4f7a31cf" />
<img width="935" height="583" alt="image" src="https://github.com/user-attachments/assets/8ba8349d-ff3e-42aa-8245-d883d94623a5" />
<img width="924" height="573" alt="image" src="https://github.com/user-attachments/assets/e39c3ac5-9a2c-4cad-b885-5d8b8e8a18c2" />
<img width="866" height="645" alt="image" src="https://github.com/user-attachments/assets/9956d5d5-8bfe-4cdc-a81e-ebb047531fac" />
<img width="758" height="602" alt="image" src="https://github.com/user-attachments/assets/69673e31-087d-4b97-99c5-f87b6b0d78d1" />
<img width="932" height="549" alt="image" src="https://github.com/user-attachments/assets/20f654fe-78e4-4a17-a7e1-a13fa9c40654" />
<img width="1220" height="638" alt="image" src="https://github.com/user-attachments/assets/222dc0ac-7bfc-48f7-89dc-011f6b92b939" />
<img width="958" height="522" alt="image" src="https://github.com/user-attachments/assets/d7328629-1150-47c8-a464-164d66bbe9e6" />
<img width="914" height="562" alt="image" src="https://github.com/user-attachments/assets/bc9c3924-5223-49c4-ab5a-c779194bc6c4" />
<img width="934" height="644" alt="image" src="https://github.com/user-attachments/assets/762c990b-4124-42b1-b16a-faf7bd89c194" />
<img width="942" height="576" alt="image" src="https://github.com/user-attachments/assets/1745a046-3269-4a37-8d34-a10f79d1113e" />
<img width="918" height="619" alt="image" src="https://github.com/user-attachments/assets/21f09a01-7404-4d91-a8b9-340f584fb975" />
<img width="827" height="650" alt="image" src="https://github.com/user-attachments/assets/493f10e3-6c94-42fc-b980-aef9925bffc3" />

 2: Deploy models
 
<img width="661" height="568" alt="image" src="https://github.com/user-attachments/assets/b4dab586-ccfe-4ff4-9de1-4d66ea0a79a6" />
<img width="1033" height="640" alt="image" src="https://github.com/user-attachments/assets/0f9185c6-e3ee-42e3-b3a0-31679e0c691f" />

After you deploy the gpt-4o-mini, deploy the text-embedding-ada-002 model. Select the Deployment Type as Standard.
<img width="957" height="453" alt="image" src="https://github.com/user-attachments/assets/b4d4fe11-9734-4e6b-80d2-e1e078fd6b5a" />

3: Create an Azure AI Search service

<img width="952" height="420" alt="image" src="https://github.com/user-attachments/assets/ed0aa9aa-e62c-4a98-8c92-fc7498ce0362" />
<img width="534" height="497" alt="image" src="https://github.com/user-attachments/assets/61e32397-47e7-4c47-b4c4-4ac1caec9c14" />
<img width="811" height="564" alt="image" src="https://github.com/user-attachments/assets/2b0b52c7-82c5-4c5e-a82a-317d2f2b6ce0" />
<img width="994" height="577" alt="image" src="https://github.com/user-attachments/assets/30345ca3-b04d-4a47-ad00-749810db155b" />

4: Connect the Azure AI Search to your project

<img width="761" height="543" alt="image" src="https://github.com/user-attachments/assets/2df42d7b-35cf-4b75-98bb-e851e259dc6c" />
<img width="788" height="469" alt="image" src="https://github.com/user-attachments/assets/17a67f10-a867-4698-85b9-f7d7619a3929" />
<img width="794" height="475" alt="image" src="https://github.com/user-attachments/assets/e41457e6-4960-4a2f-8393-39c65d4d75bc" />
<img width="954" height="620" alt="image" src="https://github.com/user-attachments/assets/1b1fae77-a649-41b9-a790-4a4a386c2128" />
<img width="707" height="562" alt="image" src="https://github.com/user-attachments/assets/266c86f7-5829-4a0c-bc21-d0b9416993ec" />

5: Install the Azure CLI and sign in

1-Search for PowerShell from the Windows search bar and open it in the Administrator mode. Accept if prompted for the launch to continue.

2-
$progressPreference = 'silentlyContinue'
Write-Host "Installing WinGet PowerShell module from PSGallery..."
Install-PackageProvider -Name NuGet -Force | Out-Null
Install-Module -Name Microsoft.WinGet.Client -Force -Repository PSGallery | Out-Null
Write-Host "Using Repair-WinGetPackageManager cmdlet to bootstrap WinGet..."
Repair-WinGetPackageManager
Write-Host "Done."
3-Install the Azure CLI from your terminal using the following command: (I downloaded the msi because command line didnot work)
winget install -e --id Microsoft.AzureCLI
4-adfter install do az login
<img width="541" height="515" alt="image" src="https://github.com/user-attachments/assets/c4f167ba-71fc-42cf-a197-87097b440da0" />

6: Create a new Python environment

<img width="267" height="524" alt="image" src="https://github.com/user-attachments/assets/94b557b8-decc-4be7-8c6d-035d42e4b68f" />
<img width="259" height="615" alt="image" src="https://github.com/user-attachments/assets/6d96bf58-3ec2-4662-b2fd-e1b1277f8c3c" />
Open VS Code. Select File -> Open Folder and select RAGproject folder that we created in the previous steps (from C:\Users\Admin).

7: Install packages

<img width="259" height="610" alt="image" src="https://github.com/user-attachments/assets/a85c31f5-0997-435a-828c-aeef3d04358b" />
<img width="269" height="787" alt="image" src="https://github.com/user-attachments/assets/e3a9486e-9f53-42ae-b48a-3e80753d5173" />
<img width="264" height="566" alt="image" src="https://github.com/user-attachments/assets/48252d26-db11-42b1-8d06-4d4df8437210" />

8: Create helper script
1-create config.py under src
2-add .env under src with the code checked in

Build a custom knowledge retrieval (RAG) app with the Azure AI Foundry SDK

1: Create example data for your chat app
From your VS Code set up that is open, create a folder named assets under the src folder. and create products.csv
In VS code, create a file named create_search_index.py in your src folder.
Right click on the create_search_index.py and select Open in integrated terminal option.

From your terminal, log in to your Azure login credential and follow instructions for authenticating your account:
az login
<img width="452" height="516" alt="image" src="https://github.com/user-attachments/assets/8c66bee6-ea2a-453d-980f-6ecff1a8b164" />

Run the code to build your index locally and register it to the cloud project:
python create_search_index.py

Once the script is run, you can view your newly created index in from Azure portal.

Navigate to the assigned Resource Group -> Your search service created(aisearchLabinstanceID) -> Search management -> Indexes.
<img width="1057" height="632" alt="image" src="https://github.com/user-attachments/assets/4f0df77a-e362-48cd-9211-63f8de8f5d4a" />

2: Create script to get product documents:

When the chat gets a request, it searches through your data to find relevant information. This script uses the Azure AI SDK to query the search index for documents that match a user's question. It then returns the documents to the chat app. From VS Code, create a file named get_product_documents.py in the src folder.

3: Create prompt template for intent mapping:

The get_product_documents.py script uses a prompt template to convert the conversation to a search query. The template instructs how to extract the user's intent from the conversation. Before you run the script, create the prompt template. Create a file named intent_mapping.prompty under your assets folder

4: Test the product document retrieval script:
Now that you have both the script and template, run the script to test out what documents the search index returns from a query. From the terminal window run,

python get_product_documents.py --query "I need a new tent for 4 people, what would you recommend?"

5: Develop custom knowledge retrieval (RAG) code:
Next you create custom code to add retrieval augmented generation (RAG) capabilities to a basic chat application.

Create a chat script with RAG capabilities

In your src folder, create a new file called chat_with_products.py. This script retrieves product documents and generates a response to a user's question

6: Create a grounded chat prompt template
The chat_with_products.py script calls a prompt template to generate a response to the user's question. The template instructs how to generate a response based on the user's question and the retrieved documents. Create this template now. In your assets folder, add the file grounded_chat.prompty

7: Run the chat script with RAG capabilities
Now that you have both the script and the template, run the script to test your chat app with RAG capabilities:

python chat_with_products.py --query "I need a new tent for 4 people, what would you recommend?"

8: Add telemetry logging
From the Azure portal, select Subscriptions, select your subscription and then select Resource providers under Settings from the left navigation pane.

Search for and select Microsoft.OperationalInsights and click on the three dots for this resource provider and select Register. also resiter Microsoft.Search,Microsoft.Web,Microsoft.ManagedIdentity

From your Project in the Azure AI Foundry, select Tracing under Access and improve from the left pane. Select Create New.

<img width="1044" height="608" alt="image" src="https://github.com/user-attachments/assets/608e0f54-c74a-4129-b600-21df7e45abdc" />


<img width="1048" height="585" alt="image" src="https://github.com/user-attachments/assets/999382c4-e2f9-48d0-a87b-c360c90c85bf" />

Back in the VS Code, to enable logging of telemetry to your project, install azure-monitor-opentelemetry.

pip install azure-monitor-opentelemetry

Add the --enable-telemetry flag when you use the chat_with_products.py script:

python chat_with_products.py --query "I need a new tent for 4 people, what would you recommend?" --enable-telemetry
<img width="857" height="278" alt="image" src="https://github.com/user-attachments/assets/0f3c83f2-bd7c-4f0d-9a20-a52b5d23c532" />

Evaluate the custom chat application with the Azure AI Foundry SDK
1: Evaluate the quality of the chat app responses
Now that you know your chat app responds well to your queries, including with chat history, it's time to evaluate how it does across a few different metrics and more data.You use an evaluator with an evaluation dataset and the get_chat_response() target function, then assess the evaluation results. Once you run an evaluation, you can then make improvements to your logic, like improving your system prompt, and observing how the chat app responses change and improve.

Create evaluation dataset:

Use the following evaluation dataset, which contains example questions and expected answers (truth). Create a file called chat_eval_data.jsonl in your assets folder.

 2: Evaluate with Azure AI evaluators
 Now define an evaluation script that will:

Generate a target function wrapper around our chat app logic.

Load the sample .jsonl dataset.

Run the evaluation, which takes the target function, and merges the evaluation dataset with the responses from the chat app.

Generate a set of GPT-assisted metrics (relevance, groundedness, and coherence) to evaluate the quality of the chat app responses.

Output the results locally, and logs the results to the cloud project.

The script allows you to review the results locally, by outputting the results in the command line, and to a json file.

The script also logs the evaluation results to the cloud project so that you can compare evaluation runs in the UI.

Create a file called evaluate.py under src folder.

3: Configure the evaluation model
Since the evaluation script calls the model many times, you might want to increase the number of tokens per minute for the evaluation model. Initially, you created a .env file that specifies the name of the evaluation model, gpt-4o-mini. Try to increase the tokens per minute limit for this model, if you have available quota. If you don't have enough quota to increase the value, don't worry. The script is designed to handle limit errors.

From your project in Azure AI Foundry portal, select Models + endpoints and select gpt-4o-mini.
<img width="1011" height="649" alt="image" src="https://github.com/user-attachments/assets/2c8342ca-4b85-40bc-b7f9-7eb3f237afcd" />
<img width="767" height="585" alt="image" src="https://github.com/user-attachments/assets/a81d0381-eb8d-4d66-9a05-7f4660e1f1e8" />
<img width="735" height="638" alt="image" src="https://github.com/user-attachments/assets/8aae1c6e-00a7-4e89-a345-ae614b196d2d" />

4: Run the evaluation
Back in the VS Code terminal, execute the below command to install the required packages.

pip install azure-ai-evaluation[remote]

Execute the below code to run the evaluation script.

python evaluate.py

The evaluation will take around 5 to 10 minutes to complete.

5: View evaluation results in Azure AI Foundry portal

Once the evaluation run completes, follow the link to view the evaluation results on the Evaluation page in the Azure AI Foundry portal.
<img width="670" height="190" alt="image" src="https://github.com/user-attachments/assets/3fb8f560-b533-4afb-bb94-4ab46e455f35" />
<img width="732" height="446" alt="image" src="https://github.com/user-attachments/assets/b60ec20e-a0c1-4c0a-8e52-12623535d049" />
<img width="726" height="495" alt="image" src="https://github.com/user-attachments/assets/c4f967f4-024e-422d-91c3-17b1968d1803" />



























