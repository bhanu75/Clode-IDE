# Cloud IDE 🚀

A self-hosted cloud development environment that runs entirely in your browser. Build React, Next.js, and full-stack applications without local setup requirements.

## ✨ Features

- 🌐 **Web-based IDE** - VS Code-like interface in browser
- ⚡ **Pre-configured Environment** - React, Next.js, Node.js ready to use
- 🔧 **Integrated Terminal** - Full bash terminal access
- 📁 **File Management** - Complete file explorer with drag & drop
- 🔄 **Live Preview** - Real-time application preview
- 🐳 **Docker-based** - Isolated, reproducible development environments
- 🚀 **One-click Deploy** - Deploy to Vercel/Netlify directly

## 🏗️ Architecture

```
┌─────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│   Frontend      │───▶│   Backend API    │───▶│ Dev Container   │
│   (Vite + JS)   │    │   (Node.js)      │    │ (Ubuntu + Tools)│
└─────────────────┘    └──────────────────┘    └─────────────────┘


┌─────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│   Frontend      │───▶│   Backend API    │───▶│ Dev Container   │
│   (Vercel)      │    │ (Railway/Render) │    │ (Docker Hub)    │
└─────────────────┘    └──────────────────┘    └─────────────────┘
        │                        │                        │
        │                        │                        │
   ┌────▼────┐              ┌────▼────┐              ┌────▼────┐
   │Custom   │              │Database │              │File     │
   │Domain   │              │PostgreSQL│              │Storage  │
   │+ SSL    │              │         │              │Volume   │
   └─────────┘              └─────────┘              └─────────┘


```

## 🚀 Quick Start

### Prerequisites
- Docker & Docker Compose
- Node.js 18+ (for local development)
- Git

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/Bhanu75/cloud-ide.git
cd cloud-ide
```

2. **Set up environment**
```bash
cp .env.example .env
# Edit .env with your configurations
```

3. **Install dependencies**
```bash
npm run setup
```

4. **Start development environment**
```bash
npm run dev
```

5. **Access your Cloud IDE**
- Frontend: http://localhost:3000
- Backend API: http://localhost:3001

## 📦 Project Structure

```
cloud-ide/
├── 📁 backend/                 # API server & WebSocket
├── 📁 frontend/                # Web IDE interface
├── 📁 dev-container/           # Development environment
├── 📁 infrastructure/          # Docker & deployment configs
├── 📁 docs/                    # Documentation
├── docker-compose.yml          # Container orchestration
└── package.json               # Root workspace config
```

## 🛠️ Development

### Available Scripts

```bash
# Development
npm run dev                    # Start all services
npm run dev:backend           # Backend only
npm run dev:frontend          # Frontend only

# Building
npm run build                 # Build all services
npm run build:backend         # Build backend
npm run build:frontend        # Build frontend

# Testing
npm test                      # Run all tests
npm run test:backend          # Backend tests
npm run test:frontend         # Frontend tests

# Docker
npm run docker:build          # Build containers
npm run docker:up             # Start containers
npm run docker:down           # Stop containers
```

### Adding New Features

1. **Backend API endpoints**: Add to `backend/src/routes/`
2. **Frontend components**: Add to `frontend/src/components/`
3. **Development tools**: Modify `dev-container/Dockerfile`

## 🌐 Deployment

### Vercel (Recommended)

1. **Frontend deployment**
```bash
cd frontend
npx vercel --prod
```

2. **Backend deployment**
- Use Railway, Render, or DigitalOcean
- Set environment variables
- Deploy backend container

### Self-hosted

```bash
# Production deployment
npm run deploy
```

## 📚 Documentation

- [Backend API Documentation](./docs/backend.md)
- [Frontend Development Guide](./docs/frontend.md)
- [Deployment Guide](./docs/deployment.md)
- [Contributing Guidelines](./docs/contributing.md)

## 🤝 Contributing

1. Fork the repository
2. Create feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Monaco Editor](https://microsoft.github.io/monaco-editor/) - Code editor
- [Xterm.js](https://xtermjs.org/) - Terminal emulator
- [Socket.io](https://socket.io/) - Real-time communication
- [Docker](https://www.docker.com/) - Containerization

## 🐛 Issues & Support

If you encounter any issues or need support:

1. Check [existing issues](https://github.com/Bhanu75/cloud-ide/issues)
2. Create [new issue](https://github.com/Bhanu75/cloud-ide/issues/new)
3. Join our [Discord community](https://discord.gg/your-invite)

---

**Built with ❤️ for developers who want coding freedom**