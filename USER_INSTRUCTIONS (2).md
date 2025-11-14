# Privacy Mask - Complete User Instructions

## What This Tool Does

Privacy Mask is a Chrome extension that masks sensitive data entirely in your browser before you share it with AI tools. No servers involved. No cloud processing. Just you, your browser, and safer AI usage.

---

## Installation Instructions

### Step 1: Download the Extension
https://github.com/moxiemediation-svg/privacymask.git 

### Step 2: Extract the ZIP File
- **Windows:** Right-click → "Extract All"
- **Mac:** Double-click the ZIP file
- Save it somewhere you'll remember (like your Documents folder)

### Step 3: Install in Chrome
1. Open Chrome
2. Type `chrome://extensions/` in your address bar and press Enter
3. Look for the toggle switch that says **"Developer mode"** (top-right corner)
4. Turn it **ON**
5. Click the **"Load unpacked"** button that appears
6. Navigate to and select the **privacy-mask-extension** folder you extracted
7. Click **"Select Folder"**

### Step 4: Verify Installation
- You should see a lock icon (🔒) appear in your Chrome toolbar
- The extension card should show "Privacy Mask" with no errors

**Troubleshooting Installation:**
- If you get an error, make sure you selected the folder that contains `manifest.json`
- Make sure "Developer mode" is turned ON
- Try refreshing the extensions page

---

## How to Use It: Three Methods

### Method 1: Copy with Masking (Recommended - Easiest!)

**Use this when:** You want to copy text from anywhere and paste it into ChatGPT/Claude

**Steps:**
1. Select text that contains sensitive data
2. Right-click on the selected text
3. Choose **"Copy with masking"** from the menu
4. Watch for the notification (tells you how many items were masked)
5. Paste into ChatGPT, Claude, or wherever you need it (Ctrl+V or Cmd+V)

**Example:**
- You select: "Contact Maria Rodriguez at maria@example.com about $50,000 settlement"
- Notification shows: "Copied with 3 item(s) masked"
- You paste: "Contact [NAME_1] at [EMAIL_1] about [AMOUNT_1] settlement"

---

### Method 2: Right-Click to Mask (For Editable Fields)

**Use this when:** You're typing in Gmail, Google Docs, or a text box and want to mask what you just typed

**Steps:**
1. Select text you've typed
2. Right-click → **"Mask sensitive data"**
3. Watch it replace right there in the field
4. Continue typing or send

**Where this works:**
- Gmail compose window
- Google Docs
- Any text input or textarea
- Most editable fields

**Where this copies to clipboard instead:**
- PDFs
- News articles
- Most websites (read-only content)
- Non-editable areas

---

### Method 3: Using the Popup (For Bulk Masking)

**Use this when:** You have a large document or want more control

**Steps:**
1. Click the 🔒 Privacy Mask icon in your Chrome toolbar
2. Paste your text into the "Text to mask" box
3. Choose which data types to mask (checkboxes)
4. Click **"Mask Text"**
5. Review the result in the output box
6. Click **"Copy Result"**
7. Paste wherever you need it

**Tip:** This method lets you see exactly what will be masked before you use it

---

## What Gets Masked (And What Doesn't)

### Masked by Default:
✅ **Email addresses** → `[EMAIL_1]`, `[EMAIL_2]`, etc.  
✅ **Phone numbers** → `[PHONE_1]`, `[PHONE_2]`, etc.  
✅ **Social Security Numbers** → `[SSN_1]`, `[SSN_2]`, etc.  
✅ **Credit card numbers** → `[CARD_1]`, `[CARD_2]`, etc.  
✅ **Dollar amounts** → `[AMOUNT_1]`, `[AMOUNT_2]`, etc.  
✅ **Dates** → `[DATE_1]`, `[DATE_2]`, etc.  
✅ **Street addresses** → `[ADDRESS_1]`, `[ADDRESS_2]`, etc.

### Optional (Off by Default):
⚠️ **Names** → `[NAME_1]`, `[NAME_2]`, etc.

**Why names are optional:** Automatic name detection is imperfect. It might catch things like "Happy Friday" or miss actual names. 

**To use name masking:**
1. Use the popup method (click extension icon)
2. Check "Names (experimental)"
3. Review the masked result carefully before using

---

## Unmasking: Getting Original Data Back

### When You Need It:
After ChatGPT/Claude gives you a response with masked tokens like [NAME_1], you want to restore the real names.

### How to Unmask:
1. Select the AI's response (the text with [NAME_1], [EMAIL_1], etc.)
2. Right-click → **"Unmask data"**
3. All tokens replace back to original values

**Example:**
- AI says: "I recommend [NAME_1] contact [NAME_2] about the [AMOUNT_1] payment"
- You unmask: "I recommend Maria Rodriguez contact John Smith about the $50,000 payment"

---

## Managing Your Mappings

### Viewing Mappings
Click the extension icon → "Mappings" tab

You'll see all your current masks and what they represent.

### Exporting Mappings (IMPORTANT - Do This!)
1. Click extension icon → "Mappings" tab
2. Click **"Export"**
3. Save the JSON file somewhere safe

**Why this matters:** If you clear your browser data or reinstall the extension, you'll lose your mappings. Export regularly!

### Importing Mappings
1. Click extension icon → "Mappings" tab
2. Click **"Import"**
3. Select your exported JSON file

### Clearing Everything
1. Click extension icon → "Mappings" tab
2. Click **"Clear All"**
3. Confirm (this cannot be undone!)

**When to clear:** If you want to start fresh or if name detection created too many false positives

---

## Important Privacy Notes

### What This Tool Does:
✅ Processes all data locally in your browser  
✅ Stores mappings locally in Chrome storage  
✅ Never sends data to any server  
✅ No tracking, no analytics, no data collection  

### What This Tool Doesn't Do:
❌ It doesn't guarantee perfect masking  
❌ It doesn't replace compliance policies  
❌ It doesn't protect data once you paste it somewhere  

### Your Responsibilities:
1. **Review masked text** before sharing it
2. **Export your mappings** regularly
3. **Use appropriate AI tools** (don't use free tiers with client data)
4. **Follow your compliance obligations** (this is one layer of protection)

---

## Typical Workflows

### Workflow 1: Email with Sensitive Info → ChatGPT
1. Open the email
2. Select all text (Ctrl+A or Cmd+A)
3. Right-click → "Copy with masking"
4. Open ChatGPT
5. Paste
6. Get AI's response
7. Select the response
8. Right-click → "Unmask data"
9. Use the unmasked version

**Time saved:** ~10 seconds vs. manual redaction

---

### Workflow 2: Document Analysis
1. Copy text from your document
2. Click Privacy Mask icon
3. Paste into "Text to mask" box
4. Review what will be masked
5. Click "Mask Text"
6. Copy result
7. Paste into Claude for analysis
8. Get response and unmask

**Time saved:** Minutes to hours depending on document size

---

### Workflow 3: Drafting with AI
1. Type your draft in Google Docs
2. Include real names/data as you write
3. When done, select all
4. Right-click → "Copy with masking"
5. Paste into ChatGPT: "Please improve this draft"
6. Get improved version
7. Unmask it
8. Use the result

**Benefit:** Write naturally, mask automatically

---

## Common Questions

**Q: Does this work in Firefox/Safari/Edge?**  
A: Currently Chrome only. Firefox version possible in the future.

**Q: Is my data really private?**  
A: Yes. All processing happens in your browser. No network requests are made. You can verify this in Chrome DevTools.

**Q: What if the AI figures out who [NAME_1] is from context?**  
A: Good question. If you say "the CEO of Apple," masking the name doesn't help. Use judgment about context clues.

**Q: Can I customize the masking patterns?**  
A: Yes! Edit the `masking.js` file. It's well-commented JavaScript.

**Q: What happens if I clear my browser data?**  
A: Your mappings are lost unless you exported them. Export regularly!

**Q: Is this HIPAA/attorney-client privilege compliant?**  
A: This tool helps with compliance by preventing unmasked data from leaving your control. But it's not sufficient alone - you still need proper AI usage policies, BAAs where required, etc.

**Q: The name detection isn't working well.**  
A: That's why it's off by default. Automatic name detection is hard. For critical work, manually replace names instead.

**Q: Can I share my mappings with my team?**  
A: You can export and share the mapping file, but they'll need the extension installed to import it.

---

## Troubleshooting

### "Context menu doesn't appear"
- Refresh the page you're trying to mask on
- Check that the extension is enabled in chrome://extensions/
- Make sure you've selected text before right-clicking

### "Nothing happens when I click mask"
- Check for a notification in the top-right corner
- If it says "copied to clipboard," the page is read-only - paste the result
- Try using the popup method instead

### "Text looks weird after masking"
- This is normal - [NAME_1] type tokens are how it works
- When you unmask, it restores the original

### "I lost my mappings"
- If you didn't export them, they're gone
- This is why exporting regularly is important
- Start fresh by masking your data again

### "Name detection masked too much"
- Clear all mappings (click icon → Mappings → Clear All)
- Reload the extension (chrome://extensions/ → reload button)
- Names are now off by default in the updated version

---

## Best Practices

### DO:
✅ Export your mappings weekly  
✅ Review masked text before sharing  
✅ Use with AI providers that don't train on your data  
✅ Combine with other security measures  
✅ Test with sample data first  

### DON'T:
❌ Rely solely on automatic name detection  
❌ Skip reviewing the masked output  
❌ Forget to export your mappings  
❌ Assume this replaces compliance policies  
❌ Use with AI tools that have poor privacy policies  

---

## Support

**Issues or Questions?**  
Email: lindsey@wagnerlegalpc.com

**Want to Improve It?**  
The code is open source. Feel free to modify and enhance it.

**Found a Bug?**  
Let me know what happened and I'll work on a fix.

---

## Version Information

**Current Version:** 1.0.0  
**Last Updated:** November 2025
**Works With:** Chrome (and Chromium-based browsers)

---

**Remember:** This tool is one layer of protection in a comprehensive compliance strategy. Use it wisely, review your results, and maintain good data hygiene practices.
