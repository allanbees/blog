---
draft: False
date: 2024-06-05
slug: 01-openai-assistants-getting-started
categories:
  - LLMs
authors:
  - abarrantes
---

# Getting started with the OpenAI Assistants API

The OpenAI assistants API allows developers to create agents for automating lots of tasks in their workflows. In this tutorial, I want to show how to create a simple agent for scraping data from Hacker News and getting the output in a JSON file.

Before diving into the code, I want to explain some important concepts related to assistants:

**Assistant**
They are entities with instructions to respond or behave the way we tell them to. They receive the following paremeters: name, instructions, model (e.g., gpt-4o) and tools (code interpreter, file search and function calling)

**Thread**
A thread is a conversation between an assistant and a user. The thread gets created when the user or application starts the conversation.

**Messages**
Messages are created and added to the thread. They can contain both text and files.

**Run**
Once your messages have been added to the thread, a run can be triggered in order to start a conversation with the assistant. The response generated when the run completes is then added to the thread’s messages.

Now we can dive into the code. The requirements are **python** and an **OpenAI API Key**.

First, we’ll have to install the **openai**, **python-dotenv**, **requests** and **beautifulsoup4** packages:

```
pip install openai python-dotenv requests beautifulsoup4
```
