# Commands.com

The platform for creating, sharing, and discovering reusable AI commands and prompts with Model Context Protocol (MCP) integration.

## 🚀 Quick Start: Create Your First MCP Server

Get started in seconds with our MCP creation tool:

```bash
npx create-commands-mcp my-server
cd my-server
npm install
npm start
```

That's it! You now have a working MCP server ready to customize.

## 📋 What is Commands.com?

Commands.com is a platform that makes it easy to:

- **Create powerful AI commands** with parameterized templates and MCP server integration
- **Share your prompts** with the developer community
- **Discover curated solutions** from our marketplace
- **Build MCP servers** using our intuitive creation tools
- **Monetize your work** through our creator program

## 🛠 Commands & Prompts YAML Format

Commands.com uses a powerful YAML format to define reusable AI commands and prompts:

### Basic Structure

```yaml
commands:
  - name: "Screenshot Website"
    type: "prompt"              # Either "prompt" or "command"
    category: "productivity"    
    description: "Take a screenshot of any website URL"
    content: |
      Please take a screenshot of the following website: {{url}}
      
      Capture the full page and save it as a high-quality image.
    inputParameters:
      - name: "url"
        label: "Website URL"
        description: "The URL of the website to screenshot"
        type: "text"
        required: true
        defaultValue: ""
    mcpRequirements:
      - serverId: "puppeteer"
        tier: "required"
        version: "1.0.0"
    aiPlatform: "claude-code@2025.06"
```

### Input Parameters

Define template variables that users can customize:

```yaml
inputParameters:
  - name: "parameter_name"      # Used in {{parameter_name}} templating
    label: "Human Readable Label"
    description: "Description of the parameter"
    type: "text"               # Types: text, path, number, select, textarea
    required: true
    defaultValue: "default"
    options: ["option1", "option2"]  # For select type only
```

**Available Types:**
- `text` - Single line text input
- `textarea` - Multi-line text input
- `path` - File or directory path
- `number` - Numeric input
- `select` - Dropdown selection (requires `options`)

### MCP Requirements

Specify which MCP servers your command needs:

```yaml
mcpRequirements:
  - serverId: "puppeteer"      # Curated server ID
    tier: "required"           # "required" or "optional"
    version: "1.0.0"          # Optional minimum version
```

**Available Curated Servers:**
- `puppeteer` - Browser automation
- `memory` - Persistent memory storage
- `filesystem` - File system operations
- `sqlite` - SQLite database access
- `github` - GitHub integration
- `calendar` - Calendar management
- `email` - Email functionality
- [View all 22+ servers](https://commands.com/mcp-servers)

## 🎯 Example Commands

### Web Research Command
```yaml
- name: "Research and Document"
  type: "command"
  category: "research"
  description: "Research topic with screenshots and notes"
  content: |
    Research {{topic}} by:
    1. Taking screenshots of {{num_sites}} relevant websites
    2. Storing key findings in memory
    3. Creating a summary document
  inputParameters:
    - name: "topic"
      label: "Research Topic"
      type: "text"
      required: true
    - name: "num_sites"
      label: "Number of Sites"
      type: "number"
      required: true
      defaultValue: "5"
  mcpRequirements:
    - serverId: "puppeteer"
      tier: "required"
    - serverId: "memory"
      tier: "required"
    - serverId: "filesystem"
      tier: "optional"
  aiPlatform: "claude-code@2025.06"
```

### Database Query Prompt
```yaml
- name: "SQL Report Generator"
  type: "prompt"
  category: "development"
  description: "Generate reports from SQL queries"
  content: |
    Connect to {{database_path}} and run the following query:
    
    {{query}}
    
    Format the results as a {{format}} report.
  inputParameters:
    - name: "database_path"
      label: "Database Path"
      type: "path"
      required: true
    - name: "query"
      label: "SQL Query"
      type: "textarea"
      required: true
    - name: "format"
      label: "Output Format"
      type: "select"
      required: true
      defaultValue: "markdown"
      options: ["markdown", "csv", "json", "html"]
  mcpRequirements:
    - serverId: "sqlite"
      tier: "required"
  aiPlatform: "claude-code@2025.06"
```

## 📚 Documentation

### Getting Started
- **[Quick Start Guide](https://commands.com/docs/getting-started)** - Create your first command
- **[YAML Schema Reference](https://commands.com/docs/yaml-schema)** - Complete format documentation
- **[Template Variables](https://commands.com/docs/templates)** - Using input parameters

### MCP Integration
- **[MCP Overview](https://commands.com/docs/mcp/overview)** - Understanding Model Context Protocol
- **[Available Servers](https://commands.com/mcp-servers)** - Browse all 22+ curated servers
- **[Creating MCP Servers](https://commands.com/docs/mcp/create)** - Build custom servers

### Publishing & Monetization
- **[Publishing Guide](https://commands.com/docs/publishing)** - Share with the community
- **[Creator Program](https://commands.com/docs/creators)** - Monetization options
- **[Best Practices](https://commands.com/docs/best-practices)** - Quality guidelines

## 🚦 Getting Started

1. **Create your commands.yaml**
   ```yaml
   commands:
     - name: "My First Command"
       type: "prompt"
       category: "productivity"
       description: "A helpful command"
       content: "Do something with {{input}}"
       inputParameters:
         - name: "input"
           label: "Input"
           type: "text"
           required: true
       aiPlatform: "claude-code@2025.06"
   ```

2. **Test locally**
   Use the Commands.com CLI or Claude Desktop to test

3. **Publish to GitHub**
   Add `commands.yaml` to your repository

4. **Import to Commands.com**
   Connect your GitHub repo on the platform

5. **Share with the community**
   Your commands are now discoverable!

## 🤝 Community

- **[Discord](https://discord.gg/commands-com)** - Join our developer community
- **[GitHub Discussions](https://github.com/commands-com/discussions)** - Technical discussions
- **[Showcase](https://commands.com/showcase)** - Featured commands and creators

## 💡 Use Cases

Commands.com enables powerful workflows:

- **Automated Testing** - Run test suites with parameterized inputs
- **Content Generation** - Create blogs, docs, and reports
- **Code Analysis** - Review and refactor codebases
- **Data Processing** - Transform and analyze datasets
- **DevOps Automation** - Deploy and monitor infrastructure
- **Research Tools** - Gather and synthesize information

## 📈 For Creators

### Monetization Options
- **Free Tier** - Share open-source commands
- **Premium Commands** - Charge for advanced functionality
- **Subscriptions** - Recurring revenue models
- **Custom Solutions** - Enterprise offerings

### Creator Benefits
- **85% Revenue Share** - Keep most of what you earn
- **Direct Payments** - Via Stripe Connect
- **Analytics Dashboard** - Track usage and earnings
- **Marketing Support** - Featured placement opportunities

## 🔗 Resources

- **[Commands.com](https://commands.com)** - Main platform
- **[Documentation](https://commands.com/docs)** - Complete docs
- **[NPM Package](https://www.npmjs.com/package/create-commands-mcp)** - MCP creation tool
- **[GitHub](https://github.com/Commands-com/create-commands-mcp)** - Source code
- **[Blog](https://commands.com/blog)** - Updates and tutorials

## 🏷 Tags

`mcp` `model-context-protocol` `claude` `ai-commands` `ai-prompts` `automation` `developer-tools` `yaml` `cli`

---

**Start building powerful AI commands today at [Commands.com](https://commands.com)**

Built with ❤️ by the Commands.com team