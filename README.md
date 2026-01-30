<p align="center">
  <img src="images/logo.png" alt="Planex Logo" width="120" height="120">
</p>

<h1 align="center">Planex - Smart Task Management</h1>

<p align="center">
  <strong>A modern task management platform with AI integration, real-time whiteboard, and powerful team collaboration features</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Next.js-14.2-black?style=for-the-badge&logo=next.js" alt="Next.js">
  <img src="https://img.shields.io/badge/Flask-3.0-green?style=for-the-badge&logo=flask" alt="Flask">
  <img src="https://img.shields.io/badge/PostgreSQL-15-blue?style=for-the-badge&logo=postgresql" alt="PostgreSQL">
  <img src="https://img.shields.io/badge/Supabase-Realtime-3ECF8E?style=for-the-badge&logo=supabase" alt="Supabase">
  <img src="https://img.shields.io/badge/TailwindCSS-3.4-38B2AC?style=for-the-badge&logo=tailwind-css" alt="TailwindCSS">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Author-Lieu%20Vinh%20Toan-ff69b4?style=flat-square" alt="Author">
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=flat-square" alt="License">
</p>

---

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Configuration](#configuration)
- [Running the Application](#running-the-application)
- [API Documentation](#api-documentation)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [Author](#author)

---

## Introduction

**Planex** is a modern task management platform designed to help individuals and teams organize, track, and complete their work efficiently. With an intuitive interface, smart AI integration, and powerful collaboration tools, Planex delivers a new standard in task management experience.

### Problem Statement

- Difficulty tracking task progress across projects
- Lack of effective team collaboration tools
- No AI integration for intelligent assistance
- Complex document export workflows

### Solution

- Intuitive dashboard with statistics and charts
- Team system with clear role-based permissions
- AI integration (MCP) for querying and updating tasks
- Export to Word, Google Docs, and Google Forms
- Real-time collaborative whiteboard

---

## Features

### Task Management
- Create, edit, and delete tasks with drag-and-drop interface
- Subtasks and detailed checklists
- Tags, priority levels, and deadlines
- Comments and discussions on each task

### Team Management
- Create and manage multiple teams
- Invite members via email
- Role-based permissions: Owner, Admin, Member
- Share tasks between team members

### AI Integration (MCP)
- Query task lists through natural language
- Update progress using conversational commands
- Context-aware suggestions and insights

### Document Management
- Export tasks to Word documents (.docx)
- Google Docs integration
- Create Google Forms from tasks
- Upload and manage file attachments

### Whiteboard
- Real-time collaborative whiteboard
- Draw, write, and add images
- Powered by [tldraw](https://tldraw.com)
- Export and share capabilities

### Sales and Income Tracking
- Track income by project
- Revenue statistics and charts
- Financial reporting

### Notifications
- Real-time notifications
- Deadline reminders
- Team activity updates

### Spreadsheet
- Integrated spreadsheet (FortuneSheet)
- Import/Export Excel files

---

## Tech Stack

### Frontend
| Technology | Version | Description |
|------------|---------|-------------|
| Next.js | 14.2 | React Framework with App Router |
| TypeScript | 5.x | Type-safe JavaScript |
| TailwindCSS | 3.4 | Utility-first CSS framework |
| Lucide React | 0.562 | Icon library |
| tldraw | 4.2 | Whiteboard engine |
| FortuneSheet | 1.0 | Spreadsheet component |
| React Quill | 2.0 | Rich text editor |
| Axios | 1.13 | HTTP client |

### Backend
| Technology | Version | Description |
|------------|---------|-------------|
| Flask | 3.0 | Python web framework |
| SQLAlchemy | 2.0 | ORM |
| Flask-JWT-Extended | 4.6 | JWT Authentication |
| Flask-SocketIO | 5.3 | WebSocket support |
| Supabase | 2.3 | Database and Realtime |
| Cloudinary | 1.36 | Image storage |
| Resend | 2.0 | Email service |
| python-docx | 0.8 | Word document generation |
| Google APIs | 2.70 | Google Docs/Forms integration |

### Database and Infrastructure
- **PostgreSQL** - Primary database
- **Supabase** - Realtime subscriptions and authentication
- **Cloudinary** - Image CDN and storage
- **Gunicorn + Eventlet** - Production server

---

## Installation

### System Requirements

- **Node.js** >= 18.x
- **Python** >= 3.10
- **PostgreSQL** >= 15
- **Git**

### Clone Repository

```bash
git clone https://github.com/lvt17/planex.git
cd planex
```

### Backend Setup

```bash
cd backend

# Create virtual environment
python -m venv venv

# Activate virtual environment
# macOS/Linux:
source venv/bin/activate
# Windows:
venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

### Frontend Setup

```bash
cd frontend

# Install dependencies
npm install
```

---

## Configuration

### Backend Environment

Create a `.env` file in the `backend/` directory:

```env
# Flask
FLASK_ENV=development
SECRET_KEY=your-secret-key-here
JWT_SECRET_KEY=your-jwt-secret-key-here
JWT_ACCESS_TOKEN_EXPIRES=3600

# Database (Supabase PostgreSQL)
DATABASE_URL=postgresql://postgres:YOUR_PASSWORD@db.xxxxx.supabase.co:5432/postgres
SUPABASE_URL=https://xxxxx.supabase.co
SUPABASE_KEY=your-supabase-anon-key

# Resend Email
RESEND_API_KEY=re_xxxxx
RESEND_FROM_EMAIL=noreply@yourdomain.com

# Gmail SMTP (Fallback)
MAIL_SERVER=smtp.gmail.com
MAIL_PORT=587
MAIL_USE_TLS=True
MAIL_USERNAME=your-email@gmail.com
MAIL_PASSWORD=your-app-password
MAIL_DEFAULT_SENDER=your-email@gmail.com

# Cloudinary
CLOUDINARY_CLOUD_NAME=your-cloud-name
CLOUDINARY_API_KEY=your-api-key
CLOUDINARY_API_SECRET=your-api-secret

# Frontend URL
FRONTEND_URL=http://localhost:3000
```

### Frontend Environment

Create a `.env.local` file in the `frontend/` directory:

```env
NEXT_PUBLIC_API_URL=http://localhost:5000/api
NEXT_PUBLIC_SUPABASE_URL=https://xxxxx.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=your-supabase-anon-key
```

---

## Running the Application

### Development Mode

**Terminal 1 - Backend:**
```bash
cd backend
source venv/bin/activate  # or venv\Scripts\activate on Windows
python run.py
```
Backend will run at: `http://localhost:5000`

**Terminal 2 - Frontend:**
```bash
cd frontend
npm run dev
```
Frontend will run at: `http://localhost:3000`

### Database Migration

```bash
cd backend
flask db init          # Initialize migrations (first time only)
flask db migrate -m "Initial migration"
flask db upgrade       # Apply migrations
```

### Production Mode

**Backend:**
```bash
cd backend
gunicorn -k eventlet -w 1 -b 0.0.0.0:5000 run:app
```

**Frontend:**
```bash
cd frontend
npm run build
npm start
```

---

## API Documentation

### Authentication

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/auth/register` | Register new account |
| POST | `/api/auth/login` | Login |
| POST | `/api/auth/forgot-password` | Forgot password |
| POST | `/api/auth/reset-password` | Reset password |

### Tasks

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/tasks` | Get task list |
| POST | `/api/tasks` | Create new task |
| GET | `/api/tasks/:id` | Get task details |
| PUT | `/api/tasks/:id` | Update task |
| DELETE | `/api/tasks/:id` | Delete task |

### Teams

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/teams` | Get team list |
| POST | `/api/teams` | Create new team |
| POST | `/api/teams/:id/invite` | Invite member |
| PUT | `/api/teams/:id/members/:userId` | Update member role |

### AI Integration (MCP)

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/mcp/tasks` | AI query tasks |
| GET | `/api/mcp/tasks/:id` | AI get task detail |
| PUT | `/api/mcp/tasks/:id/progress` | AI update progress |
| GET | `/api/mcp/context` | AI get current context |

### Documents

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/documents/task/:id/export/word` | Export to Word |
| POST | `/api/documents/task/:id/export/gg-docs` | Export to Google Docs |
| POST | `/api/documents/task/:id/export/gg-forms` | Create Google Form |

### Whiteboard

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/documents/whiteboard/create` | Create whiteboard |
| GET | `/api/documents/whiteboard/:id` | Get whiteboard |
| GET | `/api/documents/whiteboard/user` | Get all user whiteboards |
| POST | `/api/documents/whiteboard/:id/export` | Export whiteboard |

---

## Project Structure

```
planex/
|-- backend/
|   |-- app/
|   |   |-- api/           # API endpoints
|   |   |-- models/        # Database models
|   |   |-- services/      # Business logic
|   |   |-- utils/         # Utilities
|   |   +-- config.py      # Configuration
|   |-- migrations/        # Database migrations
|   |-- tests/             # Unit tests
|   |-- requirements.txt
|   |-- run.py
|   +-- .env.example
|
|-- frontend/
|   |-- src/
|   |   |-- app/           # Next.js App Router
|   |   |-- components/    # React components
|   |   |-- contexts/      # React contexts
|   |   |-- hooks/         # Custom hooks
|   |   |-- utils/         # Utilities
|   |   +-- types/         # TypeScript types
|   |-- public/            # Static assets
|   |-- package.json
|   +-- tailwind.config.ts
|
|-- images/                # Project images
+-- README.md
```

---

## Contributing

Contributions are always welcome! To contribute:

1. **Fork** the repository
2. Create a new branch: `git checkout -b feature/AmazingFeature`
3. Commit your changes: `git commit -m 'Add some AmazingFeature'`
4. Push to the branch: `git push origin feature/AmazingFeature`
5. Open a **Pull Request**

### Coding Standards

- ESLint + Prettier for Frontend
- PEP 8 for Backend Python
- Conventional Commits for commit messages

---

## License

Distributed under the MIT License. See `LICENSE` for more information.

---

## Author

<p align="center">
  <img src="https://github.com/lvt17.png" width="100" height="100" style="border-radius: 50%;">
</p>

<p align="center">
  <strong>Lieu Vinh Toan</strong>
</p>

<p align="center">
  <a href="https://github.com/lvt17">
    <img src="https://img.shields.io/badge/GitHub-lvt17-181717?style=for-the-badge&logo=github" alt="GitHub">
  </a>
  <a href="mailto:Lieutoan7788a@gmail.com">
    <img src="https://img.shields.io/badge/Email-Lieutoan7788a@gmail.com-EA4335?style=for-the-badge&logo=gmail" alt="Email">
  </a>
</p>

---

<p align="center">
  If you find this project useful, please give it a star!
</p>

<p align="center">
  Made with passion by <strong>Lieu Vinh Toan</strong>
</p>
