# Risk Scoring & Threat Intelligence Dashboard

## Overview
This project implements a **real-time risk scoring model** that monitors and prevents suspicious activities using machine learning. The system features real-time fraud detection, authentication, logging, and alerting via a dashboard.

## Features
- **Machine Learning Model:** Uses a **Random Forest Classifier** to detect suspicious activities.
- **Real-Time Risk Scoring API:** Flask-based API endpoint for scoring transactions.
- **Authentication:** Secured API with token-based authentication.
- **Logging & Monitoring:** Tracks risk scores and generates **real-time alerts**.
- **Interactive Dashboard:** Built with **Dash** to visualize risk scores, failed transactions, and login attempts.
- **Real-Time Alerts:** Detects suspicious activities and updates the dashboard automatically.

## Technologies Used
- **Python** (Flask, Dash, NumPy, Pandas, Scikit-learn, Joblib)
- **Machine Learning** (Random Forest Classifier)
- **Dash & Plotly** (For real-time visualization)
- **Logging & Authentication** (Flask authentication & Python logging)

## Installation & Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/risk-scoring-dashboard.git
   cd risk-scoring-dashboard
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Flask app:
   ```bash
   python risk_scoring_dashboard.py
   ```
4. Access the dashboard:
   - API Endpoint: `http://127.0.0.1:5000/risk_score`
   - Dashboard: `http://127.0.0.1:5000/dashboard/`

## API Usage
- **Endpoint:** `/risk_score`
- **Method:** `POST`
- **Headers:**
  - `Authorization: Bearer secure_token`
  - `Content-Type: application/json`
- **Payload Example:**
  ```json
  {
    "transaction_amount": 5000,
    "login_attempts": 5,
    "failed_transactions": 3,
    "account_age": 180
  }
  ```
- **Response Example:**
  ```json
  {
    "risk_score": 85.5,
    "suspicious_activity": 1
  }
  ```

## Dashboard Features
- **Risk Score Visualization:** Displays transaction amounts vs. risk scores.
- **Failed Transactions & Login Attempts:** Bar charts to track suspicious behavior.
- **Real-Time Alerts:** Displays latest security alerts dynamically.

## Future Improvements
- Enhance risk scoring using **deep learning**.
- Deploy on **cloud services** (AWS, GCP, Azure) for scalability.
- Integrate **Kafka for real-time data streaming**.

## Contributing
Contributions are welcome! Feel free to open issues or submit pull requests.



