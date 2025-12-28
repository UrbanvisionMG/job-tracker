# Micah Auto Job Application Tracker

## 🚀 Live Deployment Instructions

### Quick Deploy (5 minutes)

1. **Create GitHub Repository**
   - Go to https://github.com/new
   - Repository name: `job-tracker`
   - Make it **Public**
   - Click "Create repository"

2. **Upload Files**
   - Click "uploading an existing file"
   - Drag and drop `index.html` and `data.json`
   - Commit the files

3. **Enable GitHub Pages**
   - Go to repository Settings
   - Click "Pages" in left sidebar
   - Under "Source", select "main" branch
   - Click Save

4. **Get Your Live URL**
   - Wait 1-2 minutes
   - Your site will be live at: `https://[your-username].github.io/job-tracker`

---

## 📝 How It Works

- **index.html** - Your job tracker app (React-based)
- **data.json** - Your job applications database (lives on GitHub)

---

## 🔄 Updating Data

When you add jobs via the app:
1. Data saves to your browser (localStorage)
2. Tell Claude: "Save my tracker data to GitHub"
3. Claude will update data.json
4. Your live site refreshes automatically!

---

## ✨ Features

- ✅ Add/Edit/Delete applications
- ✅ Quick Paste Import (AI-powered)
- ✅ Status tracking with color codes
- ✅ Gmail auto-import (via Claude)
- ✅ Screenshot links
- ✅ Personal notes
- ✅ Download backups
- ✅ Email reports
- ✅ Fully responsive (works on mobile)

---

## 🔗 Sharing with Therapist

Just send them the URL: `https://[your-username].github.io/job-tracker`

They can view your applications anytime. No login required!

---

## 🛠️ Tech Stack

- Pure HTML/CSS/JS
- React 18 (via CDN)
- Lucide Icons
- GitHub Pages hosting
- JSON file storage
