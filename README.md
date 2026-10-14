# PhishGuard — AI-Powered Scam Call & Audio Protection

> **Cybersecurity defense system designed to protect users against voice-phishing (vishing), OTP theft, banking impersonation, and conversational social-engineering attacks in real-time.**

---

## 1. Project Overview

**PhishGuard** analyzes spoken phone conversations and transcripts to detect fraudulent manipulation tactics before sensitive data is surrendered. It features an explainable AI scam detection engine, live Web Audio API waveform visualization, continuous speech transcription, high-priority animated alerts, and interactive offline-ready demo scenarios.

### Core Attack Vectors Monitored:
1. **Credential Theft:** Requests for one-time passwords (OTPs), PINs, banking passwords, CVVs, or login codes.
2. **Urgency Manipulation:** Artificial deadlines ("5 minutes", "immediately"), imminent account blocking/suspension threats, or arrest warrants.
3. **Impersonation:** Fraud department officials, police/CBI/FBI agents, courier services (DHL/FedEx held parcel), or tech support.
4. **Payment Fraud:** Demands for unexpected release fees, external payment links, gift cards, or wire transfers.
5. **Social Engineering:** Remote desktop installation (AnyDesk, TeamViewer), forced secrecy ("don't tell anyone"), and intimidation.

---

## 2. Technology Stack

- **Frontend Framework:** React 19 + TypeScript + Vite.
- **Styling:** Tailwind CSS with dark navy surfaces (`#080D1A`), cyber cyan accents (`#00F0FF`), and accessible risk indicators.
- **Iconography:** Lucide React.
- **Data Visualizations:** Recharts (Vector bar distribution) + Custom SVG circular radial risk gauges.
- **Audio Processing:** Browser MediaRecorder & Web Audio API (real-time `AnalyserNode` oscilloscope waveform & frequency spectrum).
- **Speech Transcription:** Web Speech API (`webkitSpeechRecognition` / `SpeechRecognition`) with manual text editing fallback.
- **AI Engine:** Explainable rule-based pattern matching with compound synergy scoring (0–100) and false-positive reduction.
- **Optional Backend:** Python FastAPI for local speech recognition (Whisper) or LLM model integration.
- **Storage:** HTML5 LocalStorage for scan audit logs, sensitivity settings, and offline demo history.

---

## 3. Key Pages & Features

### A. Security Dashboard
- Overall protection status with real-time defense indicators.
- Prominent **“Start Audio Scan”** call to action.
- Live audio monitoring panel and current conversational risk level.
- 4 primary metric cards (System Protection, Total Scans, High-Risk Threats Flagged, AI Sensitivity).
- Interactive 5-vector threat distribution graph.
- Recent scan audit history feed with one-click drill-down modals.
- Quick cybersecurity safety rules.

### B. Live Audio Scanner
- Explicit user-initiated microphone capture with permission management.
- Live HTML5 Canvas visualizer rendering real-time oscilloscope waveforms and frequency spectrum bars.
- Live streaming speech transcription with highlighted tokens and interim text.
- Manual edit/type mode allowing users to paste or adjust call transcripts.
- Dynamic 0–100 risk gauge meter with color states:
  - `0–29`: Low Risk (Emerald)
  - `30–59`: Suspicious (Amber)
  - `60–79`: High Risk (Orange)
  - `80–100`: Critical Risk (Deep Red)
- Transparent explanations, detected points, and recommended safety guidance.

### C. High-Priority Scam Alert
- Prominently styled alert panel triggered on high or critical threat patterns.
- Displays risk score, highlighted transcript keywords, heuristic trigger evaluation, and critical instructions:
  > *"Do not share your OTP or banking credentials. Verify the request through an independently obtained official contact number."*
- One-click **Copy Incident Report** and **Emergency Verification Protocol** actions.

### D. Interactive Demo Mode (3 Fictional Scenarios)
Works **100% offline without API keys**:
1. **Demo 1 — Urgent Bank OTP Scam:**
   *“Your bank account will be blocked in five minutes. Tell me the OTP you just received to keep your account active.”*
   - Simulates streaming telephony audio and text.
   - Triggers **Critical Risk (Score: 90/100)** and High-Priority Alert within **~3.8 seconds**.
2. **Demo 2 — Held Parcel Release Fee:**
   *“Your parcel is on hold. Pay an unexpected release fee immediately using the payment link I sent you.”*
   - Evaluated as **High Risk (Score: 70/100)** with courier and unverified payment flags.
3. **Demo 3 — Legitimate Appointment Call:**
   *“Hello, your appointment is confirmed for tomorrow at 10 AM. Please bring your identification document.”*
   - Evaluated as **Low Risk (Score: 0/100)** with safe context dampeners.

### E. Scan Audit History
- Timestamped log of previous scans with risk badges and summaries.
- Keyword search and risk level filtering (All, Critical, High, Suspicious, Low).
- Detailed scan inspection modal.
- Export scan history to formatted JSON.
- Clear history with confirmation safeguard.

### F. Safety Center & Educational Knowledge Base
- 4-Stage Anatomy of a Vishing Attack (The Hook, The Pressure, The Isolation, The Extraction).
- 5 Golden Rules of Call Defense ("Hang Up & Verify").
- What to do immediately if credentials were compromised.
- Directory of official fraud reporting agencies (FTC, IC3, Action Fraud, Indian Cybercrime 1930, INTERPOL).

---

## 4. Getting Started Locally

### Prerequisites
- Node.js (v20+ or v22 LTS)
- npm

### Installation & Run Commands

```powershell
# 1. Install dependencies
npm install

# 2. Run unit tests (7 passing tests covering all scam categories & negations)
npm test

# 3. Start development server
npm run dev

# 4. Build production bundle
npm run build
```

Open your browser at `http://localhost:5173`.

---

## 5. Optional Python FastAPI Backend

To run the optional Python backend for external model integration:

```powershell
cd backend
pip install -r requirements.txt
python main.py
```
The FastAPI backend server runs at `http://127.0.0.1:8000` with Swagger documentation at `http://127.0.0.1:8000/docs`.

---

## 6. Privacy & Security Disclosures

- **100% Client-Side Processing:** All audio analysis, waveform rendering, and transcript evaluations occur locally inside the user's browser.
- **Zero Credential Logging:** One-time passwords, banking PINs, and credentials are never saved or sent to external servers.
- **Honest Technical Capabilities:** PhishGuard monitors microphone input or user-provided transcripts. It does not wiretap hardware cellular calls in the background without explicit browser authorization.
- **Probabilistic Estimate:** Scam scores are heuristic assessments designed to assist user vigilance and do not replace legal or financial counsel.
