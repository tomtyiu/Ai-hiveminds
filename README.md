HiveMindsAI
HiveMindsAI is a sophisticated AI orchestration framework designed to manage and delegate tasks across multiple AI agents seamlessly. Leveraging OpenAI's powerful language models and Tavily's advanced search capabilities, HiveMindsAI ensures efficient task moderation, delegation, and execution, making it ideal for complex projects that require coordinated AI interactions.

Table of Contents
Features
Prerequisites
Installation
Configuration
Usage
How It Works
Contributing
License
Acknowledgements
Features
Task Moderation: Ensures that all tasks adhere to predefined guidelines, preventing malicious or illegal activities.
Hierarchical AI Delegation: Utilizes a "Queen AI" to oversee and delegate tasks to subordinate and sub-subordinate AI agents.
Web Search Integration: Incorporates Tavily's search API to fetch real-time information from the web.
Code Interpretation: Includes a specialized code interpreter assistant for tasks involving programming or mathematical computations.
Extensible Architecture: Easily add or modify AI agents and functionalities to suit specific project needs.
Prerequisites
Before setting up HiveMindsAI, ensure you have the following:

Python 3.8+ installed on your system.
OpenAI API Key: Obtain from OpenAI.
Tavily API Key: Obtain from Tavily.
Serper API Key: Obtain from Serper.
Installation
Clone the Repository

'''
git clone https://github.com/yourusername/HiveMindsAI.git
cd HiveMindsAI
'''

Create a Virtual Environment

It's recommended to use a virtual environment to manage dependencies.

bash
Copy code
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
Install Dependencies

bash
Copy code
pip install -r requirements.txt
If a requirements.txt is not provided, you can install the necessary packages manually:

bash
Copy code
pip install openai requests tavily
Configuration
Set up the required environment variables to securely manage your API keys.

Create a .env File

In the root directory of the project, create a .env file:

bash
Copy code
touch .env
Add Your API Keys

Open the .env file in a text editor and add the following:

env
Copy code
OPENAI_API_KEY=your_openai_api_key
TAVILY_API_KEY=your_tavily_api_key
SERPER_API_KEY=your_serper_api_key
Load Environment Variables

Ensure that your Python script loads these environment variables. You can use the python-dotenv package for this purpose.

bash
Copy code
pip install python-dotenv
Then, modify your Python script to load the .env file:

python
Copy code
from dotenv import load_dotenv
load_dotenv()
Usage
HiveMindsAI is designed to be run as a standalone Python script. Follow these steps to start delegating tasks:

Run the Script

bash
Copy code
python main.py
Input Tasks

Enter Task Name: Provide a name for the task you want the AI to handle.
Enter Task Description: Describe the task in detail. Type 'done' when you have finished entering tasks.
AI Processing

Queen AI: Processes the main task and delegates it to subordinate AIs.
Subordinate AI: Executes the delegated task and can further delegate to sub-subordinate AIs if necessary.
Code Interpreter (Optional): If the task involves coding or mathematical computations, the code interpreter assistant will handle it.
View Summary

After all tasks are processed, a summary of tasks and their respective AI responses will be displayed.

How It Works
1. Task Moderation
Before any task is processed, it undergoes moderation to ensure compliance with safety and policy guidelines. The moderation function checks the task description for any prohibited content.

2. Guardian AI Task
The guardian_ai_task function assesses whether a task is allowed based on predefined guardrails. It ensures tasks are not malicious, illegal, or involve injection attacks.

3. Queen AI Task
The queen_ai_task function represents the central AI overseeing all operations. It delegates tasks to subordinate AIs by providing detailed instructions.

4. Subordinate AI Task
Subordinate AIs handle specific tasks as instructed by the Queen AI. They can further delegate sub-tasks to sub-subordinate AIs, ensuring efficient task management.

5. Code Interpreter Task
For tasks involving code or mathematics, the code_interpreter_task function utilizes a specialized assistant to write and execute code, providing accurate solutions.

6. Web Search Integration
The perform_web_search and tavily_search functions integrate Tavily's search API to fetch real-time information, enhancing the AI's response accuracy.

Example
Running the Script:

bash
Copy code
python main.py
Sample Interaction:

less
Copy code
Enter tasks for the Queen AI to delegate. Type 'done' when finished.
Enter task name: Data Analysis
Enter task description: Analyze the sales data for Q4 and provide insights.
Enter task name: Code Generation
Enter task description: Write a Python script to automate data cleaning.
Enter task name: done

HiveMindsAI processing queen task: {'Data Analysis'}
Queen AI response for Data Analysis:
[Queen AI's detailed instructions]

HiveMindsAI processing subordinate task: {'Data Analysis'}
Subordinate AI response for Data Analysis:
[Subordinate AI's analysis]

HiveMindsAI processing queen task: {'Code Generation'}
Queen AI response for Code Generation:
[Queen AI's detailed instructions]

HiveMindsAI processing subordinate task: {'Code Generation'}
Subordinate AI response for Code Generation:
[Subordinate AI's code script]

Code Interpreter response for Code Generation:
[Code execution results]

Summary of tasks and responses:

Task: Data Analysis
Queen AI response: [Queen AI's detailed instructions]
Subordinate AI response: [Subordinate AI's analysis]

Task: Code Generation
Queen AI response: [Queen AI's detailed instructions]
Subordinate AI response: [Subordinate AI's code script]
Code Interpreter response: [Code execution results]
Contributing
Contributions are welcome! Please follow these steps to contribute:

Fork the Repository

Create a Feature Branch

bash
Copy code
git checkout -b feature/YourFeature
Commit Your Changes

bash
Copy code
git commit -m "Add your feature"
Push to the Branch

bash
Copy code
git push origin feature/YourFeature
Open a Pull Request

Please ensure your code follows the project's coding standards and includes relevant tests.

License
This project is licensed under the MIT License.

Acknowledgements
OpenAI for providing powerful language models.
Tavily for their advanced search API.
Serper for search capabilities.
The open-source community for their invaluable tools and libraries.
Disclaimer: Ensure that you comply with all relevant terms of service and usage policies for the APIs and tools used in this project.
