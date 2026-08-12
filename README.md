# 🎂 Birthday Wish Email Automation

An automated birthday reminder application built with Python that checks a birthday database and sends a personalized birthday email when a matching date is found.

## 📖 Overview

This project automates the process of sending birthday wishes. The program gets the current date, compares it with birthday information stored in a CSV file, and identifies whether someone has a birthday today.

If a birthday matches, the application randomly selects one of three letter templates, replaces the `[NAME]` placeholder with the person's name, and sends the personalized message using Gmail SMTP. :contentReference[oaicite:1]{index=1}

The project demonstrates practical Python concepts such as CSV data processing, dictionaries, file handling, random selection, date handling, and SMTP-based email automation.

## ✨ Features

- 🎂 Automatically checks birthdays
- 📅 Compares birthdays with the current date
- 🎲 Randomly selects a birthday message
- ✍️ Personalizes the message with the recipient's name
- 📧 Sends emails automatically using SMTP
- 📊 Uses Pandas to process birthday data
- 📄 Uses text templates for customizable messages

## 🛠️ Technologies Used

- Python 3
- Pandas
- SMTP
- Gmail SMTP
- CSV
- Datetime
- Random Module

## 📂 Project Structure

```text
Birthday-Wish/
│
├── main.py
├── birthdays.csv
│
├── letter_templates/
│   ├── letter_1.txt
│   ├── letter_2.txt
│   └── letter_3.txt
│
└── README.md
```

## 📋 Birthday Data Format

The `birthdays.csv` file should contain information such as:

```csv
name,email,year,month,day
Alex,alex@example.com,2000,8,13
```

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/Tejass-raj/Birthday-Wish.git
```

### 2. Navigate to the project

```bash
cd Birthday-Email-Automation
```

### 3. Install Pandas

```bash
pip install pandas
```

### 4. Configure your email securely

Do **not** hard-code your Gmail password or app password in the source code.

Use environment variables instead:

```python
import os

MY_EMAIL = os.getenv("MY_EMAIL")
PASSWORD = os.getenv("EMAIL_PASSWORD")
```

### 5. Run the program

```bash
python main.py
```

## ⚙️ How It Works

1. The program gets today's date.
2. The birthday CSV file is loaded using Pandas.
3. Birthday records are converted into a dictionary using month and day as keys.
4. Today's date is checked against the birthday records.
5. If a birthday is found, one of the three templates is randomly selected.
6. `[NAME]` is replaced with the birthday person's name.
7. The personalized message is sent through SMTP.

The project currently contains three different birthday message templates. :contentReference[oaicite:2]{index=2} :contentReference[oaicite:3]{index=3} :contentReference[oaicite:4]{index=4}

## 📚 Concepts Demonstrated

- File Handling
- CSV Data Processing
- Pandas DataFrames
- Dictionaries
- Date and Time Handling
- Random Selection
- String Replacement
- SMTP Email Automation
- Exception-Free Workflow Design

## 🔐 Security

Never upload email passwords, Gmail app passwords, API keys, or other credentials to GitHub.

Add sensitive files to `.gitignore`:

```gitignore
.env
*.json
data.txt
__pycache__/
*.pyc
```

If a real Gmail app password has already been uploaded to a repository or shared publicly, **revoke it and generate a new one**.

## 🔮 Future Improvements

- Send the email directly to the birthday person's email address
- Add multiple birthday databases
- Add email scheduling
- Support HTML email templates
- Add logging
- Add a GUI
- Use environment variables for secure credentials
- Add support for multiple email providers

## 👨‍💻 Author

**Tejas Raj**

If you found this project useful, consider giving it a ⭐ on GitHub!
