# 🔍 OSINTBox Data

> **Community-driven repository of OSINT tools and resources**  
> Curated collection of Open Source Intelligence tools organized by category

[![Validation](https://img.shields.io/badge/validation-passing-brightgreen)](https://github.com/vixkram/OSINTBox-data/actions)
[![Contributors](https://img.shields.io/badge/contributors-welcome-blue)](#-contribute)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)

---

## 📁 Repository Structure

```
├── 📄 tools.json         # Core categories and tools (required)
├── ⚙️ widgets.json       # Widget configuration (optional)
└── 📋 schema/            # JSON schemas for validation
    ├── tools.schema.json
    └── widgets.schema.json
```

### 🔧 File Descriptions

| File | Status | Description |
|------|--------|-------------|
| `tools.json` | **Required** | Main database of OSINT tools organized by categories |
| `widgets.json` | *Optional* | Configuration for dashboard widgets (world clock, feeds, etc.) |

---

## 🤝 Contribute

We welcome contributions from the OSINT community! Here's how you can help:

### 📝 Quick Start
1. **Fork** this repository
2. **Edit** `tools.json` (and `widgets.json` if needed)
3. **Open** a Pull Request
4. **Wait** for automated validation to pass

> 💡 **Tip**: All submissions are automatically validated through our CI pipeline

### ✅ Local Validation (Optional)

Want to test your changes before submitting? Follow these steps:

```bash
# 1. Install validation tools
npm i -D ajv-cli@5

# 2. Validate your changes
npx ajv validate -s schema/tools.schema.json -d tools.json --all-errors

# 3. Validate widgets (if modified)
if [ -f widgets.json ]; then 
  npx ajv validate -s schema/widgets.schema.json -d widgets.json --all-errors
fi
```

---

## 📊 Data Schema

### 🛠️ Tool Object
```json
{
  "name": "Tool Name",
  "url": "https://example.com",
  "description": "Brief description (optional)",
  "icon": "https://www.google.com/s2/favicons?domain=example.com&sz=64"
}
```

### 📂 Category Object
```json
{
  "category": "Category Name",
  "tools": [
    // Array of tool objects
  ]
}
```

---

## 💡 Best Practices

### ✏️ Writing Guidelines
- **Descriptions**: Only include if they add clear value beyond the tool name
- **Icons**: Use favicon URLs for consistency
  ```
  https://www.google.com/s2/favicons?domain=example.com&sz=64
  ```
- **URLs**: Ensure all links are active and lead to the correct resources

### 🎯 Quality Standards
- ✅ Verify tool functionality before adding
- ✅ Use clear, descriptive names
- ✅ Categorize appropriately
- ✅ Test all URLs

---

## 🚀 Getting Started

1. **Browse** the `tools.json` file to see existing categories and tools
2. **Identify** gaps or new tools to add
3. **Follow** the schema structure
4. **Submit** your contribution via Pull Request

---

## 📞 Support

- 🐛 **Issues**: Report bugs or suggest improvements
- 💬 **Discussions**: Join community conversations
- 📖 **Documentation**: Check our wiki for detailed guides

---

## 🙏 Acknowledgments

Thanks to all contributors who help maintain and expand this valuable OSINT resource!

---

<div align="center">

**[⭐ Star this repo](https://github.com/your-repo) | [🍴 Fork it](https://github.com/your-repo/fork) | [📝 Contribute](#-contribute)**

</div>