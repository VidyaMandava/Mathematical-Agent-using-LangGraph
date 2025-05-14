# Mathematical Agent using LangGraph

A mathematical agent built with LangGraph that can perform mathematical operations and answer general knowledge questions. The agent intelligently routes queries to specialized tools or provides direct answers based on the nature of the question.

## Features

- **Dual Functionality**: Handles both mathematical calculations and general knowledge questions
- **Tool-based Architecture**: Uses specialized tools for mathematical operations
- **Graph-based Workflow**: Built with LangGraph to manage routing and processing
- **Large Language Model Integration**: Leverages LLMs for understanding and generating responses

## Requirements

- Python 3.8+
- LangChain 0.3.14
- LangGraph
- OpenAI API key (for GPT models)

## Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/mathematical-agent.git
cd mathematical-agent
```

2. Install the required packages:
```bash
pip install -r requirements.txt
```

3. Set up your OpenAI API key:
```bash
# In Google Colab
from google.colab import userdata
import os
os.environ["OPENAI_API_KEY"] = userdata.get('OPENAI_API_KEY')

# Or locally
export OPENAI_API_KEY="your-api-key"
```

## Usage

Run the Jupyter notebook to initialize and test the agent:

```python
# Example usage
query = 'what is 2*5?'
call_agent(mathematical_agent, query)

# Output:
# The result of 2 multiplied by 5 is 10.

query = 'what is AI?'
call_agent(mathematical_agent, query)

# Output:
# AI, or Artificial Intelligence, refers to the simulation of human intelligence in machines...
```

## How It Works

1. **User Input**: The user submits a question
2. **Analysis**: The LLM analyzes whether the query is mathematical or general
3. **Routing**: 
   - Mathematical queries are routed to the appropriate tool (plus, subtract, multiply, divide)
   - General questions are answered directly by the LLM
4. **Response**: The final response is returned to the user

## Project Structure

- `Mathematical_Agent_using_LangGraph.ipynb`: Main Jupyter notebook with all code and examples
- `requirements.txt`: Required Python packages
- `README.md`: Project documentation

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
