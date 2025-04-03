## tool for reserve soldiers in Israel

## Description
A simple Flask-based tool for reserve soldiers in Israel to check their eligibility for compensation.

The app scans IDF Form 3010 (PDF), extracts service dates using OCR (pytesseract), and generates a personalized link to the official miluimnik.info site.

- 🧾 PDF parsing using `pdf2image` and `pytesseract`
- 🕒 Filters out dates older than October 7, 2023
- 🌐 Simple frontend in Hebrew to upload forms and select eligibility criteria

---

## Features
- Extract service date ranges from scanned PDF (Form 3010)
- Automatically validate the date range
- Submit additional details such as number of reserve days before 7.10.2023, and flags like "student", "independent", etc.
- Get a link to check your grant eligibility on **miluimnik.info**

---

## Tech Stack
- Python 3.10
- Flask
- Tesseract OCR
- pdf2image, pytesseract, pdfplumber
- Docker (optional for deployment)

---

## Installation (Local)
1. Clone the repository:
   ```bash
   git clone https://github.com/arielhalevy123/miluim-grant.git
   cd miluim-grant
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the app:
   ```bash
   python app.py
   ```

4. Open browser at: [http://127.0.0.1:5000](http://127.0.0.1:5000)

---

## Deployment (Docker)
1. Build the Docker image:
   ```bash
   docker build -t miluim-grant .
   ```

2. Run the container:
   ```bash
   docker run -d -p 5000:5000 miluim-grant
   ```

3. Visit the app using your server's IP:
   ```
   http://<your-ec2-ip>:5000
   ```

---

## Author
Created by **Ariel Halevy** ✨  
📞 052-7289992  
[LinkedIn Profile](https://www.linkedin.com/in/ariel-halevy/)  
Actively looking for a student role in development!

---

## License
MIT

