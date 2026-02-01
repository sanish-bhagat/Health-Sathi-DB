# Health Sathi 🏥

**Health Sathi** is a multimodal AI health assistant designed to bridge the gap between patients and medical clarity. It uses Google's Gemini models to analyze medical records (PDFs, Images) and voice symptoms, providing clinical guidance that is verified by doctors.

![Health Sathi Banner](https://via.placeholder.com/1200x400/0d9488/ffffff?text=Health+Sathi+AI+Assistant)

## 🚀 Key Features

### For Patients 🧘‍♂️
*   **Default Regional Language**: Medical advice is provided in **Hindi by default** to ensure accessibility, with manual switching for other languages.
*   **Multimodal Input**: 
    *   **Voice**: Record symptoms naturally using speech-to-text.
    *   **Vision**: Upload photos of handwritten prescriptions or medicine bottles.
    *   **Documents**: Upload PDF lab reports for analysis.
*   **Document Preview**: Preview files instantly upon attachment and view the original document in a dedicated modal after upload.
*   **AI Assessment**: Instantly extracts vitals, medication schedules, and provides clinical guidance using **Google Gemini 1.5/3 Flash**.
*   **Language Barrier Breaker**: Translate medical advice into **10+ Indian Regional Languages** (Hindi, Tamil, Marathi, etc.).
*   **Text-to-Speech (TTS)**: Listen to the guidance in a natural voice.
*   **Download Reports**: Generate professional **PDF Health Assessments** to share with caregivers.

### For Doctors 👨‍⚕️
*   **Mobile-Optimized Dashboard**: A responsive triage sidebar that can be toggled on mobile devices, allowing full access to analysis and patient details on the go.
*   **Triage Dashboard**: View a prioritized list of patient reports (Critical vs. Pending) with unified profile styling.
*   **Clinical Verification**: Review AI-generated insights against original files.
*   **One-Click Actions**: Approve, Modify, or Escalate cases with a single click.
*   **RAG Context**: AI analysis is anchored in a simulated "Health Sathi Medical Library" to ensure hallucination-free responses based on protocols (e.g., Cardiology, Renal).

---

## 🛠️ Technology Stack

*   **Frontend**: React 19, TypeScript, Vite
*   **Styling**: Tailwind CSS (Fully responsive UI)
*   **AI Engine**: Google GenAI SDK (`@google/genai`)
    *   *Analysis*: `gemini-3-flash-preview`
    *   *TTS*: `gemini-2.5-flash-preview-tts`
*   **Backend & Auth**: Firebase (Authentication & Firestore)
*   **State Management**: Zustand
*   **PDF Generation**: `jspdf` & `jspdf-autotable`

---

## ⚙️ Installation & Setup

### Prerequisites
*   Node.js (v18 or higher)
*   A Google Gemini API Key (Get one at [aistudio.google.com](https://aistudio.google.com/))
*   Firebase Project (For Authentication and Firestore)

### Steps

1.  **Clone the repository**
    ```bash
    git clone https://github.com/your-username/health-sathi.git
    cd health-sathi
    ```

2.  **Install Dependencies**
    ```bash
    npm install
    ```

3.  **Configure Environment Variables**
    *   Create a `.env` file in the root directory.
    *   Add your Gemini and Firebase credentials:
    ```env
    VITE_GEMINI_API_KEY=your_gemini_key
    VITE_FIREBASE_API_KEY=your_firebase_key
    VITE_FIREBASE_AUTH_DOMAIN=your_auth_domain
    VITE_FIREBASE_PROJECT_ID=your_project_id
    VITE_FIREBASE_STORAGE_BUCKET=your_storage_bucket
    VITE_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
    VITE_FIREBASE_APP_ID=your_app_id
    ```

4.  **Run the App**
    ```bash
    npm run dev
    ```
    Open `http://localhost:5173` in your browser.

---

## 📱 How to Use

1.  **Authentication**:
    *   Click "Create Account" or "Login".
    *   Select **Patient Portal** to upload data or **Doctor Portal** to review cases.

2.  **Generate a Report**:
    *   As a Patient, record symptoms via microphone or upload a report.
    *   Preview the file before clicking "Generate Health Assessment".

3.  **Doctor Review**:
    *   Log in as a Doctor.
    *   Use the toggleable sidebar on mobile to select patients from the triage list.
    *   Verify AI insights and click "Approve & Send".

4.  **Download PDF**:
    *   Back in the Patient Dashboard, download the finalized A4 PDF assessment.

---