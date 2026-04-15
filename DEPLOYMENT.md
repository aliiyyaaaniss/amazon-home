# TechLuxe Affiliate Website - Deployment Guide

## 🚀 Project Overview

This is a premium Amazon affiliate website with a complete admin panel featuring:

- **Frontend**: React + Vite + Tailwind CSS
- **Animations**: Framer Motion
- **Security**: JWT Authentication + bcrypt
- **SEO**: Complete optimization with sitemap, robots.txt, meta tags
- **AI Generator**: Content generation with advanced prompts

## 📦 Features Implemented

### 1. Public Website
- ✅ Home page with animated hero section
- ✅ Products listing with search & filters
- ✅ Product detail pages with affiliate links
- ✅ Blog with articles
- ✅ About & Contact pages
- ✅ Dark/Light mode toggle
- ✅ Fully responsive design
- ✅ Smooth scroll animations
- ✅ Amazon affiliate integration

### 2. Admin Panel
- ✅ **Secure Login** (`/admin/login`)
  - Email/password authentication
  - Brute force protection (lockout after 5 attempts)
  - JWT token-based sessions
  - Secure password handling

- ✅ **Dashboard** (`/admin/dashboard`)
  - Statistics overview
  - Quick actions
  - Recent activity

- ✅ **Product Management** (`/admin/products`)
  - Add, edit, delete products
  - Search & filter
  - Category management

- ✅ **Blog Management** (`/admin/blog`)
  - Article creation/editing
  - Categories & tags
  - Draft management

- ✅ **AI Content Generator** (`/admin/ai-generator`)
  - SEO-optimized article generation
  - Product descriptions
  - Include Pros/Cons sections
  - FAQ generation
  - CTA buttons
  - SEO score calculation

- ✅ **Settings** (`/admin/settings`)
  - General site settings
  - Appearance (theme, colors)
  - Notifications
  - Security (2FA ready)
  - Affiliate configuration
  - API keys management

### 3. Security Features
- ✅ JWT authentication
- ✅ Protected routes
- ✅ Input validation
- ✅ XSS protection (via React)
- ✅ Secure token storage
- ✅ Session management
- ✅ Login attempt tracking

### 4. SEO Features
- ✅ Dynamic meta tags
- ✅ Sitemap generation
- ✅ Robots.txt
- ✅ Structured data (JSON-LD)
- ✅ SEO-friendly URLs
- ✅ Heading structure
- ✅ Meta descriptions

## 🔐 Default Admin Credentials

```
Email: admin@techluxe.com
Password: TechLuxe2026!
```

**Important**: Change these credentials in production!

## 📁 Project Structure

```
src/
├── components/
│   ├── ui/
│   │   └── Button.tsx         # UI Button component
│   ├── Header.tsx
│   ├── Footer.tsx
│   ├── AnimatedSection.tsx
│   └── ProductCard.tsx
├── context/
│   └── ThemeContext.tsx      # Dark/Light mode
├── data/
│   ├── products.ts           # Mock products
│   └── articles.ts            # Mock articles
├── pages/
│   ├── Home.tsx
│   ├── Products.tsx
│   ├── ProductDetail.tsx
│   ├── Blog.tsx
│   ├── BlogArticle.tsx
│   ├── About.tsx
│   └── admin/
│       ├── AdminLogin.tsx     # Secure login
│       ├── AdminDashboard.tsx  # Overview
│       ├── AdminProducts.tsx   # Product CRUD
│       ├── AdminProductForm.tsx
│       ├── AdminBlog.tsx      # Blog CRUD
│       ├── AdminArticleForm.tsx
│       ├── AdminSettings.tsx    # Site settings
│       └── AIGenerator.tsx    # AI content
├── utils/
│   ├── auth.ts               # Authentication
│   ├── seo.ts                # SEO utilities
│   └── cn.ts                # Class name utility
├── App.tsx                   # Main app with routes
└── main.tsx                  # Entry point
```

## 🚀 Deployment Instructions

### Vercel (Recommended)

1. **Push to GitHub**
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/yourusername/techluxe.git
git push -u origin main
```

2. **Deploy on Vercel**
- Go to [vercel.com](https://vercel.com)
- Click "New Project"
- Import your GitHub repository
- Configure:
  - Framework Preset: Vite
  - Build Command: `npm run build`
  - Output Directory: `dist`
- Click "Deploy"

### Cloudflare Pages

1. **Push to GitHub** (same as above)

2. **Deploy on Cloudflare**
- Go to [cloudflare.com](https://cloudflare.com)
- Go to Pages → Create new project
- Connect to GitHub
- Configure:
  - Build command: `npm run build`
  - Build output: `dist`
- Deploy

### Netlify

1. **Push to GitHub** (same as above)

2. **Deploy on Netlify**
- Go to [netlify.com](https://netlify.com)
- Click "Add new site" → "Import an existing project"
- Connect to GitHub
- Configure:
  - Base directory: `src`
  - Build command: `npm run build`
  - Publish directory: `dist`
- Deploy

## 🔧 Environment Variables

For production, create a `.env` file:

```env
REACT_APP_JWT_SECRET=your-secure-random-secret-key
REACT_APP_SITE_URL=https://yoursite.com
REACT_APP_AMAZON_TAG=your-amazon-tag
```

## 🛠️ Available Scripts

```bash
# Development
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## 📈 SEO Configuration

The site includes:

1. **Dynamic Meta Tags** - Each page has unique titles and descriptions
2. **Sitemap** - Automatically generated at `/sitemap.xml`
3. **Robots.txt** - Located at `/robots.txt`
4. **Structured Data** - JSON-LD for products and articles

## 🔒 Security Best Practices (Production)

1. **Change default admin credentials**
2. **Use strong JWT_SECRET**
3. **Enable HTTPS**
4. **Set secure headers**:
   ```
   Content-Security-Policy: default-src 'self'
   X-Frame-Options: DENY
   X-Content-Type-Options:-nosniff
   Referrer-Policy: strict-origin-when-cross-origin
   ```

## 📞 Support

For issues or questions:
- Email: admin@techluxe.com
- GitHub Issues: [Create new issue](https://github.com/yourusername/techluxe/issues)

---

**Version**: 2.0.0  
**Last Updated**: January 2026  
**Built with**: React + Vite + Tailwind CSS + Framer Motion