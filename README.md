# 🎨 Personal Portfolio Website

A modern, responsive personal portfolio website built with **React**, **Vite**, and **Tailwind CSS**. Showcase your projects, skills, and experience with an interactive contact form powered by EmailJS.

![React](https://img.shields.io/badge/React-19.2.4-blue?logo=react)
![Vite](https://img.shields.io/badge/Vite-8.0.1-purple?logo=vite)
![Tailwind CSS](https://img.shields.io/badge/TailwindCSS-4.2.2-06B6D4?logo=tailwindcss)
![JavaScript](https://img.shields.io/badge/JavaScript-98.4%25-yellow?logo=javascript)
![License](https://img.shields.io/badge/License-MIT-green)

## ✨ Features

- 📱 **Fully Responsive Design** - Works seamlessly on desktop, tablet, and mobile devices
- ⚡ **Fast & Optimized** - Built with Vite for lightning-fast development and production builds
- 🎨 **Modern UI** - Styled with Tailwind CSS for a clean, contemporary look
- 📧 **Contact Form** - Integrated EmailJS for direct email notifications
- 🎯 **Interactive Elements** - Smooth animations and transitions using Lucide React icons
- 🔧 **Developer Friendly** - ESLint configuration for code quality
- 🌙 **Hot Module Replacement (HMR)** - Real-time development experience

## 🚀 Quick Start

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/it22318466/Portfolio_Web_Personal.git
   cd Portfolio_Web_Personal
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env
   ```
   Then add your EmailJS credentials to the `.env` file

4. **Start the development server**
   ```bash
   npm run dev
   ```
   The portfolio will open in your browser at `http://localhost:5173`

## 📦 Available Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start the development server with HMR |
| `npm run build` | Build the project for production |
| `npm run preview` | Preview the production build locally |
| `npm run lint` | Run ESLint to check code quality |

## 🛠️ Tech Stack

### Core
- **React** 19.2.4 - JavaScript library for building user interfaces
- **Vite** 8.0.1 - Next generation frontend build tool
- **Tailwind CSS** 4.2.2 - Utility-first CSS framework

### Libraries
- **@emailjs/browser** 4.4.1 - Client-side email service for contact forms
- **Lucide React** 1.7.0 - Beautiful SVG icon library
- **React Icons** 5.6.0 - Popular icon sets for React

### Development Tools
- **ESLint** 9.39.4 - JavaScript linter for code quality
- **TypeScript** Support via @types packages
- **Vite React Plugin** 6.0.1 - Fast refresh support

## 📧 EmailJS Setup

To enable the contact form functionality, follow these detailed steps:

### 1. Create an EmailJS Account
- Visit [EmailJS](https://www.emailjs.com/)
- Sign up for a free account (200 emails/month)
- Verify your email address

### 2. Configure Email Service
- Go to **Email Services** in your EmailJS dashboard
- Click **Add New Service** and select your email provider (Gmail, Outlook, etc.)
- Follow the authentication steps to connect your email

### 3. Create Email Template
- Navigate to **Email Templates**
- Click **Create New Template**
- Use the variables: `{{from_name}}`, `{{from_email}}`, `{{message}}`, `{{to_email}}`
- Save your template

### 4. Get Your Credentials
- **Public Key**: Account → General
- **Service ID**: Email Services page
- **Template ID**: Email Templates page

### 5. Update .env File
```env
VITE_EMAILJS_PUBLIC_KEY=your_public_key_here
VITE_EMAILJS_SERVICE_ID=your_service_id_here
VITE_EMAILJS_TEMPLATE_ID=your_template_id_here
```

> ⚠️ **Security Note**: Never commit your `.env` file. It's already in `.gitignore`.

For detailed setup instructions, see [EMAILJS_SETUP.md](./EMAILJS_SETUP.md)

## 📂 Project Structure

```
Portfolio_Web_Personal/
├── src/                      # React components and logic
├── public/                   # Static assets
├── dist/                     # Production build output
├── index.html               # HTML entry point
├── package.json             # Project dependencies
├── vite.config.js          # Vite configuration
├── tailwind.config.js      # Tailwind CSS configuration
├── eslint.config.js        # ESLint rules
├── .env.example            # Environment variables template
├── EMAILJS_SETUP.md        # EmailJS integration guide
└── README.md               # This file
```

## 🎯 Getting Started with Development

### File Structure Best Practices

Organize your React components like this:

```
src/
├── components/
│   ├── Header.jsx
│   ├── Hero.jsx
│   ├── About.jsx
│   ├── Projects.jsx
│   ├── Contact.jsx
│   └── Footer.jsx
├── styles/
│   └── index.css
└── App.jsx
```

### Creating Components

Example component structure:

```jsx
import React from 'react';

export default function MyComponent() {
  return (
    <div className="flex items-center justify-center">
      <h1 className="text-3xl font-bold">Welcome</h1>
    </div>
  );
}
```

## 🎨 Customization

### Tailwind CSS
Customize the design in `tailwind.config.js`:
- Change color scheme
- Modify spacing and typography
- Add custom utilities

### React Components
- Create new sections in the `src/components/` directory
- Import and use them in `src/App.jsx`
- Leverage Lucide React icons and React Icons for visual elements

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## 🐛 Troubleshooting

### Contact Form Not Working
- Verify `.env` file has correct EmailJS credentials
- Check EmailJS dashboard for error logs
- Ensure email service is active in EmailJS

### Build Errors
- Delete `node_modules` and `package-lock.json`
- Run `npm install` again
- Clear Vite cache: `rm -rf dist`

### Styles Not Appearing
- Restart the dev server
- Clear browser cache (Ctrl+Shift+Delete or Cmd+Shift+Delete)
- Verify Tailwind CSS is properly imported in your main CSS file

## 🚀 Deployment

### Deploy to Vercel (Recommended)
1. Push your code to GitHub
2. Connect your repo to [Vercel](https://vercel.com)
3. Vercel auto-deploys on every push
4. Add environment variables in Vercel dashboard

### Deploy to Netlify
1. Build: `npm run build`
2. Connect your GitHub repo to [Netlify](https://netlify.com)
3. Set build command: `npm run build`
4. Set publish directory: `dist`

### Deploy to GitHub Pages
```bash
npm run build
# Commit and push dist folder to gh-pages branch
```

## 📊 Performance Metrics

- **Language Composition**: JavaScript (98.4%), CSS (1.4%), HTML (0.2%)
- **Build Time**: < 1 second with Vite
- **Bundle Size**: Optimized with tree-shaking and code splitting

## 📝 License

This project is open source. Feel free to use it as a template for your own portfolio.

## 🤝 Contributing

Suggestions and improvements are welcome! Feel free to:
- Report issues
- Submit pull requests
- Share feedback

## 👨‍💻 Author

**it22318466** - [GitHub Profile](https://github.com/it22318466)

## 📚 Additional Resources

- [React Documentation](https://react.dev)
- [Vite Guide](https://vitejs.dev)
- [Tailwind CSS Docs](https://tailwindcss.com)
- [EmailJS Documentation](https://www.emailjs.com/docs)
- [Lucide Icons](https://lucide.dev)

## 💡 Tips for Success

1. **Keep it Updated** - Regularly update dependencies for security and performance
2. **Test Responsively** - Always test on different screen sizes
3. **Optimize Images** - Compress images before adding to portfolio
4. **SEO Friendly** - Add meta tags and descriptive content
5. **Mobile First** - Design for mobile, then enhance for larger screens

---

**Built with ❤️ using React, Vite, and Tailwind CSS**

⭐ If you found this template helpful, please consider giving it a star!
