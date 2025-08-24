# Adobe Illustrator Layer Name Extractor

A simple ExtendScript (JSX) tool to extract all layer names from an Adobe Illustrator document and export them as either a Markdown file or plain text file.

## Features

- 📋 Extracts all layer names including nested sublayers
- 📝 Two output formats: Markdown or Plain Text
- 🗂️ Maintains hierarchical structure of layers
- 💾 Automatically saves files to Desktop
- 📊 Shows layer count and generation date
- 🔍 Preview in alert dialog for quick copying

## Installation

1. Download the `get_layer_names.jsx` file
2. Save it to your preferred scripts folder (optional)

## Usage

### Method 1: Run the Script
1. Open your Adobe Illustrator document
2. Go to **File → Scripts → Other Script...**
3. Navigate to and select `get_layer_names.jsx`
4. Choose your preferred output format when prompted

### Method 2: Install as Permanent Script (Optional)
1. Copy `get_layer_names.jsx` to your Illustrator Scripts folder:
   - **Windows:** `C:\Program Files\Adobe\Adobe Illustrator [version]\Presets\[language]\Scripts\`
   - **Mac:** `/Applications/Adobe Illustrator [version]/Presets/[language]/Scripts/`
2. Restart Illustrator
3. Access via **File → Scripts → get_layer_names**

## Output Options

When you run the script, you'll see a dialog with two options:

### Option 1: Markdown File (Click OK)
Creates a formatted `.md` file with:
- Document title as header
- Generation date
- Hierarchical bullet list structure
- Total layer count
- Professional formatting for documentation

**Example Output:**
```markdown
# Layer Names for: my_design

Generated on: 8/24/2025

## Layer Structure

- Background
- Content
  - Header
    - Logo
    - Navigation
  - Main Content
    - Text Layer
    - Images

---

Total layers: 7
```

### Option 2: Plain Text File (Click Cancel)
Creates a simple `.txt` file with:
- Plain text hierarchy using indentation
- Shows content in alert dialog for quick copying
- Suitable for simple lists or importing into other tools

**Example Output:**
```
Background
Content
  Header
    Logo
    Navigation
  Main Content
    Text Layer
    Images
```

## File Naming

Output files are automatically named based on your Illustrator document:
- Markdown: `[document_name]_layers.md`
- Text: `[document_name]_layers.txt`

Files are saved to your Desktop by default.

## Compatibility

- **Adobe Illustrator:** CS6 and later
- **Operating Systems:** Windows and macOS
- **File Types:** Works with any AI document format

## Technical Details

- Built with Adobe ExtendScript (JavaScript for Adobe apps)
- Recursively traverses all layer hierarchies
- Handles nested sublayers of any depth
- Character limit handling for alert dialogs (truncates if needed)
- Automatic file extension removal from document names

## Troubleshooting

### Common Issues

**"No active document" error:**
- Make sure you have an Illustrator document open before running the script

**Script doesn't appear in File → Scripts menu:**
- Verify the file is saved with `.jsx` extension
- Check if it's placed in the correct Scripts folder
- Restart Illustrator after adding scripts

**Permission errors when saving:**
- Ensure you have write permissions to the Desktop
- Try running Illustrator as administrator (Windows) or check folder permissions (Mac)

### Limitations

- Alert dialog has character limits (~2000 chars) - longer lists will be truncated but full content is always saved to file
- Requires an active Illustrator document to run

## Use Cases

- **Documentation:** Create layer structure documentation for design handoffs
- **Asset Management:** Inventory layers for large, complex designs  
- **Quality Control:** Review layer naming conventions across projects
- **Client Communication:** Share layer structure with clients or team members
- **Design System Documentation:** Document component layer hierarchies

## Contributing

Feel free to submit issues, fork the repository, and create pull requests for any improvements.

## License

This project is open source and available under the [MIT License](LICENSE).

## Changelog

### v1.0.0
- Initial release
- Markdown and plain text export options
- Hierarchical layer structure preservation
- Desktop file saving with automatic naming

---

**Created by:** [Your Name]  
**Last Updated:** August 2025

## Related Tools

- [Adobe Illustrator Scripting Guide](https://ai-scripting.docsforadobe.dev/)
- [ExtendScript Documentation](https://extendscript.docsforadobe.dev/)
