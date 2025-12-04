# GraphRAG - Digitization and Natural Language Querying (CLI Version)

This project uses **GraphRAG** to digitize and structure book information into a knowledge graph. It is a **Command-Line Interface (CLI) application**, meaning all operations are executed from the terminal in a Linux environment. It then allows natural language queries through the terminal in a Linux environment.

## Requirements

- **Operating System:** Ubuntu 20.04, 22.04 or 24.04
- **Python:** 3.10+
- **GraphRAG:** 0.5.0
  
## Installation

1. Clone the repository using HTTPS:
   ```bash
   git clone https://github.com/gustavomarcelonunez/oceangraphrag.git
   ```
 <!--  Or using SSH:
   ```bash
   git clone git@github.com:gustavomarcelonunez/oceangraphrag.git
   ```-->
   Then navigate into the project directory:
   ```bash
   cd oceangraphrag
   ```

2. Install the required dependencies (GraphRAG):
   ```bash
   pip install graphrag==0.5.0
   ```

## Usage

### 1. Adding your OpenAI API key
You need to provide your own OpenAI API key in the [.env file](https://github.com/gustavomarcelonunez/oceangraphrag/blob/main/ragtest/.env).
Add the following line to your .env file:
```
GRAPHRAG_API_KEY=your_openai_api_key_here  
```
For more information on how to get your OpenAI API key, check [this link](https://platform.openai.com/api-keys).

### 2. Book Digitization

This project contains digitized text ([see here](https://github.com/gustavomarcelonunez/oceangraphrag/blob/main/ragtest/input/resumen.txt)). If you want to use your own text to generate a new knowledge graph, simply replace the existing file with your own and then run:
```bash
graphrag index --root ./ragtest
```

### 2. Natural Language Queries

For global query method run:
```bash
graphrag query --method global --root ./ragtest --query "your query"
```

For local query method run:
```
graphrag query --method local --root ./ragtest --query "your query"
```
More information about global and local query methods [here](https://microsoft.github.io/graphrag/query/overview/).

## Additional Documentation

For more information on GraphRAG and its commands, visit the [official page](https://microsoft.github.io/graphrag/).

