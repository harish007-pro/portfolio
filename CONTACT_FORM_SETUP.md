# Portfolio Contact Form Setup

## Your contact form currently doesn't send emails. Here's how to fix it:

### Option 1: Formspree (Recommended - Easiest)

1. Go to https://formspree.io
2. Sign up for free (50 submissions/month)
3. Create a new form
4. Copy your form endpoint URL (looks like: `https://formspree.io/f/YOUR_FORM_ID`)
5. In `index.html`, find the contact form and change:
   ```html
   <form class="contact-form" id="contact-form">
   ```
   To:
   ```html
   <form class="contact-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
6. Remove the JavaScript form handling in `script.js` (lines handling form submit)

### Option 2: Use mailto (Works immediately, but less professional)

Change the form to:
```html
<form class="contact-form" action="mailto:ajayharisharun@gmail.com" method="POST" enctype="text/plain">
```

This will open the user's email client.

### Option 3: Web3Forms (Free, unlimited)

1. Go to https://web3forms.com
2. Enter your email: ajayharisharun@gmail.com
3. Get your access key
4. Add to form:
   ```html
   <form action="https://api.web3forms.com/submit" method="POST">
       <input type="hidden" name="access_key" value="YOUR_ACCESS_KEY">
       <!-- rest of form fields -->
   </form>
   ```

## Current Status
- Portfolio is ready to deploy
- Just need to add one of the above solutions for contact form
- All other features are working perfectly

## Files in Your Portfolio
- index.html - Main page (needs form fix)
- index.css - Styling
- script.js - Interactivity  
- profile.png - Your photo
- project1.png, project2.png - Project images

## Next Steps
1. Fix contact form using one of the options above
2. Push changes to GitHub: `git add . && git commit -m "Add working contact form" && git push`
3. Deploy to Vercel (it will auto-update)
