
# 📖 On-Screen Manga/Manhwa Translator

## 🧠 Project Description

**On-Screen Manga/Manhwa Translator** is a lightweight desktop tool designed to help users translate Japanese or Korean text from manga/manhwa images directly on their screen. It continuously captures screen content, detects text (from bubbles, captions, etc.), translates it roughly to English, and displays it in a small floating window. The translations don’t need to be accurate — just enough for contextual understanding.

---

## 🎯 Goal

Provide a convenient, minimal tool that allows users to read untranslated raw manga/manhwa from any website or app by:
- Capturing screen images in real-time or near-real-time
- Performing OCR on Japanese/Korean text
- Translating the text into English
- Displaying the translation without interrupting the reading flow

---

## 💡 Project Rationale

- Verifying personal understanding of raw Japanese/Korean manga content
- Enabling faster reading without switching between windows or using external apps
- Focused on **function over perfection** — rough translations are acceptable

---

## 🖥️ Target Platform

- **Operating System:** Windows (initial target)
- **Languages Supported:** Japanese, Korean
- **Translation Output:** English
- **Preferred Programming Language:** Python

---

## 🧰 Technologies & Libraries

| Category           | Library/Tool         | Purpose                           |
|--------------------|----------------------|-----------------------------------|
| Screen Capture     | [`mss`](https://github.com/BoboTiG/python-mss)            | Capture screen region             |
| OCR                | [`EasyOCR`](https://github.com/JaidedAI/EasyOCR)         | Detect JP/KR text in images       |
| Translation        | [`googletrans`](https://pypi.org/project/googletrans/)   | Translate extracted text          |
| UI & Overlay       | `Tkinter`, `OpenCV`, `pywin32` (optional)                | Floating window & text rendering  |

---

## ⚙️ Core Features

| Feature             | Description                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| **Screen Capture**  | Continuously grab a portion of or the full screen.                          |
| **OCR Detection**   | Detect Japanese/Korean text from the screen using EasyOCR.                  |
| **Translation**     | Translate detected text to English using `googletrans`.                     |
| **Overlay Display** | Show translated text either in a floating window or over the original image.|
| **Control Panel**   | Minimal always-on-top floating UI with buttons: `Start`, `Stop`, `Screenshot`, `Exit`. |

---

## 🧭 Workflow (High-Level Steps)

1. **Select Capture Region** (optional for MVP)
2. **Continuously Capture** screen content from the selected area.
3. **Detect Text** using OCR (EasyOCR) focused on JP/KR.
4. **Translate** extracted text to English.
5. **Display Result** in a floating, always-on-top UI widget.
6. Allow toggling translation on/off via UI button.

---

## 🗂️ Suggested Project Structure

```
manga_translator/
├── main.py                 # Entry point
├── screen_capture.py       # Screen grabbing logic
├── ocr_engine.py           # OCR processing module
├── translator.py           # Handles translation logic
├── overlay_display.py      # Responsible for drawing or displaying translations
├── ui_controller.py        # Small GUI control widget
├── utils.py                # Helper functions
├── assets/                 # Icons, fonts, etc.
├── logs/                   # Debug logs
└── requirements.txt        # Project dependencies
```

---

## 📅 MVP Development Timeline

| Date        | Task                                                            |
|-------------|-----------------------------------------------------------------|
| **July 9**  | Project setup, install dependencies, implement screen capture  |
| **July 10** | Integrate OCR & basic UI toggle                                |
| **July 11** | Add translation and overlay display                            |
| **July 12** | Final testing, bug fixes, packaging (PyInstaller or equivalent)|

---

## ✅ MVP Completion Criteria

- [ ] Program runs on Windows with minimal setup
- [ ] Small floating window is always on top
- [ ] User can start/stop continuous translation
- [ ] Screen is captured and checked for text every few seconds
- [ ] Japanese/Korean text is extracted and translated to English
- [ ] Translated text is shown in an overlay or pop-up window

---

## 🧪 Potential Stretch Features (Post-MVP)

- Region selection via drag-box interface
- Save translated screenshots for later review
- Vertical Japanese support (tate-chu-yoko)
- Text bubble segmentation (image processing)
- Multithreaded OCR and translation
- Hotkey controls for quick toggling

---

## 📦 Packaging

- Use [`PyInstaller`](https://www.pyinstaller.org/) or `cx_Freeze` to bundle the app into a standalone `.exe`
- Strip unnecessary features and dependencies for the MVP build

---

## 📝 License

This project is a personal utility. You are free to fork, modify, or build upon it as needed.

---

## 👨‍💻 Author

Don Joacquin Perez  
_Contact: [Your Email or GitHub Profile URL]_
