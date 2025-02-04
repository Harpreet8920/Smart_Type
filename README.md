# Smart_Type
# Predictive Keyboard with NLP

A modern, intelligent predictive keyboard system that uses Natural Language Processing (NLP) to provide real-time word suggestions and autocorrect functionality. Built with Python (Flask) backend and React TypeScript frontend.

## Features

- **Real-time Word Predictions**: Uses N-gram language models to predict the next word based on context
- **Intelligent Autocorrect**: Automatically suggests corrections for common misspellings
- **Modern UI**: Clean, responsive interface built with React and Tailwind CSS
- **Docker Support**: Easy deployment with Docker and Docker Compose
- **RESTful API**: Flask-based backend with CORS support

## Tech Stack

### Backend
- Python 3.9
- Flask
- NLTK
- NumPy
- Scikit-learn
- Python-Levenshtein
- Gunicorn
- Flask-CORS

### Frontend
- React 18
- TypeScript
- Tailwind CSS
- Vite
- Lucide React (for icons)

## Getting Started

### Prerequisites
- Docker and Docker Compose
- Node.js (for local development)
- Python 3.9+ (for local development)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/predictive-keyboard.git
cd predictive-keyboard
```

2. Start the application using Docker Compose:
```bash
docker-compose up --build
```

The application will be available at:
- Frontend: http://localhost:5173
- Backend API: http://localhost:5000

### Local Development

1. Install backend dependencies:
```bash
pip install -r requirements.txt
```

2. Install frontend dependencies:
```bash
npm install
```

3. Start the backend server:
```bash
python app.py
```

4. Start the frontend development server:
```bash
npm run dev
```

## API Endpoints

### POST /predict
Predicts the next word based on the given context.

Request body:
```json
{
  "context": "i am"
}
```

Response:
```json
{
  "predictions": ["going", "happy", "a", "not", "the"]
}
```

### POST /autocorrect
Suggests corrections for potentially misspelled words.

Request body:
```json
{
  "word": "teh"
}
```

Response:
```json
{
  "correction": "the"
}
```

## Project Structure

```
.
├── src/
│   ├── components/
│   │   └── PredictiveKeyboard.tsx
│   ├── lib/
│   │   └── languageModel.ts
│   ├── App.tsx
│   └── main.tsx
├── app.py
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
└── package.json
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [NLTK](https://www.nltk.org/) for natural language processing capabilities
- [React](https://reactjs.org/) for the frontend framework
- [Tailwind CSS](https://tailwindcss.com/) for styling
- [Flask](https://flask.palletsprojects.com/) for the backend framework
