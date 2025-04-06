# MCP Draw Application

A Python application that uses the Model Context Protocol (MCP) to interact with Freeform on macOS, allowing for automated drawing and text placement.

## Features

- Opens and manages Freeform application
- Creates new boards
- Draws squares with specified dimensions
- Adds text to squares
- Uses AppleScript for macOS automation
- Integrates with Model Context Protocol (MCP)

## Prerequisites

- macOS operating system
- Python 3.7 or higher
- Freeform application installed
- `cliclick` command-line tool installed (`brew install cliclick`)

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd mcp_draw
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On macOS/Linux
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Create a `.env` file in the project root and add your Gemini API key:
```
GEMINI_API_KEY=your_api_key_here
```

## Usage

Run the main application:
```bash
python talk2mcp-2.py
```

The application will:
1. Connect to the MCP server
2. Initialize the session
3. Process commands through the Gemini model
4. Execute drawing operations in Freeform

## Project Structure

- `example2-3.py`: Contains the MCP server implementation and tool definitions
- `talk2mcp-2.py`: Main client application that interfaces with the MCP server
- `.env`: Configuration file for API keys (create this file)

## Available Tools

- `open_freeform()`: Opens the Freeform application
- `create_board_in_freeform()`: Creates a new board in Freeform
- `create_square_in_freeform()`: Draws a square with specified dimensions
- `write_text_in_square_in_freeform(text)`: Adds text to the square

## Error Handling

The application includes comprehensive error handling for:
- Freeform application state
- Tool execution
- API communication
- Parameter validation

## Contributing

Feel free to submit issues and enhancement requests!
 
