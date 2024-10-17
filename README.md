# Data-Chatbot V 1.0
## by: Mohammad R. Abu Ayyash

![chatbot](https://github.com/user-attachments/assets/a4765f6f-363b-4b96-8f70-0e8c46a815a6)


This Streamlit app allows users to upload PDF, CSV, DOCX, or Excel files, extract their content, and interact with the extracted text using the Gemini API for chatbot-like responses. The app provides options to download the conversation history in various formats such as PDF, DOCX, and CSV. Here’s a breakdown of the app's key features:

## Key Features:

**1- File Upload and Text Extraction:**

Users can upload files in PDF, CSV, DOCX, or Excel (XLSX) formats.
The app processes the uploaded file and extracts its text content.
Extracted text is preprocessed by converting it to lowercase to standardize the text for better query handling.

**2- Gemini API Integration:**

**The app uses the Gemini 1.5 Flash model** to generate responses based on the uploaded file's content.
Users provide a query, and the app sends it along with the extracted text to the API.
The API response is displayed as a chatbot response, simulating an interactive conversation with the content of the file.

**3- Conversation History:**

All user queries and chatbot responses are stored in the session as a chat history.
The chat history is dynamically displayed on the app's interface, formatted for easy viewing.

**4- Downloadable Chat History:**

Users can download their conversation history in PDF, DOCX, or CSV format.

* PDF: The chat history is formatted for readability, with user queries and chatbot responses clearly separated and wrapped to fit the A4 page size.
* DOCX: The chat history is saved in a Word document, with clear headings for each query and response.
* CSV: The chat history is saved in a CSV file with two columns: 'Query' and 'Response'.

**5- File Handling:**

Supports multiple file types for uploading: PDF, CSV, DOCX, and Excel files.
Text extraction for each file type is done using:
PyMuPDF (fitz) for PDF.
pandas for CSV and Excel.
python-docx for DOCX.

**6- UI and Interaction:**

Users input their Gemini API key and can ask questions about the file’s content using a simple text input.
File type and extracted content are automatically detected and processed.
Download buttons for chat history are provided in the selected format (PDF, DOCX, or CSV).

## How it Works:

* The user uploads a file and the app extracts text using appropriate libraries depending on the file type.
* The user then asks a question, and the app sends the query along with the extracted text to the Gemini API to get a response.
* The response is displayed on the app, and both the user’s query and the chatbot’s response are stored in the chat history.
* The chat history can be downloaded in the user's preferred format (PDF, DOCX, CSV).
* This app provides a simple interface for interacting with document content through a chatbot and allows users to easily download the conversation history for future reference.

# Steps to Get a Gemini 1.5 flash API Key from Google AI Studio:
To interact with the Gemini model, **you need an API key.** Follow these steps to obtain one:

## 1- Create a Google Cloud Project:

* Go to the Google Cloud Console.
* Sign in with your Google account, or create one if you don't have it yet.
* Click on the Project dropdown at the top and select New Project.
* Name your project and click Create.

## 2- Enable Google Generative Language API:

* Once your project is created, go to the APIs & Services section from the left-hand menu.
* Click on Enable APIs and Services.
* Search for Generative Language API.
* Click on it, then click Enable to activate the API for your project.

## 3- Generate API Key:

* In the APIs & Services section, click on Credentials from the left-hand menu.
* Click Create Credentials and select API Key.
* An API key will be generated. Copy this key, as it will be used to interact with the Gemini model in the app.
* In the Streamlit app, enter your API key when prompted in the text input field labeled “Enter Gemini API Key”.

#### Make sure you've chosen Gemini 1.5 Flash Model.

## You can now ask questions related to the content of your uploaded files and receive responses from the Gemini model.
