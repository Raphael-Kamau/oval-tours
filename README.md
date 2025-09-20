# 🌍 Oval Tours — Contact Form Backend

Oval Tours is a modular Flask-based backend for handling contact form submissions securely and scalably. Messages are stored in a Railway-hosted MySQL database, with optional email notifications via SMTP.

---

## 🚀 Features

- ✅ Contact form API (`/api/contact`)
- ✅ Cloud-based MySQL storage (Railway)
- ✅ Automatic table creation
- ✅ Frontend integration via `fetch()`
- ✅ Optional SMTP email notifications
- ✅ Modular config and onboarding-friendly structure

---

## 🧱 Tech Stack

- **Backend**: Flask (Python)
- **Database**: MySQL (hosted on Railway)
- **Frontend**: HTML/CSS/JS (form + hero section)
- **Email**: SMTP (Gmail-compatible, optional)

---

## 📁 Folder Structure

```
oval-tours/
├── app.py           # Flask app entry point
├── db.py            # MySQL logic and table creation
├── config.py        # DB and SMTP credentials
├── static/          # Frontend assets (images, CSS, JS)
└── templates/       # HTML pages (optional)
```

---

## ⚙️ Setup Instructions

### 1. Clone the repo

```bash
git clone https://github.com/Raphael-Kamau/oval-tours.git
cd oval-tours
```

### 2. Install dependencies

```bash
pip install flask mysql-connector-python
```

### 3. Configure your credentials

Edit `config.py`:

```python
DB_HOST = 'your-railway-host'
DB_PORT = 3306
DB_USER = 'your-db-user'
DB_PASS = 'your-db-password'
DB_NAME = 'your-db-name'

SMTP_SERVER = 'smtp.gmail.com'
SMTP_PORT = 465
SMTP_USER = 'your-email@gmail.com'
SMTP_PASS = 'your-app-password'
RECEIVER_EMAIL = 'your-email@gmail.com'
```

> You can skip SMTP if you're only using database storage.

### 4. Run the server

```bash
python app.py
```

---

## 📬 API Endpoint

### `POST /api/contact`

**Payload:**

```json
{
  "name": "Jane Doe",
  "email": "jane@example.com",
  "message": "I'd love to book a safari tour!"
}
```

**Response:**

```json
{ "success": true }
```

---

## 🧪 Testing

- Submit the form from your frontend
- Check Railway’s MySQL dashboard → Query: `SELECT * FROM messages;`
- (Optional) Check your email inbox if SMTP is enabled

---

## Deployment 
- GitHub pages


## 🧠 Future Enhancements

- Admin dashboard to view messages
- CAPTCHA or honeypot spam protection
- Email reply automation
- Tour booking integration

---

## 👨‍💻 Author

**Raphael Kamunyu**  
Web Developer & Platform Architect  
📍 Thika, Kenya  
📧 rahvickam@gmail.com

---

## 📄 License

MIT — free to use, modify, and distribute.
