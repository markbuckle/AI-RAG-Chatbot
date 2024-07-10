<h1>AiDocChatBot</h1>

<p align="center"><img src="https://github.com/markbuckle/AiDocChatBot/blob/main/Githubimg1.png" alt="AiChatbotImg1" /></p>

[Flowise AI](https://flowiseai.com/) is an open source low-code tool for developers to build LLM apps easily. It provides a user-friendly and aesthetic visual builder. Under the hood it is predominately [Langchain](https://www.langchain.com/). Langchain is a framework with libraries to build with LLMs.

For this to work you need an [OpenAI](https://platform.openai.com/api-keys) (paid) API Key and a [Pinecone](https://sdk.pinecone.io/python/pinecone.html) (free) API Key.

Steps:
1. Create a langchain-experiments workspace
2. git clone https://github.com/daveebbelaar/langchain-experiments.git
3. git clone https://github.com/FlowiseAI/Flowise.git #do this inside of the langchain-experiments workspace
4. Go to https://github.com/FlowiseAI/Flowise README.md #decide whether you want to use npm/nodeJS or Docker. Docker can provide more localhost flexibility as it allows you to specifiy the port
5. In VS Code go to ./Flowise/docker/.env-example. Rename the folder to just ./env. Change the default port from 3000 to something else i.e. 3050.
6. Follow docker or npm/nodeJS installation steps as per https://github.com/FlowiseAI/Flowise/README.md
7. Move into the docker folder: cd C:\Users\Marks-Desktop\Coding\AiDocChatbot\langchain-experiments\Flowise\docker
8. Run: docker compose up -d to start a local server
9. Open a new browser (edge or chrome) and run: http://localhost:3050/
10. Go to marketplace and select 'Conversational Retrieval QA Chain' then hit 'use template'. Save and rename i.e. 'Document Chatbot'
11. Copy and paste your OpenAI_API_Key into the ChatOpenAI box 'Connect Credential*'
11. Copy and paste your Pinecone API Key into the Pinecone box 'Connect Credential*'
12. Create a new index in Pinecone and enter the 'Pinecone Index*' name in the Pinecone box
13. Convert the README.md file in https://github.com/daveebbelaar/langchain-experiments.git into a .txt file and save it on your computer. Upload it to the localhost textfile box and then save (Document Chatbot)
14. Hit the 'Upset Vector Database' (green button) and then 'Save' (purple button)
15. Enter a prompt/question (i.e. "What is this doc about?") in the chatbox and determine if the answer makes sense. If it does, congratulations, you successfuly setup an AI Chat Box using Flowise. Play around with different chatflows and see what you can come up with.

Full tutorial here: [How to Build an AI Document Chatbot with Flowise](https://www.youtube.com/watch?v=riXpu1tHzl0)
