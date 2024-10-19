# Interactive QA Bot with Gradio Interface

This repository contains an interactive Question Answering (QA) bot that allows users to input queries, upload PDF documents, and retrieve real-time answers. The system is built with Python, Gradio for the user interface, and leverages various AI/ML models for document processing and question answering. The project is containerized using Docker for easy deployment.

## Features
- **Real-time QA Bot**: Users can ask questions and get answers based on provided documents.
- **PDF Upload Support**: Users can upload PDFs, and the system processes them to answer queries.
- **Gradio Interface**: Simple and interactive interface for user interaction.
- **Dockerized**: Containerized for easy setup and deployment.
- **API Key Management**: Securely manage API keys using environment variables.

## Requirements

- **Python 3.10** or higher
- **Gradio**: For the user interface
- **Cohere API**: For generative responses (optional)
- **Pinecone**: For efficient document embedding and retrieval (optional)

## Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name
2. Install Dependencies
Ensure you have Python 3.10 installed. Install the required dependencies via pip:

bash
Copy code
pip install -r requirements.txt
3. API Key Configuration
For using external services (like Cohere and Pinecone), you need to set the API keys in the environment. Create a .env file and add your keys:

bash
Copy code
COHERE_API_KEY=your_cohere_api_key
PINECONE_API_KEY=your_pinecone_api_key
Alternatively, you can pass these keys directly as environment variables when running the Docker container.

4. Run the App Locally
You can run the Gradio app locally by executing the following command:

bash
Copy code
python Part_2.py
The app will start on http://localhost:7860 by default.

5. Running with Docker
a. Build the Docker Image
Ensure Docker is installed on your system, then build the image:

bash
Copy code
docker build -t qa-bot .
b. Run the Docker Container
Run the container, exposing port 7860:

bash
Copy code
docker run -p 7860:7860 --env-file .env qa-bot
The app will now be accessible at http://localhost:7860.

Project Structure
bash
Copy code
📁 your-repo-name/
├── 📁 app/               # Contains main application files
├── Part_2.ipynb          # Jupyter Notebook with Gradio app
├── requirements.txt      # Project dependencies
├── Dockerfile            # Docker configuration
└── README.md             # This readme file
Troubleshooting
Notebook Errors: If you encounter issues related to Jupyter notebook dependencies, ensure the notebook is properly converted to a Python script as part of the Docker build process.
Missing API Keys: Ensure that the required API keys (e.g., Cohere, Pinecone) are correctly set in environment variables.
Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements, bug fixes, or feature additions.

Steps to Contribute:
Fork the repository.
Create a new branch (git checkout -b feature-branch).
Make your changes and commit (git commit -m 'Add new feature').
Push to the branch (git push origin feature-branch).
Open a pull request.
License
This project is licensed under the MIT License - see the LICENSE file for details.