# 🛡️ CareerShield AI
**Real-Time Multimodal Recruitment Fraud Detection Platform**

CareerShield AI is a stateless, zero-trust cybersecurity platform engineered to protect job seekers from sophisticated employment scams. By leveraging an ensemble of edge-deployed AI models and strict client-side data sanitization, the platform evaluates threat vectors across communication, financial, urgency, and compensation dimensions before candidates ever apply.

---

## 👥 Team & Contributions
This project was developed collaboratively with strict separation of concerns between frontend UI and backend architecture to ensure a clean, maintainable codebase.

*   **Vedant Singh (Team Lead, Backend & Architecture)**
    *   Engineered the 100% stateless Next.js Serverless API architecture on Vercel Edge.
    *   Integrated the Google Gemini 2.5 Flash API with strict JSON schema enforcement.
    *   Developed the client-side Regex PII Sanitization pipeline.
    *   Designed the FBI-Aligned Fraud Typology Rubric and system prompt logic.
    *   Managed repository architecture, Git synchronization, and build configurations.

*   **Amay (Frontend & UI/UX)**
    *   Built the responsive Next.js 15 and React 19 user interface.
    *   Designed and implemented the animated 4-Vector Trust Score Gauge and data visualizations using Tailwind CSS.
    *   Developed the multimodal Input Panel (drag-and-drop file uploads, text parsing).
    *   Engineered the dynamic Results Panel and state management for real-time scanning feedback.
    *   Maintained static assets, CSS architecture, and UI component hierarchy.

---

## ⚡ Core Architecture & Zero-Trust Privacy
Our platform's defining feature is its absolute adherence to data privacy. We analyze the job offer, not the candidate.

*   **100% Stateless Execution:** Deployed on Vercel Edge. Zero database. Zero persistence. Every request is ephemeral, eliminating the attack surface entirely.
*   **Client-Side PII Redaction:** A custom Regex pipeline automatically strips emails, phone numbers, and sensitive identifiers from documents *in the browser* before the HTTP request is formed.
*   **Prompt Injection Protection:** Strict JSON schema formatting prevents malicious job descriptions from overriding the forensic evaluation model.

## 🎯 Key Features
*   **Multimodal Intake:** Safely analyzes raw pasted text, PDF offer letters, and screenshots of recruiter chats across platforms like Telegram and LinkedIn.
*   **FBI-Aligned Fraud Rubric:** Hardcoded auto-fail thresholds bypass standard LLM gullibility to instantly flag check fraud, upfront fees, and identity theft patterns.
*   **4-Vector Explainable AI:** Breaks down risk into four transparent sub-scores: Communication Security, Financial Risk, Urgency/Pressure, and Compensation Match.
*   **Forensic PDF Export:** Generates an actionable, downloadable verification report that candidates can share.

## 🛠️ Technical Stack
*   **Framework:** Next.js 15 (App Router)
*   **UI/Styling:** React 19, Tailwind CSS, Lucide Icons
*   **Backend:** Next.js Serverless API Routes (Edge Deployment)
*   **AI Engine:** Google Gemini 2.5 Flash API

## 🚀 Local Setup Instructions

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/workspacevedant/CareerShield-AI.git](https://github.com/workspacevedant/CareerShield-AI.git)
   cd CareerShield-AI
   Install dependencies: npm install
   Environment Variables:
   Create a .env file in the root directory (do not commit this file) and add your API key:
   Code snippet
   GEMINI_API_KEY=your_google_gemini_api_key_here
   Run the development server: npm run dev

   The application will securely launch on http://localhost:4028.
