# 🤖 AI Document Intelligence & Q&A

An AI-powered document intelligence system that allows users to upload documents, ask questions, generate summaries, and extract information from document content using OCR and AI.

This project is **Day 10 of my 30 Days AI Automation Challenge**, where I am building and documenting practical automation projects using **n8n, AI Agents, OCR, APIs, webhooks, JavaScript, and automation workflows**.

## 🌐 Live Demo

🚀 **Live Website:**  
https://junaidzulfiqar07.github.io/AI-Document-Intelligence/

> ⚠️ **Live Demo Availability:** The live demo will be available until **25th August 2026** only.

## 📌 Project Overview

**AI Document Intelligence & Q&A** is a web-based document analysis and question-answering system designed to make it easier to understand and interact with uploaded documents.

Users can upload a document and ask questions such as:

- Summarize this document.
- What are the eligibility criteria?
- What requirements are mentioned?
- What are the important dates?
- List the key points from this document.
- What qualifications are required?

The system uses **Mistral OCR** to extract content from scanned or image-based PDFs and an **AI Agent powered by OpenAI** to answer questions based on the extracted document content.

## ✨ Features

- 📄 PDF document upload
- 🔍 OCR for scanned and image-based PDFs
- 🤖 AI-powered document question answering
- 📝 Automatic document summarization
- 🔎 Information extraction
- 📚 Document-based answers
- 🚫 Reduced hallucination through document-grounded instructions
- ⚡ n8n workflow automation
- 🔗 Webhook integration
- 🌐 GitHub Pages deployment
- 📱 Responsive web interface
- 🎯 AI-generated responses based on uploaded document content

## 🧠 How It Works

User Uploads Document → Frontend → n8n Webhook → Mistral OCR → Extract Document Content → OpenAI AI Agent → Process User Question → Generate Answer → Respond to Webhook → Frontend Displays Result

## 🔧 n8n Workflow

### 1. Webhook

The frontend sends the uploaded document and user's question to an n8n Webhook.

**HTTP Method:** POST

The webhook receives:

- Uploaded document
- User question

### 2. Mistral OCR

The uploaded document is processed using **Mistral OCR**.

**Model:** mistral-ocr-latest

**Input Type:** Binary Data

Mistral OCR extracts readable content from scanned and image-based documents.

This is especially useful for documents where traditional PDF text extraction cannot retrieve the actual content.

### 3. AI Agent

The extracted OCR content is passed to an AI Agent together with the user's question.

The AI Agent is instructed to:

- Use only the provided document content
- Answer questions based on the document
- Generate summaries when requested
- Avoid unsupported assumptions
- Preserve important names, dates, numbers, and requirements
- Clearly state when requested information is not available

### 4. Respond to Webhook

The AI Agent's response is returned to the frontend through the **Respond to Webhook** node.

**Response Type:** JSON

The frontend then displays the generated response.

## 🛠️ Tech Stack

### Frontend

- HTML5
- CSS3
- JavaScript

### Automation

- n8n
- Webhooks

### AI & OCR

- OpenAI
- Mistral OCR

### Deployment

- GitHub
- GitHub Pages

## 📂 Project Structure

AI-Document-Intelligence/
├── index.html
└── README.md

## 💡 Example Questions

After uploading a document, users can ask:

- Summarize this document.
- What are the eligibility criteria?
- What requirements are mentioned?
- What are the important dates?
- List the main points from this document.
- What qualifications are required?

## 🧪 Example Use Case

A user uploads a scanned PDF containing qualification criteria.

The system:

1. Receives the PDF through the n8n Webhook.
2. Sends the document to Mistral OCR.
3. Extracts the actual text from the document pages.
4. Passes the extracted content to the AI Agent.
5. Sends the user's question to the AI Agent.
6. Generates an answer based on the document.
7. Returns the response through the Webhook.
8. Displays the result on the frontend.

## 🎯 Problem Solved

Traditional PDF text extraction can fail when documents contain scanned images instead of selectable text.

During development, the initial PDF extraction process returned mostly:

CamScanner  
CamScanner  
CamScanner

instead of the actual document content.

To solve this problem, **Mistral OCR** was integrated into the workflow.

The OCR layer extracts meaningful content from scanned documents before sending it to the AI Agent.

## 🔐 AI Response Rules

The AI Agent is instructed to:

- Use only the uploaded document content
- Avoid hallucinating information
- Avoid unsupported assumptions
- Preserve important names, dates, and numbers
- Answer questions directly
- Summarize documents when requested
- Clearly state when information is not available

## 🚀 Deployment

The frontend is deployed using **GitHub Pages**.

### Live Application

https://junaidzulfiqar07.github.io/AI-Document-Intelligence/

**Live Demo Availability:** Until **25th August 2026** only.

## 📈 Future Improvements

Potential improvements include:

- 📚 Multiple document support
- 💬 Conversation history
- 📑 DOCX and PPTX support
- 🔎 Advanced document search
- 📊 Document analytics
- 🧠 RAG-based document retrieval
- 📥 Downloadable AI summaries
- 🔐 User authentication
- ☁️ Cloud document storage
- 🌍 Multi-language OCR
- 🎙️ Voice-based document questions

## 👨‍💻 Developer

**Junaid Zulfiqar**

Computer Engineering Student  
**UET Taxila**

## 📅 30 Days AI Automation Challenge

This project is part of my **30 Days AI Automation Challenge**.

### Day 10 — AI Document Intelligence & Q&A

Building practical AI automation projects using:

- n8n
- AI Agents
- OCR
- APIs
- Webhooks
- JavaScript
- Automation workflows

## ⭐ Support

If you found this project useful, consider giving the repository a ⭐.

---

© 2026 Junaid Zulfiqar. All Rights Reserved.
