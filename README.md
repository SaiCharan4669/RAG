# Multimodal Video Retrieval System using RAG + CLIP + Whisper + LanceDB

This project demonstrates a locally processed multimodal RAG (Retrieval-Augmented Generation) system built using a downloaded YouTube video.  
The pipeline processes video, audio, text, and frames, converts them into embeddings, stores them efficiently, and performs high-speed multimodal retrieval using LanceDB.

---

##  Project Overview

This system allows you to:
- Download YouTube videos locally using PyTube
- Extract high-precision transcriptions using OpenAI Whisper
- Extract representative keyframes using MoviePy
- Parse metadata (title, views, description)
- Generate multimodal embedding using OpenAI CLIP
- Store embeddings in LanceDB for efficient vector search
- Process user queries → convert to embeddings → run similarity search
- Retrieve the most relevant 
- Achieve fast processing 

##  Architecture

YouTube Video → PyTube Download
↓
Audio-to-Text → Whisper
↓
Keyframe Extraction → MoviePy
↓
Text + Image Embeddings → OpenAI CLIP
↓
Vector Storage → LanceDB
↓
User Query → Query Embedding
↓
Similarity Search → Retrieve Relevant Frames + Transcript
↓
Final Output


# Features

# Local Multimodal Processing
- Works fully offline once the video is downloaded.
- No cloud storage required.

# Whisper Transcription
- High-precision speech-to-text from OpenAI Whisper.

#  Keyframe Extraction
- Reduced data size while maintaining contextual integrity.
- Extracted using MoviePy.

# CLIP Embeddings
- Generates semantic embeddings for:
  - video frames (images)
  - transcript text
  - metadata text

# LanceDB Vector Database
- Efficient, file-based vector store.
- Supports hybrid multimodal similarity search.

# Query Processing
- Converts user query into CLIP embeddings.
- Retrieves:
  - relevant frames  
  - transcript chunks  
  - metadata  

# Performance
- End-to-end processing of a 4-minute video in ~20 seconds.

---
