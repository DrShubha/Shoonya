# 🚀 Deployment Guide - Shoonya Holistics

## Local Testing (Your Current Setup)

Your website is currently running on:
```
http://localhost:8000
```

### Start/Stop Server

**Start Server**
```bash
cd /workspaces/Shoonya
python3 -m http.server 8000
```

**Stop Server**
```bash
# Press Ctrl+C in terminal, or:
pkill -f "http.server 8000"
```

---

## Free Deployment Options

### 1. GitHub Pages (Recommended)

**Why GitHub Pages?**
- ✅ Free forever
- ✅ Custom domain support
- ✅ Automatic deployment from git
- ✅ https included
- ✅ No server needed
- ✅ Fast CDN

**Steps:**

1. **Create GitHub Repository**
   - Go to https://github.com/new
   - Repository name: `shoonya-holistics` (or any name)
   - Make it public
   - Create repository

2. **Push Your Code**
   ```bash
   cd /workspaces/Shoonya
   
   # Initialize git if not done
   git init
   git add .
   git commit -m "Initial commit: Shoonya Holistics website"
   
   # Add remote (replace YOUR_USERNAME and REPO_NAME)
   git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git
   git branch -M main
   git push -u origin main
   ```

3. **Enable GitHub Pages**
   - Go to repository settings
   - Scroll to "Pages" section
   - Source: Select `main` branch
   - Save
   - Wait 2-3 minutes for deployment

4. **Access Your Site**
   - URL: `https://YOUR_USERNAME.github.io/REPO_NAME`
   - Example: `https://drshubha.github.io/shoonya-holistics`

5. **Custom Domain (Optional)**
   - Go to repository settings → Pages
   - Enter your custom domain
   - Update DNS records at your domain provider
   - GitHub provides instructions

---

### 2. Netlify (Simple Drag & Drop)

**Why Netlify?**
- ✅ Free tier sufficient
- ✅ Easiest deployment
- ✅ Auto-deployment from git
- ✅ Form handling available
- ✅ Fast global CDN
- ✅ Great UI

**Option A: Drag & Drop**
1. Go to https://app.netlify.com
2. Drag and drop your project folder
3. Done! Your site is live

**Option B: Git Integration**
1. Sign up at https://netlify.com
2. Click "New site from Git"
3. Connect GitHub repository
4. Select `main` branch
5. Click "Deploy"
6. Site goes live automatically

**Your URL**: `your-site-name.netlify.app`

**Form Handling**: (Optional)
```html
<form name="contact" netlify>
    <!-- Your form fields -->
</form>
```

---

### 3. Vercel (Optimized for Speed)

**Why Vercel?**
- ✅ Extremely fast
- ✅ Free tier
- ✅ Git integration
- ✅ Analytics included
- ✅ Edge functions available
- ✅ Image optimization

**Steps:**
1. Go to https://vercel.com
2. Click "Import Project"
3. Select GitHub repository
4. Click "Import"
5. Click "Deploy"
6. Live instantly!

**Your URL**: `shoonya-holistics.vercel.app`

---

### 4. Cloudflare Pages

**Why Cloudflare?**
- ✅ Free and fast
- ✅ Global CDN
- ✅ Security features included
- ✅ Analytics free
- ✅ Zero config deployment

**Steps:**
1. Go to https://pages.cloudflare.com
2. Connect GitHub account
3. Select repository
4. Automatic deployment configured
5. Done!

**Your URL**: `shoonya-holistics.pages.dev`

---

### 5. Firebase Hosting

**Why Firebase?**
- ✅ Google-backed
- ✅ Free tier with generous limits
- ✅ CLI deployment
- ✅ Rollback capability
- ✅ Preview URLs

**Steps:**
```bash
# Install Firebase CLI
npm install -g firebase-tools

# Login to Firebase
firebase login

# Initialize Firebase project
firebase init hosting

# Build and deploy
firebase deploy
```

---

## Paid Hosting Options (If Needed)

### 1. AWS (Scalable)
- **Service**: S3 + CloudFront
- **Cost**: Very low (~$1-5/month)
- **Perfect for**: High traffic sites
- **Setup**: More complex

### 2. Bluehost/SiteGround (WordPress-style)
- **Cost**: $2-10/month
- **Includes**: Email hosting, backups
- **Perfect for**: Non-technical users

### 3. DigitalOcean (Professional)
- **Cost**: $5+/month
- **Includes**: Full server control
- **Perfect for**: Developers

---

## Custom Domain Setup

### How to Connect Custom Domain

**Example Domain**: `shoonya-holistics.com`

#### Step 1: Purchase Domain
- GoDaddy, Namecheap, Google Domains, etc.
- Cost: $10-15/year typically

#### Step 2: Update DNS Records
Depends on your hosting provider:

**GitHub Pages**
```
Add CNAME file: CNAME
Content: your-username.github.io

DNS Records:
- @ A record: 185.199.108.153
- @ A record: 185.199.109.153
- @ A record: 185.199.110.153
- @ A record: 185.199.111.153
```

**Netlify**
```
DNS Records:
- @ A record: 75.2.60.5
```

**Vercel**
```
DNS Records (follow Vercel instructions)
- ALIAS/ANAME: cname.vercel-dns.com
```

#### Step 3: Verify & Wait
- Takes 24-48 hours for DNS propagation
- Check status with: `nslookup yourdomain.com`

---

## Continuous Deployment Workflow

### Automatic Updates
Once deployed to GitHub, any changes automatically deploy:

```bash
# Make changes locally
nano index.html

# Commit and push
git add .
git commit -m "Update services section"
git push origin main

# Site automatically updates within seconds!
```

---

## Pre-Deployment Checklist

- [ ] All files created and tested locally
- [ ] Website renders correctly in all browsers
- [ ] Mobile responsiveness verified
- [ ] Contact form tested
- [ ] All links working
- [ ] Images/SVGs displaying correctly
- [ ] Animations smooth and performant
- [ ] No console errors (F12)
- [ ] Site loads in under 3 seconds
- [ ] Favicon displaying
- [ ] Meta tags and title correct
- [ ] Email address verified (shubha.pmishra@gmail.com)

---

## Post-Deployment

### Analytics Setup (Optional)

**Google Analytics**
```html
<!-- Add to index.html <head> -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_ID');
</script>
```

**Cloudflare Analytics** (Free with Cloudflare)
- Automatically tracks if using Cloudflare

---

### Monitoring & Maintenance

**Uptime Monitoring**
- Use UptimeRobot.com (free)
- Get alerts if site goes down
- Check status from anywhere

**Performance Monitoring**
- Google PageSpeed Insights
- GTmetrix
- WebPageTest

**Security**
- Enable HTTPS (all providers include this)
- Regular backups (automatic with most providers)
- Update contact email if needed

---

## Environment-Specific Setup

### Local Development
```bash
cd /workspaces/Shoonya
python3 -m http.server 8000
# Visit: http://localhost:8000
```

### Staging (Before Live)
Use a subdomain:
```
staging.shoonya-holistics.com
or
preview.shoonya-holistics.com
```

### Production (Live)
```
shoonya-holistics.com
or custom domain
```

---

## Rollback Procedure

If something breaks after deployment:

**GitHub Pages**
```bash
git revert HEAD  # Undo last commit
git push origin main
```

**Netlify**
- Netlify Dashboard → Deploys → Click previous version → Publish

**Vercel**
- Vercel Dashboard → Deployments → Click previous → Promote to Production

---

## File Structure for Deployment

**Everything is included:**
```
Shoonya/
├── index.html          # ✅ Needed
├── styles.css          # ✅ Needed
├── script.js           # ✅ Needed
├── README.md           # ✅ Recommended (shows on GitHub)
├── QUICKSTART.md       # Optional (documentation)
├── STYLE_GUIDE.md      # Optional (documentation)
└── .git/               # Auto-managed by git
```

**What to deploy**: All `.html`, `.css`, and `.js` files only

---

## Performance Optimization Tips

### Reduce Load Time
1. **Minify CSS & JavaScript** (Optional)
   ```bash
   # Using online tools like minifier.org
   ```

2. **Enable Gzip Compression** (Automatic on most hosts)

3. **Leverage Browser Caching** (Automatic on CDNs)

4. **Reduce Image Sizes** (Already using SVG - optimized!)

### Monitor Performance
```bash
# Test locally
curl -o /dev/null -s -w "%{time_total}\n" http://localhost:8000
```

---

## SSL/HTTPS Setup

**Automatic (Recommended)**
- GitHub Pages: ✅ Automatic HTTPS
- Netlify: ✅ Automatic HTTPS
- Vercel: ✅ Automatic HTTPS
- Cloudflare Pages: ✅ Automatic HTTPS
- Firebase: ✅ Automatic HTTPS

**No additional configuration needed!**

---

## Troubleshooting Deployment

### Site Shows 404
- Check files are in correct directory
- Ensure index.html exists in root
- Clear browser cache
- Wait 5 minutes for propagation

### Styles/Scripts Don't Load
- Verify file paths are correct
- Check file names match exactly
- Clear browser cache (Ctrl+Shift+Delete)
- Hard refresh page (Ctrl+Shift+R)

### Contact Form Doesn't Work
- Verify email address is correct
- Test mailto links manually
- Check browser console for errors

### Site Is Slow
- Check Lighthouse score
- Verify no large unoptimized images
- Check network waterfall
- Consider upgrading hosting

---

## Recommended Deployment Path

### For Beginners
1. **Start**: Netlify (easiest)
2. Drag & drop your project folder
3. Get instant free domain
4. Done in 2 minutes!

### For Git Users
1. **Start**: GitHub Pages
2. Push to GitHub
3. Enable Pages in settings
4. Automatic deployment
5. Free forever

### For Best Performance
1. **Use**: Vercel or Cloudflare Pages
2. Connect GitHub
3. Auto-deploys on push
4. Fastest CDN worldwide

---

## Domain Services Comparison

| Service | Cost | Features |
|---------|------|----------|
| Namecheap | $8.88/yr | Cheap, basic features |
| GoDaddy | $12.99/yr | Expensive, lots of upsells |
| Google Domains | $12/yr | Clean UI, good support |
| Cloudflare | $10/yr | Includes DNS + protection |

---

## Final Verification

Once live:

1. **Visit your domain**
   - Check if site loads
   - Verify all sections visible

2. **Test Responsiveness**
   - Desktop: Full width
   - Tablet: Optimized layout
   - Mobile: Single column

3. **Check Functionality**
   - Navigate all links
   - Test form submission
   - Verify animations smooth

4. **Browser Testing**
   - Chrome ✅
   - Firefox ✅
   - Safari ✅
   - Edge ✅

5. **Mobile Testing**
   - iPhone Safari ✅
   - Android Chrome ✅
   - Touch interactions ✅

---

## Support & Help

### Common Hosting Support
- GitHub Pages: docs.github.com/pages
- Netlify: docs.netlify.com
- Vercel: vercel.com/docs
- Cloudflare: developers.cloudflare.com

### Need Help?
- Email: shubha.pmishra@gmail.com
- Check README.md for more info

---

**Your website is production-ready! 🎉**

Pick your deployment method and launch! All options are free and take less than 5 minutes.

*Recommended: Start with Netlify for simplicity or GitHub Pages for automation.*
