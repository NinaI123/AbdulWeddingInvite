# Wedding Card Setup Guide

## 🚀 Quick Setup

### 1. Clone the Repository
```bash
git clone <your-repo-url>
cd WeddingCardAbdul
```

### 2. Configure Supabase Credentials
```bash
# Copy the example config file
cp config.example.js config.js

# Edit config.js and add your Supabase credentials
```

Open `config.js` and replace with your actual values:
```javascript
window.CONFIG = {
    SUPABASE_URL: "https://your-project.supabase.co",
    SUPABASE_ANON_KEY: "your-anon-key-here"
};
```

### 3. Set Up Database Tables
Go to your Supabase dashboard → SQL Editor and run the SQL from [database_setup.md](./database_setup.md)

### 4. Run Locally
```bash
# Using Python
python -m http.server 8000

# Or using Node.js
npx serve
```

Open `http://localhost:8000`

## 📁 Files Overview

| File | Purpose | Commit to Git? |
|------|---------|----------------|
| `config.js` | Your actual credentials | ❌ NO (gitignored) |
| `config.example.js` | Template for others | ✅ YES |
| `script.js` | Main application logic | ✅ YES |
| `index.html` | Main page | ✅ YES |
| `.env` | Old env file (not used) | ❌ NO (gitignored) |

## 🔒 Security Notes

- ✅ `config.js` is gitignored - your credentials are safe
- ✅ The ANON key is safe to expose (protected by Row Level Security)
- ❌ Never commit `SUPABASE_SERVICE_ROLE_KEY` (you don't have this)
- ✅ Anyone cloning your repo will need to create their own `config.js`

## 🎨 Customization

Edit these files to customize:
- `index.html` - Names, dates, venue details
- `styles.css` - Colors and styling
- `script.js` - Functionality and translations
