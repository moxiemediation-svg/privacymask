# Privacy Mask

**Client-side data masking for AI tools**

Stop choosing between AI efficiency and data privacy. Privacy Mask lets you use ChatGPT and Claude safely with sensitive information.

[![Download Latest Release](https://img.shields.io/badge/download-latest-blue.svg)](https://github.com/YOUR-USERNAME/privacy-mask-extension/releases/latest)
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Chrome Extension](https://img.shields.io/badge/Chrome-Extension-orange.svg)

---

## 🔒 What It Does

Privacy Mask is a Chrome extension that masks sensitive data **entirely in your browser** before you share it with AI tools. 

- ✅ **100% client-side processing** - no servers, no cloud, no data exposure
- ✅ **Automatic detection** - finds emails, phones, SSNs, credit cards, amounts, dates, addresses
- ✅ **Right-click masking** - select text, mask, paste into ChatGPT/Claude
- ✅ **Easy unmask** - restore original data with one click
- ✅ **No tracking** - zero analytics, zero data collection

Built for legal professionals, HR teams, healthcare providers, and anyone who needs to use AI without exposing sensitive information.

---

## 🎯 How It Works

```
1. Select text with sensitive data
2. Right-click → "Copy with masking"
3. Paste into ChatGPT or Claude
4. Get AI response
5. Select response → Right-click → "Unmask data"
```

**Example:**
```
Before: Contact Maria Rodriguez at maria@example.com about $50,000 settlement
After:  Contact [NAME_1] at [EMAIL_1] about [AMOUNT_1] settlement
```

---

## 📦 Installation

### Quick Install
1. [Download the latest release](https://github.com/YOUR-USERNAME/privacy-mask-extension/releases/latest)
2. Extract the ZIP file
3. Open Chrome and go to `chrome://extensions/`
4. Enable **"Developer mode"** (toggle in top-right)
5. Click **"Load unpacked"**
6. Select the extracted folder
7. Done! Look for the 🔒 icon in your toolbar

### Full Installation Guide
See [INSTALL.md](INSTALL.md) for detailed instructions with screenshots.

---

## ✨ Features

### What Gets Masked (By Default)
- ✅ **Email addresses** → `[EMAIL_1]`, `[EMAIL_2]`, etc.
- ✅ **Phone numbers** → `[PHONE_1]`, `[PHONE_2]`, etc.
- ✅ **Social Security Numbers** → `[SSN_1]`, `[SSN_2]`, etc.
- ✅ **Credit card numbers** → `[CARD_1]`, `[CARD_2]`, etc.
- ✅ **Dollar amounts** → `[AMOUNT_1]`, `[AMOUNT_2]`, etc.
- ✅ **Dates** → `[DATE_1]`, `[DATE_2]`, etc.
- ✅ **Street addresses** → `[ADDRESS_1]`, `[ADDRESS_2]`, etc.
- ⚠️ **Names** → Optional (off by default - automatic detection is imperfect)

### Three Ways to Use

**1. Right-Click Context Menu** (Easiest)
- Select text anywhere
- Right-click → "Copy with masking"
- Paste into your AI tool

**2. Direct Replacement** (For editable fields)
- Type in Gmail, Google Docs, etc.
- Select text → Right-click → "Mask sensitive data"
- Text replaces in place

**3. Popup Interface** (For bulk work)
- Click extension icon
- Paste large documents
- Choose what to mask
- Review and copy result

### Data Management
- **Export mappings** - Backup your masked data mappings as JSON
- **Import mappings** - Restore from previous backup
- **View all mappings** - See what's been masked
- **Clear all** - Start fresh

---

## 🎓 Use Cases

### Legal Professionals
Draft demand letters, analyze cases, research issues - all without exposing client names, case details, or privileged information.

### HR Teams  
Get AI help with policies, employee situations, and communications while protecting PII and maintaining confidentiality.

### Healthcare Providers
Use AI for clinical documentation and analysis without exposing PHI or violating HIPAA.

### Small Businesses
Access AI capabilities without enterprise budgets or data exposure concerns.

---

## 🔐 Privacy & Security

### What This Extension Does
✅ Processes all data locally in your browser  
✅ Stores mappings in Chrome's local storage (never synced)  
✅ Makes zero network requests  
✅ No tracking, analytics, or telemetry  
✅ Open source - verify the code yourself  

### What This Extension Doesn't Do
❌ Guarantee perfect masking (always review output)  
❌ Replace compliance policies (one layer of protection)  
❌ Protect data after you paste it (use appropriate AI tools)  
❌ Work on non-Chromium browsers (Chrome/Edge only)  

### Your Responsibilities
1. Review masked text before sharing
2. Export mappings regularly (backup)
3. Use with AI providers that respect data privacy
4. Follow your organization's compliance requirements

This tool helps you comply with regulations - it doesn't replace them.

---

## 📚 Documentation

- [Installation Guide](INSTALL.md) - Step-by-step setup
- [User Guide](README.md) - This document
- [Workflow Examples](#common-workflows) - Real-world use cases
- [Troubleshooting](#troubleshooting) - Common issues

---

## 🚀 Common Workflows

### Email → ChatGPT Analysis
```
1. Open email with sensitive info
2. Select all (Ctrl+A / Cmd+A)
3. Right-click → "Copy with masking"
4. Paste into ChatGPT
5. Get analysis
6. Select response → Right-click → "Unmask data"
```

### Document Drafting with AI
```
1. Write draft in Google Docs (use real names)
2. When done, select all
3. Right-click → "Copy with masking"
4. Paste into Claude: "Please improve this draft"
5. Get improved version
6. Unmask and use
```

### Bulk Document Processing
```
1. Click extension icon
2. Paste entire document
3. Choose data types to mask
4. Review masked version
5. Copy → Use with AI tool
```

---

## 🛠️ Technical Details

### File Structure
```
privacy-mask-extension/
├── manifest.json       # Extension configuration
├── background.js       # Context menu handler  
├── content.js         # Page interaction
├── content.css        # Notification styles
├── masking.js         # Core masking logic
├── popup.html         # Extension popup
├── popup.js           # Popup functionality
├── popup.css          # Popup styles
└── icons/             # Extension icons
```

### Pattern Detection
The extension uses regular expressions to detect sensitive data. All patterns are configurable in `masking.js`.

### Storage
Data is stored using Chrome's `chrome.storage.local` API:
- `maskMappings` - Object mapping tokens to original values
- `maskCounters` - Counters for each data type

Storage is per-user and never synced to the cloud.

---

## 🔧 Customization

### Add Custom Patterns
Edit `masking.js` to add your own detection patterns:

```javascript
patterns: {
  yourPattern: {
    regex: /your-pattern-here/g,
    prefix: 'YOUR_PREFIX'
  }
}
```

### Modify Default Behavior
- Change which types are masked by default in `content.js`
- Adjust notification duration in `content.js`
- Customize popup interface in `popup.html`

---

## ❓ Troubleshooting

**Context menu doesn't appear**
- Refresh the page
- Check extension is enabled in `chrome://extensions/`
- Make sure text is selected before right-clicking

**Nothing happens when I click mask**
- Look for notification (top-right corner)
- If on read-only page, text is copied to clipboard (paste it!)
- Try using the popup interface instead

**Name detection masked too much**
- Name detection is off by default (it's imperfect)
- To use: Click icon → Enable "Names (experimental)" → Review results
- For critical work, manually replace names

**Lost my mappings**
- If you didn't export, they're gone
- Storage is local only - clearing browser data deletes them
- Export regularly!

---

## 📝 Changelog

### Version 1.0.0 (November 2024)
- Initial release
- Automatic detection for 7 data types
- Right-click context menu
- Browser popup interface
- Export/import functionality
- 100% client-side processing

---

## 🤝 Contributing

Found a bug? Have a feature request? Want to improve the code?

1. Check existing [Issues](https://github.com/YOUR-USERNAME/privacy-mask-extension/issues)
2. Open a new issue with details
3. Or submit a pull request

All contributions welcome!

---

## 📄 License

MIT License - see [LICENSE](LICENSE) file for details.

You're free to use, modify, and distribute this extension.

---

## ⚠️ Disclaimer

This tool provides one layer of data protection. It does not guarantee perfect masking or replace comprehensive compliance policies. Always:
- Review masked output before sharing
- Use appropriate AI tools that respect data privacy
- Follow your organization's security and compliance requirements
- Consider context that might reveal identity
- Export mappings regularly

The authors are not liable for any data exposure resulting from use of this tool.

---

## 💬 Support

**Questions?** Open an [issue](https://github.com/YOUR-USERNAME/privacy-mask-extension/issues)

**Feedback?** We'd love to hear how you're using it

**Want updates?** Watch this repo or subscribe to [The AI Shift newsletter](https://theaishift.com)

---

## 🙏 Acknowledgments

Built for legal professionals, HR teams, and healthcare providers who deserve to use AI safely.

Created by [Wagner Legal PC](https://wagnerlegal.com) | [The AI Shift LLC](https://theaishift.com)

---

**Remember:** Use AI wisely. Protect your clients, patients, and employees.
