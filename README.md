# AI Meeting Assistant

## Overview

AI Meeting Assistant is an end-to-end meeting intelligence platform that transforms meeting recordings, audio files, and YouTube videos into actionable insights.

The system automatically transcribes conversations, generates concise summaries, extracts important information, and enables users to interact with meeting content through an AI-powered chat interface.

It supports both English and Hindi/Hinglish meetings and combines Speech-to-Text, Retrieval-Augmented Generation (RAG), Vector Databases, and Large Language Models to provide a complete meeting analysis workflow.

---

## Features

### Meeting Transcription

* Upload audio/video files or provide a YouTube URL.
* Automatic audio extraction and preprocessing.
* English transcription using OpenAI Whisper.
* Hindi and Hinglish transcription using Sarvam AI.

### AI-Powered Summarization

* Generate concise meeting summaries.
* Create meaningful meeting titles automatically.
* Produce structured bullet-point summaries.

### Action Item Extraction

* Identify tasks discussed during meetings.
* Extract owners responsible for tasks.
* Capture deadlines when mentioned.

### Key Decision Detection

* Automatically identify decisions made during discussions.
* Present important outcomes in a structured format.

### Open Questions & Follow-Ups

* Detect unresolved questions.
* Highlight pending discussions and follow-up items.

### Chat with Your Meeting

* Ask natural language questions about meeting content.
* Retrieval-Augmented Generation (RAG) powered search.
* Context-aware answers from meeting transcripts.

### Export Reports

* Download meeting reports as PDF.
* Export meeting data as TXT files.

---

## System Architecture

1. Input Processing

   * YouTube URL
   * Audio File
   * Video File

2. Audio Processing

   * Audio extraction
   * Audio chunking
   * Format conversion

3. Speech-to-Text

   * Whisper (English)
   * Sarvam AI (Hindi/Hinglish)

4. Transcript Analysis

   * Summary Generation
   * Action Item Extraction
   * Key Decision Extraction
   * Open Question Extraction

5. RAG Pipeline

   * Text Chunking
   * Embedding Generation
   * ChromaDB Storage
   * Similarity Retrieval

6. AI Assistant

   * Question Answering
   * Context Retrieval
   * Response Generation

---

## Technology Stack

### Programming Language

* Python

### Speech Recognition

* OpenAI Whisper
* Sarvam AI

### Large Language Models

* Mistral AI

### RAG & Vector Search

* LangChain LCEL
* ChromaDB
* HuggingFace Embeddings

### User Interface

* Streamlit

### Audio Processing

* FFmpeg
* Pydub
* yt-dlp

### Document Export

* ReportLab
* FPDF2

---

## Project Structure

```text
AI-Meeting-Assistant/
│
├── app.py
├── main.py
├── requirements.txt
├── .env
│
├── core/
│   ├── transcriber.py
│   ├── summarizer.py
│   ├── extractor.py
│   ├── rag_engine.py
│   └── vector_store.py
│
├── utils/
│   ├── audio_processor.py
│   └── helpers.py
│
├── exports/
│
├── temp/
│
└── README.md
```

---

## Installation

### Clone Repository

```bash
git clone https://github.com/your-username/AI-Meeting-Assistant.git
cd AI-Meeting-Assistant
```

### Create Virtual Environment

```bash
python -m venv .venv
```

### Activate Environment

Windows:

```bash
.venv\Scripts\activate
```

Linux / macOS:

```bash
source .venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Install FFmpeg

Windows:

```bash
winget install Gyan.FFmpeg
```

Verify installation:

```bash
ffmpeg -version
```

---

## Environment Variables

Create a `.env` file in the project root:

```env
MISTRAL_API_KEY=your_mistral_api_key

SARVAM_API_KEY=your_sarvam_api_key
```

---

## Running the Application

### Streamlit Interface

```bash
streamlit run app.py
```

Application will be available at:

```text
http://localhost:8501
```

### Command Line Interface

```bash
python main.py
```

---

## Example Workflow

1. Enter a YouTube URL or upload a meeting recording.
2. Select meeting language.
3. Generate transcript.
4. Create meeting summary.
5. Extract action items.
6. Extract key decisions.
7. Identify open questions.
8. Chat with meeting content.
9. Export final report.

---

## RAG Pipeline

The project uses Retrieval-Augmented Generation (RAG) for question answering.

### Process

1. Meeting transcript is generated.
2. Transcript is split into chunks.
3. Embeddings are created using HuggingFace models.
4. Embeddings are stored in ChromaDB.
5. Relevant chunks are retrieved based on user questions.
6. Mistral AI generates contextual responses.

This approach improves accuracy while reducing hallucinations.

---

## Use Cases

* Team Meeting Analysis
* Project Review Meetings
* Client Discussions
* Academic Lectures
* Research Interviews
* Product Planning Sessions
* Online Workshops
* Recorded Webinars

---

## Future Enhancements

* Multi-speaker diarization
* Real-time meeting transcription
* Meeting sentiment analysis
* Multi-language support
* Calendar integration
* Email report delivery
* Cloud deployment
* Team collaboration features

---

## Deployment

The application can be deployed using:

* Streamlit Community Cloud
* Render
* Railway
* AWS
* Azure
* Google Cloud Platform

---

## Author

Divyanshi Agarwal

Computer Science Engineering (AI & Data Science)

Graphic Era Deemed to be University

---

## License

This project is intended for educational, research, and portfolio purposes.
