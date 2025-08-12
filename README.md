# Battle Showdown Backend

Backend API untuk game Battle Showdown dengan fitur real-time multiplayer menggunakan Socket.IO.

## 🚀 Fitur

- **Real-time Communication** dengan Socket.IO
- **Google Sheets Integration** untuk data pertanyaan
- **Player Management** dengan sistem tim
- **Battle System** real-time
- **Lobby Management** untuk pemain

## 🛠️ Tech Stack

- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **Socket.IO** - Real-time communication
- **Google Sheets API** - Data storage
- **CORS** - Cross-origin support

## 📁 Struktur Project

```
battleshowdown-backend/
├── server.js              # Main server file
├── package.json           # Dependencies
├── env.local              # Environment variables
├── routes/                # API routes
│   ├── auth.js           # Authentication routes
│   ├── battle.js         # Battle routes
│   ├── pemain.js         # Player routes
│   ├── pertanyaan.js     # Question routes
│   └── pertanyaan-sheets.js # Google Sheets routes
├── services/              # Business logic
│   └── googleSheets.js   # Google Sheets service
├── models/                # Data models
│   ├── pemain.js         # Player model
│   └── pertanyaan.js     # Question model
└── scripts/               # Utility scripts
    ├── import-from-sheets.js
    ├── seed-pertanyaan.js
    └── seed-sheets.js
```

## 🔧 Setup

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Setup environment variables:**
   ```bash
   cp env.local.example env.local
   # Edit env.local dengan credentials Google Sheets
   ```

3. **Run development server:**
   ```bash
   npm run dev
   ```

## 🌐 API Endpoints

- `GET /api/pertanyaan/sheets` - Get all questions
- `GET /api/pertanyaan/sheets/random` - Get random question
- `GET /api/pertanyaan/sheets/kategori/:kategori` - Get questions by category
- `GET /api/pertanyaan/sheets/statistik` - Get statistics
- `POST /api/pertanyaan/sheets` - Add new question

## 🔌 Socket.IO Events

- `join-lobby` - Player joins lobby
- `leave-lobby` - Player leaves lobby
- `lobby-update` - Lobby status update
- `battle-start` - Battle begins
- `battle-selesai` - Battle ends

## 📊 Environment Variables

```env
PORT=5000
GOOGLE_SHEET_ID=your_sheet_id
GOOGLE_SERVICE_ACCOUNT_EMAIL=your_service_account
GOOGLE_PRIVATE_KEY=your_private_key
```

## 🚀 Deployment

Backend ini bisa di-deploy ke:
- **Railway** (recommended)
- **Heroku**
- **Vercel**
- **DigitalOcean**

## 📝 License

MIT License 