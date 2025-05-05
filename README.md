# 📘 English Vocabulary Flashcard Generator

A Python script that generates English vocabulary flashcards in Markdown format for use in **Obsidian**, tailored for the **Spaced Repetition** plugin.

# ✨ Features

- **Multisource Word Enrichment**:
  - Translations, examples and forms from [Linguee.com](https://www.linguee.com) using an [unofficial API wrapper](https://linguee-api.fly.dev/docs)
  - Definitions and examples from:
    - [Merriam-Webster Collegiate Dictionary](https://www.merriam-webster.com/)
    - [dictionaryapi.dev](https://dictionaryapi.dev/)
- **Audio Support**:
  - Embeds playable **British** and **American English** audio (if available).
- **Markdown Output**:
  - Generates Obsidian-compatible Markdown flashcards.
  - Format compatible with the [Spaced Repetition](https://github.com/st3v3nmw/obsidian-spaced-repetition) plugin for [Obsidian](https://www.obdisian.md)
- **Automated Processing**:
  - Reads words from `wordlist.md`, appends flashcards to `vocabulary.md`, and removes processed words.
  - Retrieves multiple examples, definitions, and translations per word.
- **Server Support**:
  - Optionally starts a local `linguee-api` server via `uvicorn` for faster/controlled access.

# 🧰 1. Install Required Software
## ✅ Step 1: Install Python

### Windows:
1. Go to https://www.python.org/downloads/
2. Click "Download Python 3.x.x"
3. Run the installer.

>[!Important]
>During installation, check ✅ “Add Python to PATH”, then click Install Now
### macOS:
1. Install Homebrew
2. Open Terminal and run:
3. brew install python
### Linux (Debian/Ubuntu):
```bash
sudo apt update
sudo apt install python3 python3-pip
```
## 📦 Download the Project Files
1. At the top of the page click the green `Code` button and `Download ZIP`  
2. Extract Zip to a folder

## 🔧 Install Dependencies
1. Navigate to the folder, right click it and `open in terminal/command line`
2. Execute the following command
```bash
pip install -r requirements.txt
```

## 🗝️Get Merriam-Webster API Key
1. Visit: https://dictionaryapi.com/register/index
2. Create an account
3. Choose the Collegiate Dictionary API
4. After registration, go to `My Keys`
5. Copy your API Key
6. In the folder create a file named `.env`
7. Open it and write the following to it:
```
API_KEY="your-api-key-here"
```
(Replace your-api-key-here with the actual API key from Merriam-Webster.)
8. Save the file.
## 📂 Set Up Obsidian Vault
1. Install Obsidian
	- Go to https://obsidian.md
	- Download and install for your OS
2. Create a Vault
	- Open Obsidian
	- Click "Create new vault"
	- Name it
	- Choose the folder you put all the files downloaded files inside
	- Click "Create"

### 🔌Install Spaced Repetition Plugin
1. Enable Community Plugins
	- In Obsidian, go to ⚙️ Settings > Community Plugins
	- Click Turn off Safe Mode (if it's off)
	- Click Browse
2. Search and Install:
	- Type Spaced Repetition
	- Click Install
	- Then click Enable
## 🚀 Running the Script
1. Open the folder in the terminal/command line once more
2. Run the script:
```bash
python vocabulary.py <amount of words to generate flashcards for>
```
3. In your Obsidian vault you should see new file called `vocabulary(.md)` with the flashcards inside it.
4. Press `ctrl + p` in obsidian and search for `Review flashcards in this note`

-> Output will be appended to vocabulary.md in flashcard format.

# 📁 File Structure

wordlist.md – Input file containing English words (one per line).

vocabulary.md – Output file where Markdown-formatted flashcards are appended.

.env – File storing your Merriam-Webster API key.

# 🔊 Flashcard Format (Example)

![Example](flashcard_example_light.png)
