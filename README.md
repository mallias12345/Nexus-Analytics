# ⚡ Nexus Analytics Dashboard

> **Real-time insights into your business performance**

A modern, animated dashboard built with React, Tailwind CSS, and Framer Motion. Features a beautiful gradient logo, smooth animations, and a clean Shadcn-inspired design.

![Nexus Analytics](https://img.shields.io/badge/Nexus-Analytics-blueviolet?style=for-the-badge&logo=react)
![Bun Compatible](https://img.shields.io/badge/Bun-Compatible-orange?style=for-the-badge&logo=bun)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-CSS-blue?style=for-the-badge&logo=tailwindcss)
![Framer Motion](https://img.shields.io/badge/Framer-Motion-pink?style=for-the-badge&logo=framer)

## 🌟 Features

- **🎨 Animated Logo**: Rotating gradient cube with lightning bolt
- **📱 Responsive Design**: Mobile-first with collapsible sidebar
- **✨ Smooth Animations**: Powered by Framer Motion
- **📊 Dashboard Components**: Stats cards, charts, and data tables
- **🎯 Modern UI**: Shadcn-inspired design with Tailwind CSS
- **⚡ Bun Compatible**: Optimized for Bun runtime
- **🔥 Interactive Elements**: Hover effects and micro-animations

## 🚀 Quick Start

### Prerequisites

- **Bun** installed on your system ([Install Bun](https://bun.sh/))
- **Node.js** 16+ (if using npm/yarn instead of Bun)

### One-Line Setup

```bash
mkdir nexus-analytics && cd nexus-analytics && bun init -y && bun add react react-dom framer-motion lucide-react && bun add -d vite @vitejs/plugin-react tailwindcss postcss autoprefixer && bunx tailwindcss init -p
```

### Step-by-Step Installation

1. **Create Project Directory**
```bash
mkdir nexus-analytics
cd nexus-analytics
```

2. **Initialize Project**
```bash
bun init -y
```

3. **Install Dependencies**
```bash
# Core dependencies
bun add react react-dom framer-motion lucide-react

# Development dependencies
bun add -d vite @vitejs/plugin-react tailwindcss postcss autoprefixer
```

4. **Initialize Tailwind CSS**
```bash
bunx tailwindcss init -p
```

## 📁 Project Structure

```
nexus-analytics/
├── public/
├── src/
│   ├── components/
│   │   └── Dashboard.jsx
│   ├── App.jsx
│   ├── main.jsx
│   └── index.css
├── index.html
├── package.json
├── tailwind.config.js
├── postcss.config.js
├── vite.config.js
└── README.md
```

## ⚙️ Configuration Files

### `tailwind.config.js`

```javascript
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {
      animation: {
        'gradient': 'gradient 8s linear infinite',
        'pulse-slow': 'pulse 3s cubic-bezier(0.4, 0, 0.6, 1) infinite',
      },
      backgroundImage: {
        'gradient-radial': 'radial-gradient(var(--tw-gradient-stops))',
      }
    },
  },
  plugins: [],
}
```

### `vite.config.js`

```javascript
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'

export default defineConfig({
  plugins: [react()],
  server: {
    port: 3000,
    open: true
  }
})
```

### `package.json` (scripts section)

```json
{
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "preview": "vite preview"
  }
}
```

## 📝 Source Files

### `index.html`

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='.9em' font-size='90'>⚡</text></svg>" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Nexus Analytics - Real-time Business Insights</title>
    <meta name="description" content="Modern analytics dashboard with real-time business insights and beautiful animations" />
  </head>
  <body>
    <div id="root"></div>
    <script type="module" src="/src/main.jsx"></script>
  </body>
</html>
```

### `src/index.css`

```css
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer base {
  * {
    @apply border-border;
  }
  body {
    @apply bg-background text-foreground;
    font-feature-settings: "rlig" 1, "calt" 1;
  }
}

/* Custom animations */
@keyframes gradient {
  0%, 100% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
}

/* Smooth scrollbar */
::-webkit-scrollbar {
  width: 6px;
}

::-webkit-scrollbar-track {
  @apply bg-gray-100;
}

::-webkit-scrollbar-thumb {
  @apply bg-gray-300 rounded-full;
}

::-webkit-scrollbar-thumb:hover {
  @apply bg-gray-400;
}
```

### `src/main.jsx`

```jsx
import React from 'react'
import ReactDOM from 'react-dom/client'
import App from './App.jsx'
import './index.css'

ReactDOM.createRoot(document.getElementById('root')).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
)
```

### `src/App.jsx`

```jsx
import Dashboard from './components/Dashboard'

function App() {
  return (
    <div className="min-h-screen bg-gray-50">
      <Dashboard />
    </div>
  )
}

export default App
```

### `src/components/Dashboard.jsx`

```jsx
// Copy the complete Dashboard component from the artifact
// This includes the Nexus Analytics logo, animations, and full dashboard UI
```

## 🏃‍♂️ Running the Application

### Development Mode

```bash
# Start development server
bun run dev
```

The application will be available at `http://localhost:3000`

### Production Build

```bash
# Build for production
bun run build

# Preview production build
bun run preview
```

## 🎨 Customization

### Logo Customization

```jsx
// Change gradient colors
className="w-8 h-8 bg-gradient-to-br from-blue-500 via-purple-500 to-pink-500"

// Change rotation speed
transition={{ duration: 8, repeat: Infinity, ease: "linear" }}

// Change brand name
<span className="text-lg font-bold">Your Brand</span>
```

### Color Scheme

```jsx
// Primary gradient
bg-gradient-to-r from-blue-600 via-purple-600 to-pink-600

// Background gradient
bg-gradient-to-br from-blue-50 via-purple-50 to-pink-50
```

## 📦 Deployment

### Vercel (Recommended)

```bash
npm i -g vercel
vercel
```

### Netlify

```bash
bun run build
# Upload dist/ folder to Netlify
```

### Other Static Hosts

Build the project and upload the `dist/` folder to any static hosting service.

## 🛠️ Advanced Features

### Environment Variables

Create `.env.local`:

```env
VITE_APP_NAME=Nexus Analytics
VITE_API_URL=https://api.nexus.dev
VITE_VERSION=1.0.0
```

### Adding Real Charts

```bash
bun add recharts
```

## 🐛 Troubleshooting

### Common Issues

**Tailwind styles not loading:**
```bash
bunx tailwindcss -i ./src/index.css -o ./dist/output.css --watch
```

**Bun compatibility issues:**
```bash
bun pm cache rm
rm -rf node_modules bun.lockb
bun install
```

## 📱 Screenshots

![Dashboard Overview](https://via.placeholder.com/800x400/6366f1/ffffff?text=Nexus+Analytics+Dashboard)

*Modern dashboard with animated logo and real-time stats*

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/AmazingFeature`
3. Commit your changes: `git commit -m 'Add some AmazingFeature'`
4. Push to the branch: `git push origin feature/AmazingFeature`
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [React](https://reactjs.org/) - UI Library
- [Tailwind CSS](https://tailwindcss.com/) - Styling
- [Framer Motion](https://www.framer.com/motion/) - Animations
- [Lucide React](https://lucide.dev/) - Icons
- [Bun](https://bun.sh/) - Runtime & Package Manager

## ⭐ Show your support

Give a ⭐️ if this project helped you!

---

**Built with ❤️ using React, Tailwind CSS, and Framer Motion**
