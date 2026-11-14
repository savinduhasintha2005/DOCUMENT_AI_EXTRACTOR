# 🧾 Document AI Extractor

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Google-Gemini-8E75B2?logo=googlegemini&logoColor=white" />
  <img src="https://img.shields.io/badge/Pydantic-Data%20Validation-E92063?logo=pydantic&logoColor=white" />
  <img src="https://img.shields.io/badge/Status-Active-success" />
</p>

<p align="center">
  <b>Transform unstructured invoice text into structured, validated JSON using Google Gemini AI.</b>
</p>

---

## 📌 Overview

**Document AI Extractor** is a Python-based AI application that extracts structured invoice information from unstructured text using Google's Gemini API.

It combines the power of **Google Gemini, LangChain PromptTemplate, and Pydantic** to identify invoice details, generate structured data, and validate the extracted information before exporting it as a JSON file.

## ✨ Features

- 🤖 **AI-Powered Extraction** – Extract invoice information using Google Gemini.
- 📄 **Text Processing** – Process unstructured invoice text.
- 🧩 **Structured Output** – Convert extracted information into organized JSON.
- ✅ **Data Validation** – Validate extracted data using Pydantic.
- 📅 **Date Validation** – Check invoice date formats.
- 🔢 **Quantity Validation** – Ensure item quantities are positive.
- 💰 **Amount Validation** – Prevent negative monetary values.
- 🧮 **Total Verification** – Check invoice total consistency.
- 📦 **JSON Export** – Save validated results to `output.json`.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| 🐍 Python | Core application development |
| ✨ Google Gemini API | AI-powered information extraction |
| 🔗 Google Gen AI SDK | Gemini API integration |
| 🦜 LangChain PromptTemplate | Structured prompt management |
| 🛡️ Pydantic | Data modeling and validation |
| 📋 JSON | Structured data output |
| 🔐 Python dotenv | Environment variable management |

## 📂 Project Structure

```text
Document-AI-Extractor/
│
├── 📄 main.py
├── 📄 requirements.txt
├── 📄 .env
├── 📄 .gitignore
├── 📄 sample_invoice.txt
├── 📄 output.json
└── 📄 README.md
```

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/Document-AI-Extractor.git
```

```bash
cd Document-AI-Extractor
```

### 2️⃣ Create a Virtual Environment

```bash
python -m venv .venv
```

### 3️⃣ Activate the Virtual Environment

**Windows:**

```bash
.venv\Scripts\activate
```

**Linux / macOS:**

```bash
source .venv/bin/activate
```

### 4️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 5️⃣ Configure Environment Variables

Create a `.env` file in the project root directory:

```env
GEMINI_API_KEY=your_gemini_api_key_here
```

Get your API key from [Google AI Studio](https://aistudio.google.com/apikey).

### 6️⃣ Add Invoice Text

Add your unstructured invoice content to:

```text
sample_invoice.txt
```

### 7️⃣ Run the Application

```bash
python main.py
```

## 📤 Output

After successful extraction and validation, the application generates:

```text
output.json
```

The output contains structured invoice information in JSON format.

Example output structure:

```json
{
  "invoice_number": "INV-2026-001",
  "invoice_date": "2026-11-14",
  "items": [
    {
      "description": "Laptop",
      "quantity": 2,
      "unit_price": 1500.00,
      "amount": 3000.00
    }
  ],
  "total": 3000.00
}
```

*Note: This is an illustrative output structure. Actual fields depend on your Pydantic schema.*

## 🛡️ Data Validation

The application uses Pydantic to validate extracted invoice information.

| Validation | Description |
|---|---|
| 📅 Invoice Date | Ensures the invoice date follows the expected format |
| 🔢 Item Quantity | Quantity must be greater than zero |
| 💵 Monetary Amounts | Amounts must be non-negative |
| 🧮 Invoice Total | Verifies consistency between item amounts and invoice total |

## 🔐 Security

- Never commit your `.env` file or API keys.
- Add `.env` and `.venv/` to `.gitignore`.
- Avoid uploading confidential or sensitive invoice documents.
- Keep your Google Gemini API key private.

## 🚀 Future Improvements

- 📑 Support PDF and image-based invoice extraction.
- 🌐 Build a REST API using FastAPI.
- 🗄️ Store extracted invoices in a database.
- 📊 Create an invoice management dashboard.
- 🔍 Support multiple invoice formats and currencies.

## 👨‍💻 Author

**Savindu Hasintha**

🐍 Python Developer | 🤖 AI & Software Engineering Enthusiast

- GitHub: [@savinduhasintha2005](https://github.com/savinduhasintha2005)

---

<p align="center">
  ⭐ If you find this project useful, consider giving it a star!
  <br/>
  <b>Built with Python, Google Gemini AI, and ❤️</b>
</p>