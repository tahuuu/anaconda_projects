# AI Python for Beginner

A collection of Jupyter notebooks for learning Python programming with AI integration using Google's Gemini API.

## 📚 Contents

This repository contains learning materials organized into modules:

### Module 1: Python Basics & AI Integration
**File:** `Module1.ipynb`

- Introduction to Python fundamentals
- Working with variables and data types
- String formatting with f-strings
- Basic AI integration with Gemini API
- Creating prompts for AI-generated content

**Topics Covered:**
- Print statements
- Variables (strings, integers, floats)
- F-string formatting
- Working with lists
- AI-powered content generation

### Module 2: Working with Lists
**Files:** `module2lesson1.ipynb`, `module2Lesson2.ipynb`

**Lesson 1: List Fundamentals**
- Creating and manipulating lists
- Accessing list elements
- Adding and removing items
- Using lists with AI prompts
- Batch processing tasks with AI

**Lesson 2: Loops and Automation**
- For loops basics
- Iterating through lists
- Automating repetitive tasks with AI
- Generating promotional content
- Translation and text correction

## 🚀 Getting Started

### Prerequisites

- Python 3.12+
- Anaconda Navigator (recommended)
- Google Gemini API key

### Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/AI-Python-for-Beginner.git
cd "AI Python for Beginner"
```

2. Install required packages:
```bash
pip install google-generativeai python-dotenv
```

3. Set up your API key:

Create a `.env` file in the project root:
```bash
touch .env
```

Add your Google API key:
```
GOOGLE_API_KEY=your_api_key_here
```

**Important:** Never commit your `.env` file to Git!

### Running the Notebooks

1. Open Anaconda Navigator
2. Launch Jupyter Notebook
3. Navigate to the notebook you want to run
4. Execute cells sequentially

## 🔐 Security Notes

- **Never hardcode API keys** in your notebooks
- Always use environment variables (`.env` file)
- The `.env` file is gitignored and won't be committed
- Revoke and regenerate keys if accidentally exposed

## 📖 Learning Path

Recommended order for beginners:

1. **Module1.ipynb** - Start here for Python basics
2. **module2lesson1.ipynb** - Learn about lists
3. **module2Lesson2.ipynb** - Master loops and automation
4. **experiment 1.ipynb** - Practice with real examples

## 🛠️ Common Use Cases

The notebooks demonstrate:

- **Content Generation**: Birthday poems, emails, stories
- **Translation**: Multi-language support
- **Text Processing**: Spell checking, formatting
- **Batch Operations**: Processing multiple items automatically
- **Creative Writing**: Reviews, descriptions, promotional content

## 📝 Example Code

### Basic AI Query
```python
import google.generativeai as genai
from dotenv import load_dotenv
import os

load_dotenv()
api_key = os.getenv('GOOGLE_API_KEY')
genai.configure(api_key=api_key)

model = genai.GenerativeModel(model_name="gemini-2.5-flash")
response = model.generate_content("Your prompt here")
print(response.text)
```

### Batch Processing with Lists
```python
tasks = ["Task 1", "Task 2", "Task 3"]
results = []

for task in tasks:
    response = model.generate_content(task)
    results.append(response.text)
```

## 🤝 Contributing

Feel free to fork this repository and submit pull requests with improvements or additional examples.

## 📄 License

This project is for educational purposes.

## 🔗 Resources

- [Google Gemini API Documentation](https://ai.google.dev/docs)
- [Python Documentation](https://docs.python.org/)
- [Jupyter Notebook Guide](https://jupyter-notebook.readthedocs.io/)

## ⚠️ Troubleshooting

### API Key Not Found
- Ensure `.env` file exists in the project root
- Check that `GOOGLE_API_KEY` is spelled correctly
- Verify the key is valid in Google Cloud Console

### Import Errors
- Install missing packages: `pip install google-generativeai python-dotenv`
- Restart Jupyter kernel after installation

### Rate Limiting
- Google Gemini has usage limits
- Add delays between requests if processing many items

## 📧 Contact tahuuuuuuuuu@gmail.com

For questions or issues, please open an issue in this repository.
