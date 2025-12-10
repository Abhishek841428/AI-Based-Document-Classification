# PDF Sorter

An intelligent document classification and organization system using LLaMA for automated PDF sorting into categories (Finance, Procurement, Legal).

## Features

- 📄 **PDF Text Extraction**: Extract text from PDF files
- 🤖 **AI-Powered Classification**: Classify documents using LLaMA prompts
- 📁 **Automated Organization**: Route documents to appropriate folders
- 💻 **User-Friendly Interface**: Streamlit web UI for easy document processing

## Project Structure

```
pdf-sorter/
├── data/
│   ├── input/            # Temporary folder for uploaded PDFs
│   └── processed/        # Organized PDFs by category
│       ├── finance/
│       ├── procurement/
│       └── legal/
├── src/
│   ├── extract_text.py   # Extract text from PDFs
│   ├── classifier.py     # Classify text using LLaMA
│   ├── router.py         # Process and move PDFs
│   └── ui.py             # Streamlit UI
├── requirements.txt      # Project dependencies
├── run.py                # Launch the application
└── README.md             # This file
```

## Installation

1. **Clone or download the project**

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Ensure LLaMA is available** (via Ollama or similar):
   ```bash
   # If using Ollama
   ollama pull llama2
   ```

## Usage

### Run the Application

```bash
python run.py
```

The Streamlit UI will open in your default browser at `http://localhost:8501`

### Features in the UI

1. **Upload & Process**: Upload PDF files and automatically classify and sort them
2. **Classify Text**: Enter text directly to see classification results
3. **View Results**: Browse organized PDFs by category

## Configuration

Set the data directory in the sidebar of the Streamlit app to change where PDFs are stored and processed.

## Requirements

- Python 3.8+
- PyPDF2 - PDF text extraction
- Streamlit - Web UI framework
- Ollama/LLaMA - Local language model for classification

## Environment Variables

Create a `.env` file for sensitive configurations:

```
LLAMA_MODEL=llama2
DATA_DIR=./data
```

## Future Enhancements

- [ ] Fine-tune LLaMA model with domain-specific examples
- [ ] Add confidence thresholds for classification
- [ ] Support for more document categories
- [ ] Batch processing improvements
- [ ] Classification history and analytics

## License

MIT License

## Support

For issues or questions, please open an issue in the repository.
