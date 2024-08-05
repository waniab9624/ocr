# ocr
# Django OCR Application

## Project Overview

This Django application allows users to upload images or capture images via a webcam, then uses Optical Character Recognition (OCR) to extract text from the images. The extracted text can be viewed on the website and downloaded as a text file or a PDF. The extracted text and metadata are also stored in a database for future reference.

## Features

- Image upload for OCR processing
- Webcam capture for OCR processing
- Text extraction using Tesseract OCR
- Display extracted text on the web page
- Download extracted text as a text file or PDF
- Store extracted text and metadata in a database

## Prerequisites

- Python 3.x
- Django 3.x or higher
- Tesseract OCR

## Installation

1. **Clone the repository:**

```bash
git clone https://github.com/yourusername/ocr_project.git
cd ocr_project
Create a virtual environment and activate it:
bash
Copy code
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
Install the required packages:
bash
Copy code
pip install -r requirements.txt
Install Tesseract OCR:
Windows:
Download and install Tesseract from the official GitHub releases page.
Add Tesseract to your system PATH.
Configuration
Set the Tesseract executable path in your Django settings (if necessary):
ocrapp/views.py:

python
Copy code
pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'
Create and apply database migrations:
bash
Copy code
python manage.py makemigrations
python manage.py migrate
Run the development server:
bash
Copy code
python manage.py runserver
Access the application:
Open your web browser and go to http://127.0.0.1:8000/

Usage
Upload an Image:

Go to the home page.
Use the form to upload an image file.
Click "Submit" to extract text from the image.
Capture Image from Webcam:

Go to the home page.
Use the webcam capture feature to take a photo.
Click "Capture" to extract text from the image.
View Extracted Text:

After submitting the image, the extracted text will be displayed on the results page.
Download Extracted Text:

You can download the extracted text as a text file or PDF.
Project Structure
plaintext
Copy code
ocr_project/
├── ocr/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
├── ocrapp/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── forms.py
│   ├── models.py
│   ├── templates/
│   │   ├── ocrapp/
│   │   │   ├── upload.html
│   │   │   ├── result.html
│   ├── urls.py
│   ├── views.py
├── db.sqlite3
├── manage.py
└── requirements.txt
Files and Directories
ocr/: Django project settings and configuration.
ocrapp/: Main application directory containing views, models, forms, and templates.
templates/: HTML templates for the application.
manage.py: Django command-line utility.
Requirements
The requirements.txt file should contain the following:

plaintext
Copy code
Django>=3.0
pytesseract
Pillow
Contributions
Feel free to submit issues or pull requests. Contributions are welcome!

License
This project is licensed under the MIT License.
