# 🌍 Oval Tours — Travel Experience Platform

Oval Tours is a responsive, modular travel website designed to showcase global destinations and handle user inquiries through a secure contact form. Built with HTML, CSS, JavaScript, and Flask, it integrates cloud-based MySQL storage via Railway for scalable backend operations.

---

## 🚀 Features

- 🖼️ Hero section with image carousel
 <img width="1347" height="640" alt="image" src="https://github.com/user-attachments/assets/73433407-c073-4ba0-8b86-8e4f5b4245e6" />

- 📍 Destination highlights (e.g. Tokyo, Paris, Safari)
 <img width="1291" height="472" alt="image" src="https://github.com/user-attachments/assets/12c20a59-e74e-47a5-b9d7-c4c45969874e" />

- 📬 Contact form 
 <img width="872" height="586" alt="image" src="https://github.com/user-attachments/assets/e66ccd4d-8c03-48c4-9e7f-227d9a902ab3" />

- 📱 Responsive layout with mobile navigation toggle
 <img width="505" height="544" alt="image" src="https://github.com/user-attachments/assets/c1918f14-5384-4f10-a486-8d99e41431e5" />

---

## 🧱 Tech Stack

| Layer       | Tools Used                          |
|-------------|-------------------------------------|
| Frontend    | HTML, CSS, JavaScript               |
| UI Styling  | Custom styles                       |
| Backend     | Flask (Python)                      |
| Database    | MySQL (hosted on Railway)           |
| Deployment  | Railway (backend), GitHub Pages or local (frontend) |

---

## 📁 Project Structure

```
oval-tours/
├── assets/              # Images and branding
│   ├── beach.png
│   ├── mountain.png
│   ├── safari.png
│   └── ...
├── scripts/             # JavaScript and styles
│   └── scripts.js
├── back-end/            # Flask backend
│   ├── app.py
│   ├── db.py
│   └── config.py
├── index.html
├── contact.html
├── about.html
├── README.md
```

---

## ⚙️ Setup Instructions

### 1. Clone the repo

```bash
git clone https://github.com/your-username/oval-tours.git
cd oval-tours
```

### 2. Install backend dependencies

```bash
pip install flask mysql-connector-python
```

### 3. Configure your backend

Edit `config.py` with Railway credentials:

```python
DB_HOST = 'your-railway-host'
DB_PORT = 3306
DB_USER = 'your-db-user'
DB_PASS = 'your-db-password'
DB_NAME = 'your-db-name'

# Optional SMTP settings
SMTP_SERVER = 'smtp.gmail.com'
SMTP_PORT = 465
SMTP_USER = 'your-email@gmail.com'
SMTP_PASS = 'your-app-password'
RECEIVER_EMAIL = 'your-email@gmail.com'
```

### 4. Run the Flask server

```bash
python app.py
```

---

## 📬 Contact Form API

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

- Open `contact.html` in your browser
- Fill out the form and submit
- Check Railway MySQL dashboard → Query: `SELECT * FROM messages;`
- (Optional) Check your email inbox if SMTP is enabled

---

## 🧠 Future Enhancements

- Admin dashboard to view messages
- Tour booking system with calendar
- CAPTCHA or honeypot spam protection
- Email reply automation
- Multi-language support
- AI-powered itinerary suggestions

---

## 👨‍💻 Author

**Raphael Kamunyu**  
Web Developer & Platform Architect  
📍 Thika, Kenya  
📧 rahvickam@gmail.com

---

## 📄 License

MIT — free to use, modify, and distribute.
```
