# Contributing to Sourcing Cost Intelligence

We welcome contributions! Here's how you can help.

## Getting Started

1. Fork the repository
2. Clone your fork: `git clone https://github.com/YOUR-USERNAME/sourcing-cost-intelligence.git`
3. Create a feature branch: `git checkout -b feature/your-feature-name`
4. Make your changes
5. Test thoroughly
6. Commit with clear messages
7. Push to your fork
8. Open a Pull Request

## Development Setup

### Prerequisites
- A text editor (VS Code recommended)
- NW.js SDK (if building executables)
- Git

### Local Testing

1. Open `index.html` in a web browser to test UI changes
2. Use browser developer tools (F12) to debug JavaScript
3. For full NW.js testing, follow the NW.js documentation

## Code Guidelines

### HTML
- Use semantic HTML5 elements
- Maintain proper indentation
- Keep IDs and classes lowercase with hyphens

### CSS
- Use CSS variables for theming
- Mobile-first responsive design
- Maintain the dark mode support

### JavaScript
- Use clear, descriptive function names
- Add comments for complex logic
- Validate user input thoroughly
- Use const/let instead of var
- Keep functions focused and small

## Commit Message Guidelines

```
[TYPE] Brief description

Detailed explanation if needed.

Related: #issue-number (if applicable)
```

Types: feat, fix, refactor, docs, style, test, chore

Example:
```
[feat] Add PDF export functionality

Users can now export analysis reports as PDF files.
Implemented using pdfkit library.

Fixes #42
```

## Types of Contributions

### Bug Reports
- Describe the issue clearly
- Include steps to reproduce
- Mention your environment (OS, browser, file format)
- Attach sample data if possible

### Feature Requests
- Describe the desired functionality
- Explain the use case
- Suggest implementation approach if possible

### Documentation
- Fix typos and clarify existing docs
- Add examples
- Update technical specifications if needed

### Code Changes
- Follow the code guidelines above
- Test with various data sizes
- Ensure backward compatibility
- Update documentation as needed

## Pull Request Process

1. Update README.md if adding features
2. Test with sample Excel files
3. Ensure code follows guidelines
4. Update CHANGELOG.md
5. Link to related issues
6. Request review from maintainers

## Testing

### What to Test
- [ ] File upload (various formats)
- [ ] Data parsing and validation
- [ ] Filter operations
- [ ] Export functionality
- [ ] UI responsiveness
- [ ] Dark mode toggle
- [ ] Keyboard navigation
- [ ] Error handling

### Sample Data
Use representative procurement data with:
- Multiple suppliers
- Various material types
- Different buyers
- Different date ranges

## Questions?

- Open an issue with label "question"
- Check existing issues and discussions
- Review the technical documentation

Thank you for contributing! 🙏
