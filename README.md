# lukebot

Discord bot built with GPT-4

## Prompts

```py
You are an AI programming assistant.
- Follow the user's requirements carefully & to the letter.
- First think step-by-step, describe your plan for what to build in pseudocode, written out in great detail.
- Then output the code in a single code block.
- Minimize any other prose.

---
An example API call looks as follows:
# Note: you need to be using OpenAI Python v0.27.0 for the code below to work
import openai

openai.ChatCompletion.create(
  model="gpt-3.5-turbo",
  messages=[
        {"role": "system", "content": "You are a helpful assistant."},
        {"role": "user", "content": "Who won the world series in 2020?"},
        {"role": "assistant", "content": "The Los Angeles Dodgers won the World Series in 2020."},
        {"role": "user", "content": "Where was it played?"}
    ]
)
The main input is the messages parameter. Messages must be an array of message objects, where each object has a role (either "system", "user", or "assistant") and content (the content of the message). Conversations can be as short as 1 message or fill many pages.
---
Response format:
An example API response looks as follows:
{
 'id': 'chatcmpl-6p9XYPYSTTRi0xEviKjjilqrWU2Ve',
 'object': 'chat.completion',
 'created': 1677649420,
 'model': 'gpt-3.5-turbo',
 'usage': {'prompt_tokens': 56, 'completion_tokens': 31, 'total_tokens': 87},
 'choices': [
   {
    'message': {
      'role': 'assistant',
      'content': 'The 2020 World Series was played in Arlington, Texas at the Globe Life Field, which was the new home stadium for the Texas Rangers.'},
    'finish_reason': 'stop',
    'index': 0
   }
  ]
}
---
Write me a Discord bot with each of these requirements:
 - Accepts message containing image and text inputs.
 - No need special text to trigger the bot; should read & respond to every message.
 - Use the `gpt-4` model in the API rather than `gpt-3.5-turbo` and then post the results
 - Reads credentials from the DISCORD_TOKEN and OPENAI_API_KEY env vars
```
