
# Local AI with Cody for Visual Studio Code

Cody is an AI-powered coding assistant that integrates seamlessly with Visual Studio Code. This README provides an overview of how Cody works and guides you through the setup process.

## Start ollama

- docker compose up -d


## Install Cody VS Code Extension

- https://marketplace.visualstudio.com/items?itemName=sourcegraph.cody-ai

## Setting Up Cody for VS Code

Add this to the settings.json file:

```
{
    "cody.autocomplete.advanced.provider": "default",
    "cody.autocomplete.experimental.ollamaOptions": {
        "url": "http://localhost:7869",
        "model": "codellama"
    },
    "editor.inlineSuggest.suppressSuggestions": true
}
```

## Done!

- Happy AI coding!