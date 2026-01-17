# Show Tracker

A simple web app to track TV shows and movies you want to watch with your partner. Keep a shared watchlist, mark shows as watched, and rate them!

## Features
- 📺 Track TV shows and movies
- 🔍 Search online databases (TVMaze & OMDB) for show info
- ⭐ Rate shows after watching
- 📱 Works on mobile and desktop
- 🔄 Real-time sync across devices
- 🎯 Filter by streaming service, type, and genre

## Using the App

### Access the Live Version
Visit: `https://jtreitman.github.io/show-tracker/`

### Install on iPhone/iPad
1. Open the link in Safari
2. Tap the Share button (square with arrow)
3. Select "Add to Home Screen"
4. Tap "Add"
5. App appears on your home screen like a native app!

## Setting Up Your Own Version

If you want your own private watchlist, follow these steps:

### Step 1: Set Up Firebase (5 minutes, free)

1. Go to [Firebase Console](https://console.firebase.google.com/)
2. Click "Add project" or "Create a project"
3. Name it (e.g., "my-show-tracker")
4. Disable Google Analytics (not needed)
5. Click "Create project"

### Step 2: Enable Firestore Database

1. In Firebase Console, click "Build" → "Firestore Database"
2. Click "Create database"
3. Select "Standard edition"
4. Choose your location
5. Select "Start in test mode"
6. Click "Enable"

### Step 3: Get Your Firebase Config

1. Click the gear icon ⚙️ next to "Project Overview"
2. Click "Project settings"
3. Scroll to "Your apps" section
4. Click the web icon `</>`
5. Register app with a nickname (e.g., "show-tracker-web")
6. **Copy the firebaseConfig object** - it looks like this:
```javascript
const firebaseConfig = {
  apiKey: "AIza...",
  authDomain: "your-project.firebaseapp.com",
  projectId: "your-project-id",
  storageBucket: "your-project.appspot.com",
  messagingSenderId: "123456789",
  appId: "1:123456789:web:..."
};
```

### Step 4: Customize the Code

1. Download `index.html` from the [GitHub repo](https://github.com/jtreitman/show-tracker)
2. Open it in a text editor (VS Code, TextEdit in plain text mode, etc.)
3. Find lines 23-29 (the firebaseConfig section)
4. Replace it with your Firebase config from Step 3
5. Save the file

### Step 5: Use Your Version

**Option A: Use Locally**
- Just open the `index.html` file in your browser
- Works on your computer
- For mobile, you'll need to host it online (Option B)

**Option B: Host on GitHub Pages (Recommended)**
1. Create a free [GitHub](https://github.com) account
2. Create a new repository (name it whatever you want)
3. Make it public (required for free GitHub Pages)
4. Upload your customized `index.html` file
5. Go to Settings → Pages
6. Enable GitHub Pages (deploy from main branch)
7. Wait 2 minutes, then visit your URL: `https://yourusername.github.io/repositoryname/`

## Using the App

### Adding Shows
1. Click "Add Show or Movie"
2. Choose "Search API" to search online databases, or "Manual" to enter manually
3. Select TV Series or Movie
4. Search or fill in details
5. Click "Add"

### Marking as Watched
1. Click "Mark as Watched" on any show
2. Rate it 1-5 stars
3. It moves to your History

### Filtering
- Use the search box to filter by title, service, or genre
- Click "Show Filters" for dropdown filters by service and type

## Sharing with Family

If you want to share a watchlist with your partner:
- Both use the same URL (either the hosted version or local file)
- Use the same Firebase database (don't create separate ones)
- Shows sync automatically in real-time!

## Privacy & Security

- Your Firebase API keys are meant to be public (they're protected by Firebase security rules)
- Your watchlist data is private and stored in your Firebase database
- Nobody else can access your data
- If using GitHub Pages with a public repo, others can copy your code but they can't see your data

## Need Help?

Common issues:
- **Blank page**: Check browser console for errors (Right-click → Inspect → Console)
- **Shows not syncing**: Make sure all devices use the same Firebase config
- **Can't add shows**: Verify Firebase is set up correctly in test mode

## Technical Details

Built with:
- Vanilla JavaScript
- Firebase Firestore for real-time database
- TailwindCSS for styling
- TVMaze API for TV show data
- OMDB API for movie data

---

Made with ❤️ for tracking shows with the people you love
