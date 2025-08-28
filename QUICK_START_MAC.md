# Quick Start Guide for Mac

## Prerequisites Check

Open Terminal and run these commands to check if you have the required software:

```bash
# Check Node.js (should be 18+)
node --version

# Check npm
npm --version
```

If you don't have Node.js or have an older version, follow the installation steps below.

## Install Node.js on Mac

### Method 1: Using Homebrew (Recommended)

1. **Install Homebrew** (if you don't have it):
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

2. **Install Node.js**:
   ```bash
   brew install node
   ```

### Method 2: Download from Official Website

1. Go to [nodejs.org](https://nodejs.org/)
2. Download the **LTS version** for macOS
3. Run the downloaded `.pkg` installer
4. Follow the installation wizard

## Setup and Run the Application

1. **Extract the package** to your desired location (e.g., Desktop or Documents)

2. **Open Terminal** and navigate to the folder:
   ```bash
   cd ~/Desktop/marfi-complete-package-v3
   ```
   (Adjust the path based on where you extracted the files)

3. **Install dependencies**:
   ```bash
   npm install
   ```
   This will take a few minutes to download all required packages.

4. **Start the development server**:
   ```bash
   npm run dev
   ```

5. **Open in browser**:
   The application should automatically open in your default browser at `http://localhost:3000`

## What You Should See

Once the application starts, you should see:
- A navigation sidebar on the left
- The main content area with the current page (likely "Allocation")
- Modern glass-style UI design

## Navigation

Use the sidebar to navigate between different sections:
- 📊 **Allocation** - Dashboard and reporting
- 📥 **Inbox** - Manage orders and approvals  
- 📄 **Source Data** - Data management
- 📈 **Published Data** - View published reports
- 🏗️ **Build Report** - Interactive report builder
- 💾 **Saved Reports** - Manage saved reports

## Common Mac Terminal Commands

```bash
# Navigate to a folder
cd /path/to/folder

# List files in current directory
ls -la

# Go to home directory
cd ~

# Go to Desktop
cd ~/Desktop

# Go back one directory
cd ..

# Clear terminal screen
clear
```

## Stopping the Application

To stop the development server:
1. Go back to the Terminal window where the app is running
2. Press `Ctrl + C` (or `Cmd + C`)
3. The server will stop and you'll return to the command prompt

## Troubleshooting

### Permission Issues
If you get permission errors, try:
```bash
sudo npm install
```

### Port Already in Use
If port 3000 is busy:
```bash
# Kill the process using port 3000
sudo lsof -ti:3000 | xargs kill -9

# Then try running again
npm run dev
```

### Clear Cache
If you have issues, try clearing the npm cache:
```bash
npm cache clean --force
rm -rf node_modules package-lock.json
npm install
```

## Need Help?

1. Check the main README.md file for detailed information
2. Look at the browser console (F12) for any error messages
3. Ensure your Node.js version is 18 or higher: `node --version`

Happy coding! 🚀
