# Commands.com

Welcome to the official GitHub repository for **Commands.com** - the platform for sharing and discovering reusable CLI commands and AI prompts.

## 🚀 What is Commands.com?

Commands.com is a community-driven platform where developers and creators can:

- **Share CLI commands and scripts** with automatic GitHub synchronization
- **Create and distribute AI prompts** with dynamic placeholders
- **Monetize content** through direct creator payments via Stripe Connect
- **Discover solutions** from a growing library of community contributions
- **Collaborate** with other developers and prompt engineers

## 📋 Table of Contents

- [Platform Features](#-platform-features)
- [Getting Started](#-getting-started)
- [Community Guidelines](#-community-guidelines)
- [Contributing](#-contributing)
- [Commands.yaml Format](#-commandsyaml-format)
- [Support](#-support)
- [Resources](#-resources)

## ✨ Platform Features

### For Creators
- **GitHub Integration**: Automatic sync of commands.yaml files from your repositories
- **Direct Payments**: Receive 85% of sales directly via Stripe Connect
- **Content Management**: Organize commands and prompts with categories and tags
- **Analytics**: Track performance and revenue in real-time
- **Global Reach**: Accept payments in 40+ countries and multiple currencies

### For Users
- **Search & Discovery**: Find exactly what you need with powerful search
- **Try Before You Buy**: Preview content before purchasing
- **Copy & Execute**: One-click copying with syntax highlighting
- **Dynamic Prompts**: Customize AI prompts with interactive placeholders
- **Purchase History**: Access all your bought content anytime

## 🎯 Getting Started

### As a User
1. Visit [Commands.com](https://commands.com)
2. Browse the catalog or search for specific solutions
3. Try free content or purchase premium commands/prompts
4. Copy commands directly to your terminal or AI platform

### As a Creator
1. **Set up your profile** at [Commands.com/profile](https://commands.com/profile)
2. **Connect GitHub** to sync your repositories automatically
3. **Create commands.yaml files** in your repositories
4. **Connect Stripe** to receive direct payments
5. **Start earning** from your shared knowledge

### Repository Setup
```bash
# Clone your repository
git clone https://github.com/yourusername/your-repo.git
cd your-repo

# Create a commands.yaml file
touch commands.yaml

# Add your first command
cat > commands.yaml << 'EOF'
commands:
  - name: hello-world
    description: "A simple hello world command"
    type: cli
    category: "Development"
    main: scripts/hello.sh
    languageTag: "bash"
EOF

# Create the script
mkdir -p scripts
echo '#!/bin/bash\necho "Hello, Commands.com!"' > scripts/hello.sh
chmod +x scripts/hello.sh

# Commit and push
git add .
git commit -m "Add first command"
git push origin main
```

## 🤝 Community Guidelines

We're building an inclusive, helpful community. Please:

### ✅ Do
- Be respectful and constructive in all interactions
- Help others learn and solve problems
- Share knowledge and best practices openly
- Give proper credit for inspiration or derived work
- Report security vulnerabilities responsibly
- Follow our [Code of Conduct](CODE_OF_CONDUCT.md)

### ❌ Don't
- Share malicious, harmful, or insecure code
- Spam or promote unrelated content
- Harass, discriminate, or exclude others
- Share personal or confidential information
- Violate intellectual property rights
- Post off-topic content in discussions

## 🛠 Contributing

We welcome contributions to improve the platform! Here's how you can help:

### Platform Development
- Report bugs in [Issues](https://github.com/commands-com/discussions/issues)
- Suggest features in [Discussions](https://github.com/commands-com/discussions/discussions)
- Contribute to documentation improvements

### Content Creation
- Share high-quality commands and prompts
- Improve existing content through collaboration
- Create educational content and tutorials

### Community Support
- Help answer questions in Discussions
- Welcome new community members
- Share the platform with fellow developers

## 📄 Commands.yaml Format

The `commands.yaml` file is the standard format for defining commands and prompts:

### Basic Structure
```yaml
commands:
  - name: unique-command-name
    description: "Clear description of what this does"
    type: cli  # or "prompt"
    category: "Development"
    main: path/to/script.sh
    languageTag: "bash"  # for CLI commands
    platformTag: "ChatGPT-4o"  # for AI prompts
    readme: path/to/README.md
    license: LICENSE
```

### Dynamic AI Prompts
```yaml
commands:
  - name: code-reviewer
    description: "AI prompt for thorough code reviews"
    type: prompt
    category: "Development"
    main: prompts/code-review.template
    platformTag: "ChatGPT-4o"
    placeholders:
      - name: LANGUAGE
        label: "Programming language"
        default: "JavaScript"
      - name: FOCUS_AREA
        label: "Review focus"
        default: "security and performance"
```

### Repository Configuration
```yaml
# Global settings for the entire repository
repository:
  license: LICENSE
  description: "My collection of useful development tools"
```

For complete documentation, visit [Commands.com/docs](https://commands.com/docs).

## 💬 Support

### Community Support
- **GitHub Discussions**: [Technical discussions and feature requests](https://github.com/commands-com/discussions/discussions)
- **Discord**: [Real-time community chat](https://discord.gg/commands-com)

### Direct Contact
- **General Support**: [support@commands.com](mailto:support@commands.com)
- **Business Inquiries**: [business@commands.com](mailto:business@commands.com)
- **Security Issues**: [security@commands.com](mailto:security@commands.com)

### Response Times
- **Discord/Community**: Usually within minutes during active hours
- **Email Support**: 24-48 hours for general inquiries
- **Security Issues**: Within 24 hours for urgent matters

## 📚 Resources

- **[Platform Documentation](https://commands.com/docs)**: Complete technical guides
- **[Getting Started Guide](https://commands.com/getting-started)**: New user walkthrough
- **[FAQs](https://commands.com/faqs)**: Common questions and answers
- **[Community Support](https://commands.com/community)**: Help and discussion channels

## 🏷 Tags

`cli` `commands` `automation` `ai-prompts` `developer-tools` `open-source` `community` `github-integration` `stripe-connect` `monetization`

## 📈 Stats

![GitHub Discussions](https://img.shields.io/badge/discussions-active-blue?logo=github)
![Community](https://img.shields.io/badge/community-growing-brightgreen)
![Platform](https://img.shields.io/badge/platform-live-success)

---

**Join thousands of developers sharing and discovering powerful commands and prompts at [Commands.com](https://commands.com)**

Built with ❤️ by the open source community
