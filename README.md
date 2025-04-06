# PDF Q&A System

## Getting Started

1. Extract the tar file:
```bash
# On Windows (using PowerShell)
tar -xzf task3.tar.gz

# On Unix/macOS
tar -xzf task3.tar.gz
```

## Project Overview
A web application that allows users to upload PDF documents and ask questions about their content. The system uses vector embeddings and semantic search to provide accurate answers and relevant suggestions.

## Features

- Upload PDF documents
- Ask questions about the uploaded content
- Get accurate answers using semantic search
- Receive relevant question suggestions
- Modern and user-friendly interface

## Setup

1. Create a virtual environment:
```bash
python -m venv venv
```

2. Activate the virtual environment:
```bash
# Windows
venv\Scripts\activate

# Unix/macOS
source venv/bin/activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Set up environment variables:
Create a `.env` file in the root directory with your OpenAI API key:
```
OPENAI_API_KEY=your_api_key_here
```

## Running the Application

1. Start the FastAPI backend server:
```bash
uvicorn backend.main:app --reload --port 6565
```

2. Start the Streamlit frontend:
```bash
streamlit run frontend/app.py --server.port 5656
```

3. Open your browser and navigate to `http://localhost:5656`

## Project Structure

```
.
├── backend/
│   ├── main.py
│   └── utils/
│       ├── pdf_processor.py
│       └── vector_store.py
├── frontend/
│   ├── app.py
│   └── utils/
│       ├── api_client.py
│       └── constants.py
├── requirements.txt
└── README.md
```

## Technologies Used

- Backend: FastAPI, OpenAI API, PyMuPDF
- Frontend: Streamlit
- Vector Embeddings: OpenAI's text-embedding-3-small
- Natural Language Processing: OpenAI's GPT-3.5-turbo

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.
