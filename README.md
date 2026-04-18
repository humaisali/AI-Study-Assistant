<div align="center">

# AI Study Assistant

### Turn your study notes into clear explanations and practice quizzes — powered by Google Gemini AI

[![Live Demo](https://img.shields.io/badge/Live%20Demo-ai--study--assistant.vercel.app-00D4FF?style=for-the-badge)](https://ai-study-assistant-ashy.vercel.app/)
[![React](https://img.shields.io/badge/React%2018-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)](https://nodejs.org/)
[![Google Gemini](https://img.shields.io/badge/Gemini%201.5%20Flash-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://deepmind.google/technologies/gemini/)

</div>

---

## Overview

AI Study Assistant is a full-stack web application that takes your study documents and transforms them into easy-to-understand explanations, smart summaries, and interactive multiple-choice quizzes — all powered by **Google Gemini 1.5 Flash**.

**Live Demo:** [ai-study-assistant-ashy.vercel.app](https://ai-study-assistant-ashy.vercel.app/)

---

## Features

| Feature | Description |
|---|---|
| **File Upload** | Supports PDF, TXT, Markdown, and PPTX files up to 15MB |
| **AI Explanation** | Gemini explains your notes in simple, clear language |
| **Quiz Generation** | Auto-generated multiple choice practice questions |
| **Smart Summary** | Concise bullet-point summary of key concepts |
| **Difficulty Levels** | Beginner, Intermediate, or Advanced explanations |
| **Quiz Scoring** | Track your performance with a score card |

---

## Tech Stack

| Layer | Technology |
|---|---|
| **Frontend** | React 18, Vite, Tailwind CSS 3 |
| **HTTP Client** | Axios |
| **Markdown** | react-markdown |
| **Backend** | Node.js, Express |
| **File Uploads** | Multer |
| **PDF Parsing** | pdf-parse |
| **AI Engine** | Google Gemini 1.5 Flash |

---

## Project Structure

```
AI-Study-Assistant/
├── client/                        # React + Vite frontend
│   └── src/
│       ├── components/
│       │   ├── UploadBox.jsx      # Drag-and-drop file upload
│       │   ├── ExplanationPanel.jsx # AI explanation display
│       │   ├── QuizPanel.jsx      # Interactive quiz
│       │   └── Loader.jsx         # Animated loading state
│       ├── services/
│       │   └── aiService.js       # Axios API calls
│       └── pages/
│           └── Home.jsx           # Main page
├── server/                        # Node.js + Express backend
│   ├── controllers/
│   │   └── aiController.js        # Request handler + file extraction
│   ├── routes/
│   │   └── aiRoutes.js            # Express routes + multer config
│   ├── services/
│   │   └── geminiService.js       # Gemini API integration
│   └── utils/
│       └── prompts.js             # AI prompt templates
└── package.json
```

---

## Getting Started

### Prerequisites

- Node.js v18+
- Google Gemini API key — [Get one free here](https://makersuite.google.com/app/apikey)

### Installation

```bash
# Clone the repository
git clone https://github.com/humaisali/AI-Study-Assistant.git
cd AI-Study-Assistant

# Install all dependencies
npm run install:all

# Configure environment
cd server
cp .env.example .env
# Add your GEMINI_API_KEY to the .env file
```

### Run Development Servers

```bash
npm run dev
```

- Frontend: http://localhost:5173
- Backend: http://localhost:5000

---

## API Reference

### POST /api/study

| Field | Type | Required | Description |
|---|---|---|---|
| `file` | File | Yes | PDF, TXT, MD, or PPTX (max 15MB) |
| `difficulty` | string | No | `beginner`, `intermediate`, or `advanced` |

### GET /api/health

Health check endpoint.

---

## Supported File Types

| Format | Notes |
|---|---|
| `.pdf` | Text-based PDFs only (scanned PDFs not supported) |
| `.txt` | Plain text files |
| `.md` / `.markdown` | Markdown files |
| `.pptx` | PowerPoint presentations (text extraction) |

---

## Author

**Humais Ali** — Full Stack Developer at SkyTech Developers

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/humaisaliskytechdeveloper)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)](https://github.com/humaisali)
