# Crossing the Bridge 🌉

<div align="center">

**Your Personal AI Language Tutor for Seamless Chinese Learning**

[![Chrome Extension](https://img.shields.io/badge/Chrome-Extension-brightgreen.svg)](https://chrome.google.com/webstore)
[![Manifest V3](https://img.shields.io/badge/Manifest-V3-blue.svg)](https://developer.chrome.com/docs/extensions/mv3/intro/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

</div>

---

## 🌟 Inspiration

Do you want to improve your language skills by reading material online in your target language, but often find the articles too long or difficult to finish? Have you tried searching for level-appropriate reading materials, only to give up because it takes too much effort?

My friends faced the same challenges while learning Chinese. Whenever they tried to read or text, they found themselves juggling multiple apps — switching between translators, grammar checkers, and dictionaries. It was exhausting and constantly disrupted our focus.

**What if language learning could happen naturally, right where you already read, write, and communicate?**

Just like a bridge helps you cross a river without stopping, **Crossing the Bridge** helps you overcome language barriers seamlessly — turning your everyday digital life into effortless, immersive learning.

---

## ✨ What It Does

**Crossing the Bridge** is a Chrome extension that acts as your personal AI language tutor, helping you learn through daily reading and writing.

### Key Features

🎯 **Real-Time Proofreading**
- Color-coded highlights for Chinese text errors
- Categories: word choice, punctuation, word order, and grammar
- Idiomatic suggestions with bilingual explanations
- Grammarly-style feedback popups

📚 **HSK-Adaptive Summarizer**
- Simplifies any Chinese webpage to your proficiency level (HSK 1–6)
- Turns difficult articles into level-appropriate summaries
- Floating, resizable panel for distraction-free reading
- Side panel integration for convenient access

🔄 **Smart Translation**
- Real-time English-to-Chinese translation
- Context-aware sentence analysis
- Preserves meaning and natural flow

🔒 **Privacy-First AI Processing**
- Local AI processing using Chrome's Gemini Nano or Claude AI
- No data sent to external servers
- Your learning stays private

---

## 🛠️ How We Built It

**Crossing the Bridge** is built as a Chrome extension (Manifest V3) that brings real-time Chinese language feedback directly into users' browsing experience.

### Technology Stack

- **Chrome Extension (Manifest V3)** - Modern extension architecture
- **Chrome Built-in AI APIs** - Language Model, Summarizer, Translator for local processing
- **Few-Shot Learning** - Trained with 50+ categorized Chinese examples
- **Smart Text Pipeline** - Sentence-level analysis, parallel API calls, and caching

### Architecture

```
┌─────────────────────────────────────────────────┐
│              Chrome Extension UI                 │
│  ┌──────────┐  ┌──────────┐  ┌──────────────┐  │
│  │  Popup   │  │  Side    │  │   Settings   │  │
│  │  Panel   │  │  Panel   │  │    Page      │  │
│  └──────────┘  └──────────┘  └──────────────┘  │
└─────────────────────────────────────────────────┘
                      ↓
┌─────────────────────────────────────────────────┐
│           Content Script (bridge.js)            │
│  • Text analysis & overlay injection            │
│  • Color-coded error highlighting                │
│  • Real-time proofreading feedback              │
└─────────────────────────────────────────────────┘
                      ↓
┌─────────────────────────────────────────────────┐
│      Background Service Worker (background.js)  │
│  • Chrome AI API integration                    │
│  • Message routing & state management           │
└─────────────────────────────────────────────────┘
                      ↓
┌─────────────────────────────────────────────────┐
│            Chrome Built-in AI APIs              │
│  • Gemini Nano (Local Language Model)          │
│  • Summarizer API (HSK-adaptive)                │
│  • Translator API (EN ↔ ZH)                     │
└─────────────────────────────────────────────────┘
```

### Key Features Implementation

- **HSK-adaptive summarization** - Adjusts content complexity to user's proficiency level
- **Color-coded overlays** - Visual feedback system inspired by Grammarly
- **Bilingual explanations** - Supports both English and Chinese (中文)
- **Non-intrusive design** - Seamlessly integrates with browsing experience

---

## 🚀 Installation

### From Source

1. Clone the repository:
   ```bash
   git clone https://github.com/SophieQA/Crossing-the-Bridge.git
   cd Crossing-the-Bridge
   ```

2. Open Chrome and navigate to `chrome://extensions/`

3. Enable **Developer mode** (toggle in top-right corner)

4. Click **Load unpacked** and select the project directory

5. The extension icon should appear in your Chrome toolbar!

### From Chrome Web Store

*(Coming soon)*

---

## 📖 Usage

### Getting Started

1. **Click the extension icon** in your Chrome toolbar to open the popup
2. **Select your HSK level** in the settings page
3. **Browse any Chinese webpage** and let the magic happen!

### Features Guide

#### Real-Time Proofreading
- Type or select Chinese text on any webpage
- Watch as errors are highlighted with color codes:
  - 🔴 **Red** - Grammar errors
  - 🟡 **Yellow** - Word choice suggestions
  - 🔵 **Blue** - Punctuation issues
  - 🟢 **Green** - Word order improvements
- Hover over highlights for detailed explanations

#### HSK-Adaptive Summarizer
- Open the **Side Panel** (click extension icon → "Open Side Panel")
- The current webpage will be automatically summarized
- Adjust your HSK level to get appropriate difficulty
- Resize the panel to fit your reading preference

#### Translation Assistant
- Select English text on any webpage
- Click the translation icon that appears
- Get instant, context-aware Chinese translation

---

## ⚙️ Configuration

Access the settings page by:
- Right-clicking the extension icon → **Options**
- Or navigate to `chrome://extensions/` → **Crossing the Bridge** → **Details** → **Extension options**

### Available Settings

- **HSK Level** (1-6) - Set your Chinese proficiency level
- **AI Model** - Choose between Gemini Nano or Claude AI
- **Proofreading Sensitivity** - Adjust feedback strictness
- **Color Scheme** - Customize error highlight colors
- **Language Preference** - Choose explanation language (EN/中文)

---

## 🎨 Color Coding System

| Color | Error Type | Example |
|-------|------------|---------|
| 🔴 Red | Grammar | Incorrect verb tense or sentence structure |
| 🟡 Yellow | Word Choice | Better vocabulary suggestions |
| 🔵 Blue | Punctuation | Missing or incorrect punctuation marks |
| 🟢 Green | Word Order | Sentence flow improvements |
| 🟣 Purple | Idiomatic | Suggestions for more natural expressions |

---

## 🔐 Privacy & Security

**Your privacy is our priority:**

- ✅ All AI processing happens **locally** in your browser
- ✅ No text data is sent to external servers
- ✅ No user tracking or analytics
- ✅ No personal data collection
- ✅ Open source and transparent

---

## 🤝 Contributing

We welcome contributions! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Development Setup

```bash
# Clone the repo
git clone https://github.com/SophieQA/Crossing-the-Bridge.git

# Navigate to directory
cd Crossing-the-Bridge

# Load in Chrome as unpacked extension
# Open chrome://extensions/ and click "Load unpacked"
```

---

## 📝 Project Structure

```
Crossing-the-Bridge/
├── manifest.json              # Extension configuration
├── background.js              # Service worker for AI processing
├── bridge.html                # Popup interface
├── bridge.js                  # Content script for text analysis
├── sidepanel.html             # Side panel for summarization
├── sidepanel.js               # Side panel logic
├── settings.html              # Settings page
├── settings.js                # Settings configuration
├── popup.js                   # Popup logic
├── config.js                  # Extension configuration
├── proofreading-examples.js   # Training examples for AI
├── overlay.css                # Styling for text highlights
├── assets/                    # Images and icons
│   └── logo.png
├── styles/                    # Additional stylesheets
│   └── icon.css
├── LICENSE                    # MIT License
└── README.md                  # This file
```

---

## 🐛 Known Issues & Roadmap

### Current Limitations
- Requires Chrome 127+ for Built-in AI APIs
- HSK categorization is still being refined
- Some complex grammatical structures may not be detected

### Roadmap
- [ ] Support for traditional Chinese characters
- [ ] Expand to other languages (Japanese, Korean)
- [ ] Vocabulary flashcard integration
- [ ] Progress tracking and learning analytics
- [ ] Browser extension for Firefox and Edge
- [ ] Mobile app version

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Thanks to all language learners who inspired this project
- Chrome Extensions team for the Built-in AI APIs
- The open-source community for invaluable tools and libraries

---

## 📬 Contact & Support

- **Issues**: [GitHub Issues](https://github.com/SophieQA/Crossing-the-Bridge/issues)
- **Discussions**: [GitHub Discussions](https://github.com/SophieQA/Crossing-the-Bridge/discussions)

---

<div align="center">

**Made with ❤️ for language learners everywhere**

[⭐ Star this repo](https://github.com/SophieQA/Crossing-the-Bridge) if you find it helpful!

</div>
