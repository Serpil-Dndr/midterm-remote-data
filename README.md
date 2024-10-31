# Student Management API

This project is a simple RESTful API for managing student records using Flask. It supports basic CRUD operations (Create, Read, Update, Delete) for a Student entity.

## Features

- **Endpoints**:
  - `GET /students`: Retrieve a list of all students.
  - `GET /students/{id}`: Retrieve details of a student by ID.
  - `POST /students`: Add a new student.
  - `PUT /students/{id}`: Update an existing student by ID.
  - `DELETE /students/{id}`: Delete a student by ID.


## Prerequisites

Before you can run or deploy this app, you need to have the following installed:

- Python 3.x
- pip (Python package manager)
- Flask (`pip install Flask`)
- gunicorn (`pip install gunicorn`)
- Azure CLI (optional, for deployment)

## Project Structure

- app.py: Main Flask application 
- requirements.txt: List of Python dependencies 
- test-api.http: Test the REST API using the REST Client extension in Visual Studio Code
- README.md: Documentation

## Running Locally

To run the Flask API on your local machine:

1. Clone this repository:

   ```bash
   git clone https://github.com/Serpil-Dndr/midterm-remote-data.git
   
2. Navigate to the project directory:
   ```bash
   cd Midterm-remote
3. Install the dependencies:
   ```bash
   pip install -r requirements.txt
4. Run the application:
   ```bash
   python app.py
5. The API will be running at http://127.0.0.1:8000
6. Use **test-api.http** to test the REST API using the REST Client extension in Visual Studio Code.

### Steps to Deploy

### 1. Log in to Azure Portal
- Go to [Azure Portal](https://portal.azure.com/) and sign in.

### 2. Create a Resource Group
1. Click on **"Resource groups"** in the left menu.
2. Click **"+ Create"**.
3. Fill in:
   - **Resource Group Name**: e.g., `myResourceGroup`
   - **Region**: Choose a location (e.g., East US).
4. Click **"Review + Create"** and then **"Create"**.

### 3. Create a Web App
1. Click on **"App Services"**.
2. Click **"+ Add"**.
3. Fill in:
   - **Name**: Unique name for your app (e.g., `myFlaskApp`).
   - **Publish**: Select **Code**.
   - **Runtime Stack**: Choose **Python 3.8**.
   - **Region**: Match your resource group.
4. Click **"Review + Create"** and then **"Create"**.

### 4. Deploy Your Application
1. In your app service, go to **"Deployment Center"**.
2. Choose your deployment source (e.g., **GitHub**, **Zip file**).
3. Follow the prompts to complete the setup.

### 5. Access Your Web App
- Find your app's URL (e.g., `https://<your-app-name>.azurewebsites.net`).
- Click the URL to view your deployed Flask API.