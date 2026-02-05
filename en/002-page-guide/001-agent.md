---
id: agent-mode
title: Agent Mode
description: Introduction to agent mode
order: 1
parent: page-guide
demos:
  - key: model-select
    component: ModelSelect
previous: editor-mode
---

# Agent Mode

_Agent mode is still under development, welcome to feedback and suggestions._

Agent mode can quickly adjust the style by directly instructing the AI assistant, and supports global or local adjustment modes.

To use agent mode, you need to first configure the API Key and model of the AI provider.

## Set Model

_Your API Key will always be saved locally, not uploaded to our server, and only be used when using agent mode._

The currently available AI providers include:

- [Vercel AI Gateway](https://vercel.com/ai-gateway)
- [OpenAI](https://openai.com/)
- [Anthropic](https://claude.com/)
- [Google](https://gemini.google.com/)
- [Ollama](https://ollama.com/)

You can configure by clicking the settings option in the bottom left corner of the chat box.

<!-- demo:model-select -->

> The locally configured Ollama model may perform poorly due to parameter issues or hardware performance, you can try to change the model or use other AI providers.

After setting the API Key, you can select the model you want to use in the list, the specific supplier corresponding to the model will also be displayed after the option.

## Mode Selection

_By adjusting the mode, you can control the scope of the assistant's style adjustment._

|| Global Mode | Local Mode |
| --- | --- | --- |
| Token Consumption | High | Low |
| Adjustment Speed | Slow | Fast |
| Adjustment Range | All Message Types | Selected Message Types |
| Applicable Range | Overall modification or rapid generation of global styles | Local adjustment of single message styles |
| Preview Content | All Message Types | Selected Message Types |

## Prompt

After configuring the model and mode, enter the prompt in the chat box to let the assistant adjust the style for you. In addition to text content, you can also instruct the assistant to use the images you added to the project or specify the layers you want to use.

### Use Image

Click the image option below the chat box to expand the project image list.

> Currently, the reference image input function is not supported, all your images will be directly used.

### Specify Layer

Click the `@` option below the chat box to expand the layer list and specify the layer.

## History Message

_All your prompts and replies will be saved to the history message list, you can view and edit them anytime._

### Undo Changes

Below each prompt record there is a undo button, clicking it will restore the style to the state before the prompt was sent, you can edit the prompt again in the chat box and send it again.

> Although the undo shortcut key can also be used in agent mode, we do not recommend it, because agent mode will also modify some content that cannot be controlled by the shortcut key, such as global CSS and project images.