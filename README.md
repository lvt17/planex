<p align="center">
  <img src="images/logo.png" alt="Planex Logo" width="120" height="120">
</p>

<h1 align="center">🚀 Planex - Smart Task Management</h1>

<p align="center">
  <strong>Nền tảng quản lý công việc thông minh với tích hợp AI, Whiteboard và khả năng cộng tác nhóm mạnh mẽ</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Next.js-14.2-black?style=for-the-badge&logo=next.js" alt="Next.js">
  <img src="https://img.shields.io/badge/Flask-3.0-green?style=for-the-badge&logo=flask" alt="Flask">
  <img src="https://img.shields.io/badge/PostgreSQL-15-blue?style=for-the-badge&logo=postgresql" alt="PostgreSQL">
  <img src="https://img.shields.io/badge/Supabase-Realtime-3ECF8E?style=for-the-badge&logo=supabase" alt="Supabase">
  <img src="https://img.shields.io/badge/TailwindCSS-3.4-38B2AC?style=for-the-badge&logo=tailwind-css" alt="TailwindCSS">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Made%20by-Liêu%20Vĩnh%20Toàn-ff69b4?style=flat-square" alt="Author">
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=flat-square" alt="License">
</p>

---

## 📋 Mục lục

- [Giới thiệu](#-giới-thiệu)
- [Tính năng](#-tính-năng)
- [Tech Stack](#-tech-stack)
- [Cài đặt](#-cài-đặt)
- [Cấu hình](#️-cấu-hình)
- [Chạy ứng dụng](#-chạy-ứng-dụng)
- [API Documentation](#-api-documentation)
- [Cấu trúc dự án](#-cấu-trúc-dự-án)
- [Đóng góp](#-đóng-góp)
- [Tác giả](#-tác-giả)

---

## 🌟 Giới thiệu

**Planex** là một nền tảng quản lý công việc hiện đại, được thiết kế để giúp cá nhân và nhóm tổ chức, theo dõi và hoàn thành công việc một cách hiệu quả. Với giao diện trực quan, tích hợp AI thông minh và các công cụ cộng tác mạnh mẽ, Planex mang đến trải nghiệm quản lý công việc hoàn toàn mới.

### 🎯 Vấn đề giải quyết

- ❌ Khó khăn trong việc theo dõi tiến độ công việc
- ❌ Thiếu công cụ cộng tác nhóm hiệu quả
- ❌ Không có khả năng tích hợp AI để hỗ trợ
- ❌ Export tài liệu phức tạp

### ✅ Giải pháp từ Planex

- ✨ Dashboard trực quan với biểu đồ thống kê
- ✨ Hệ thống nhóm với phân quyền rõ ràng
- ✨ Tích hợp AI (MCP) để query và cập nhật task
- ✨ Export Word, Google Docs, Google Forms
- ✨ Whiteboard cộng tác real-time

---

## ✨ Tính năng

### 📝 Quản lý Task
- Tạo, sửa, xóa task với giao diện kéo thả
- Subtask và checklist chi tiết
- Tag, priority và deadline
- Comment và trao đổi trên từng task

### 👥 Quản lý Nhóm (Team)
- Tạo và quản lý nhiều nhóm
- Mời thành viên qua email
- Phân quyền: Owner, Admin, Member
- Chia sẻ task giữa các thành viên

### 🤖 Tích hợp AI (MCP Integration)
- Query danh sách task thông qua AI
- Cập nhật tiến độ bằng ngôn ngữ tự nhiên
- Context-aware suggestions

### 📄 Quản lý Tài liệu
- Export task sang file Word (.docx)
- Tích hợp Google Docs
- Tạo Google Forms từ task
- Upload và quản lý tệp đính kèm

### 🎨 Whiteboard
- Bảng trắng cộng tác real-time
- Vẽ, viết, thêm hình ảnh
- Tích hợp [tldraw](https://tldraw.com)
- Export và chia sẻ

### 💰 Quản lý Doanh thu (Sales & Income)
- Theo dõi thu nhập theo dự án
- Biểu đồ thống kê doanh thu
- Báo cáo tài chính

### 🔔 Thông báo
- Thông báo real-time
- Nhắc nhở deadline
- Cập nhật từ team

### 📊 Spreadsheet
- Bảng tính tích hợp (FortuneSheet)
- Import/Export Excel

---

## 🛠 Tech Stack

### Frontend
| Technology | Version | Description |
|------------|---------|-------------|
| Next.js | 14.2 | React Framework với App Router |
| TypeScript | 5.x | Type-safe JavaScript |
| TailwindCSS | 3.4 | Utility-first CSS |
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
| Supabase | 2.3 | Database & Realtime |
| Cloudinary | 1.36 | Image storage |
| Resend | 2.0 | Email service |
| python-docx | 0.8 | Word document generation |
| Google APIs | 2.70 | Google Docs/Forms integration |

### Database & Infrastructure
- **PostgreSQL** - Primary database
- **Supabase** - Realtime subscriptions và auth
- **Cloudinary** - Image CDN và storage
- **Gunicorn + Eventlet** - Production server

---

## 🚀 Cài đặt

### Yêu cầu hệ thống

- **Node.js** >= 18.x
- **Python** >= 3.10
- **PostgreSQL** >= 15
- **Git**

### Clone repository

```bash
git clone https://github.com/lvt17/planex.git
cd planex
```

### Cài đặt Backend

```bash
cd backend

# Tạo virtual environment
python -m venv venv

# Kích hoạt virtual environment
# macOS/Linux:
source venv/bin/activate
# Windows:
venv\Scripts\activate

# Cài đặt dependencies
pip install -r requirements.txt
```

### Cài đặt Frontend

```bash
cd frontend

# Cài đặt dependencies
npm install
```

---

## ⚙️ Cấu hình

### Backend Environment

Tạo file `.env` trong thư mục `backend/`:

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

Tạo file `.env.local` trong thư mục `frontend/`:

```env
NEXT_PUBLIC_API_URL=http://localhost:5000/api
NEXT_PUBLIC_SUPABASE_URL=https://xxxxx.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=your-supabase-anon-key
```

---

## 🏃 Chạy ứng dụng

### Development Mode

**Terminal 1 - Backend:**
```bash
cd backend
source venv/bin/activate  # hoặc venv\Scripts\activate trên Windows
python run.py
```
Backend sẽ chạy tại: `http://localhost:5000`

**Terminal 2 - Frontend:**
```bash
cd frontend
npm run dev
```
Frontend sẽ chạy tại: `http://localhost:3000`

### Database Migration

```bash
cd backend
flask db init          # Khởi tạo migrations (lần đầu)
flask db migrate -m "Initial migration"
flask db upgrade       # Áp dụng migrations
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

## 📚 API Documentation

### Authentication

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/auth/register` | Đăng ký tài khoản |
| POST | `/api/auth/login` | Đăng nhập |
| POST | `/api/auth/forgot-password` | Quên mật khẩu |
| POST | `/api/auth/reset-password` | Đặt lại mật khẩu |

### Tasks

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/tasks` | Lấy danh sách tasks |
| POST | `/api/tasks` | Tạo task mới |
| GET | `/api/tasks/:id` | Lấy chi tiết task |
| PUT | `/api/tasks/:id` | Cập nhật task |
| DELETE | `/api/tasks/:id` | Xóa task |

### Teams

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/teams` | Lấy danh sách teams |
| POST | `/api/teams` | Tạo team mới |
| POST | `/api/teams/:id/invite` | Mời thành viên |
| PUT | `/api/teams/:id/members/:userId` | Cập nhật role |

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
| POST | `/api/documents/whiteboard/create` | Tạo whiteboard |
| GET | `/api/documents/whiteboard/:id` | Lấy whiteboard |
| GET | `/api/documents/whiteboard/user` | Lấy tất cả whiteboards |
| POST | `/api/documents/whiteboard/:id/export` | Export whiteboard |

---

## 📁 Cấu trúc dự án

```
planex/
├── 📂 backend/
│   ├── 📂 app/
│   │   ├── 📂 api/           # API endpoints
│   │   ├── 📂 models/        # Database models
│   │   ├── 📂 services/      # Business logic
│   │   ├── 📂 utils/         # Utilities
│   │   └── config.py         # Configuration
│   ├── 📂 migrations/        # Database migrations
│   ├── 📂 tests/             # Unit tests
│   ├── requirements.txt
│   ├── run.py
│   └── .env.example
│
├── 📂 frontend/
│   ├── 📂 src/
│   │   ├── 📂 app/           # Next.js App Router
│   │   ├── 📂 components/    # React components
│   │   ├── 📂 contexts/      # React contexts
│   │   ├── 📂 hooks/         # Custom hooks
│   │   ├── 📂 utils/         # Utilities
│   │   └── 📂 types/         # TypeScript types
│   ├── 📂 public/            # Static assets
│   ├── package.json
│   └── tailwind.config.ts
│
├── 📂 images/                # Project images
└── README.md
```

---

## 🤝 Đóng góp

Chúng tôi luôn chào đón mọi đóng góp! Để đóng góp:

1. **Fork** repository
2. Tạo branch mới: `git checkout -b feature/AmazingFeature`
3. Commit changes: `git commit -m 'Add some AmazingFeature'`
4. Push to branch: `git push origin feature/AmazingFeature`
5. Mở **Pull Request**

### Coding Standards

- ESLint + Prettier cho Frontend
- PEP 8 cho Backend Python
- Conventional Commits cho commit messages

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

---

## 👨‍💻 Tác giả

<p align="center">
  <img src="https://github.com/lvt17.png" width="100" height="100" style="border-radius: 50%;">
</p>

<p align="center">
  <strong>Liêu Vĩnh Toàn</strong>
</p>

<p align="center">
  <a href="https://github.com/lvt17">
    <img src="https://img.shields.io/badge/GitHub-lvt17-181717?style=for-the-badge&logo=github" alt="GitHub">
  </a>
  <a href="mailto:Vtoanhihihi@gmail.com">
    <img src="https://img.shields.io/badge/Email-Vtoanhihihi@gmail.com-EA4335?style=for-the-badge&logo=gmail" alt="Email">
  </a>
</p>

---

<p align="center">
  ⭐ Nếu project này hữu ích, hãy cho chúng tôi một star nhé!
</p>

<p align="center">
  Made with ❤️ by <strong>Liêu Vĩnh Toàn</strong>
</p>
