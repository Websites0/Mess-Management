# 🏠 Mess Manager

> **A smart, simple, and collaborative web application to track meals, expenses, and finances for your student mess or shared living.**

<p align="center">
  <img src="https://img.shields.io/badge/version-1.0.0-blue.svg" alt="Version">
  <img src="https://img.shields.io/badge/license-MIT-green.svg" alt="License">
  <img src="https://img.shields.io/badge/frontend-HTML%2FCSS%2FJS-yellow.svg" alt="Frontend">
  <img src="https://img.shields.io/badge/backend-Google%20Apps%20Script-red.svg" alt="Backend">
</p>

---

## 📖 About The Project

**Mess Manager** is designed to eliminate the hassle of managing shared expenses in a student mess or shared apartment. It provides a centralized dashboard for members and managers to track daily meals, log grocery (bazaar) expenses, manage deposits, and automatically calculate individual balances at the end of the month.

Say goodbye to messy paper ledgers and confusing WhatsApp groups. Mess Manager handles the math for you!

## ✨ Key Features

- **🍽️ Meal Tracking:** Easily log daily meals (breakfast, lunch, dinner) with customizable increments (0.5, 1, etc.).
- **🛒 Bazaar (Expense) Log:** Record grocery runs, categorized expenses, and track total mess spending.
- **💰 Financial Management:** Track member deposits and automatically calculate "Balance in Hand", "Meal Rate", and individual "Cost".
- **👥 Role-Based Access:**
  - **Manager:** Can add/edit/delete deposits, edit bazaar entries, lock/unlock meals, and archive months.
  - **Member:** Can view summaries, add bazaar items, adjust their own meals, and manage a private ledger.
- **🗳️ Democratic Elections:** Built-in voting system for members to elect a new Mess Manager.
- **🧹 Cleaning Log & Leaderboard:** Keep track of who cleaned the mess and motivate members with a leaderboard.
- **📚 Monthly Archiving:** Finish the month to archive data securely and start fresh. View historical data anytime.
- **🌓 Dark/Light Mode:** Beautiful, responsive UI with theme toggling.
- **🇧🇩 Localization:** Help section available in both Bengali and English.

## 💻 Tech Stack

- **Frontend:** HTML5, CSS3 (Custom variables, animations, glassmorphism), Vanilla JavaScript
- **Backend/Database:** Google Apps Script (GAS) acting as a REST API, Google Sheets as the database.
- **Icons/Fonts:** Inter Font Family, Native Emojis.

## 📂 Architecture & Folder Structure

This project follows a lightweight, serverless Architecture. The frontend is a Single Page Application (SPA) contained entirely within `index.html`. It communicates asynchronously with a Google Apps Script Web App.

```text
Mess-Management/
├── index.html       # The main Single Page Application (UI + Logic)
├── README.md        # Project documentation
└── .git/            # Version control
```

## 🛠️ Prerequisites

To run this project locally, you only need:
- A modern web browser (Chrome, Firefox, Safari, Edge).
- A local web server (optional but recommended for preventing CORS issues when developing locally). Examples:
  - Node.js (`npx serve`)
  - Python (`python -m http.server`)
  - VS Code Live Server extension.
- A Google Account (if you are setting up your own Google Apps Script backend).

## 🚀 Installation & Local Setup

Follow these steps to get a local copy up and running.

**1. Clone the repository**
```bash
git clone https://github.com/Websites0/Mess-Management.git
cd Mess-Management
```

**2. Run the application locally**
Since this is a vanilla HTML/JS app, you can simply serve the directory.
```bash
# If using Python 3
python -m http.server 8000

# Or if using Node.js/npx
npx serve .
```
Navigate to `http://localhost:8000` in your browser.

**3. Configure the Backend (Google Apps Script)**
Currently, the app points to a specific Google Apps Script URL. To use your own database:
1. Create a new Google Sheet.
2. Go to **Extensions > Apps Script**.
3. *[Add your GAS backend code here - currently not in this repo]*
4. Deploy the script as a **Web App** (Accessible to "Anyone").
5. Copy the deployed Web App URL.

## 🔑 Environment Variables / Configuration

Since this is a static frontend app, configuration is handled directly in the JavaScript code inside `index.html`.

Locate the following line near the top of the `<script>` tag in `index.html`:

| Variable | Description |
| --- | --- |
| `API_URL` | The endpoint URL of your deployed Google Apps Script web app. |

**Example:**
```javascript
const API_URL = 'https://script.google.com/macros/s/[YOUR_GAS_DEPLOYMENT_ID]/exec';
```

## 📱 Usage

1. **Register/Login:** Open the app and create a new account.
2. **Dashboard:** View the current summary, meal rates, and your balance.
3. **Meals:** Go to the meals tab to adjust your meal count for the day. (Note: The manager must unlock meals first).
4. **Bazaar:** Add grocery expenses, amount, and who went to the bazaar.
5. **More (Settings):** If you are the manager, you can update the mess name, manage members, start/stop meals, and finalize the month.

## 📸 Screenshots / Demo

*(Add your screenshots or GIFs here to showcase the app)*

| Dashboard | Meals |
| :---: | :---: |
| `![Dashboard Demo](placeholder-link-to-dashboard-image.jpg)` | `![Meals Demo](placeholder-link-to-meals-image.jpg)` |

| Bazaar | Mobile Responsive |
| :---: | :---: |
| `![Bazaar Demo](placeholder-link-to-bazaar-image.jpg)` | `![Mobile Demo](placeholder-link-to-mobile-image.jpg)` |


## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information. *(If a license file is added in the future)*

## 📬 Contact / Maintainer

**Websites0**
- GitHub: [@Websites0](https://github.com/Websites0)
- Project Link: [https://github.com/Websites0/Mess-Management](https://github.com/Websites0/Mess-Management)

---
*Made with ❤️ for student messes everywhere.*