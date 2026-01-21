<p align = "center" draggable="false" ><img src="https://github.com/AI-Maker-Space/LLM-Dev-101/assets/37101144/d1343317-fa2f-41e1-8af1-1dbb18399719"
     width="200px"
     height="auto"/>
</p>

# AI Makerspace - Recursive Language Models (RLMs) Workshop

## What are RLMs?

**Recursive Language Models (RLMs)** are a task-agnostic inference paradigm that enables LLMs to handle **near-infinite length contexts** by allowing the model to programmatically examine, decompose, and recursively call itself over its input.

RLMs enable you to:
- Process documents far exceeding any context window (books, codebases, logs)
- Let LLMs write Python code to explore and analyze massive texts
- Make recursive sub-LLM calls via `llm_query()` on specific chunks
- Build divide-and-conquer strategies for complex analytical tasks

## About This Repository

This hands-on repository introduces **Recursive Language Models** through two practical tutorials. You'll learn how RLMs solve the context length problem and how to use them with both a standalone library and DSPy.

### What You'll Learn

Through practical examples in the notebooks, you'll explore:

1. **RLM Fundamentals** - How context-as-variable enables infinite context processing
2. **The rlm Library** - Using the standalone RLM implementation with verbose logging
3. **DSPy Integration** - Using RLM within the DSPy framework
4. **Long-Context Analysis** - Analyzing War and Peace (~3.3M chars) and Complete Shakespeare (~5.5M chars)
5. **Custom Tools & Pipelines** - Extending RLM capabilities for domain-specific tasks

### Why This Matters

RLMs represent a paradigm shift in how LLMs handle long contexts:
- **No Truncation** - Process entire documents without losing information
- **Systematic Analysis** - LLMs write code to count, search, and compare across texts
- **Transparency** - Verbose logging shows exactly how the model reasons
- **Flexibility** - Works with any LLM provider (OpenAI, Anthropic, Gemini, etc.)

Whether you're analyzing legal documents, exploring codebases, or processing research papers, RLMs unlock capabilities that RAG and traditional context windows can't match.

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/AI-Makerspace/RLM-AIM-Event.git
cd RLM-AIM-Event
```

### 2. Install Dependencies

```bash
uv sync
```

This installs:
- The local `rlm` package (editable)
- DSPy for the second tutorial
- Jupyter for running notebooks

### 3. Configure Your API Keys

Create a `.env` file in the project root:

```bash
echo "OPENAI_API_KEY=your_key_here" > .env
echo "ANTHROPIC_API_KEY=your_key_here" >> .env  # Optional
```

Or manually create `.env` with:

```
OPENAI_API_KEY=sk-...
ANTHROPIC_API_KEY=sk-ant-...
```

### 4. Run the Notebooks

```bash
uv run jupyter lab
```

Then open either notebook to begin.

## Workshop Structure

### Notebook 1: `01_RLM_Local_Repo_Tutorial.ipynb`

Using the standalone `rlm` library:

- **Setup & Installation** - Cloning the repo and configuring API keys
- **Long-Context Data** - Downloading War and Peace from Project Gutenberg
- **Basic RLM Usage** - Verbose logging and REPL execution
- **Analyzing War and Peace** - Queries that require full-text understanding
- **Log File Analysis** - Examining JSONL trajectories
- **Multi-Backend Support** - OpenAI, Anthropic, and mixed-model configurations

### Notebook 2: `02_DSPy_RLM_Tutorial.ipynb`

Using DSPy's RLM module:

- **DSPy Fundamentals** - Signatures, modules, and configuration
- **Long-Context Data** - Downloading Complete Works of Shakespeare
- **Signature-Based Interface** - Defining inputs and outputs declaratively
- **Structured Outputs** - Multiple output fields for organized responses
- **Custom Tools** - Adding domain-specific functions to the REPL
- **Module Composition** - Building pipelines with RLM and ChainOfThought

## Key Takeaways

By completing this workshop, you'll understand how to:
- Explain why RLMs solve problems that RAG and long-context models can't
- Use the standalone `rlm` library with verbose logging
- Use DSPy's RLM with signatures and custom tools
- Analyze massive documents (millions of characters) systematically
- Choose between standalone rlm and DSPy RLM for your use case
- Build custom pipelines combining RLM with other techniques

## Resources

- [RLM Paper](https://arxiv.org/abs/2512.24601) - Full technical details
- [RLM Blogpost](https://alexzhang13.github.io/blog/2025/rlm/) - Intuitive explanation
- [RLM Documentation](https://alexzhang13.github.io/rlm/) - API reference
- [RLM GitHub](https://github.com/alexzhang13/rlm) - Source code
- [DSPy GitHub](https://github.com/stanfordnlp/dspy) - DSPy framework

## Files

- `01_RLM_Local_Repo_Tutorial.ipynb` - Standalone rlm library tutorial
- `02_DSPy_RLM_Tutorial.ipynb` - DSPy RLM integration tutorial
- `rlm/` - Local clone of the rlm repository
- `.env` - Your API keys (not tracked in git)

Start exploring RLMs by opening the first notebook and running through the examples!
