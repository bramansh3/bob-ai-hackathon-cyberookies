# 🚀 TICAP — Threat Intelligence Correlation & Alert Prioritisation

> **TICAP** is a threat intelligence analysis and alert prioritisation platform designed to help defence analysts process large volumes of heterogeneous security and intelligence alerts, identify genuine threats, reduce false positives, and generate concise BLUF intelligence reports.

---

## 👥 Team

| Field         | Value                                                                   |
| ------------- | ----------------------------------------------------------------------- |
| **Team Name** | Cyberookies                                                             |
| **Track**     | Open                                                                    |
| **Team Lead** | Vansh Bhatt — [26dce009@charusat.edu.in]                                |
| **Members**   | [Hitarth Mistry], [Dharmik Dudhat], [Jiyanshu Parmar]                   |

---

## 🎯 Problem Statement

Defence analysts receive thousands of alerts every day from different sources such as SIEM systems, satellite feeds, cyber sensors, and intelligence reports. These alerts arrive in different formats, making it difficult for analysts to correlate information, identify genuine threats, and avoid wasting time on false positives.

TICAP addresses this problem by bringing heterogeneous threat information into one analysis workflow and prioritising the alerts that require immediate attention.

---

## 💡 Solution

TICAP provides a unified threat intelligence workflow that ingests alerts from multiple formats, normalises and correlates related events, evaluates their priority and confidence, and maps relevant threats to the MITRE ATT&CK framework.

The platform also generates **BLUF (Bottom Line Up Front)** intelligence reports so commanders and analysts can quickly understand the most important threat information without reading thousands of individual alerts.

---

## ✨ Key Features

* **Multi-Source Alert Ingestion:** Processes demonstration threat data from SIEM, satellite, cyber sensor, and intelligence report sources in different formats such as JSON, CSV, CEF, and TXT.

* **Threat Correlation:** Groups related events within a **30-minute rolling correlation window** to identify potential threat clusters.

* **False Positive Prioritisation:** Uses a False Positive Probability (FPP) scoring approach to help identify and automatically close high-probability false positives.

* **Threat Confidence Scoring:** Separates confidence from false-positive scoring to provide a clearer assessment of the reliability of a potential threat.

* **MITRE ATT&CK Mapping:** Maps identified threat activity to the **MITRE ATT&CK Enterprise v15** framework.

* **Threat Triage:** Classifies identified activity into critical, high, and medium priority levels for analyst attention.

* **BLUF Intelligence Reports:** Produces concise Bottom Line Up Front reports summarising important threat findings.

* **Threat Visualisation:** Provides correlation and threat-cluster visualisations to help analysts understand relationships between events.

* **Analyst Command Workflow:** Supports analyst-style commands such as `/threat-run`, `/threat-triage`, `/mitre T1059`, and `/threat-intel-analyst`.

* **False Positive Whitelist:** Provides a workflow for managing known false-positive patterns.

---

## 🛠️ Tech Stack

| Category             | Technologies                                                                                                             |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| **Languages**        | HTML5, CSS3, JavaScript                                                                                                  |
| **Frameworks**       | Vanilla JavaScript — no external frontend framework                                                                      |
| **IBM Technologies** | IBM Bob / watsonx concepts are reflected in the proposed workflow; live IBM API integration is not currently implemented |
| **Databases**        | None — demonstration data is handled client-side                                                                         |
| **Other**            | SVG visualisations, GitHub, GitHub Actions                                                                               |

---

## 📁 Repository Structure

```text
├── src/                         # All source code
│   └── index.html               # TICAP frontend prototype
│
├── docs/                        # Written documentation
│   ├── problem-statement.md
│   ├── solution-overview.md
│   ├── architecture.md
│   └── setup-guide.md
│
├── demo/                        # Demo artifacts
│   ├── screenshots/             # App screenshots
│   ├── demo-video-link.txt      # Link to demo video
│   └── live-demo-url.txt        # Link to live demo
│
├── presentation/                # Slide deck
│
├── submission.yaml              # Structured submission metadata
│
└── README.md                    # Project documentation
```

---

## ⚡ How to Run

> TICAP is currently implemented as a self-contained frontend prototype using HTML, CSS, and Vanilla JavaScript. No package installation or backend server is required for the current demonstration.

```bash
# 1. Clone the repo
git clone https://github.com/[your-github-username]/bob-ai-hackathon-cyberookies.git

# 2. Enter the repository
cd bob-ai-hackathon-cyberookies

# 3. Open the project
# Open src/index.html directly in a modern web browser
```

### Alternative

You can also serve the `src` directory using a simple local HTTP server:

```bash
cd src
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

---

## 🖥️ Demo

| Artifact        | Link                                                     |
| --------------- | -------------------------------------------------------- |
| 📹 Demo Video   | [See demo/demo-video-link.txt](demo/demo-video-link.txt) |
| 🌐 Live Demo    | [See demo/live-demo-url.txt](demo/live-demo-url.txt)     |
| 🖼️ Screenshots | [See demo/screenshots/](demo/screenshots/)               |
| 📊 Presentation | [See presentation/](presentation/)                       |

> Replace the placeholder demo files/links with your actual submission artifacts before submitting the project.

---

## ⚠️ Known Limitations

> We have intentionally kept the current prototype transparent about what is and is not implemented.

* **Demonstration Data:** The current application uses client-side demonstration threat data rather than live operational feeds.

* **No Production Backend:** There is currently no production database, backend API, or persistent storage layer.

* **No Live Feed Integration:** SIEM, satellite, sensor, and intelligence feeds are represented through demonstration data rather than live connections.

* **IBM Integration:** IBM Bob/watsonx concepts are represented in the proposed analyst workflow, but the current `index.html` does not contain a live IBM Bob or watsonx API integration.

* **Authentication:** Production-grade authentication and role-based access control are not currently implemented.

* **Prototype Scoring:** FPP, confidence, correlation, and threat prioritisation logic are demonstrated within the frontend prototype and would require backend validation and operational data for production deployment.

* **Operational Deployment:** The current project is a hackathon demonstration and is not intended to replace production security monitoring or defence intelligence systems.

---

## 🏅 What We're Most Proud Of

We are most proud of creating a **single analyst-focused workflow that turns thousands of heterogeneous alerts into a smaller number of actionable threat insights**.

TICAP combines multi-format alert ingestion, correlation, false-positive prioritisation, confidence scoring, MITRE ATT&CK mapping, threat clustering, and BLUF reporting into one interface. Instead of forcing analysts to manually examine thousands of disconnected alerts, the prototype demonstrates how the most important threats can be surfaced first and presented in a format that supports rapid decision-making.

Our strongest focus is on the **analyst experience**: reducing information overload while preserving the context needed to understand why an alert deserves attention.
