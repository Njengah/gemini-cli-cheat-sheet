# Contributing to Gemini CLI Cheatsheet

Thank you for your interest in contributing to the Gemini CLI Cheatsheet! 🎉

## Table of Contents

- [Ways to Contribute](#ways-to-contribute)
- [Getting Started](#getting-started)
- [Style Guide](#style-guide)
- [Code of Conduct](#code-of-conduct)

## Ways to Contribute

### 🐛 Report Bugs or Issues

- Found a command that doesn't work? Report it!
- Spotted a typo? Let us know!
- Missing information? Tell us what's needed!

### 📝 Improve Documentation

- Add missing commands
- Improve existing explanations
- Add examples and use cases
- Fix formatting issues

### ✨ Add New Content

- New commands or features
- Better examples
- Useful tips and tricks
- Workflow demonstrations

### 🔧 Test and Validate

- Test commands on different platforms
- Verify command syntax
- Check for deprecated commands

## Getting Started

1. **Fork the repository**

   ```bash
   git clone https://github.com/yourusername/gemini-cli-cheatsheet.git
   cd gemini-cli-cheatsheet
   ```

2. **Create a feature branch**

   ```bash
   git checkout -b feature/your-feature-name
   ```

3. **Make your changes**
   - Edit the relevant markdown files
   - Follow the style guide below

4. **Test your changes**
   - Ensure commands work as expected
   - Check markdown formatting

## Style Guide

### Command Format

Use consistent formatting for commands:

```markdown
### Section Title
```bash
command --flag value                 # Description
another-command                      # Another description
```

### Section Structure

Each level should follow this pattern:

```markdown
## 🟢 Level X: Title
*Brief description*

### Subsection
```bash
# Commands here
```

### Additional notes or explanations

### Documentation Standards

1. **Commands must be tested** - Don't add commands you haven't verified
2. **Include descriptions** - Every command should have a clear explanation
3. **Use proper markdown** - Follow consistent formatting
4. **Group related commands** - Keep similar commands together
5. **Be concise** - Keep descriptions short and clear

### Example Format

```markdown
### File Operations
```bash
gemini @file.txt                     # Include file in context
gemini @folder/                      # Include entire folder
gemini --model gemini-1.5-pro        # Switch to Pro model
```

**Note:** The `@` symbol is used for file inclusion, while `--model` changes the active model.

```markdown

## Testing Commands

Before submitting, please:

1. **Test on your system**
   - Verify commands work as documented
   - Check for any OS-specific issues

2. **Check command syntax**
   - Ensure proper formatting
   - Verify flags and parameters

3. **Test examples**
   - Make sure example outputs are realistic
   - Remove any sensitive information

### Testing Checklist
- [ ] Command runs without errors
- [ ] Output matches description
- [ ] Works on intended platform (Windows/Mac/Linux)
- [ ] No sensitive information exposed

## Submitting Changes

1. **Commit your changes**
   ```bash
   git add .
   git commit -m "Add: New section on advanced file operations"
   ```

2. **Push to your fork**

   ```bash
   git push origin feature/your-feature-name
   ```


3. **Create a Pull Request**
   - Use a clear title and description
   - Reference any related issues
   - Explain what you've added/changed

### Pull Request Template

```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature/command
- [ ] Documentation update
- [ ] Code cleanup

## Testing
- [ ] Commands tested locally
- [ ] Documentation reviewed
- [ ] Examples verified

## Additional Notes
Any additional context or notes
```

## Review Process

1. **Automated checks** - Basic formatting and links
2. **Manual review** - Content accuracy and style
3. **Testing** - Commands verified by maintainers
4. **Merge** - Changes integrated into main branch

## Code of Conduct

### Our Standards

- Be respectful and inclusive
- Focus on constructive feedback
- Help others learn and grow
- Maintain a welcoming environment

### Unacceptable Behavior

- Harassment or discrimination
- Toxic or disruptive behavior
- Sharing inappropriate content
- Spamming or off-topic discussions

## Questions or Need Help?

- **GitHub Issues** - For bugs and feature requests
- **GitHub Discussions** - For questions and general discussion
- **Email** - [your-email@example.com] for private matters

## Recognition

Contributors will be recognized in:

- README.md contributors section
- Release notes for significant contributions
- Special mentions for exceptional help

---

Thank you for helping make this cheatsheet better for everyone!
