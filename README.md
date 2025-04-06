# MCP Gmail and Calculator Application

A Python application that uses the Model Context Protocol (MCP) to interact with Gmail and perform mathematical calculations. This application demonstrates the use of multiple MCP servers working together.

## Features

- Gmail Operations:
  - Send emails
  - Read unread emails
  - Trash emails
  - Open emails in browser
  - Mark emails as read
- Mathematical Operations:
  - Basic arithmetic (add, subtract, multiply, divide)
  - Advanced operations (power, square root, etc.)
  - List operations
  - Special functions (factorial, trigonometry)

## Prerequisites

- Python 3.7 or higher
- Google account with Gmail
- Google Cloud Project with Gmail API enabled

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd mcp_gmail
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

4. Set up Google API credentials:
   - Go to Google Cloud Console
   - Create a new project or select existing one
   - Enable Gmail API
   - Create OAuth 2.0 credentials
   - Download the credentials and save as `credentials.json` in the project root

## Configuration

1. Place your Google API credentials:
   - Save your OAuth credentials as `credentials.json` in the project root
   - First run will generate `token.json` after authentication

Note: Both `credentials.json` and `token.json` are gitignored for security. Keep these files secure and never commit them to version control.

## Usage

Run the main application:
```bash
python talk2mcp-2.py
```

The application will:
1. Connect to both MCP servers (Gmail and Calculator)
2. Initialize the sessions
3. Authenticate with Gmail (first run only)
4. Process commands for both email and mathematical operations

## Project Structure

- `server.py`: Gmail MCP server implementation and email tools
- `example2-3.py`: Calculator MCP server with math tools
- `talk2mcp-2.py`: Main client application that interfaces with both servers
- `.gitignore`: Specifies files to ignore in version control
- `requirements.txt`: Python package dependencies

## Available Tools

### Gmail Tools
- `send_email(recipient_id, subject, message)`: Send an email
- `get_unread_emails()`: Get list of unread emails
- `read_email(email_id)`: Read a specific email
- `trash_email(email_id)`: Move email to trash
- `open_email(email_id)`: Open email in browser

### Math Tools
- `add(a, b)`: Add two numbers
- `subtract(a, b)`: Subtract two numbers
- `multiply(a, b)`: Multiply two numbers
- `divide(a, b)`: Divide two numbers
- `power(a, b)`: Calculate power
- `sqrt(a)`: Calculate square root
- Additional mathematical functions...

## Error Handling

The application includes comprehensive error handling for:
- Gmail API authentication and operations
- Mathematical operations
- Server connections
- Tool execution
- Parameter validation

## Security

- OAuth 2.0 authentication for Gmail
- Secure token storage
- Credentials and tokens are not committed to version control
- Environment-based configuration

## Contributing

Feel free to submit issues and enhancement requests!
 
