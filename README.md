# DraftMate AI ⚖️

### Your AI-Powered Legal Drafting and Research Assistant

DraftMate AI is an AI-powered legal assistance platform designed to simplify legal document drafting, legal research, and understanding complex legal information. It helps users turn their instructions and case details into structured legal drafts while making legal information easier to explore and understand.

The platform combines a React-based user interface with AI-powered backend services to support legal drafting and research workflows.

## ✨ Key Features

### 📝 AI Legal Drafting
- Generate structured legal documents from user-provided facts and instructions.
- Support multiple document types, including:
  - Legal Notices
  - Rental Agreements
  - Employment Contracts
  - Business Contracts
  - Affidavits
  - Complaints
  - Demand Letters
  - Formal Letters and Applications
- Select a jurisdiction to provide relevant context.
- Refine, rewrite, expand, or simplify generated content.
- Use placeholders when required information is missing.

### 🔍 Legal Research
- Ask legal questions in natural language.
- Explore legal topics with AI-generated explanations.
- Select a jurisdiction, including India, the United States, the United Kingdom, Canada, and Australia.
- View research responses through a dedicated interface.
- Designed for integration with legal sources and citation verification services.

### 📚 Legal Document Understanding
- Make complex legal language easier to understand.
- Help users interpret clauses, notices, agreements, and other legal content.
- Support a more accessible legal-information experience.

### 💬 AI Chat Assistant
- Interactive assistant interface for user queries.
- Designed to provide a convenient way to access AI assistance across the platform.

### 🎨 User Interface
- React-based frontend.
- Dedicated pages for Home, Drafter, and Research.
- Navigation for accessing different workspaces and legal tools.
- Clean, responsive-oriented interface.

## 🛠️ Tech Stack

| Layer | Technologies |
|---|---|
| Frontend | React.js, JavaScript, CSS |
| Backend | Node.js, Express.js |
| AI Integration | Google Gemini API (`gemini-2.5-flash`) |
| API Communication | REST APIs, Fetch API |
| Research Integration | Python, FastAPI, Uvicorn *(for the separate research service, when configured)* |
| Version Control | Git and GitHub |

## 🏗️ Project Structure

```text
DraftMate-AI/
├── public/
├── src/
│   ├── components/
│   │   ├── Navbar.js
│   │   └── ChatAssistant.js
│   ├── pages/
│   │   ├── Home.js
│   │   ├── Drafter.js
│   │   ├── Research.js
│   │   └── WorkspacePage.js
│   ├── App.js
│   └── index.js
├── server/
│   ├── index.js
│   ├── package.json
│   └── .env
├── package.json
└── README.md
```

*Note: The structure above represents the main application components. Your local project may contain additional files or folders.*

## 🚀 Getting Started

### Prerequisites

Make sure you have installed:

- [Node.js](https://nodejs.org/)
- npm
- A Google Gemini API key
- Python and pip, if you are running the separate FastAPI research service

### 1. Clone the Repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd draftmate-ai
```

Replace `<YOUR_GITHUB_REPOSITORY_URL>` with your actual GitHub repository URL.

### 2. Install Frontend Dependencies

From the project root:

```bash
npm install
```

### 3. Configure the Backend

Move into the server directory:

```bash
cd server
npm install
```

Create a `.env` file inside the `server/` directory:

```env
GEMINI_API_KEY=your_gemini_api_key
```

Replace the placeholder with your own API key. Never commit your actual API key to GitHub.

### 4. Start the Backend

From the `server/` directory, run:

```bash
node index.js
```

The Node.js backend is configured to run on:

```text
http://localhost:5000
```

### 5. Start the Frontend

Open a second terminal, navigate to the project root, and run:

```bash
npm start
```

The React development server typically opens at:

```text
http://localhost:3000
```

Keep the frontend and backend terminals running while using the application.

## 🔌 API Endpoints

The Node.js backend includes the following endpoints:

| Method | Endpoint | Purpose |
|---|---|---|
| GET | `/api/health` | Check backend health |
| POST | `/api/draft` | Generate an AI-assisted legal draft |
| GET | `/api/research` | Access the research route |
| POST | `/api/research` | Submit a legal research question |

**Example health check:**

```http
GET http://localhost:5000/api/health
```

The exact request body for drafting and research depends on the implementation in `server/index.js`.

If the separate FastAPI research and citation-verification service is configured, it can run independently on port `8000`. Follow that service's own setup instructions and API routes.

## 🔐 Environment Variables

| Variable | Description |
|---|---|
| `GEMINI_API_KEY` | API key used for Gemini-powered features |
| `INDIANKANOON_API_TOKEN` | Required only if the integrated legal research service uses the Indian Kanoon API |

Store secrets in environment files and exclude them from version control.

Recommended `.gitignore` entries:

```gitignore
node_modules/
.env
.env.*
!.env.example
build/
dist/
__pycache__/
.venv/
*.pyc
```

## 🧭 How It Works

1. **Provide details:** The user describes their legal situation or enters a research question.
2. **Process the request:** The frontend sends the relevant information to the backend.
3. **Generate assistance:** The configured AI service processes the request and returns a response.
4. **Review the result:** The user reads the generated draft or research explanation.
5. **Verify important information:** Users should independently confirm applicable laws, legal citations, and jurisdiction-specific requirements before relying on the output.

## ⚠️ Limitations

- AI-generated content may contain errors or incomplete information.
- Legal provisions, citations, and case references must be independently verified.
- Available functionality depends on the configured APIs and backend services.
- External legal-source integrations may require additional credentials and configuration.
- DraftMate AI is an assistance tool, not a substitute for a qualified legal professional.

## 🔮 Future Enhancements

- PDF and DOCX document uploads and text extraction.
- Automated citation verification against trusted legal sources.
- Source-linked legal research with relevant passages.
- Contract analysis and clause comparison.
- Document summarization and plain-language explanations.
- Downloadable legal drafts in PDF and DOCX formats.
- Improved multilingual assistance.
- User accounts and saved document history.

## 🤝 Contributing

Contributions, suggestions, and bug reports are welcome.

1. Fork the repository.
2. Create a feature branch.
3. Make your changes.
4. Test the relevant functionality.
5. Submit a pull request describing your changes.

## ⚖️ Disclaimer

DraftMate AI provides AI-generated legal information and drafting assistance for informational purposes only. It does not establish an attorney-client relationship and does not constitute professional legal advice. Always verify legal information and consult a qualified legal professional before taking legal action.

## 👩‍💻 Built With

**DraftMate AI** — making legal drafting and research more accessible through AI.

