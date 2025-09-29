# GitHub Copilot Teaching Mode

A custom chat mode for GitHub Copilot that transforms it into an intelligent programming teacher. This mode provides personalized explanations, interactive learning experiences, and step-by-step guidance for programming concepts.

## Features

- **Adaptive Teaching**: Automatically adjusts explanations based on your knowledge level
- **Interactive Learning**: Supports quiz mode and guided project building
- **Multi-Tool Integration**: Uses web search, code execution, and file reading capabilities
- **Step-by-Step Guidance**: Breaks down complex programming concepts into digestible parts
- **Hands-On Practice**: Suggests coding exercises and real projects

## Installation

### Prerequisites

- VS Code version 1.101 or later (custom chat modes are in preview)
- GitHub Copilot subscription (Individual, Business, or Enterprise)
- VS Code with GitHub Copilot extension installed
- Access to GitHub Copilot Chat

### Installing the Teaching Chat Mode

1. **Clone or Download this Repository**
   ```bash
   git clone https://github.com/mnriem/github-copilot-for-teaching.git
   cd github-copilot-for-teaching
   ```

2. **Install the Chat Mode**
   
   VS Code supports custom chat modes through `.chatmode.md` files. This repository is configured to automatically expose the chat mode:

   **Option A: Use This Repository Directly (Recommended)**
   - The chat mode is automatically available when you have this repository open in VS Code
   - VS Code automatically discovers chat modes in the `.github/chatmodes/` directory
   - No additional installation steps required!

   **Option B: Copy to Your Own Project (Workspace-level)**
   - Copy the `.github/chatmodes/` directory to your own repository
   - Include the `Teach Programming.chatmode.md` file in the same structure
   - The chat mode will be available when working in that project

   **Option C: User Profile Installation (Cross-workspace)**
   - Copy the `Teach Programming.chatmode.md` file to your VS Code user profile folder
   - This makes the chat mode available across all your workspaces
   - Use the Command Palette: "Chat: New Mode File" and select "User profile"

3. **Restart VS Code (if needed)**
   - If you copied files manually, restart VS Code to ensure the new chat mode is loaded
   - For Option A, the mode should be immediately available when opening this repository

4. **Verify Installation**
   - Open GitHub Copilot Chat (Ctrl+Shift+I / Cmd+Shift+I on macOS, Ctrl+Alt+I on Windows/Linux)
   - Click the chat mode dropdown at the top of the Chat view
   - "Teach Programming" should appear in the list of available modes
   - Select it to activate the teaching mode

## Usage

### Activating the Teaching Mode

Once installed, you can activate the teaching mode:

1. **Mode Dropdown**: Open the Chat view and select "Teach Programming" from the chat mode dropdown
2. **Command Palette**: Use "Chat: Switch Chat Mode" and select "Teach Programming"
3. **Automatic Discovery**: The mode is automatically available when you have this repository open

### Example Interactions

**Learning a New Concept:**
```
Can you explain what recursion is and show me some examples?
```

**Quiz Mode:**
```
I want to test my understanding of Python functions. Can you quiz me?
```

**Project Mode:**
```
Help me build a simple web scraper step by step
```

**Code Review and Learning:**
```
Can you review this code and explain what it does?
[paste your code]
```

*Note: Make sure "Teach Programming" mode is selected in the chat mode dropdown before asking these questions.*

## Chat Mode Configuration

The teaching mode is configured with the following capabilities:

- **Web Search**: Finds up-to-date programming resources and documentation
- **Code Execution**: Runs code examples to demonstrate concepts in real-time
- **File Reader**: Analyzes code files and provides detailed explanations

## Teaching Modes Available

### 1. Explanation Mode (Default)
- Provides clear, level-appropriate explanations
- Uses examples and analogies
- Adapts to your current knowledge level

### 2. Quiz Mode
- Tests your understanding with interactive questions
- Provides immediate feedback
- Offers additional explanations for incorrect answers

### 3. Project Mode
- Guides you through building real projects
- Explains each step and code component
- Encourages best practices

## Customization

You can customize the teaching mode by editing the `Teach Programming.chatmode.md` file in the `.github/chatmodes/` directory:

1. **Modify the Description**: Change the teaching style or focus areas
2. **Adjust Tools**: Add or remove available tools based on your needs
3. **Update Instructions**: Modify the teaching approach or add specific subjects

Example customization for web development focus:
```markdown
---
description: 'A specialized web development teacher that focuses on HTML, CSS, JavaScript, and modern frameworks...'
tools: [
    "web-search",
    "code-execution",
    "file-reader"
]
---
```

## Troubleshooting

### Chat Mode Not Appearing
- Ensure you're using VS Code version 1.101 or later
- Check the chat mode dropdown in the Chat view - custom modes appear there
- For workspace modes: ensure the `.github/chatmodes/` directory exists with the `.chatmode.md` file
- For user profile modes: use "Chat: Configure Chat Modes" to verify installation
- Restart VS Code if you just added the chat mode file

### Limited Functionality
- Verify your GitHub Copilot subscription includes chat features
- Check that all required tools are enabled in your Copilot settings

### Performance Issues
- Some features require internet connectivity for web search
- Code execution depends on your local development environment

## Contributing

Feel free to contribute improvements to this teaching mode:

1. Fork the repository
2. Create a feature branch
3. Submit a pull request with your enhancements

## License

This project is open source and available under the [MIT License](LICENSE).

## Support

For issues or questions:
- Create an issue in this repository
- Check GitHub Copilot documentation for general chat mode support
- Review VS Code extension troubleshooting guides

---

**Happy Learning! 🚀**

Transform your coding journey with personalized, intelligent programming instruction powered by GitHub Copilot.