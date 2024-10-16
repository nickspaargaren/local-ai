
# Local AI with Cody for Visual Studio Code

Cody is an AI-powered coding assistant that integrates seamlessly with Visual Studio Code. This README provides an overview of how Cody works and guides you through the setup process.

## Start the ollama docker image

- docker compose up -d
- exec in docker container and run `ollama pull llama3.2` to pull the model.

## Test if the api is working

```
curl -X POST http://localhost:11434/api/generate \
-H "Content-Type: application/json" \
-d '{
  "prompt": "Write a Python function that takes a string and returns the number of vowels in the string.",
  "model": "llama3.2"
}'
```


## Install Cody VS Code Extension

- https://marketplace.visualstudio.com/items?itemName=sourcegraph.cody-ai

## Setting Up Cody for VS Code

Add this to the settings.json file:

```
{
    "cody.autocomplete.advanced.provider": "default",
    "cody.autocomplete.experimental.ollamaOptions": {
        "url": "http://localhost:11434",
        "model": "llama3.2"
    },
    "editor.inlineSuggest.suppressSuggestions": true
}
```

## Done!

- Happy AI coding!