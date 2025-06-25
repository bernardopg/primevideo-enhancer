# Prime Video Enhancer 🎬

A powerful userscript that enhances your Prime Video viewing experience by removing distractions, automating interactions, and adding convenient features.

## ✨ Features

### 🚫 **X-ray Panel Hiding**

- Automatically hides the X-ray information panel that appears during playback
- Supports multiple X-ray panel variations and layouts
- Works in both normal and fullscreen modes

### ⚡ **Automatic Ad Skipping**

- Intelligently detects and clicks "Skip Ad" buttons
- Supports multiple ad button types and layouts
- Non-intrusive operation with error handling

### 🖱️ **Smart Cursor Management**

- Automatically hides cursor during video playback after 3 seconds of inactivity
- Shows cursor immediately when paused or when moving mouse
- Respects user interaction patterns

### ⌨️ **Keyboard Shortcuts**

- `Ctrl + H` - Open quality/settings menu
- `Ctrl + F` - Toggle fullscreen mode
- Works only when video player is active

### 🔄 **Auto-play Next Episode**

- Automatically plays the next episode after a brief delay
- Smart detection of "Next Episode" buttons
- Seamless binge-watching experience

## 🚀 Installation

### Prerequisites

You need a userscript manager extension installed in your browser:

- **Chrome/Edge**: [Tampermonkey](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo)
- **Firefox**: [Greasemonkey](https://addons.mozilla.org/en-US/firefox/addon/greasemonkey/) or [Tampermonkey](https://addons.mozilla.org/en-US/firefox/addon/tampermonkey/)
- **Safari**: [Tampermonkey](https://apps.apple.com/us/app/tampermonkey/id1482490089)

### Install the Script

1. **Direct Installation**:
   - Click here: [Install Prime Video Enhancer](https://raw.githubusercontent.com/bernardopg/primevideo-enhancer/main/primevideo-enhance.js)
   - Your userscript manager should prompt you to install it

2. **Manual Installation**:
   - Copy the contents of [`primevideo-enhance.js`](./primevideo-enhance.js)
   - Open your userscript manager dashboard
   - Create a new script and paste the code
   - Save the script

3. **Verify Installation**:
   - Visit [Prime Video](https://www.primevideo.com)
   - The script should load automatically
   - Enable debug mode in the script configuration to see console logs

## ⚙️ Configuration

The script includes a configuration object that you can modify:

```javascript
const CONFIG = {
    logging: false, // Set to true for debugging
    adSkip: {
        tries: 3,
        delay: 1500,
        selectors: [/* Ad button selectors */]
    },
    xray: {
        selectors: [/* X-ray panel selectors */]
    },
    cursor: {
        hideDelay: 3000, // Cursor hide delay in milliseconds
        playerSelectors: [/* Video player selectors */]
    }
};
```

### Customization Options

- **Enable Debugging**: Set `CONFIG.logging = true` to see detailed console logs
- **Adjust Cursor Hide Delay**: Modify `CONFIG.cursor.hideDelay` (default: 3000ms)
- **Customize Selectors**: Add or modify CSS selectors for better compatibility

## 🎯 Supported Features by Prime Video Version

| Feature | Web Player | Mobile Web | Smart TV Apps |
|---------|------------|------------|---------------|
| X-ray Hiding | ✅ | ✅ | ❌ |
| Ad Skipping | ✅ | ✅ | ❌ |
| Cursor Management | ✅ | ❌ | ❌ |
| Keyboard Shortcuts | ✅ | ❌ | ❌ |
| Auto-play Next | ✅ | ✅ | ❌ |

**Note:** This userscript only works on web browsers with userscript manager support

## 🐛 Troubleshooting

### Script Not Working?

1. **Check userscript manager**: Ensure it's enabled and the script is active
2. **Refresh the page**: Some features require a page reload
3. **Enable debug mode**: Set `CONFIG.logging = true` and check browser console
4. **Update the script**: Ensure you have the latest version

### Common Issues

- **X-ray still showing**: Clear browser cache and reload
- **Ads not skipping**: Some ad formats may not be supported yet
- **Cursor not hiding**: Check if you're hovering over video controls
- **Keyboard shortcuts not working**: Ensure video player has focus

### Reporting Issues

If you encounter problems:

1. Enable debug mode (`CONFIG.logging = true`)
2. Open browser console (F12)
3. Reproduce the issue
4. Copy console logs
5. [Create an issue](https://github.com/bernardopg/primevideo-enhancer/issues) with details

## 🔄 Updates

The script automatically works with Prime Video's interface updates, but major changes may require script updates. Check this repository periodically for improvements.

To update:

1. Visit the [latest version](https://raw.githubusercontent.com/bernardopg/primevideo-enhancer/main/primevideo-enhance.js)
2. Your userscript manager should detect and prompt for updates
3. Or manually replace the script code

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Report Issues**: Found a bug? [Create an issue](https://github.com/bernardopg/primevideo-enhancer/issues)
2. **Suggest Features**: Have an idea? [Open a discussion](https://github.com/bernardopg/primevideo-enhancer/discussions)
3. **Submit Code**:

   - Fork the repository
   - Create a feature branch
   - Make your changes
   - Submit a pull request

### Development Setup

```bash
git clone https://github.com/bernardopg/primevideo-enhancer.git
cd primevideo-enhancer
# Edit primevideo-enhance.js
# Test on Prime Video
# Submit PR
```

## 📝 License

This project is released under the MIT License. See [LICENSE](LICENSE) for details.

## ⚠️ Disclaimer

This userscript is for educational and personal use only. It enhances the user interface and does not:

- Bypass paid content or subscriptions
- Violate Prime Video's terms of service
- Download or redistribute copyrighted content
- Interfere with content protection systems

Use responsibly and in accordance with Prime Video's terms of service.

## 🌟 Acknowledgments

- Thanks to the userscript community for inspiration and best practices
- Prime Video for providing an extensible web interface
- All contributors and users who report issues and suggest improvements

---

**Enjoy your enhanced Prime Video experience!** 🍿

If this script improves your viewing experience, consider giving it a ⭐ star!
