List of commands:
```
python -m venv genaiVenv
. genaiVenv/Scripts/activate                                    #Activate virtual env with git bash
pip install openai jupyter                                      #Install openai and jupyter python modules
export OPENAI_API_KEY=sk-proj-XXXXXXXXXXXXX

# Here is a sample curl command to make a request to the OpenAI API (specifically for GPT models)
curl https://api.openai.com/v1/chat/completions \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer $OPENAI_API_KEY" \
  -d '{
    "model": "gpt-3.5-turbo",
    "messages": [
      {
        "role": "system",
        "content": "You are a helpful assistant."
      },
      {
        "role": "user",
        "content": "Can you translate \"Hello, how are you?\" into French?"
      }
    ],
    "max_tokens": 60
  }'
```