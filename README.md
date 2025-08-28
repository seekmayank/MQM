# MARFI Complete Package v3

A complete, standalone MARFI application package with all functionality including:
- Dashboard reporting and data visualization
- Inbox management with approval workflows  
- Source data management
- Published data viewing
- Saved reports management

## Features

✅ **Interactive Dashboard Builder**
- Multiple chart types (Line, Column, Stacked Column, Pie, Scorecard)
- Y-axis formatting (K, M, B notation)
- Drag and drop functionality
- Dynamic font sizing and rich text editing
- Real-time data visualization

✅ **Inbox Management**
- My Orders, Pending Actions, and History tabs
- Action buttons: View, Approve, Send Back, Reject
- Sortable columns with visual feedback
- Status tracking and workflow management

✅ **Source Data Management**
- File type filtering
- Recent activity and version history tracking
- Sortable data grids

✅ **Navigation System**
- Collapsible sidebar navigation
- Multiple page views
- Responsive design

✅ **Modern UI Components**
- Glass morphism design
- Tailwind CSS styling
- Lucide React icons
- Radix UI components

## Prerequisites

Before running this application, make sure you have the following installed on your Mac:

- **Node.js** (version 18 or higher)
- **npm** (comes with Node.js)

### Installing Node.js on Mac

1. **Option 1: Download from official website**
   - Go to [nodejs.org](https://nodejs.org/)
   - Download the LTS version for macOS
   - Run the installer

2. **Option 2: Using Homebrew (recommended)**
   ```bash
   # Install Homebrew if you don't have it
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   
   # Install Node.js
   brew install node
   ```

3. **Verify installation**
   ```bash
   node --version
   npm --version
   ```

## Quick Start

### 1. Download and Extract
Download the package and extract it to your desired location.

### 2. Install Dependencies
```bash
cd marfi-complete-package-v3
npm install
```

### 3. Start Development Server
```bash
npm run dev
```

The application will automatically open in your browser at `http://localhost:3000`

## Available Scripts

- `npm run dev` - Start the development server
- `npm run build` - Build for production
- `npm run preview` - Preview the production build
- `npm run typecheck` - Run TypeScript type checking

## Project Structure

```
marfi-complete-package-v3/
├── src/
│   ├── components/           # All React components
│   │   ├── ui/              # Reusable UI components
│   │   ├── AllocationPage.tsx
│   │   ├── BuildReport.tsx
│   │   ├── Inbox.tsx
│   │   ├── Navigation.tsx
│   │   ├── SourceDataManagement.tsx
│   │   ├── ViewPublishedData.tsx
│   │   └── ViewSavedReports.tsx
│   ├── hooks/               # Custom React hooks
│   ├── lib/                 # Utility functions
│   ├── pages/               # Page components
│   ├── services/            # Service functions
│   ├── App.tsx              # Main app component
│   ├── main.tsx             # Entry point
│   └── global.css           # Global styles
├── data/                    # JSON data files
├── public/                  # Static assets
├── package.json
├── vite.config.ts
├── tailwind.config.ts
└── README.md
```

## Data Files

The application uses JSON files for data:
- `data/my-orders.json` - Orders data for Inbox
- `data/pending-actions.json` - Pending actions for approval
- `data/past-actions.json` - Historical actions
- `data/recent-activity.json` - Recent activity data
- `data/version-history.json` - Version history data

## Technologies Used

- **React 18** - Frontend framework
- **TypeScript** - Type safety
- **Vite** - Build tool and dev server
- **Tailwind CSS** - Utility-first CSS framework
- **Radix UI** - Accessible UI components
- **Lucide React** - Icon library
- **Recharts** - Chart library
- **Framer Motion** - Animation library

## Troubleshooting

### Common Issues

1. **Port already in use**
   ```bash
   # Kill process on port 3000
   lsof -ti:3000 | xargs kill -9
   ```

2. **Node modules issues**
   ```bash
   # Clear and reinstall
   rm -rf node_modules package-lock.json
   npm install
   ```

3. **TypeScript errors**
   ```bash
   # Run type checking
   npm run typecheck
   ```

### Getting Help

If you encounter any issues:
1. Check the browser console for errors
2. Ensure all dependencies are installed correctly
3. Make sure Node.js version is 18 or higher

## License

This is a private package for internal use only.
