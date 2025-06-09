### ✅ tool google translator


---

### 👨‍💻 Meanwhile, here’s a *generic example*:

#### 1. Required tools

* **Python** (>=3.7)
* **PyQt5** or **PySide6** (for the GUI)
* **Translation library** (e.g., `deep-translator`, `googletrans`)

#### 2. Basic script structure
- windows 10 script
```python
from PyQt5 import QtWidgets
from deep_translator import GoogleTranslator

class TranslatorApp(QtWidgets.QWidget):
    def __init__(self):
        super().__init__()
        self.init_ui()

    def init_ui(self):
        self.input = QtWidgets.QTextEdit()
        self.output = QtWidgets.QTextEdit()
        btn = QtWidgets.QPushButton("Translate")
        btn.clicked.connect(self.translate_text)

        layout = QtWidgets.QVBoxLayout()
        layout.addWidget(self.input)
        layout.addWidget(btn)
        layout.addWidget(self.output)
        self.setLayout(layout)
        self.setWindowTitle("Translator EN↔PT")

    def translate_text(self):
        src = self.input.toPlainText()
        # Auto-detect source language
        result = GoogleTranslator(source="auto", target="pt").translate(src)
        self.output.setPlainText(result)

if __name__ == "__main__":
    app = QtWidgets.QApplication([])
    win = TranslatorApp()
    win.show()
    app.exec()
```

This template:

* Creates a window with input field, a button, and output field.
* Uses `deep-translator` to auto-detect the language and translate to Portuguese.

---

### 🛠️ Installation Instructions (Windows 10, Ubuntu, macOS):

```bash
pip install pyqt5 deep-translator
```

#### Windows

* Install Python from the official installer.
* Then run `pip install ...` as above.

#### Ubuntu

```bash
sudo apt update
sudo apt install python3 python3-pip
pip3 install pyqt5 deep-translator
```

#### macOS

* Install Python via Homebrew: `brew install python`
* Then run: `pip3 install pyqt5 deep-translator`

---

### 📝 Next Steps

If you send me your actual script (or if you’re okay with using the example above), I can:

* Add step-by-step comments,
* Improve the interface (language selectors, history, menus),
* Provide install scripts for each OS.
