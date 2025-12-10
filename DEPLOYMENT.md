# 🚀 Deployment Guide - Task Management System

## Frontend Deployment (Vercel)

### Step 1: Vercel Account Setup
1. Visit: https://vercel.com
2. Sign up with GitHub account
3. Click "Import Project"
4. Select `task-management-system` repository

### Step 2: Configure Frontend
```bash
# Build Command
cd frontend && npm install && npm run build

# Output Directory
frontend/build

# Environment Variables (Add in Vercel Dashboard)
REACT_APP_API_URL=https://your-backend-url.railway.app/api
```

### Step 3: Deploy
- Click "Deploy"
- Wait 2-3 minutes
- Your frontend will be live at: `https://task-management-system.vercel.app`

---

## Backend Deployment (Railway)

### Step 1: Railway Account Setup
1. Visit: https://railway.app
2. Sign up with GitHub account
3. Click "New Project"
4. Select "Deploy from GitHub repo"
5. Choose `task-management-system`

### Step 2: Configure Backend
```bash
# Root Directory
backend

# Start Command
npm install && npm start

# Environment Variables (Add in Railway Dashboard)
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/taskmanagement
JWT_SECRET=your_super_secret_jwt_key_12345
PORT=5000
NODE_ENV=production
```

### Step 3: MongoDB Atlas Setup
1. Visit: https://www.mongodb.com/cloud/atlas
2. Create free account
3. Create new cluster (Free tier)
4. Create database user
5. Whitelist all IPs (0.0.0.0/0)
6. Get connection string
7. Add to Railway environment variables

### Step 4: Deploy
- Railway will auto-deploy
- Get your backend URL: `https://your-app.railway.app`
- Update frontend REACT_APP_API_URL with this URL

---

## Quick Deploy Commands

### Frontend (Vercel CLI)
```bash
npm install -g vercel
cd frontend
vercel login
vercel --prod
```

### Backend (Railway CLI)
```bash
npm install -g @railway/cli
railway login
railway init
railway up
```

---

## Post-Deployment Checklist

- [ ] Frontend deployed on Vercel
- [ ] Backend deployed on Railway
- [ ] MongoDB Atlas connected
- [ ] Environment variables configured
- [ ] CORS enabled for frontend URL
- [ ] Test login/signup
- [ ] Test task CRUD operations

---

## Live URLs

**Frontend:** https://task-management-system-keshavja29.vercel.app
**Backend API:** https://task-management-api.railway.app
**API Docs:** https://task-management-api.railway.app/health

---

## Troubleshooting

### CORS Error
Add frontend URL to backend CORS configuration:
```javascript
app.use(cors({
  origin: 'https://task-management-system-keshavja29.vercel.app'
}));
```

### MongoDB Connection Error
- Check connection string
- Verify IP whitelist (0.0.0.0/0)
- Check database user credentials

### Build Errors
- Clear node_modules: `rm -rf node_modules && npm install`
- Check Node version: Use Node 18+
