Contain:

What is Spring AI
how many way way you can run/connect to LLM model a. OpenAI b. Ollama c. Docker
Message Roles a. System (Instraction how LLM should behave) b. User c. Assistant (LLM Response) d. Function/tool (Special instruction to run function or fetch data)
default System (you can override)
default User (you can override)
Prompt Template
Prompt Stuffing: When you have limited amount of data you can use this if more data use RAG. We use system message with a one/two page messageTemplate file.
Why we should use Prompt Stuffing: Limited number of context token, billing base on input and output token,  each time it will 
Adviser : User → ChatClient → [Advisors] → LLM → Response → [Advisors] → User
  Default Adviser
  Order - higher order number Adviser will excute first.
Built-in Adviser   SafeGuardAdviser,SimpleLoggerAdvisor
Custum Adviser
  

https://platform.openai.com/tokenizer is to see how many token

There are many way you can run/intereact with LLM model. 
  1. using ollama at local (working on my mac)
  2. using docker desktop at local (not working... mac chip not suppoted)
  3. using external openapi (not working... due to organization restiction)


- https://github.com/driekeerJ/ai-chat-poc Spring-AI using openai by "Wal van der, JP (Jeroen)"
- https://github.com/eazybytes/spring-ai  Springai by udemy eazybytes nice one, I refer this to create my repo


Spring Al Makes Generative Al Spring-Native
- Spring Al wraps complex Al model APls (OpenAl, Olama, Bedrock) in familiar Spring interfaces.
- Gives you ChatClient, ImageModel, SpeechModel, and even Memory, all with Spring idioms.
- Makes Al integration feel like configuring a @Bean, not batling a black-box.

<img width="1252" height="611" alt="image" src="https://github.com/user-attachments/assets/ea7d88d0-6ab6-44c3-86f3-35b508501da4" />
<img width="1252" height="611" alt="image" src="https://github.com/user-attachments/assets/6fa7c189-249b-4cf5-b12a-15063c680101" />
<img width="1271" height="529" alt="image" src="https://github.com/user-attachments/assets/815d6ea1-8f25-4844-9d78-811b51e0c531" />
<img width="1222" height="571" alt="image" src="https://github.com/user-attachments/assets/5314eee9-3b58-4374-b35c-dd4d07a10f4c" />
<img width="1226" height="546" alt="image" src="https://github.com/user-attachments/assets/c3f0692f-5503-4296-8e35-5bf0c0ba6fac" />
<img width="1262" height="618" alt="image" src="https://github.com/user-attachments/assets/897b65a4-f820-46c0-ba90-d385070ea5ea" />
for code refer project ollama, opeanai, dockerai and multimodel
<img width="1281" height="627" alt="image" src="https://github.com/user-attachments/assets/508d3e59-b7f6-446c-830e-028b88b1eb0a" />



--------------------------------------------------------------------------------------------------------------------------------
<img width="1280" height="644" alt="image" src="https://github.com/user-attachments/assets/f532f041-a268-4131-8bab-e9d083c0a8c5" />
<img width="1280" height="644" alt="image" src="https://github.com/user-attachments/assets/30683dce-4d19-4669-8394-4849a9895f01" />









