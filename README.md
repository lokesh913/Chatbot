# Agricultural Chatbot with PDF Knowledge Base

An intelligent agricultural assistant built using Flask and Google's Gemini 2.5 Flash AI that provides farmers with expert agricultural information. The assistant can answer general agriculture-related questions and analyze uploaded PDF documents to provide specific information based on their content.

## Features

- **Dual-Mode Chatbot**: Can answer general agricultural questions or specific queries based on uploaded PDF documents
- **Modern ChatGPT-like Interface**: Clean, intuitive UI with a sidebar for PDF management
- **PDF Document Analysis**: Upload and analyze any PDF document to extract information
- **Vector Database Storage**: Stores PDF content using ChromaDB for semantic search
- **Gemini AI Integration**: Powered by Google's Gemini 2.5 Flash model
- **Responsive Design**: Works on desktop and mobile devices
- **Session Management**: Maintains conversation context

## Tech Stack

- **Backend**: Flask (Python)
- **Frontend**: HTML, CSS, JavaScript, Bootstrap 5
- **PDF Processing**: PyMuPDF
- **AI Model**: Google Gemini 2.5 Flash
- **Vector Database**: ChromaDB
- **Environment Variables**: python-dotenv

## Installation

1. Clone the repository:
```bash
git clone https://github.com/lokesh913/Chatbot.git
cd Chatbot
```

2. Create a virtual environment and activate it:
```bash
python -m venv .venv
# On Windows
.venv\Scripts\activate
# On macOS/Linux
source .venv/bin/activate
```

3. Install the dependencies:
```bash
pip install -r requirements.txt
```

4. Create a `.env` file in the project root with your Google API key:
```
GOOGLE_API_KEY=your_google_api_key_here
SECRET_KEY=your_secret_key_for_flask_session
```

5. Run the application:
```bash
python app.py
```

6. Open your browser and navigate to `http://127.0.0.1:5000/`

## How It Works

1. **General Agriculture Queries**:
   - Ask any agriculture-related question directly in the chat interface
   - The Gemini AI model provides detailed information on farming, crops, livestock, etc.

2. **PDF Document Analysis**:
   - Upload a PDF document using the sidebar
   - The system extracts text from the PDF and stores it in a vector database
   - Ask questions specifically about the PDF content
   - The system retrieves relevant sections and generates accurate answers

3. **Chat Management**:
   - Start a new chat anytime by clicking "New chat" in the sidebar
   - Current PDF context is reset when starting a new chat

## Project Structure

```
Chatbot/
├── app.py                # Main Flask application file
├── requirements.txt      # Project dependencies
├── .env                  # Environment variables (not in repo)
├── static/
│   ├── css/
│   │   └── style.css     # Custom styling
│   ├── js/               # JavaScript files (unused)
│   └── uploads/          # Uploaded PDF files
└── templates/
    ├── index.html        # Home page template
    └── chat.html         # Chat interface template
```

## API Routes

- `/`: Home page
- `/chat`: Chat interface page
- `/new_chat`: Reset chat and start a new conversation
- `/upload`: Upload a PDF document
- `/query`: API endpoint for processing chat queries

## Development

To contribute to this project:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin feature-name`
5. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements

- Google Gemini for the powerful AI model
- ChromaDB for the vector database
- PyMuPDF for PDF text extraction
- Bootstrap team for the UI components

## Author

- **Lokesh Chavan** - [lokesh913](https://github.com/lokesh913) 
