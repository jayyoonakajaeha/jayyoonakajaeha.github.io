# Jaeha Yoon Portfolio Website

A modern, responsive portfolio website showcasing research experience, projects, and achievements in AI and Machine Learning.

## 🚀 Quick Start

### Option 1: Deploy on GitHub Pages (Recommended - Completely Free)

1. **Create a GitHub Repository**
   ```bash
   # Create a new repository on GitHub named: [your-username].github.io
   # Or create any repository name for a project page
   ```

2. **Upload Files**
   - Save the HTML file as `index.html`
   - Push to your repository:
   ```bash
   git init
   git add index.html
   git commit -m "Initial portfolio commit"
   git branch -M main
   git remote add origin https://github.com/[your-username]/[repository-name].git
   git push -u origin main
   ```

3. **Enable GitHub Pages**
   - Go to repository Settings → Pages
   - Source: Deploy from a branch
   - Branch: main, folder: / (root)
   - Save

4. **Access Your Site**
   - For user page: `https://[your-username].github.io`
   - For project page: `https://[your-username].github.io/[repository-name]`

### Option 2: Deploy on Netlify (Free Tier Available)

1. **Prepare Your File**
   - Save the HTML as `index.html`
   - Create a folder and place the file inside

2. **Deploy via Drag & Drop**
   - Go to [Netlify Drop](https://app.netlify.com/drop)
   - Drag your folder containing `index.html`
   - Your site will be instantly deployed!

3. **Custom Domain (Optional)**
   - Create a free Netlify account
   - Claim your site
   - Add custom domain in Site settings

### Option 3: Deploy on Vercel (Free Tier Available)

1. **Create a GitHub Repository**
   - Push your `index.html` to a GitHub repository

2. **Connect to Vercel**
   - Go to [Vercel](https://vercel.com)
   - Sign up/Login with GitHub
   - Import your repository
   - Deploy automatically

3. **Access Your Site**
   - Vercel provides a free `.vercel.app` domain
   - Custom domains available

### Option 4: Deploy on Render (Free Static Site Hosting)

1. **Prepare Your Repository**
   - Create a GitHub/GitLab repository
   - Push your `index.html` file

2. **Create Render Static Site**
   ```yaml
   # Create a render.yaml file (optional)
   services:
     - type: web
       name: portfolio-jaehayoon
       env: static
       buildCommand: "" # No build needed for static HTML
       staticPublishPath: .
       headers:
         - path: /*
           name: Cache-Control
           value: public, max-age=31536000
   ```

3. **Deploy on Render**
   - Go to [Render Dashboard](https://dashboard.render.com)
   - New → Static Site
   - Connect your GitHub repository
   - Name: `portfolio-jaehayoon`
   - Build Command: (leave empty)
   - Publish Directory: `.`
   - Click "Create Static Site"

4. **Access Your Site**
   - URL: `https://portfolio-jaehayoon.onrender.com`
   - Custom domains available in Settings

### Option 5: Deploy on Cloudflare Pages (Free)

1. **Using Direct Upload**
   ```bash
   # Install Wrangler CLI
   npm install -g wrangler
   
   # Login to Cloudflare
   wrangler login
   
   # Deploy
   wrangler pages publish . --project-name=portfolio
   ```

2. **Using Git Integration**
   - Push to GitHub
   - Go to [Cloudflare Pages](https://pages.cloudflare.com)
   - Connect repository
   - Deploy automatically

## 📁 File Structure

```
portfolio/
├── index.html          # Main portfolio file
├── README.md          # This file
└── render.yaml        # (Optional) Render configuration
```

## 🛠️ Customization

### Update Content
1. **Personal Information**
   - Edit name, email, phone in the Hero section
   - Update social media links (GitHub, LinkedIn, Notion)

2. **Research Experience**
   - Modify research items in the Research section
   - Add new research projects following the existing structure

3. **Projects**
   - Update project cards with your projects
   - Modify tags to match your tech stack

4. **Skills**
   - Edit skill categories and items
   - Add or remove skills as needed

5. **Awards**
   - Update the awards timeline
   - Add new achievements

### Styling Customization
```css
/* Change primary color */
:root {
    --primary-color: #2563eb; /* Change this hex code */
}
```

## 🌐 Custom Domain Setup

### For GitHub Pages
1. Create a `CNAME` file in your repository
2. Add your domain: `www.yourdomain.com`
3. Configure DNS:
   - A Record: `185.199.108.153`
   - A Record: `185.199.109.153`
   - A Record: `185.199.110.153`
   - A Record: `185.199.111.153`
   - CNAME: `www` → `[username].github.io`

### For Other Platforms
- Follow platform-specific documentation for custom domain setup
- Most platforms provide free SSL certificates

## 🔄 Continuous Updates

### Using GitHub Actions (for GitHub Pages)
Create `.github/workflows/deploy.yml`:
```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Deploy to GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./
```

## 📱 Mobile Optimization

The portfolio is fully responsive and works on:
- Desktop (1920px+)
- Laptop (1024px - 1919px)
- Tablet (768px - 1023px)
- Mobile (320px - 767px)

## 🔧 Troubleshooting

### Site Not Loading
- Check if `index.html` is in the root directory
- Verify GitHub Pages is enabled
- Wait 5-10 minutes for initial deployment

### CSS Not Loading
- Ensure all styles are in the `<style>` tag
- Check for syntax errors in CSS

### Mobile Menu Not Working
- JavaScript must be enabled
- Check browser console for errors

## 📊 Performance Optimization

The site is optimized for:
- **Fast Loading**: Single HTML file, no external dependencies
- **SEO**: Proper meta tags and semantic HTML
- **Accessibility**: ARIA labels and semantic structure
- **Performance**: Minimal JavaScript, CSS animations use GPU

## 🤝 Contributing

Feel free to fork this repository and customize it for your own portfolio!

## 📄 License

This portfolio template is free to use and modify for personal and commercial purposes.

## 🙋‍♂️ Support

For questions or issues:
- Email: 613jay@sju.ac.kr
- GitHub: [jayyoonakajaeha](https://github.com/jayyoonakajaeha)

---

**Last Updated**: September 2025
**Version**: 1.0.0
