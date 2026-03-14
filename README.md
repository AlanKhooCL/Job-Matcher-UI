# 🚀 Job Matcher AI

An AI-powered career portal designed to analyze, evaluate, and enhance resumes against real-world job descriptions. Built with a sleek, dark-mode Japandi aesthetic, this full-stack application utilizes Google's latest Gemini 3 model to give job seekers a data-driven edge.

## ✨ Features

* **Targeted Job Evaluation:** Upload your PDF resume and input up to three job URLs. The app scrapes the job descriptions and uses AI to generate a "Fit Score" and custom verdict.
* **Anti-Bot Bypass:** Features a dynamic toggle to paste raw job descriptions manually, bypassing heavy enterprise security (like Workday or LinkedIn) that block standard web scrapers.
* **Resume DNA Dashboard:** Extracts technical and soft skills from your resume to automatically generate an interactive, data-rich radar chart using Chart.js.
* **AI Resume Enhancer:** Acts as an executive recruiter, rewriting your past experience with strong action verbs and quantifiable metrics. Outputs directly to the UI with a one-click "Copy to Clipboard" function.
* **Automated Tracking:** Seamlessly logs every job evaluation directly into a connected Google Sheet for effortless application tracking.

## 🛠️ Tech Stack

* **Frontend:** HTML5, CSS3 (Dark Japandi theme), Vanilla JavaScript, Chart.js
* **Backend:** Node.js, Express.js, Multer (PDF handling), Puppeteer/Cheerio (Web scraping)
* **AI Engine:** Google Generative AI (`gemini-3.1-flash-lite-preview`)
* **Database:** Google Sheets API v4
* **Hosting:** Render (Backend API) & GitHub Pages (Frontend UI)

## ⚙️ Local Setup & Installation

### Prerequisites
* Node.js (v18 or higher)
* A Google Gemini API Key
* A Google Cloud Project with the Google Sheets API enabled (and a Service Account JSON key)

### 1. Clone the repository
\`\`\`bash
git clone https://github.com/YOUR_USERNAME/Job-Matcher-API.git
cd Job-Matcher-API
\`\`\`

### 2. Install dependencies
\`\`\`bash
npm install
\`\`\`

### 3. Environment Variables
Create a `.env` file in the root directory and add the following:
\`\`\`env
PORT=3000
GEMINI_API_KEY=your_gemini_api_key_here
\`\`\`

### 4. Google Sheets Configuration
1. Place your Service Account key file in the root directory and name it `credentials.json`.
2. Open your target Google Sheet and share it (as an Editor) with the `client_email` found inside your `credentials.json` file.
3. Update the `spreadsheetId` in `server.js` with your specific Google Sheet ID.

### 5. Start the Server
\`\`\`bash
npm start
\`\`\`
The backend will run on `http://localhost:3000`. 

*(Note: If testing the frontend locally, ensure the `fetch` URLs in `app.js` point to your localhost instead of your live Render URL).*

## 🎨 UI/UX Design
The interface is designed with a "Zen Sci-Fi" philosophy—merging the clinical, futuristic elegance of *Westworld* with a warm, minimalist Japandi color palette. It features glassmorphism panels, pill-shaped interactive buttons, and responsive layout adjustments.

## 📝 License
This project is open-source and available under the MIT License.
