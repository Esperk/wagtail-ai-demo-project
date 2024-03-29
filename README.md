# This is a demo project to demo wagtail-ai combined with a local ollama server.

https://github.com/wagtail/wagtail-ai

install:

```
source env/bin/activate
pip install -r requirements.txt
```

Install and serve ollama. See their docs on how to download and serve models.

Install the llm-ollama plugin (llm is installed as wagtail-ai dependency from requirements.txt).

See https://github.com/taketwo/llm-ollama.

```
llm install llm-ollama
``` 

When the ollama server is running (ollama serve), the ollama models should now be listed when listing available 
models with LLM.

Note that the OpenAI models are always available as they are remote models. They do require payment and a valid API key.

```
> llm models
OpenAI Chat: gpt-3.5-turbo (aliases: 3.5, chatgpt)
OpenAI Chat: gpt-3.5-turbo-16k (aliases: chatgpt-16k, 3.5-16k)
OpenAI Chat: gpt-4 (aliases: 4, gpt4)
OpenAI Chat: gpt-4-32k (aliases: 4-32k)
OpenAI Chat: gpt-4-1106-preview
OpenAI Chat: gpt-4-0125-preview
OpenAI Chat: gpt-4-turbo-preview (aliases: gpt-4-turbo, 4-turbo, 4t)
OpenAI Completion: gpt-3.5-turbo-instruct (aliases: 3.5-instruct, chatgpt-instruct)
Ollama: codellama:7b-python
Ollama: llama2:latest (aliases: llama2)
Ollama: llama2-uncensored:latest (aliases: llama2-uncensored)
Ollama: llava:latest (aliases: llava)
Ollama: yarn-mistral:7b-128k
```

Optionally edit the WAGTAIL_AI settings in base.py.


Run project:

```
source env/bin/activate
cd wagtailaidemo
python manage.py runserver
```
