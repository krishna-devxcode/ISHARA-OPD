# 🏥 ISHARA-OPD
### Making Healthcare Communication Accessible to Everyone

**ISHARA-OPD** is an accessibility-focused healthcare solution designed to help deaf and hard-of-hearing patients communicate their symptoms, medical history, and immediate needs during hospital Outpatient Department (OPD) visits.

The platform uses visual symptom pictograms, an interactive body map, a Pain Drawing Tool, adaptive questions, and a Quick Communication Board to make patient intake easier. It organizes the collected information into a structured, doctor-ready clinical summary.

> **Our mission:** To reduce communication barriers in healthcare and make OPD visits more accessible, inclusive, and patient-friendly.

---

## 📌 Problem Statement

Deaf and hard-of-hearing patients can face communication barriers during hospital visits, particularly when sign-language interpreters are unavailable.

Explaining pain, describing symptoms, sharing medical history, and communicating immediate needs can become difficult when healthcare staff and patients do not share an accessible communication method.

Traditional patient intake processes often rely heavily on spoken communication or written forms, which may not be suitable for every patient.

## 💡 Our Solution

ISHARA-OPD provides a visual, patient-friendly interface that allows patients to communicate health-related information through selectable pictograms, body-map interactions, simple questions, and visual communication cards.

The collected information is organized into a structured clinical summary that healthcare professionals can review during consultation.

## ✨ Key Features

### 🩺 1. Visual Symptom Selection
- Select symptoms using visual pictograms.
- Examples include pain, fever, cough, and dizziness.
- Provide a custom symptom entry option.

### 🧍 2. Interactive Body Map
- Select the affected body part.
- Identify the exact pain location.
- Indicate the direction in which pain spreads.

### ✏️ 3. Pain Drawing Tool
- Draw or mark the affected area directly on the body map.
- Show the approximate location and spread of pain.
- Help communicate pain visually instead of relying only on verbal descriptions.

### 💬 4. Quick Communication Board
Provides ready-to-use visual cards for communicating immediate needs, including:

- “I have pain”
- “I need water”
- “Please repeat”
- “I don't understand”

The board helps patients express essential needs during intake and consultation.

### 🧠 5. Adaptive Questions
- Ask relevant follow-up questions based on previous answers.
- Use simple, easy-to-understand visual answer options.
- Collect more structured symptom information.

### 📋 6. Medical History
- Record relevant medical history.
- Review current medicines and allergies.
- Allow patients to add emergency contacts.
- Keep optional fields skippable.

### 📄 7. Doctor-Ready Clinical Summary
- Organize the patient's responses into a structured summary.
- Include selected symptoms, affected body areas, pain markings, and relevant medical history.
- Help doctors review the information before or during consultation.

### 🌐 8. Accessibility and Language Support
- Prioritize a clear, visual interface.
- Plan support for Indian Sign Language (ISL).
- Design multilingual communication to accommodate diverse users.

### 📶 9. Offline-First Support
- Plan local data storage using IndexedDB.
- Queue eligible information when connectivity is unavailable.
- Synchronize queued data when connectivity returns.

### 🔐 10. Privacy and Security
- Design for controlled access to patient information.
- Protect sensitive medical records.
- Apply appropriate authentication and access controls.

*Features described as planned must be validated against the current implementation before being presented as completed.*

---

## 🔄 How It Works

```text
        PATIENT OPENS ISHARA-OPD
                    |
                    v
        SELECT SYMPTOMS VISUALLY
                    |
                    v
       MARK PAIN ON THE BODY MAP
                    |
                    v
       ANSWER ADAPTIVE QUESTIONS
                    |
                    v
       PROVIDE MEDICAL HISTORY
                    |
                    v
       GENERATE CLINICAL SUMMARY
                    |
                    v
          DOCTOR REVIEWS DETAILS
```

The Quick Communication Board is available to help patients express immediate needs throughout the interaction.

## 🛠️ Technology Stack

The following is the proposed project architecture. Update it to reflect the technologies actually implemented in the repository.

| Component | Technology |
|---|---|
| Frontend | HTML, CSS, JavaScript |
| Backend | Python, FastAPI |
| API | REST API |
| Database | PostgreSQL |
| Offline Storage | IndexedDB |
| Accessibility | Visual pictograms, interactive body map, planned ISL support |
| Security | Authentication and access controls |

## 🏗️ System Architecture

```text
┌──────────────────────────────┐
│       Patient Interface      │
│ Symptoms • Body Map • Board  │
└──────────────┬───────────────┘
               |
               v
┌──────────────────────────────┐
│     Patient Intake Logic     │
│ Adaptive Questions • History │
└──────────────┬───────────────┘
               |
               v
┌──────────────────────────────┐
│       Backend API            │
│       Python + FastAPI       │
└──────────────┬───────────────┘
               |
               v
┌──────────────────────────────┐
│         PostgreSQL           │
│ Structured Intake Records    │
└──────────────┬───────────────┘
               |
               v
┌──────────────────────────────┐
│     Clinical Summary         │
│      Doctor Review           │
└──────────────────────────────┘
```

*IndexedDB is intended for local offline storage and synchronization when the connection is restored. Its implementation and conflict-handling behavior should be verified in the actual application.*

## 🎯 Target Users

- Deaf and hard-of-hearing patients.
- Patients who benefit from visual communication.
- Doctors and OPD healthcare professionals.
- Hospitals and clinics seeking more accessible intake workflows.
- Healthcare organizations working toward inclusive patient experiences.

## 🌟 What Makes ISHARA-OPD Different?

- **Visual-first communication:** Reduces dependence on spoken interaction.
- **Pain drawing:** Helps patients indicate the location and spread of discomfort.
- **Quick Communication Board:** Supports communication of immediate needs.
- **Structured information:** Organizes patient responses for clinical review.
- **Accessibility-focused design:** Prioritizes inclusive interaction in OPD settings.
- **Offline-first direction:** Aims to support intake workflows when internet connectivity is unreliable.

ISHARA-OPD is designed to support communication, not replace professional medical judgment, qualified interpreters, or clinical diagnosis.

## 🚀 Getting Started

Setup instructions will depend on the implementation available in this repository.

### Prerequisites

- Python 3.10 or a compatible version.
- A modern web browser.
- PostgreSQL, if the database-backed functionality is implemented.
- Git.

### Installation

Clone the repository:

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd <YOUR_PROJECT_FOLDER>
```

Create and activate a virtual environment:

```bash
python -m venv venv
```

On Windows:

```bash
venv\Scripts\activate
```

Install dependencies if a `requirements.txt` file is available:

```bash
pip install -r requirements.txt
```

Run the FastAPI application if the backend entry point is `main.py`:

```bash
uvicorn main:app --reload
```

Open the local API documentation, if enabled:

```text
http://127.0.0.1:8000/docs
```

**Note:** These are example setup commands for the proposed stack. Confirm the repository structure, dependency file, database configuration, and application entry point before using them.

## 🗺️ Future Enhancements

- Expanded Indian Sign Language support.
- Additional Indian language options.
- Improved visual symptom libraries.
- Patient-friendly report export and sharing.
- Reliable offline synchronization and recovery.
- Usability testing with deaf and hard-of-hearing patients.
- Accessibility testing with healthcare professionals.
- Stronger privacy, consent, and data-retention controls.

## 🔒 Privacy and Medical Disclaimer

ISHARA-OPD is intended to assist with patient communication and information collection. It is not a substitute for professional medical evaluation or emergency care.

Use synthetic or appropriately de-identified data during development and demonstrations. Do not commit real patient records, credentials, API keys, or other sensitive information to a public repository.

Any deployment involving medical information must implement appropriate consent, security, access controls, and applicable privacy requirements.

## 👥 Team XTRUE

**Project:** ISHARA-OPD

## 🤝 Contributing

Contributions, suggestions, and accessibility feedback are welcome.

1. Fork the repository.
2. Create a feature branch.
3. Make your changes.
4. Test your changes.
5. Submit a pull request with a clear description.

## 📄 License

A license has not yet been specified. Add an appropriate open-source license before inviting external contributions or redistributing the project.

---

**Built by Team XTRUE with the goal of making healthcare communication more accessible, inclusive, and patient-friendly.** 💙
