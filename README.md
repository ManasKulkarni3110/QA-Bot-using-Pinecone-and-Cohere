# Interactive QA Bot with Gradio Interface

[![Python Version](https://img.shields.io/badge/python-3.10%2B-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This repository contains an interactive Question Answering (QA) bot that allows users to input queries, upload PDF documents, and retrieve real-time answers. The system is built with Python, Gradio for the user interface, and leverages various AI/ML models for document processing and question answering.

## 🚀 Features

- **Real-time QA Bot**: Ask questions and get answers based on provided documents.
- **PDF Upload Support**: Upload PDFs for document processing and analysis.
- **Gradio Interface**: Simple and interactive web-based user interface.
- **Dockerized**: Containerized for easy setup and deployment across different environments.
- **API Key Management**: Secure handling of API keys using environment variables.
- **Scalable Architecture**: Designed to handle multiple users and large documents efficiently.

## 📋 Requirements

- Python 3.10 or higher
- Gradio
- Cohere API (optional, for enhanced generative responses)
- Pinecone (optional, for efficient document embedding and retrieval)

## 🛠️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/interactive-qa-bot.git
cd interactive-qa-bot
```

### 2. Install Dependencies

Ensure you have Python 3.10+ installed, then set up a virtual environment and install dependencies:

```bash
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
pip install -r requirements.txt
```

### 3. API Key Configuration

Create a `.env` file in the root directory and add your API keys:

```
COHERE_API_KEY=your_cohere_api_key
PINECONE_API_KEY=your_pinecone_api_key
```

### 4. Run the App Locally

Start the Gradio app:

```bash
python app/main.py
```

Access the app at `http://localhost:7860`.

### 5. Running with Docker

a. Build the Docker image:

```bash
docker build -t interactive-qa-bot .
```

b. Run the Docker container:

```bash
docker run -p 7860:7860 --env-file .env interactive-qa-bot
```

Access the app at `http://localhost:7860`.

```

## 🧪 Testing

Run the test suite to ensure everything is working correctly:

```bash
pytest tests/
```

## 🔧 Troubleshooting

- **Notebook Errors**: If using Jupyter notebooks, ensure they are properly converted to Python scripts for Docker builds.
- **Missing API Keys**: Verify that all required API keys are correctly set in your environment variables or `.env` file.
- **Docker Issues**: Make sure Docker is installed and running on your system. Check Docker logs for detailed error messages.

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/AmazingFeature`)
3. Make your changes
4. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
5. Push to the branch (`git push origin feature/AmazingFeature`)
6. Open a Pull Request


## 📄 License

This project is licensed under the MIT License 

## 🙏 Acknowledgments

- [Gradio](https://www.gradio.app/) for the amazing interface framework
- [Cohere](https://cohere.ai/) for their powerful language models
- [Pinecone](https://www.pinecone.io/) for vector similarity search capabilities

## 📬 Contact

For any queries or support, please open an issue in the GitHub repository or contact the maintainers directly.

---

Happy coding! 🚀👨‍💻👩‍💻
