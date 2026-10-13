# 🛡️ Card Loss Prediction System

### AI-Inspired Cybercrime Investigation & Card Withdrawal Forecasting Dashboard

The **Card Loss Prediction System** is a web-based cybercrime investigation platform designed to assist investigators in analyzing lost or stolen card cases, reviewing transaction histories, identifying suspicious withdrawal patterns, and forecasting potential next withdrawal locations.

The platform combines transaction analysis, risk scoring, geospatial visualization, historical activity mapping, and role-based access interfaces to demonstrate how technology can support financial fraud investigations.

> **Project Status:** Prototype / Demonstration  
> **Data:** Synthetic demo data  
> **Purpose:** Cybercrime investigation and fraud-risk analysis

## 🚀 Key Features

### 🔐 1. Role-Based Authentication
- Separate login interfaces for investigators, complainants, bank personnel, and administrators.
- Demonstration two-step verification.
- Multiple complainant authentication methods.
- Session inactivity timeout.
- Role-based access restrictions.

### 📋 2. Complaint Registration & Case Management
- Register card loss or suspected unauthorized-use complaints.
- Capture card details and the last known location.
- Record the approximate time of card loss.
- Upload supporting statement screenshots.
- Generate and display case reference information.
- Review predefined demonstration cases.

### 📍 3. Location Tracking & Geospatial Visualization
- Visualize transaction locations and historical activity.
- Display simulated ATM and point-of-sale locations.
- Add investigator-reported sightings.
- Support manual location entry and browser GPS access.
- Display location coordinates and estimated nearby addresses.
- Export hotspot information in KML format for Google Maps.

### 📊 4. Transaction Analysis
- Review card transaction histories.
- Display transaction amounts, timestamps, and locations.
- Track withdrawal activity against a demonstration ₹50,000 per-card limit.
- Simulate tap-and-pay activity.
- Review the last legitimate transaction.
- Support statement screenshot uploads.

### 🎯 5. Withdrawal Location Forecasting
- Analyze historical transaction patterns.
- Identify simulated high-activity hotspots.
- Rank potential next withdrawal locations.
- Calculate forecast scores using proximity, movement direction, and historical hotspot density.
- Display estimated probabilities and approximate travel times.
- Provide explanations for the factors contributing to predictions.

### ⚠️ 6. Risk Scoring & Alerts
- Calculate a risk score from 0 to 100.
- Consider transaction frequency, movement velocity, transaction amounts, and location information.
- Display risk indicators and explanatory factors.
- Generate simulated investigation alerts.
- Identify the nearest simulated police or cybercrime unit.

### 🏦 7. Card Management & Response Actions
- Demonstrate temporary card blocking.
- Demonstrate permanent card blocking.
- Simulate card unblocking where permitted.
- Record notification and escalation actions.
- Display card status and transaction activity.

### 🧠 8. Feedback & Model Monitoring
- Record whether the highest-ranked forecast was correct.
- Update simulated hotspot weights using investigator feedback.
- Adjust the ranking of locations following negative feedback.
- Display a feedback-based accuracy indicator.

### 🛠️ 9. Administrator Dashboard
- Review demonstration cases and officer accounts.
- Add and remove investigator accounts.
- Demonstrate officer password resets.
- View authentication and activity logs.
- Monitor feedback statistics.

## 🧰 Technology Stack

| Technology | Purpose |
|---|---|
| HTML5 | Application structure |
| CSS3 | Responsive dashboard and styling |
| JavaScript | Application logic and interactive features |
| SVG | Maps, location markers, and visualizations |
| Browser Local Storage | Remembered login-interface details |
| Browser Geolocation API | Optional user location access |
| Google Maps | External map navigation |
| KML | Geographic hotspot export |
| Firebase Authentication | Optional integration point; configuration required |

**Note:** The current implementation is primarily a single-page HTML, CSS, and JavaScript application. A production backend, persistent database, and trained machine-learning model are not established by the current prototype.

## 🏗️ System Workflow

The demonstration system follows this workflow:

1. **Complaint Received** — Select a demonstration case or submit complaint details.
2. **Case Registration** — Record the complaint and reference information.
3. **Authentication** — Verify the demonstration user's credentials and applicable second-step code.
4. **Transaction Review** — Examine available transaction records.
5. **Location Analysis** — Review the last known location and geographic activity.
6. **Historical Analysis** — Identify simulated transaction hotspots.
7. **Location Forecasting** — Rank potential future withdrawal locations.
8. **Risk Assessment** — Calculate and display the case risk score.
9. **Investigation Alert** — Present a simulated alert and nearest mapped unit.
10. **Action & Feedback** — Demonstrate response actions and record forecast feedback.

## 📂 Project Structure

The current prototype can be organized as follows:

```text
card-loss-prediction-system/
│
├── index.html       # Main application, styling, and JavaScript logic
├── README.md        # Project documentation
└── LICENSE          # Optional license file
```

Additional files may be introduced as the project evolves.

## ⚙️ Getting Started

### Prerequisites

- A modern web browser.
- Git installed on your computer, if you want to clone the repository.
- A code editor such as Visual Studio Code.

### Installation

**1. Clone the repository**

Replace `YOUR_USERNAME` with your GitHub username.

```bash
git clone https://github.com/YOUR_USERNAME/card-loss-prediction-system.git
```

**2. Open the project directory**

```bash
cd card-loss-prediction-system
```

**3. Run the application**

Open `index.html` directly in your browser.

Alternatively, use the Live Server extension in Visual Studio Code.

No Node.js installation or package installation is required for the current standalone prototype.

## 🔑 Demo Access

The prototype includes predefined demonstration accounts for different roles.

| Role | Demo Login |
|---|---|
| Investigator | `officer01` |
| Complainant | Use the predefined demonstration complaint credentials |
| Bank | `sbi.ops@bank.demo` |
| Administrator | `admin@cardloss.demo` |

The source code contains demonstration passwords and verification codes. Consult the demo-login hint inside `index.html` when running the application locally.

**Security warning:** These credentials and verification codes are publicly visible in the client-side source code. They are for demonstration only and must never be used to protect real accounts or sensitive information.

## 🧪 Demo Data & Limitations

This project currently demonstrates a potential workflow for card-loss investigation using synthetic transaction records and simulated geographic activity.

Important limitations:

- The displayed ATM locations, transaction events, and investigation-unit locations are demonstration data.
- Location forecasts are produced using a heuristic scoring algorithm, not a trained or validated machine-learning model.
- Forecast percentages are normalized scores, not verified real-world probabilities.
- The displayed risk score is a demonstration indicator, not a validated fraud-detection score.
- Accuracy statistics are based on manually submitted feedback and do not establish real-world model performance.
- Card blocking, notifications, bank integrations, and police alerts are simulated interface actions.
- Firebase authentication requires additional configuration and is not enabled by default.
- Browser-side demonstration credentials do not provide production-grade authentication.
- Persistent server-side storage and real bank transaction feeds are not implemented in the current standalone prototype.

## 🔮 Future Enhancements

Planned improvements for a production-oriented version could include:

- [ ] Secure backend using Python FastAPI or Flask.
- [ ] PostgreSQL database for persistent case and transaction records.
- [ ] Secure authentication using server-side authorization and properly implemented MFA.
- [ ] Integration with authorized bank APIs and transaction feeds.
- [ ] Real geographic mapping and verified location data.
- [ ] Machine-learning models trained and evaluated on suitable authorized datasets.
- [ ] Explainable predictions and model-performance evaluation.
- [ ] Secure evidence storage and controlled file uploads.
- [ ] Encrypted sensitive data and comprehensive audit logging.
- [ ] Authorized notification and incident-response integrations.
- [ ] Automated testing and deployment pipelines.

## 🔒 Security & Privacy

This project is intended for educational, demonstration, and defensive cybercrime investigation use.

For any real-world deployment:

- Never expose passwords, OTPs, API keys, or sensitive configuration in client-side code.
- Enforce authentication and authorization on the server.
- Protect personal, financial, and location data.
- Obtain appropriate authorization before accessing transaction records or tracking locations.
- Use synthetic data during development and demonstrations.
- Validate the security, reliability, and fairness of any forecasting model before operational use.

## 🎯 Project Objectives

- Demonstrate a technology-assisted workflow for investigating card-loss incidents.
- Visualize transaction histories and geographic activity.
- Explore heuristic risk scoring and location forecasting.
- Provide role-based interfaces for investigation and administration.
- Demonstrate how investigator feedback could influence future predictions.
- Establish a foundation for future development into a secure, data-driven fraud investigation platform.

## 👨‍💻 Author

**Ramakrishna Nalla**

Computer Science Engineering | Cybersecurity Enthusiast

GitHub: [nallaramakrishna73-hub](https://github.com/nallaramakrishna73-hub)

## 📜 License

This project can be released under the MIT License if you choose to distribute it under those terms. Add a `LICENSE` file to the repository before claiming that the project is MIT-licensed.

---

⭐ If you find this project interesting, consider starring the repository and following its development.
