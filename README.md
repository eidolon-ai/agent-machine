# Eidolon Git Search Recipe

In this recipe we have created a github copilot who can answer questions about the Eidolon monorepo. It dynamically pulls in information via similarity search to answer user queries.
This is important if you have a body of information that is constantly changing, but you need real time information about (ie, a git repository).

## Core Concepts
* Multi-agent communication
* Sub-component customization
* Dynamic embedding management

## Agents
### Repo Expert
The user facing copilot. Ask this agent questions about a repository, and it will go and find the answer with the 
assistance of the repo search agent.

### Repo Search
Handles loading, embedding, and re-embedding documents ensuring they are up-to-date.

Translates queries into a vector search query and returns the top results.

## Directory Structure

- `resources`: This directory contains additional resources for the project. An example agent is provided for reference.
- `components`: This directory is where any custom code should be placed.

## Running the Server

To run the server in dev mode, use the following command:

```bash
export GITHUB_TOKEN=<YOUR GITHUB TOKEN>
make serve-dev
```

🚨 Make sure you sure you set `GITHUB_TOKEN` otherwise you will hit rate limit errors.

This will start the Eidolon http server without MongoDB along with some other dev tools such as recordings.
