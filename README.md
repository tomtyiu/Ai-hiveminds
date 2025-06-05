# HiveMindsAI

HiveMindsAI is a sophisticated AI orchestration framework designed to manage and delegate tasks across multiple AI agents seamlessly. Leveraging OpenAI's powerful language models and built-in web search capabilities, HiveMindsAI ensures efficient task moderation, delegation, and execution, making it ideal for complex projects that require coordinated AI interactions.

## Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Example](#example)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Features
- Queen AI: Central orchestrator that breaks down tasks, delegates to specialized agents, and synthesizes results.
- Subordinate AI Agents: Execute specific tasks assigned by the Queen AI.
- Dynamic Worker Assignment: Deploys multiple agents dynamically based on task complexity.
- Worker Agent Support: Include "workers can use computer use agent" or "workers can use web search agent" in a task description to spawn specialized helper agents.
- Moderation and Security: Built-in moderation checks and policy compliance for ethical AI behavior.
- Web Search Integration: Fetch real-time data using OpenAI's web search tool for enhanced information retrieval.

## Prerequisites

Before setting up HiveMindsAI, ensure you have the following:

- **Python 3.8+** installed on your system.
- **OpenAI API Key:** Obtain from [OpenAI](https://openai.com/api/).

## Installation

### Clone the Repository

```bash
git clone https://github.com/yourusername/HiveMindsAI.git
cd HiveMindsAI
```

Create a Virtual Environment

It's recommended to use a virtual environment to manage dependencies.

```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

Install Dependencies

```bash
pip install -r requirements.txt
```

If a requirements.txt is not provided, you can install the necessary packages manually:

```bash
pip install openai
```

Configuration
Set up the required environment variables to securely manage your API keys.

Create a .env File

In the root directory of the project, create a .env file:

```bash
touch .env
```

Add Your API Keys

Open the .env file in a text editor and add the following:

env
```bash
OPENAI_API_KEY=your_openai_api_key
```

Load Environment Variables

Ensure that your Python script loads these environment variables. You can use the python-dotenv package for this purpose.

```bash
pip install python-dotenv
```

Then, modify your Python script to load the .env file:

```
from dotenv import load_dotenv
load_dotenv()
```

Usage
HiveMindsAI is designed to be run as a standalone Python script. Follow these steps to start delegating tasks:

Run the Script

```
python SuperHiveMinds,py
```

# How it works

Interactive Workflow
- Enter the tasks you want the Queen AI to manage.
- The Queen AI will decompose the tasks and delegate them to subordinate agents.
- Include phrases like "workers can use computer use agent" or "workers can use web search agent" to let each worker spawn specialized helper agents.
- Results will be synthesized and presented in a clear, cohesive format.

Example
Running the Script:

```bash
python main.py
Sample Interaction:

Enter tasks for the Queen AI to delegate. Type 'done' when finished.
Enter task name: Data Analysis
Enter task description: Analyze sales data for Q4 and identify trends.
Enter task name: Web Search
Enter task description: Search for the latest AI advancements.
Enter task name: done
```
## Output

```bash
HiveMindsAI processing queen task: Data Analysis
Queen AI response for Data Analysis:
[Detailed instructions for subordinate AI]

HiveMindsAI processing subordinate task: Data Analysis
Subordinate AI response for Data Analysis:
[Analysis of sales data]

HiveMindsAI processing queen task: Web Search
Queen AI response for Web Search:
[Detailed instructions for subordinate AI]

HiveMindsAI processing subordinate task: Web Search
Subordinate AI response for Web Search:
[Latest AI advancements]

Summary of tasks and responses:
Task: Data Analysis
Queen AI response: [Detailed instructions]
Subordinate AI response: [Sales data analysis]

Task: Web Search
Queen AI response: [Detailed instructions]
Subordinate AI response: [AI advancements]

```

```
git checkout -b feature/YourFeature
```

Commit Your Changes

```
Copy code
git commit -m "Add your feature"
```
Push to the Branch

```bash
Copy code
git push origin feature/YourFeature
```

Open a Pull Request

Please ensure your code follows the project's coding standards and includes relevant tests.

## Open-Source
Open-Source, you can  add or upgrade any code.

## License
This project is licensed under the MIT License.

## Acknowledgements
- OpenAI for providing powerful language models.
- The open-source community for their invaluable tools and libraries.

#### Disclaimer: Ensure that you comply with all relevant terms of service and usage policies for the APIs and tools used in this project.
