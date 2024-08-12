
# EduQuizPro

Welcome to **EduQuizPro**! This repository features an innovative application designed for generating quizzes and interacting with PDF content. Utilizing Streamlit for the web interface, Langchain for document processing, and Google Cloud's VertexAI for advanced NLP, EduQuizPro transforms static PDF documents into interactive learning tools.

## Table of Contents

- [Introduction](#introduction)
- [Use Case](#use-case)
- [Tasks Overview](#tasks-overview)
  - [Task 1: PDF Processing](#task-1-pdf-processing)
  - [Task 2: Embedding Client](#task-2-embedding-client)
  - [Task 3: Chroma Collection Creator](#task-3-chroma-collection-creator)
  - [Task 4: Quiz Builder](#task-4-quiz-builder)
  - [Task 5: Quiz Generator](#task-5-quiz-generator)
  - [Task 6: Quiz Generation and Validation](#task-6-quiz-generation-and-validation)
  - [Task 7: Quiz Manager](#task-7-quiz-manager)
  - [Task 8: Complete Quiz Application](#task-8-complete-quiz-application)
  - [Task 9: Chat with PDF](#task-9-chat-with-pdf)
- [Setup and Installation](#setup-and-installation)
  - [Google Cloud Setup](#google-cloud-setup)
- [Usage](#usage)
- [Contributing](#contributing)

## Introduction

**EduQuizPro** is a cutting-edge application designed to enhance educational experiences by converting PDF documents into interactive quizzes and enabling real-time interactions with the document content. The application integrates modern NLP techniques and cloud-based AI to facilitate both quiz creation and content exploration.

## Use Case

**EduQuizPro** is tailored for:

1. **Educators:** Generate quizzes from textbooks or lecture notes to create customized assessments and review materials.
2. **Students:** Create quizzes from study materials for self-assessment and to reinforce learning.
3. **Training Professionals:** Convert manuals or training materials into quizzes to test comprehension and provide interactive learning experiences.

By leveraging EduQuizPro, users can efficiently create and manage quizzes, interact with content in dynamic ways, and streamline the learning and review process.

## Tasks Overview

### Task 1: PDF Processing

**File:** `tasks/task_1/task_1.py`

- Develop the `DocumentProcessor` class to handle the processing of PDF documents using Langchain's `PyPDFLoader`.
- Extract and display page details from the uploaded PDFs.

### Task 2: Embedding Client

**File:** `tasks/task_2/task_2.py`

- Implement the `EmbeddingClient` class to connect with Google Cloud's VertexAI for generating text embeddings.
- Manage document and query embeddings using the specified model.

### Task 3: Chroma Collection Creator

**File:** `tasks/task_3/task_3.py`

- Create the `ChromaCollectionCreator` class to build and index Chroma collections from processed documents.
- Split documents into manageable text chunks and index using the embedding model.

### Task 4: Quiz Builder

**File:** `tasks/task_4/task_4.py`

- Build the `QuizBuilder` application with Streamlit to allow document uploads, quiz topic specification, and quiz generation.

### Task 5: Quiz Generator

**File:** `tasks/task_5/task_5.py`

- Design the `QuizGenerator` class to create quiz questions based on the provided topic.
- Utilize vectorstore and LLM for structured quiz question generation in JSON format.

### Task 6: Quiz Generation and Validation

**File:** `tasks/task_6/task_6.py`

- Extend the `QuizGenerator` class to validate the uniqueness of questions and compile a unique set for the quiz.

### Task 7: Quiz Manager

**File:** `tasks/task_7/task_7.py`

- Develop the `QuizManager` class to handle quiz operations, including question navigation and retrieval.

### Task 8: Complete Quiz Application

**File:** `tasks/task_8/task_8.py`

- Integrate all previous components into a cohesive quiz application, encompassing the full workflow from PDF uploading to quiz management.

### Task 9: Chat with PDF

**File:** `tasks/task_9/task_9.py`

- Add the `ChatWithPDF` feature to enable users to interactively query PDF content and receive contextual answers based on the integrated components.

## Setup and Installation

To get started with EduQuizPro, follow these steps:

1. **Clone the repository:**

   ```sh
   git clone https://github.com/your-username/eduquizpro.git
   cd eduquizpro
   ```

2. **Create and activate a virtual environment:**

   ```sh
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install the required dependencies:**

   ```sh
   pip install -r requirements.txt
   ```

4. **Run the Streamlit application:**

   ```sh
   streamlit run tasks/task_9/task_9.py
   ```

### Google Cloud Setup

1. **Create a Google Cloud Project:**

   - Go to the Google Cloud Console.
   - Click on the project drop-down and select "New Project".
   - Provide a project name and click "Create".

2. **Enable Vertex AI API:**

   - Navigate to "APIs & Services" > "Library" in the Google Cloud Console.
   - Search for "Vertex AI" and click "Enable".

3. **Set up Authentication:**

   - Install the Google Cloud SDK.
   - Authenticate your installation with:
     ```sh
     gcloud auth login
     ```
   - Set your project in the SDK:
     ```sh
     gcloud config set project your-project-id
     ```

4. **Download and Configure Service Account Key:**

   - Go to "IAM & Admin" > "Service Accounts".
   - Select your project and click "Create Service Account".
   - Create a key and download the JSON file.
   - Set the `GOOGLE_APPLICATION_CREDENTIALS` environment variable:
     ```sh
     export GOOGLE_APPLICATION_CREDENTIALS="/path/to/your/service-account-file.json"
     ```

## Usage

1. **Upload PDF Documents:**
   Use the interface to upload PDF documents for processing.

2. **Generate Quizzes:**
   Define quiz topics and specify the number of questions to generate quizzes based on the uploaded content.

3. **Chat with PDF:**
   Interact with the PDF content by asking questions and receiving detailed answers through the chat interface.

