# SJSU Mental Health Concierge

An ethical AI prototype for a university mental health concierge that connects students with CAPS (Counseling & Psychological Services) resources through a secure chat interface.

## Project Overview

This web application provides a chat interface that connects to an IBM watsonx Orchestrate (wxO) agent to help SJSU students find mental health resources including booking, drop-in services, and crisis support. The system follows strict ethical AI guidelines: transparency, user consent, privacy, fairness, and safety.

## Architecture

- **Frontend**: React + Vite + TypeScript + TailwindCSS
- **Backend**: Express + TypeScript (Node 20)
- **Package Manager**: pnpm
- **Monorepo Structure**:
  - `/web` - Frontend application
  - `/api` - Backend API server
  - `/types` - Shared TypeScript interfaces

## Getting Started

### Prerequisites
- Node.js 20+
- pnpm

### Installation

1. Clone the repository:
```bash
git clone https://github.com/sriboienipelly/SpartanSupport.git
cd SpartanSupport
```

2. Install dependencies:
```bash
pnpm install
```

3. Set up environment variables:
```bash
cp .env.example .env
# Edit .env with your configuration
```

4. Start development servers:
```bash
# Start both frontend and backend
pnpm dev

# Or start individually
pnpm dev:web    # Frontend only
pnpm dev:api    # Backend only
```

## Environment Variables

```env
# Backend
PORT=3001
WXO_AGENT_URL=your_watsonx_orchestrate_endpoint
NODE_ENV=development

# Frontend
VITE_API_URL=http://localhost:3001
```

## Features

### ✅ Implemented
- [x] Monorepo setup with pnpm workspaces
- [x] Consent-first chat interface
- [x] Crisis detection and safety cards
- [x] Support cards for CAPS resources
- [x] Ethical AI transparency features
- [x] IBM watsonx Orchestrate integration

### 🔄 In Progress
- [ ] Real-time chat functionality
- [ ] Email planning tools
- [ ] Check-in preview system

## Ethical AI Principles

This application follows strict ethical guidelines:

- **Transparency**: Always show official SJSU CAPS sources
- **Consent**: Session-only processing with explicit user consent
- **Privacy**: No personal data stored beyond session
- **Fairness**: Neutral and inclusive resource suggestions
- **Safety**: Crisis-first logic with immediate support options
- **Accountability**: Visible explanation of resource selection

## Project Structure

```
SpartanSupport/
├── web/                    # React frontend
│   ├── src/
│   │   ├── components/     # React components
│   │   ├── pages/         # Page components
│   │   ├── hooks/         # Custom hooks
│   │   └── types/         # Frontend types
│   └── package.json
├── api/                   # Express backend
│   ├── src/
│   │   ├── routes/        # API routes
│   │   ├── middleware/    # Custom middleware
│   │   ├── services/      # Business logic
│   │   └── types/         # Backend types
│   └── package.json
├── types/                 # Shared TypeScript interfaces
│   ├── index.ts
│   └── package.json
└── package.json          # Root package.json
```

## Development

```bash
# Install dependencies
pnpm install

# Run tests
pnpm test

# Build for production
pnpm build

# Lint code
pnpm lint
```

## 📞 Crisis Support

If you or someone you know is in crisis:
- **CAPS 24/7 Line**: (408) 924-5678
- **National Suicide Prevention Lifeline**: 988
- **Crisis Text Line**: Text HOME to 741741

## License

This project is licensed under the MIT License.

## Contributing

This is a university prototype project. For contributions, please contact the development team.

---

**⚠️ Important**: This is a prototype for educational purposes. For real mental health support, please contact SJSU CAPS directly.
