# Blog Research and Writing Automation with CrewAI

This repository demonstrates a modular approach to automate researching and writing tech-focused blogs by leveraging YouTube videos. It employs the CrewAI library to manage agents and tasks, integrating a YouTube tool to gather content effectively.

## Features

- **Blog Researcher Agent**: Extracts detailed information from YouTube videos for a given topic.
- **Blog Writer Agent**: Crafts engaging blog content from the extracted YouTube video information.
- **Sequential Task Execution**: Ensures research and writing tasks are performed in a logical order.
- **Memory and Caching**: Maintains context and optimizes performance with in-built memory and caching.

## File Structure

- **`agents.py`**: Defines two agents - Blog Researcher and Blog Writer, each with distinct roles and goals.
- **`crew.py`**: Configures the Crew with agents and tasks, defining task execution processes.
- **`tasks.py`**: Sets up research and writing tasks, with descriptions, expected outputs, and tools.
- **`tools.py`**: Includes the YouTube tool used for fetching video information from a specific channel.

## Requirements

This project requires Python 3.8 or higher.

### Install dependencies
Create a `requirements.txt` file to manage dependencies.

```plaintext
crewai
crewai-tools
dotenv
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

## Environment Variables

Use a `.env` file to securely manage sensitive configurations like API keys. Ensure the following variables are set in your `.env` file:

```plaintext
OPENAI_API_KEY=<your_openai_api_key>
OPENAI_MODEL_NAME=gpt-4-0125-preview
```

## Usage

1. **Setup Agents**: Define the Blog Researcher and Blog Writer agents in `agents.py`.
2. **Configure Tasks**: Specify the research and writing tasks in `tasks.py`.
3. **Run the Process**:
    - Use `crew.py` to initialize the Crew and start task execution.
    - Pass the desired topic as input:

    ```python
    result = crew.kickoff(inputs={'topic': 'AI VS ML VS DL vs Data Science'})
    print(result)
    ```

4. **Output**:
    - The result will include a blog post generated based on the topic, saved in `new-blog-post.md`.

## Contribution

Feel free to fork the repository and submit pull requests for any enhancements or bug fixes.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.
