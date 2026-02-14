# YouTube Video Summarizer and Q&A

An AI-powered application that fetches YouTube video transcripts, generates summaries, and answers questions about video content using IBM Watsonx AI and LangChain.

## Features

- Fetch transcripts from YouTube videos automatically
- Generate concise summaries of video content
- Ask questions about the video and get AI-powered answers
- Uses RAG (Retrieval Augmented Generation) with FAISS vector search
- Interactive web interface built with Gradio

## Prerequisites

- Python 3.8+
- IBM Watsonx AI account with project access

## Installation

1. Clone this repository
2. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

## Usage

Run the application:
```bash
python main.py
```

The Gradio interface will launch at `http://localhost:7860`

### How to Use

1. Enter a YouTube video URL in the input field
2. Click "Summarize Video" to get a summary of the video content
3. Type a question in the question field and click "Ask a Question" to get answers based on the video content

## Technologies Used

- **Gradio**: Web interface
- **YouTube Transcript API**: Fetch video transcripts
- **LangChain**: LLM orchestration and text processing
- **IBM Watsonx AI**: Language model (Granite 3.2 8B) and embeddings
- **FAISS**: Vector similarity search for RAG
- **RecursiveCharacterTextSplitter**: Text chunking for efficient processing

## How It Works

1. Extracts video ID from YouTube URL
2. Fetches English transcript using YouTube Transcript API
3. Processes and chunks the transcript
4. For summaries: Sends transcript to IBM Granite model
5. For Q&A: Creates FAISS vector index, retrieves relevant context, and generates answers

## License

MIT
