# GLOOM: Your All-in-One AI Agent

## Features

### Multi-Platform Compatibility

Integrate seamlessly with over 20 leading LLM platforms through a unified interface. Supported platforms include OpenAI, Claude, Gemini (Google AI Studio), Ollama, Groq, Azure-OpenAI, VertexAI, Bedrock, Huggingface, Github Models, Mistral, Deepseek, AI21, XAI Grok, Cohere, Perplexity, Cloudflare, OpenRouter, Ernie, Qianwen, Moonshot,  ZhipuAI, Lingyiwanwu, Deepinfra, Fireworks, Siliconflow, Together, Jina, VoyageAI, any OpenAI-Compatible platforms.

### CMD Mode

Explore powerful command-line functionalities with GLOOM's CMD mode.

![GLOOM-cmd](https://github.com/user-attachments/assets/6c58c549-1564-43cf-b772-e1c9fe91d19c)

### REPL Mode

Experience an interactive Chat-REPL with features like tab autocompletion, multi-line input support, history search, configurable keybindings, and custom REPL prompts.

![GLOOM-repl](https://github.com/user-attachments/assets/218fab08-cdae-4c3b-bcf8-39b6651f1362)

### Shell Assistant

Elevate your command-line efficiency. Describe your tasks in natural language, and let GLOOM transform them into precise shell commands. GLOOM intelligently adjusts to your OS and shell environment.

![GLOOM-execute](https://github.com/user-attachments/assets/0c77e901-0da2-4151-aefc-a2af96bbb004)

### Multi-Form Input

Accept diverse input forms such as stdin, local files and directories, and remote URLs, allowing flexibility in data handling.

| Input             | CMD                                  | REPL                             |
| ----------------- | ------------------------------------ | -------------------------------- |
| CMD               | `GLOOM hello`                       |                                  |
| STDIN             | `cat data.txt \| GLOOM`             |                                  |
| Local files       | `GLOOM -f image.png -f data.txt`    | `.file image.png data.txt`       |
| Local directories | `GLOOM -f dir/`                     | `.file dir/`                     |
| Remote URLs       | `GLOOM -f https://example.com`      | `.file https://example.com`      |
| Combine Inputs    | `GLOOM -f dir/ -f data.txt explain` | `.file dir/ data.txt -- explain` |

### Role Management

Customize roles to tailor LLM behavior, enhancing interaction efficiency and boosting productivity.

![GLOOM-role](https://github.com/user-attachments/assets/023df6d2-409c-40bd-ac93-4174fd72f030)

> The role consists of a prompt and model configuration.

### Session Management

Maintain context-aware conversations through sessions, ensuring continuity in interactions.

![GLOOM-session](https://github.com/user-attachments/assets/56583566-0f43-435f-95b3-730ae55df031)

> The left side uses a session, while the right side does not use a session.

### RAG (Chat with your documents)

Integrate external documents into your LLM conversations for more accurate and contextually relevant responses.


![GLOOM-rag](https://github.com/user-attachments/assets/359f0cb8-ee37-432f-a89f-96a2ebab01f6)

### Function Calling

Function calling supercharges LLMs by connecting them to external tools and data sources. This unlocks a world of possibilities, enabling LLMs to go beyond their core capabilities and tackle a wider range of tasks.

We have created a new repository [https://github.com/sigoden/llm-functions](https://github.com/sigoden/llm-functions) to help you make the most of this feature.

#### AI Tools

Integrate external tools to automate tasks, retrieve information, and perform actions directly within your workflow.

![GLOOM-tool](https://github.com/user-attachments/assets/7459a111-7258-4ef0-a2dd-624d0f1b4f92)

#### AI Agents (CLI version of OpenAI GPTs)

AI Agent = Instructions (Prompt) + Tools (Function Callings) + Documents (RAG).

![GLOOM-agent](https://github.com/user-attachments/assets/0b7e687d-e642-4e8a-b1c1-d2d9b2da2b6b)

### Local Server Capabilities

GLOOM includes a lightweight built-in HTTP server for easy deployment.

```
$ GLOOM --serve
Chat Completions API: http://127.0.0.1:8000/v1/chat/completions
Embeddings API:       http://127.0.0.1:8000/v1/embeddings
Rerank API:           http://127.0.0.1:8000/v1/rerank
LLM Playground:       http://127.0.0.1:8000/playground
LLM Arena:            http://127.0.0.1:8000/arena?num=2
```

#### Proxy LLM APIs

The LLM Arena is a web-based platform where you can compare different LLMs side-by-side. 

Test with curl:

```sh
curl -X POST -H "Content-Type: application/json" -d '{
  "model":"claude:claude-3-5-sonnet-20240620",
  "messages":[{"role":"user","content":"hello"}], 
  "stream":true
}' http://127.0.0.1:8000/v1/chat/completions
```

#### LLM Playground

A web application to interact with supported LLMs directly from your browser.

![GLOOM-llm-playground](https://github.com/user-attachments/assets/aab1e124-1274-4452-b703-ef15cda55439)

#### LLM Arena

A web platform to compare different LLMs side-by-side.

![GLOOM-llm-arena](https://github.com/user-attachments/assets/edabba53-a1ef-4817-9153-38542ffbfec6)

## License

Copyright (c) 2023-2025 GLOOM-developers.

GLOOM is made available under the terms of either the MIT License or the Apache License 2.0, at your option.

See the LICENSE-APACHE and LICENSE-MIT files for license details.
