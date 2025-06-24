# 🧠 LangGraph Chatbot - News Search Tool

LangGraph Chatbot is an advanced AI-powered chatbot built using LangGraph and LangChain ecosystem tools. It provides real-time news search capabilities powered by Tavily, integrated with a Streamlit-based UI for interactive exploration.

![LangGraph Chatbot](https://img.shields.io/badge/License-MIT-yellow.svg)
![Python](https://img.shields.io/badge/Python-3.12-blue)
![LangChain](https://img.shields.io/badge/LangChain-Community-green)

## Features

- 🗞️ News search functionality using Tavily API
- 🤖 LangGraph-based agentic architecture
- 🚀 Multiple LLM backends (Groq, OpenAI)
- 💾 Vector storage with FAISS
- 🎨 Streamlit-based user interface
- 🔧 Modular architecture with separate components

## Technologies Used

- [LangGraph](https://github.com/langchain-ai/langgraph)
- [LangChain](https://github.com/langchain-ai/langchain)
- [LangChain Community](https://github.com/langchain-ai/langchain-community)
- [Groq](https://groq.com/) (via langchain_groq)
- [OpenAI](https://openai.com/) (via langchain_openai)
- [FAISS](https://github.com/facebookresearch/faiss) (CPU version)
- [Streamlit](https://streamlit.io/)
- [Tavily](https://tavily.com/) (for search)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Hari-Kec/Langgraph-Chatbot.git
   cd Langgraph-Chatbot
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Set up your environment variables:
   - Create a `.env` file in the root directory
   - Add your API keys:
     ```
     OPENAI_API_KEY=your_openai_key
     GROQ_API_KEY=your_groq_key
     TAVILY_API_KEY=your_tavily_key
     ```

## Usage

Run the Streamlit application:
```bash
streamlit run app.py
```

## Project Structure

```
📁Langraph Chatbots/
├── config/                # Configuration files
├── src/                  # Source code
│   ├── langgraphagenticai/  # Main application package
│   │   ├── graph/          # Graph construction logic
│   │   ├── LLMS/           # Language model implementations
│   │   ├── nodes/          # Individual graph nodes
│   │   ├── state/          # State management
│   │   ├── tools/          # Custom tools
│   │   ├── ui/             # User interface components
│   │   └── vectorstore/    # Vector storage implementation
│   └── __init__.py
├── .gitignore
├── app.py                # Main application entry point
└── requirements.txt      # Python dependencies
```

## Components

### Graph Builder
- Located in `src/langgraphagenticai/graph/`
- Constructs the LangGraph workflow for the chatbot

### Nodes
- `basic_chatbot_node.py`: Basic conversational capabilities
- `chatbot_with_Tool_node.py`: Enhanced with search tool integration
- `ai_news_node.py`: Specialized for news-related queries

### Tools
- `search_tool.py`: Implements news search functionality using Tavily

### LLMs
- `groqllm.py`: Groq LLM implementation

### UI
- Streamlit-based interface in `src/langgraphagenticai/ui/streamlitui/`

## Configuration

Edit `src/langgraphagenticai/ui/uiconfigfile.ini` to customize:
- Default LLM provider
- UI settings
- Search parameters

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## Acknowledgments

- LangChain team for the amazing framework
- Groq for their high-performance LLM infrastructure
- Tavily for their search API
