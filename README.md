# Gemini CLI Cheatsheet

![Alt text](images/gemini_cli_cheat_sheet.png)

> **Your complete guide to mastering Gemini CLI - from zero to hero in minutes!**

After testing Gemini CLI I've developed this comprehensive cheat sheet that will take you from basic to advanced user without wasting time. Whether you're completely new to Gemini CLI or looking to master advanced features, this guide has you covered.

## Quick Start

```bash
# Install globally
npm install -g @google/gemini-cli

# Or run without installing
npx @google/gemini-cli

# Launch interactive CLI
gemini
```

## 📚 Table of Contents

- [🟢 Level 1: Basic Commands](#-level-1-basic-commands)
- [🟡 Level 2: Intermediate Commands](#-level-2-intermediate-commands)
- [🟠 Level 3: Advanced Commands](#-level-3-advanced-commands)
- [🔴 Level 4: Expert Commands](#-level-4-expert-commands)
- [🔵 Level 5: Power User Commands](#-level-5-power-user-commands)
- [🟣 Level 6: Master Commands](#-level-6-master-commands)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

---

## 🟢 Level 1: Basic Commands

Essential commands to get started

### Installation & Getting Started

```bash
npm install -g @google/gemini-cli     # Install globally
npx @google/gemini-cli                # Run without installing
gemini                                # Launch interactive CLI
gemini --version                      # Check version
```

### Basic Navigation

```bash
/about                    # Check version
/help                     # Show available commands
/tools                    # List available tools
/clear                    # Clear current conversation
/quit                     # Exit CLI (or Ctrl+C)
```

### Basic File Operations

```bash
ReadFolder                # Read folder contents
ReadFile                  # Read single file
ReadManyFiles             # Read multiple files
```

### File System Operations - Natural Language

```bash
# Using natural language
"List files in current directory"
"Show me the contents of package.json"
"Find all HTML files in this project"
```

### Basic Tools

```bash
/tools                     # List available tools
/tools desc                # Show tool descriptions
/tools nodesc              # Hide tool descriptions
```

### Basic Configuration

```bash
/theme                     # Change visual theme
/auth                      # Change authentication method
/editor                    # Select supported editors
```

### Basic Shell Command

```bash
shell ls                    # List directory contents
```

### Keyboard Shortcuts

```bash
Enter                       # Send message
Esc                         # Cancel operation
Ctrl+L                      # Clear screen
Ctrl+C x2                   # Exit CLI / Quit application
Ctrl+T                      # Toggle tool descriptions
Up/Down                     # Cycle through prompt history || Tools
Alt+Left/Right              # Jump through words
```

### Troubleshooting & Tips

```bash
/privacy                   # View privacy settings
/bug                       # Submit bug report
/docs                      # Open documentation
/about                     # Check version info
```

---

## 🟡 Level 2: Intermediate Commands

File management and basic customization

### File Management

```bash
/tools 
read_folder <directory>              # Read entire folder
@src/my_project/                     # Read entire project directory
@path/to/file.txt                    # Read specific file
@My\ Documents/file.txt              # Handle spaces in paths
```

### Conversation Management

```bash
/chat save <tag>                     # Save current conversation
/chat resume <tag>                   # Resume saved conversation
/chat list                           # List saved conversations
/compress                            # Compress chat context to summary
```

### Model Configuration

```bash
--model                             # Show current model
--model gemini-1.5-flash            # Switch to Flash (fastest)
--model gemini-1.5-pro              # Switch to Pro (most capable)
--model gemini-1.5-pro-002          # Switch to latest Pro version
```

### Memory Management

```bash
/memory show                        # Show current memory context
/memory add <text>                  # Add text to memory
/memory refresh                     # Reload GEMINI.md files
```

---

## 🟠 Level 3: Advanced Commands

Configuration, context, and power features

### Execution Methods

```bash
gemini -p "your prompt here"         # Direct prompt execution
gemini -y                            # Auto-confirm all prompts (YOLO mode)
gemini --sandbox                     # Run in sandbox mode
gemini --checkpointing               # Enable checkpointing
```

### Statistics & Monitoring

```bash
/stats                               # Show session statistics
/stats model                         # Show model usage stats
/stats tools                         # Show tool usage stats
```

### Shell Integration

```bash
!<shell_command>                     # Execute shell command
!ls -la                              # Example: list files
!git status                          # Example: git status
!                                    # Toggle shell mode
```

### Context Management

```bash
@<path_to_file>                     # Include file content in prompt
@<directory>                        # Include directory content
@README.md                          # Example: include README
@src/myFile.ts                      # Add specific file to context
@folder/                            # Add entire folder to context
```

---

## 🔴 Level 4: Expert Commands

MCP servers, automation, and advanced integrations

### MCP Server Management

```bash
/mcp list                 # List available MCP servers
/mcp desc                 # Show detailed MCP descriptions
/mcp nodesc               # Hide MCP descriptions
/mcp schema               # Show full JSON schema
```

### Advanced Execution

```bash
npx @google/gemini-cli                          # Run latest version
npx https://github.com/google-gemini/gemini-cli  # Run from GitHub
```

### Sandbox Configuration

```bash
gemini -s                           # Enable sandboxing (short flag)
export GEMINI_SANDBOX=true          # Environment variable
export GEMINI_SANDBOX=docker        # Specify Docker
export GEMINI_SANDBOX=podman        # Specify Podman
export GEMINI_SANDBOX=sandbox-exec  # Specify sandbox-exec (macOS)
```

### Advanced File Operations

```bash
# Git-aware filtering automatically excludes:
# node_modules/, dist/, .env, .git/
# Can be configured via fileFiltering settings
```

---

## 🔵 Level 5: Power User Commands

Advanced workflows and integrations

### Container-based Execution

```bash
docker run --rm -it us-docker.pkg.dev/gemini-code-dev/gemini-cli/sandbox:0.1.1
gemini --sandbox -y -p "your prompt here"
```

### Development Mode

```bash
npm run start                        # Hot-reloading development
npm link packages/cli                # Link local package globally
```

### Environment Variables

```bash
export SEATBELT_PROFILE=permissive-open     # macOS sandbox profile
export SEATBELT_PROFILE=restrictive-closed  # Strict macOS sandbox
export SANDBOX_SET_UID_GID=true             # Force host UID/GID
export DEBUG=1                              # Enable debug mode
```

### Checkpointing & Restore

```bash
/restore                             # List available checkpoints
/restore <checkpoint_file>           # Restore specific checkpoint
/restore 2025-06-22T10-00-00_000Z-my-file.txt-write_file
```

---

## 🟣 Level 6: Master Commands

Advanced automation and custom workflows

### Bug Reporting & Issues

```bash
/bug "Issue description"             # File GitHub issue
                                     # Customizable via bugCommand setting
```

### Extension Management

```bash
# Extensions loaded from:
# <workspace>/.gemini/extensions
# <home>/.gemini/extensions
```

### Advanced Settings (settings.json)

```json
{
  "sandbox": "docker",
  "checkpointing": { "enabled": true },
  "bugCommand": "custom command",
  "mcpServers": {
    "my-server": {
      "command": "node my-server.js"
    }
  }
}
```

---

## 🤝 Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

### Ways to Contribute

- 🐛 Report bugs or issues
- 📝 Improve documentation
- ✨ Add new commands or examples
- 🔧 Test commands and report results

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ⭐ Support

If this cheatsheet helped you, please give it a star! It helps others discover this resource.

---

## 📞 Connect

- **Contact**: [Email](mail.njengah@gmail.com)

---

Last updated: July 2025
