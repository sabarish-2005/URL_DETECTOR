# AI URL Malicious Detection Web App

A complete AI-based web application that detects malicious URLs using machine learning-style heuristics and pattern recognition.

## 🚀 Features

- **AI-Powered Detection**: Uses intelligent algorithms to analyze URL patterns
- **Real-time Analysis**: Instant results with confidence scores
- **User-Friendly Interface**: Clean, modern, responsive design
- **Privacy-First**: All analysis happens locally on your machine
- **No External APIs**: Works completely offline

## 📋 Requirements

- Python 3.7+
- Flask
- Flask-CORS

## 🛠️ Installation

1. **Navigate to project directory:**
   ```bash
   cd AI_URL_DETECTOR
   ```

2. **Install required packages:**
   ```bash
   pip install -r requirements.txt
   ```

## ▶️ Running the Application

1. **Start the Flask backend:**
   ```bash
   python app.py
   ```

2. **Open your browser and go to:**
   ```
   http://127.0.0.1:5000
   ```

3. **Enter a URL and click "Check URL"**

## 📁 Project Structure

```
AI_URL_DETECTOR/
│
├── app.py              # Flask backend server
├── detector.py         # AI detection logic
├── requirements.txt    # Python dependencies
├── index.html          # Frontend HTML
├── style.css           # Frontend styling
├── script.js           # Frontend JavaScript
└── README.md           # Project documentation
```

## 🧠 How It Works

The AI detector analyzes URLs using multiple factors:

1. **URL Length**: Excessively long URLs are suspicious
2. **Domain Analysis**: Checks for IP addresses, suspicious TLDs
3. **Pattern Recognition**: Detects phishing patterns (@ symbols, multiple hyphens)
4. **Keyword Detection**: Identifies suspicious keywords (login, verify, urgent, etc.)
5. **Security**: Checks for HTTPS usage
6. **Risk Scoring**: Calculates overall risk score (0-100)

## 🧪 Test Examples

### Safe URLs:
- `https://www.google.com`
- `https://github.com`
- `https://stackoverflow.com`

### Suspicious URLs:
- `http://192.168.1.1/login`
- `http://paypal-verify-account-login.tk`
- `http://secure-banking-update@malicious.com`
- `http://free-prize-winner-claim-urgent.com`

## 🎨 API Documentation

### POST `/check`
Check if a URL is malicious

**Request:**
```json
{
  "url": "https://example.com"
}
```

**Response:**
```json
{
  "success": true,
  "url": "https://example.com",
  "result": {
    "status": "Safe",
    "confidence": 95,
    "risk_score": 5,
    "reason": "URL appears to be safe based on AI analysis"
  }
}
```

## 🔧 Customization

You can customize the detection logic in `detector.py`:

- Modify `suspicious_keywords` list
- Add new `suspicious_tlds`
- Adjust risk scoring weights in `calculate_risk_score()`
- Add new detection patterns

## 📝 Notes

- The detector uses heuristic-based AI analysis (not machine learning models)
- Detection is based on common phishing and malicious URL patterns
- Results are probabilistic and should be used as guidance, not absolute truth
- No user data is collected or transmitted

## 🤝 Contributing

Feel free to enhance the detection algorithm or improve the UI!

## 📄 License

This project is open source and available for educational purposes.

## 👨‍💻 Author

Built with ❤️ using Flask, HTML, CSS, and JavaScript

---

**Enjoy safe browsing! 🛡️**
