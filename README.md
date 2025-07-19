# HelpPro: Your All-in-One File & Image Utility

HelpPro is a versatile web application built with Flask, designed to streamline various file and image manipulation tasks. From advanced image editing to comprehensive document conversions, HelpPro provides a user-friendly interface for common digital operations.

## Features

### 1. Image Editor
Transform your images with a powerful set of editing tools:
-   **Brightness & Contrast Adjustment:** Fine-tune the visual appearance of your photos.
-   **Sharpening:** Enhance details and clarity.
-   **Rotation & Zoom:** Adjust orientation and scale.
-   **Watermarking:** Add custom text watermarks with control over position, size, color, rotation, and opacity.
-   **Background Removal:** Effortlessly remove backgrounds from images using AI.

### 2. File Converter
Convert documents and images between various popular formats:
-   **PDF to Text:** Extract text content from PDF files, with optional OCR for scanned documents.
-   **Text to PDF:** Convert plain text files into PDF documents, supporting Arabic text.
-   **PDF to DOCX:** Convert PDF files to editable Word documents, with optional OCR.
-   **DOCX to Text:** Extract text content from Word documents.
-   **XLSX to PDF:** Convert Excel spreadsheets to PDF, supporting Arabic text.
-   **Image to Text:** Extract text from images using OCR (supports Arabic and English).

### 3. Canvas
A dynamic canvas feature for creative tasks or interactive drawing. (Further details on specific functionalities can be added here if applicable).

### 4. PDF & Image Tools
Dedicated tools for handling PDF and image conversions:
-   **PDF to Image:** Convert PDF pages into image files.
-   **Image to PDF:** Combine multiple images into a single PDF document.

## Setup and Installation

To get HelpPro up and running on your local machine, follow these steps:

### Prerequisites
-   Python 3.x
-   pip (Python package installer)
-   Tesseract OCR (for image-to-text and OCR functionalities)

### 1. Clone the Repository
```bash
git clone git@github.com:kama1983kama1983/HelpPro.git
cd HelpPro
```

### 2. Create a Virtual Environment (Recommended)
```bash
python -m venv myvenv
# On Windows
myvenv\Scripts\activate
# On macOS/Linux
source myvenv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt # You might need to create this file first
```
*(Note: If `requirements.txt` is not present, you will need to manually install the dependencies listed in `app.py` such as `Flask`, `Pillow`, `pytesseract`, `rembg`, `pdfplumber`, `fpdf`, `pdf2docx`, `python-docx`, `openpyxl`, `arabic-reshaper`, `python-bidi`, `Flask-WTF`, `SQLAlchemy`.)*

### 4. Configure Tesseract OCR
Ensure Tesseract OCR is installed on your system and its executable is in your system's PATH, or specify its path in your `app.py` if needed (e.g., `pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'`).

### 5. Run the Application
```bash
python app.py
```

The application will typically run on `http://127.0.0.1:5000/`.

## Usage

-   **Image Editor:** Navigate to `/img_editor` to upload and process images.
-   **File Converter:** The main page (`/`) handles various file conversions. Upload your file and select the desired conversion type.
-   **Canvas:** Access the canvas at `/canvas`.
-   **PDF/Image Tools:** Find these tools at `/pdfimg`.

## Project Structure
```
HelpPro/
├── app.py                # Main Flask application logic
├── models.py             # Database models (if any, for example, for CVs)
├── static/               # Static files (CSS, JS, images)
│   ├── css/
│   │   └── style.css
│   ├── outputs/          # Converted files output directory
│   └── uploads/          # Uploaded files directory
├── templates/            # HTML templates
│   ├── base.html
│   ├── index.html
│   ├── image-editor.html
│   ├── pdf-to-img-img-to-pdf.html
│   ├── canvas.html
│   └── error.html
├── instance/             # Instance folder (e.g., for SQLite database)
│   └── cv_database.db
├── myvenv/               # Python virtual environment
├── outputs/              # Another output directory (can be consolidated)
├── install.txt           # Installation notes (can be moved to README)
├── project_structure.txt # Project structure notes (can be moved to README)
└── README.md             # This file
```

## Contributing

Contributions are welcome! Please feel free to fork the repository, create a new branch, and submit a pull request.

## License

This project is open-source and available under the [MIT License](LICENSE). (You might need to create a LICENSE file).

```
