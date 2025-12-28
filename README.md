# Job Application Tracker with AI Quick Paste

Live job application tracker with AI-powered paste import using Claude AI.

🔗 **Live Site**: https://urbanvisionmg.github.io/job-tracker/

## Features

- ✨ **AI Quick Paste**: Paste job details from Indeed, LinkedIn, emails - AI extracts everything automatically
- ➕ **Manual Entry**: Traditional form for adding applications
- 📊 **Status Tracking**: Applied → Screening → Interview → Offer
- 📝 **Personal Notes**: Add private thoughts on each job
- 📷 **Screenshot URLs**: Link to saved job posting images
- 💾 **Auto-Save**: All data persists in browser localStorage
- ⬇️ **Download Backup**: Export as JSON
- 📧 **Email Reports**: Send tracker summary via email

## 🚀 Setup Instructions

### Step 1: Get Your Anthropic API Key

1. Go to https://console.anthropic.com
2. Sign up or log in
3. Navigate to "API Keys"
4. Click "Create Key"
5. Copy the key (starts with `sk-ant-...`)

### Step 2: Add Your API Key

1. Go to the GitHub repository
2. Click on `index.html`
3. Click the pencil icon (Edit this file)
4. Find this line near the top (around line 26):
   ```javascript
   const ANTHROPIC_API_KEY = 'sk-ant-your-api-key-here'; // REPLACE THIS WITH YOUR KEY
   ```
5. Replace `'sk-ant-your-api-key-here'` with your actual API key:
   ```javascript
   const ANTHROPIC_API_KEY = 'sk-ant-api03-xyz123...'; // Your actual key
   ```
6. Scroll down and click "Commit changes"
7. Wait ~30 seconds for GitHub Pages to rebuild

### Step 3: Start Using AI Quick Paste!

1. Visit https://urbanvisionmg.github.io/job-tracker/
2. Click the green **✨ AI Quick Paste** button
3. Copy a job posting from Indeed/LinkedIn/email
4. Paste it in the text area
5. Click "Import Application"
6. Watch AI extract the position, company, location, and salary!

## ⚠️ Security Note

Your API key is visible in the HTML source code. This is fine for **personal use only**. Don't share your repository URL with others, or they'll see your key.

**For personal use**: This is the simplest solution - no backend needed!

**For sharing with others**: Consider:
- Using environment variables with Netlify/Vercel
- Building a serverless function
- Or just use manual entry and share the tracker read-only

## Usage

### AI Quick Paste (Recommended)
1. Find a job posting on Indeed, LinkedIn, or in an email
2. Select all the text (Ctrl+A / Cmd+A)
3. Copy it (Ctrl+C / Cmd+C)
4. Click "AI Quick Paste" button
5. Paste the text
6. Click "Import Application"
7. AI will extract: Position, Company, Location, Salary

### Manual Entry
1. Click "Add New Application"
2. Fill out the form
3. Click "Submit"

### Track Progress
- Click the status dropdown to update: Applied → Screening → Interview → Offer
- Add personal notes (thoughts, feelings, strategy)
- Add screenshot URL (link to saved job posting image)
- Click edit icon (✏️) to modify details
- Click trash icon (🗑️) to delete

### Share with Therapist
- Send them your GitHub Pages URL
- They can view all applications
- Update your tracker anytime, they see changes in real-time

## How AI Parsing Works

The tracker calls the Anthropic API directly from your browser:
1. You paste job details
2. Browser sends text to `api.anthropic.com`
3. Claude AI extracts structured data
4. Returns JSON with position, company, location, salary
5. Tracker adds it to your list

**Cost**: ~$0.01 per 1000 job parsings (very cheap!)

## File Structure

```
job-tracker/
├── index.html   # Main app (React + AI integration)
├── data.json    # Initial job data (12 sample applications)
└── README.md    # This file
```

## Data Storage

- **Primary**: Browser localStorage (persists across sessions)
- **Backup**: data.json file (12 sample jobs loaded on first visit)
- **Export**: Download JSON backup anytime

## Troubleshooting

**AI Quick Paste shows "Please set your API key"**
- You haven't added your Anthropic API key yet
- Follow Step 2 above

**AI Paste returns "API request failed"**
- Check if your API key is correct
- Check if you have API credits (https://console.anthropic.com)
- Open browser console (F12) for error details

**Data disappeared**
- Check if localStorage was cleared
- Download a backup regularly
- Initial data in data.json loads if localStorage is empty

**Button shows "Cancel" but form is closed**
- Reload the page (Ctrl+R / Cmd+R)

## Tech Stack

- **Frontend**: React 18 (via CDN, no build step)
- **AI**: Anthropic Claude API (direct fetch calls)
- **Storage**: Browser localStorage + data.json fallback
- **Hosting**: GitHub Pages (free, fast, reliable)
- **Styling**: Inline React styles (purple gradient theme)

## Future Ideas

- Gmail integration (auto-import from job emails)
- Calendar integration (track interview dates)
- Analytics dashboard (success rates, time to offer)
- Export to PDF/CSV
- Company research (AI-powered insights)

## License

MIT - Use however you want!

## Credits

Built with Claude AI by Anthropic
