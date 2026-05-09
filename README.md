# X.com Clone - Full Stack Social Media Platform

一個完整嘅 X.com (Twitter) 克隆網站，包括用戶認證、推文系統、關注功能、搜索、趨勢等。

## 📋 功能特性

- ✅ 用戶認證 (註冊/登錄)
- ✅ 用戶個人資料管理
- ✅ 發佈推文/貼文
- ✅ 讚/轉推功能
- ✅ 關注/取消關注用戶
- ✅ 搜索用戶和推文
- ✅ 實時趨勢
- ✅ 通知系統
- ✅ 響應式設計

## 🛠️ 技術棧

### 前端
- React 18+
- TypeScript
- Tailwind CSS
- React Router
- Axios (API 調用)

### 後端
- Node.js
- Express.js
- MongoDB
- JWT 認證
- Mongoose ORM

## 📁 項目結構

```
X.com/
├── client/                 # React 前端應用
│   ├── src/
│   │   ├── components/     # React 組件
│   │   ├── pages/          # 頁面
│   │   ├── services/       # API 服務
│   │   ├── App.tsx
│   │   └── index.tsx
│   └── package.json
├── server/                 # Express 後端應用
│   ├── src/
│   │   ├── models/         # MongoDB 模型
│   │   ├── routes/         # API 路由
│   │   ├── middleware/     # 中間件
│   │   ├── controllers/    # 控制器
│   │   └── index.ts
│   └── package.json
└── package.json            # Monorepo 配置

```

## 🚀 快速開始

### 1. 克隆 Repository
```bash
git clone https://github.com/15twu/X.com.git
cd X.com
```

### 2. 安裝依賴
```bash
npm run install-all
```

### 3. 設置環境變量

在 `server/` 目錄建立 `.env`:
```
MONGODB_URI=mongodb://localhost:27017/xcom
JWT_SECRET=your_secret_key
PORT=5000
```

在 `client/` 目錄建立 `.env`:
```
REACT_APP_API_URL=http://localhost:5000/api
```

### 4. 啟動開發伺服器
```bash
npm run dev
```

前端會運行在 `http://localhost:3000`
後端會運行在 `http://localhost:5000`

## 📚 API 端點

### 認證
- `POST /api/auth/register` - 用戶註冊
- `POST /api/auth/login` - 用戶登錄
- `GET /api/auth/me` - 獲取當前用戶

### 用戶
- `GET /api/users/:id` - 獲取用戶信息
- `PUT /api/users/:id` - 更新用戶信息
- `POST /api/users/:id/follow` - 關注用戶
- `POST /api/users/:id/unfollow` - 取消關注

### 推文
- `GET /api/tweets` - 獲取所有推文
- `POST /api/tweets` - 發佈推文
- `DELETE /api/tweets/:id` - 刪除推文
- `POST /api/tweets/:id/like` - 點讚
- `POST /api/tweets/:id/retweet` - 轉推

### 搜索和趨勢
- `GET /api/search?q=keyword` - 搜索
- `GET /api/trends` - 獲取趨勢

## 🔐 安全性

- JWT 令牌認證
- 密碼加密 (bcrypt)
- CORS 配置
- 環境變量管理

## 📝 許可證

MIT License

## 👨‍💻 開發者

15twu

## 🤝 貢獻

歡迎提交 Pull Requests！

---

**開始構建你的社交媒體平台吧！🚀**
