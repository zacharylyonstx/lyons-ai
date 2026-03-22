# Lyons AI — Website & Outreach Kit

## Quick Deploy

### Netlify (Easiest)
1. Go to [app.netlify.com](https://app.netlify.com)
2. Drag the entire `lyons-ai/` folder onto the deploy area
3. Done. You'll get a URL like `random-name.netlify.app`
4. Add custom domain in Site Settings → Domain Management

### Vercel
```bash
npm i -g vercel
cd lyons-ai
vercel
```
Follow the prompts. Add custom domain in dashboard.

### GitHub Pages
1. Push this folder to a GitHub repo
2. Settings → Pages → Source: main branch, root folder
3. Your site is live at `username.github.io/repo-name`

## Custom Domain Setup

1. Buy a domain (Namecheap, Cloudflare, Google Domains)
   - Suggested: `lyonsai.com`, `lyons-ai.com`, `lyonsautomation.com`
2. In your hosting provider, add the custom domain
3. Update DNS records as instructed (usually a CNAME to your deploy URL)
4. SSL is automatic on Netlify/Vercel

## Contact Form Setup

The form currently logs to console. To make it functional:

### Option A: Netlify Forms (free, easiest)
Add `netlify` attribute to the form tag:
```html
<form class="contact-form" id="contactForm" netlify>
```
That's it. Submissions appear in your Netlify dashboard.

### Option B: Formspree (free tier: 50 submissions/month)
1. Sign up at [formspree.io](https://formspree.io)
2. Create a form, get your endpoint
3. Update the form action:
```html
<form class="contact-form" action="https://formspree.io/f/YOUR_ID" method="POST">
```

### Option C: EmailJS (sends directly to your email)
1. Sign up at [emailjs.com](https://emailjs.com)
2. Configure service + template
3. Add their SDK and update the submit handler

## Customization Checklist

- [ ] Replace `hello@lyonsai.com` with your real email
- [ ] Add real social media links in footer
- [ ] Update testimonials when you get real ones (placeholders are there)
- [ ] Add a real headshot in the About section
- [ ] Set up contact form backend (see above)
- [ ] Add Google Analytics or Plausible for tracking
- [ ] Buy and connect custom domain

## File Structure

```
lyons-ai/
├── index.html              # Full website (single file, no dependencies)
├── README.md               # This file
└── outreach/
    ├── cold-email-templates.md
    ├── linkedin-outreach.md
    ├── local-business-script.md
    ├── fiverr-gig-descriptions.md
    └── upwork-profile.md
```

## Tech Notes

- Pure HTML/CSS/JS — no build step, no frameworks, no dependencies
- Mobile responsive down to 320px
- Dark theme with amber/gold accents
- ~83KB total (loads instantly)
- Scroll animations, interactive demos, animated workflow
- SEO meta tags included
- Accessible (semantic HTML, aria labels, keyboard navigation)
