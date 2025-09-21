
# **Flashy: French-English Flashcards**

**Flashy** is a simple, interactive flashcard app built with Python and Tkinter to help you learn French vocabulary. The program shows a French word, then flips the card after a few seconds to reveal the English translation. Users can mark words as “known” or “unknown” to track learning progress.

---

## **Features**

* Displays random flashcards from a CSV file.
* Automatically flips cards after 3 seconds to show the translation.
* Tracks learned words and saves progress in `words_to_learn.csv`.
* Friendly UI with “Well done!” message when all words are learned.
* Easy to extend to other languages by modifying the CSV files.

---

## **Installation**

1. Clone the repository:

```bash
git clone <repository-url>
```

2. Navigate to the project folder:

```bash
cd flash-card-project
```

3. (Optional) Create a virtual environment and install dependencies:

```bash
python -m venv .venv
source .venv/bin/activate  # Linux/macOS
.venv\Scripts\activate     # Windows

pip install pandas
```

4. Make sure you have the following files:

```
data/french_words.csv
images/card_front.png
images/card_back.png
images/right.png
images/wrong.png
```
---

## 🎥 Demo Video

See the 3D viewer in action:

![Demo](demo/demo.mp4)


---

## **Usage**

Run the main program:

```bash
python main.py
```

* Click the **✓** button if you know the word.
* Click the **✗** button to skip to the next word.
* The app automatically updates `words_to_learn.csv` so you can resume where you left off.

---

## **Modifying for Other Languages**

Flashy is designed to be flexible. To use it with a different language pair:

1. Replace `data/french_words.csv` with a CSV containing your language pair.
2. Ensure the CSV has **two columns**, e.g.:

| Language1 | Language2 |
| --------- | --------- |
| Hallo     | Hello     |
| Tschüss   | Goodbye   |

3. Update the `next_card()` function if you want to change the text labels (`"French"` → `"German"`, etc.).

---

## **Folder Structure**

```
flash-card-project/
│
├── data/
│   ├── french_words.csv       # Original word list
│   └── words_to_learn.csv     # Updated as you learn
│
├── images/
│   ├── card_front.png
│   ├── card_back.png
│   ├── right.png
│   └── wrong.png
│
├── main.py                    # Flashcard app
└── README.md                  # This file
```

---

## **Future Improvements**

* Smooth card flipping animations.
* Multiple language sets selectable from the UI.
* Configurable flip time and fonts.
* Add sound pronunciation for words.

