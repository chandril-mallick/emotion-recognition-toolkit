# Emotion Detector Chat App

A real-time chat application that detects emotions in messages using Natural Language Processing (NLP) and displays corresponding emojis in the navbar.

## Features

- Real-time emotion detection as you type
- Displays emotion emojis in the navbar
- Modern and responsive UI
- Dark mode support
- Built with React and FastAPI

## Tech Stack

- **Frontend**: React, Vite, Axios
- **Backend**: FastAPI, Python
- **NLP Model**: j-hartmann/emotion-english-distilroberta-base from Hugging Face

## Prerequisites

- Node.js (v14 or higher)
- Python (3.8 or higher)
- pip (Python package manager)

## Setup Instructions

### Backend Setup

1. Navigate to the backend directory:
   ```bash
 
   cd backend
   ```

2. Create a virtual environment (recommended):
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

4. Start the FastAPI server:
   ```bash
   uvicorn app:app --reload
   ```
   The backend server will be available at `http://localhost:8000`

### Frontend Setup

1. Open a new terminal and navigate to the frontend directory:
   ```bash
   cd emotion-detector
   cd frontend
   ```

2. Install the required Node.js packages:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```
   The frontend will be available at `http://localhost:5173`

## Usage

1. Open the application in your web browser
2. Start typing messages in the chat input
3. The app will detect the emotion in your message and display the corresponding emoji in the navbar
4. Sent messages will be displayed with their detected emotion emoji

## API Endpoints

- `POST /detect_emotion` - Analyzes text and returns the detected emotion
  - Request body: `{ "message": "Your text here" }`
  - Response: 
    ```json
    {
      "emotion": "joy",
      "emoji": "😊",
      "score": 0.98,
      "message": "Your original message"
    }
    ```

## Project Structure

```
emotion-detector/
├── backend/
│   ├── app.py              # FastAPI application
│   └── requirements.txt     # Python dependencies
└── frontend/
    ├── public/              # Static files
    ├── src/
    │   ├── components/      # React components
    │   │   └── ChatEmotionApp.jsx  # Main chat component
    │   ├── App.jsx          # Main application component
    │   ├── App.css          # Application styles
    │   └── main.jsx         # Application entry point
    ├── package.json         # Node.js dependencies
    └── vite.config.js       # Vite configuration
```

## License

This project is open source and available under the [MIT License](LICENSE).
