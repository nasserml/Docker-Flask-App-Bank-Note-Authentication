# Docker-Flask-App-Bank-Note-Authentication

This project is a Dockerized Flask application for bank note authentication. It provides a RESTful API with Swagger documentation.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Endpoints](#endpoints)
- [License](#license)

## Prerequisites
Before running the application, make sure you have the following dependencies installed:
- Python (version 3.8.0)
- Docker (version 20.10.24)

## Installation
1. Clone the repository: `git clone https://github.com/nasserml/Docker-Flask-App-Bank-Note-Authentication.git`
2. Change into the project directory: `cd Docker-Flask-App-Bank-Note-Authentication`
3. Create a virtual environment (optional but recommended): `python -m venv venv`
4. Activate the virtual environment: `source venv/bin/activate`
5. Install the required packages: `pip install -r requirements.txt`

## Usage
1. Build the Docker image: `docker build -t flask-app .`
2. Run the Docker container: `docker run -d -p 8000:8000 flask-app`

## Endpoints
The following endpoints are available:

- `GET /api/predict`: Predict the authenticity of a bank note.
  - Parameters:
    - `variance`: Variance of Wavelet Transformed image (required)
    - `skewness`: Skewness of Wavelet Transformed image (required)
    - `curtosis`: Curtosis of Wavelet Transformed image (required)
    - `entropy`: Entropy of image (required)
  - Example: `http://localhost:5000/api/predict?variance=2.5&skewness=1.5&curtosis=0.5&entropy=0.8`

- `GET /api/docs`: Swagger documentation for the API.

## License
This project is licensed under the [MIT License](LICENSE).
