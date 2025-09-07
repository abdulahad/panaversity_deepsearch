# Deep Search Agent

A sophisticated AI-powered research assistant that performs deep, multi-phase web searches to provide comprehensive, reliable answers to complex questions.

## Features

- **Multi-Phase Research System**: Implements a professional research workflow with planning, fact-finding, conflict detection, source evaluation, synthesis, and report writing.
- **Web Search Integration**: Uses Tavily API for advanced web search capabilities with parallel searching.
- **AI-Powered Analysis**: Leverages Google's Gemini 2.5 Flash model (or AWS Bedrock) for intelligent analysis and synthesis.
- **Conflict Resolution**: Automatically detects and resolves conflicting information from multiple sources.
- **Citation Management**: Professional citation formatting and bibliography generation.
- **Quality Assessment**: Evaluates source reliability and research quality.
- **Async Processing**: Efficient concurrent searches for faster results.

## Requirements

- Python 3.11 or higher
- API Keys:
  - `GEMINI_API_KEY` (for Google Gemini API)
  - `TAVILY_API_KEY` (for web search)
  - Optional: `AWS_API_KEY` (for AWS Bedrock alternative)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/abdulahad/panaversity_deepsearch.git
   cd panaversity_deepsearch
   ```

2. Install dependencies using uv:
   ```bash
   uv sync
   ```

3. Create a `.env` file in the root directory and add your API keys:
   ```
   GEMINI_API_KEY=your_gemini_api_key_here
   TAVILY_API_KEY=your_tavily_api_key_here
   AWS_API_KEY=your_aws_api_key_here  # Optional
   ```

## Usage

### Running the Research Agent

The main implementation is in `agent.ipynb`. To use the agent:

1. Open `agent.ipynb` in Jupyter Notebook or VS Code.
2. Run the cells in order to set up the environment and agents.
3. Use the test functions to ask research questions.

### Example Usage

```python
# Basic research
result = Runner.run_streamed(starting_agent=basic_agent, input="What is renewable energy?")

# Professional research (multi-phase)
result = Runner.run_streamed(starting_agent=professional_lead_researcher, input="Analyze the economic impact of remote work")
```

### Running Tests

- Use `test_basic_research()` for basic functionality
- Use `test_phase4_professional_system()` for advanced multi-phase research

## Project Structure

- `agent.ipynb`: Main notebook with agent implementations and test functions
- `main.py`: Simple test script for basic agent setup
- `pyproject.toml`: Project configuration and dependencies
- `uv.lock`: Dependency lock file
- `README.md`: This file

## Architecture

The system consists of multiple specialized agents:

1. **BasicResearcher**: Simple web search and answer formatting
2. **ProfessionalPlanningAgent**: Research methodology planning
3. **ProfessionalFactFinder**: Comprehensive fact gathering with parallel searches
4. **AdvancedConflictDetector**: Conflict identification and resolution
5. **ProfessionalSourceChecker**: Source quality evaluation
6. **AdvancedSynthesisAgent**: Creative analysis and synthesis
7. **ProfessionalReportWriter**: Publication-quality report generation

## API Keys Setup

### Google Gemini API
1. Go to [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Create a new API key
3. Add it to your `.env` file as `GEMINI_API_KEY`

### Tavily API
1. Sign up at [Tavily](https://tavily.com/)
2. Get your API key
3. Add it to your `.env` file as `TAVILY_API_KEY`

### AWS Bedrock (Optional)
1. Set up AWS credentials
2. Add your API key to `.env` as `AWS_API_KEY`

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Built with [OpenAI Agents](https://github.com/openai/openai-agents)
- Web search powered by [Tavily](https://tavily.com/)
- AI models from [Google Gemini](https://ai.google.dev/)