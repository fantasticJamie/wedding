# Ibiza Wedding Website

A clean, modern static website for your Ibiza celebration with RSVP tracking via Formspree.

## What's Included

- **index.html** - Homepage with welcome and quick info
- **schedule.html** - Day-by-day itinerary (pre-wedding, celebration day, Sunday funday)
- **travel.html** - Travel and accommodation information
- **rsvp.html** - RSVP form with Formspree integration
- **styles.css** - Complete styling (responsive design)

## Setup Instructions

### 1. Upload Your Files

1. Upload all HTML files, styles.css, and the **images** folder to your web server
2. Make sure the images folder is in the same directory as your HTML files
3. The hero photo (hero-photo.jpg) should be in the images folder

### 2. Formspree Setup (for RSVP tracking)

1. Go to [formspree.io](https://formspree.io) and create a free account
2. Create a new form project
3. Copy your form ID (looks like: `abc123def`)
4. In `rsvp.html`, find this line:
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
5. Replace `YOUR_FORM_ID` with your actual form ID

### 2. Customize Content

Search for and replace these placeholders throughout the files:

- `[your email]` - Your contact email
- `Date TBC` - Add your actual dates
- `[your month]` / `[add weather info]` - In travel.html, add weather details

### 3. Optional: Add Meal Choices Later

When you're ready to add meal selection (after deciding between Passion/Romance menus):

1. Open `rsvp.html`
2. Find the commented-out meal choice section (around line 70)
3. Uncomment that section by removing `<!--` and `-->`
4. Update the meal options to match your menu choices

Example:
```html
<div class="form-group" id="mealChoiceGroup">
    <label>Meal Preferences</label>
    <small>Please select a meal option for each guest</small>
    <textarea id="mealChoice" name="mealChoice" rows="3" 
              placeholder="Guest 1: Passion Menu (€165)
Guest 2: Romance Menu (€190)
Any dietary requirements?"></textarea>
</div>
```

### 4. Hosting

Since you already know how to host:

1. Upload all files to your web server
2. Make sure all files are in the same directory
3. Set `index.html` as your default page
4. Test the site and RSVP form

### 5. Testing the RSVP Form

After setting up Formspree:

1. Submit a test RSVP through your website
2. Check your Formspree dashboard to see the submission
3. Formspree will email you when someone RSVPs (you can configure email settings)
4. You can export all responses as CSV from Formspree dashboard

## How RSVP Tracking Works

- Guest fills out form on your website
- Form submits to Formspree
- You receive email notification
- All responses stored in Formspree dashboard
- Export to spreadsheet anytime for tracking

## Features

✅ Fully responsive (works on mobile, tablet, desktop)
✅ Clean, modern design
✅ No database needed
✅ RSVP tracking via Formspree (free tier allows 50 submissions/month - more than enough)
✅ Easy to customize
✅ Optional meal choice field (add when ready)
✅ Handles dietary requirements
✅ Guest count tracking

## File Structure

```
wedding-site/
├── index.html          # Homepage (with your photo!)
├── schedule.html       # Full weekend schedule
├── travel.html         # Travel & accommodation info
├── rsvp.html          # RSVP form
├── styles.css         # All styling
├── images/
│   └── hero-photo.jpg # Your uploaded photo
└── README.md          # This file
```

## Need to Update?

Just edit the HTML files directly - all content is clearly marked and easy to find.

## Questions?

The form currently captures:
- Guest name(s)
- Email
- Attendance (yes/no)
- Number of guests
- Dietary requirements
- Optional message

You can add/remove fields as needed - just add more `<input>` or `<select>` elements in the form.
