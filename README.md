# LangChain Prompt Chain

A first chain built with [LangChain](https://python.langchain.com/): a `PromptTemplate` piped into an LLM using LCEL (`prompt | llm`). It takes a text about a person and returns a short summary plus two interesting facts about them.

## Stack

- Python 3.14 + [uv](https://docs.astral.sh/uv/)
- LangChain (`langchain-core`, `langchain-ollama`, `langchain-openai`)
- [Ollama](https://ollama.com/) running `gpt-oss:20b` locally (default), or OpenAI as an alternative

## Getting started

```bash
# 1. Install dependencies
uv sync

# 2. Pull the local model
ollama pull gpt-oss:20b

# 3. Run
uv run langchain-course
```

To use OpenAI instead of Ollama, create a `.env` file with `OPENAI_API_KEY=...` and swap the `llm` in [`src/langchain_course/__init__.py`](src/langchain_course/__init__.py).