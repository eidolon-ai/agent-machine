# Eidolon Git Search Recipe

Interact with a RAG enabled copilot that has access to a repository via vector search.

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
make serve-dev
```

This will start the Eidolon http server without MongoDB along with some other dev tools such as recordings.
