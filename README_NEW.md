# 🌟 My Portfolio Website

A modern, responsive portfolio website built with Vue 3, TypeScript, and Tailwind CSS v4, featuring interactive particles background and dark mode support.

## ✨ Features

- **🎨 Modern Design**: Clean, professional layout with glassmorphism effects
- **🌙 Dark/Light Mode**: Seamless theme switching with automatic preference detection
- **📱 Fully Responsive**: Optimized for all devices from mobile to desktop
- **🎯 Interactive Navigation**: Smooth scrolling with active section highlighting
- **✨ Particles Background**: Beautiful animated particles that adapt to theme
- **⚡ Performance Optimized**: Fast loading with Vite build tool
- **🎭 Smooth Animations**: Subtle transitions and hover effects
- **♿ Accessible**: Built with accessibility best practices

## 🚀 Tech Stack

- **Frontend**: Vue 3 (Composition API)
- **Language**: TypeScript
- **Styling**: Tailwind CSS v4
- **Build Tool**: Vite
- **Icons**: Lucide Vue
- **Particles**: particles.js
- **Dark Mode**: VueUse
- **Deployment**: Ready for Vercel/Netlify

## 📦 Installation

```bash
# Clone the repository
git clone <your-repo-url>
cd my-resume

# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## 🎯 Project Structure

```
src/
├── components/          # Reusable Vue components
│   ├── CustomParticles.vue
│   ├── Nav.vue
│   ├── Main.vue
│   ├── About.vue
│   ├── Experience.vue
│   ├── Project.vue
│   └── Contact.vue
├── views/              # Page components
│   └── HomeView.vue
├── assets/             # Static assets
│   └── style.css
└── main.ts            # App entry point
```

## 🎨 Customization

### Colors & Themes
Edit `src/assets/style.css` to modify:
- Navigation colors and animations
- Dark mode color scheme
- Project tag colors

### Content
Update the following components:
- `Main.vue` - Personal info and resume link
- `About.vue` - About section content
- `Experience.vue` - Work experience
- `Project.vue` - Portfolio projects
- `Contact.vue` - Contact information

### Particles
Customize particles in `CustomParticles.vue`:
- Particle count and colors
- Animation speed and behavior
- Interactive effects

## 📱 Responsive Design

- **Mobile (< 640px)**: Single column layout, compact navigation
- **Tablet (640px - 1024px)**: Optimized spacing and typography
- **Desktop (1024px+)**: Two-column layout with fixed sidebar

## 🌙 Dark Mode

Automatic theme detection with manual toggle:
- System preference detection
- Persistent user choice
- Smooth transitions
- Particles color adaptation

## 🚀 Deployment

### GitHub Pages (Automatic with GitHub Actions)
This project is configured for automatic deployment to GitHub Pages:

1. **Push to GitHub**:
   ```bash
   git add .
   git commit -m "Add deployment workflow"
   git push origin main
   ```

2. **Enable GitHub Pages**:
   - Go to your repository settings
   - Navigate to "Pages" section
   - Source: "GitHub Actions"
   - The workflow will automatically deploy your site

3. **Your site will be available at**: `https://yourusername.github.io/resume`

The deployment workflow (`.github/workflows/deploy.yml`) automatically:
- Installs dependencies
- Builds the project
- Deploys to GitHub Pages
- Runs on every push to `main` branch

### Alternative Deployments

#### Vercel
1. Push to GitHub
2. Connect repository to Vercel
3. Deploy automatically

#### Netlify
1. Push to GitHub
2. Connect repository to Netlify
3. Build command: `npm run build`
4. Publish directory: `dist`

## 📄 License

MIT License - Feel free to use this template for your own portfolio!

## 👤 Author

**Werasak Mayer**
- Frontend Developer
- 📧 Email: werasak.mayer0@gmail.com
- 💼 LinkedIn: [Werasak Mayer](https://www.linkedin.com/in/werasak-mayer-3348a4287/)
- 🐱 GitHub: [weerr12](https://github.com/weerr12)

---

⭐ If you found this helpful, please give it a star!
