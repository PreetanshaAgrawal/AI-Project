# Chat Bot Streaming Client

This is a simple Python project that demonstrates interacting with a chat API via HTTP POST requests. It sends a query to a local API endpoint and streams back responses. The code also includes commented-out sections for using the Ollama library as an alternative approach.

## Features

- Sends a JSON payload containing:
  - The model identifier (e.g., `llama3.2:latest`)
  - An array of messages (starting with a user message)
- Posts to the chat endpoint running on `http://localhost:11434/api/chat`.
- Streams the response line-by-line and prints the assistant's message content to the console.
- Provides basic error handling based on the response status.

## Requirements

- Python 3.x
- `requests` library (install via `pip install requests`)

## Usage

1. Make sure the chat API server is running on `http://localhost:11434`.
2. Run the script:
   ```sh
   python main.py
   ```
3. The script will send a predefined user query ("What is python?") to the API and print out the streaming response.

## Notes

- The script uses the `requests` library's streaming capabilities to iteratively process the response.
- There is an alternative (commented) code block at the top that shows how one could integrate with the Ollama library if desired.
- Adjust the payload or API endpoint as needed for your specific setup.

Happy coding!