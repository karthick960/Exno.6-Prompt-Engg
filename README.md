# Exno.6-Prompt-Engg
# Date:30/04/2005
# Register no:212222040070
# Aim: 
Development of Python Code Compatible with Multiple AI Tools



# Algorithm:
Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights.

Target Users: AI researchers, automation engineers, data scientists

## Objective:

1. Reduce manual API interactions

2. Automatically benchmark multiple AI models

3. Extract usable insights from varied outputs (e.g., sentiment, clarity, relevance)

## 1. Prompt Patterns for Design Aspects

### A. Idea Generation Prompt
#### Prompt: 
“What modules and design strategies can make a Python program modular and AI-tool agnostic?”

#### Features:

Abstract AIClient base class with query() method

Plugins for each tool (OpenAI, Hugging Face, etc.)

Output comparison strategy (e.g., similarity score, sentiment match)

Logging and visualization module

### B. Persona and Context Prompt
#### Prompt: 
“Design the interface for a Python module usable by non-experts in AI, with readable documentation and error messages.”

#### Result:

Simple CLI interface: python run_query.py --prompt "Summarize climate change"

Configurable YAML/JSON for API keys and settings

Built-in --explain mode to output how each AI tool processed the prompt

### C. Exploratory Prompt
#### Prompt: 
“List all AI APIs supporting text generation and summarize their input/output format.”

#### Tools Explored:

OpenAI GPT: JSON input, streaming output

Cohere: Text input, embeddings

Hugging Face Transformers: Model-specific format, requires tokenization

Google PaLM: REST API with rich metadata

### D. Refinement Prompt
#### Prompt: 
“Modify the pipeline to support asynchronous querying and retry logic in case of rate-limiting or failure.”

#### Update:

Added aiohttp for async requests

Implemented retry decorators with exponential backoff

### E. Scenario Testing Prompt
#### Prompt: 
“Run the same query (‘Explain quantum computing in simple terms’) through all tools and compare clarity.”

#### Execution Result:

GPT-4: Best at analogies

Cohere: Technical but concise

Hugging Face model: Verbose and less accurate

### F. Error Handling Prompt
#### Prompt: “How should the script handle API timeouts, incorrect credentials, and unstructured responses?”

#### Solutions:

Custom error classes: APIConnectionError, InvalidResponseError

Environment variable validation on startup

JSON schema validation of responses

### 2. Implementation Plan
#### 1. Setup:

Install libraries: openai, requests, aiohttp, dotenv, jsonschema

Load credentials from .env

#### 2. Modular API Wrappers:

clients/openai_client.py

clients/cohere_client.py

clients/hf_client.py

#### 3. Async Execution Manager:

Collects all responses in parallel

#### 4. Output Comparison Engine:

Uses difflib + NLP metrics (e.g., BLEU, ROUGE)

#### 5. Insight Generator:

Produces a summary + actionable decision (e.g., “GPT-4 output preferred for educational content”)

#### 6. Logging/Report:

Auto-generates markdown + CSV log

### 3. Evaluation and Feedback Collection
#### Prompt:
“What feedback did users give after running the tool for a week?”

#### Method:
Feedback collected via CLI prompts and GitHub Issues

#### Findings:

#### Pros:
Speed, clarity, comparison matrix

#### Cons: 
Minor bugs with new API formats

#### Response:

Added auto-schema detection

Scheduled weekly tool updates

### 4. Prototype/System Outline
#### Repo Structure:

```python
/ai_compare_tool/
├── run_query.py
├── clients/
│   ├── base.py
│   ├── openai_client.py
│   ├── cohere_client.py
│   └── hf_client.py
├── insights/
│   └── compare.py
├── utils/
│   └── logger.py
└── .env
```
#### Output Format:

Markdown table + CSV log

#### Summary: 
“Tool X produced most readable output”

### 5. User Testing Results and Improvement Plan
#### Sample Feedback:

“Great for quick benchmarking between tools”

“Would love plugin support for Claude and Gemini”

#### Next Steps:

Add support for Claude & Gemini

Build web dashboard for visualization




# Result: 
The corresponding Prompt is executed successfully
