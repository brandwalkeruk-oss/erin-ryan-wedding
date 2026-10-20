# Erin & Ryan wedding site: editable version

## What's in here
- `index.html`: the site. It looks the same as before, but the words now load from `content/`.
- `content/*.json`: all the text, photos, schedule, FAQs and RSVP settings.
- `admin/`: the editing screen (Decap CMS) at yoursite.netlify.app/admin
- `images/hero.jpg`: the header photo. It was embedded inside the old HTML file.
- `images/uploads/`: where photos uploaded through the editor are saved.

## One-time setup (about 15 minutes)
1. Create a new GitHub repository and upload the contents of this folder to it.
   If the repo's default branch isn't `main`, change `branch:` in `admin/config.yml` to match.
2. In Netlify, open the existing site and go to Site configuration → Build & deploy → Link repository.
   Pick the repo. Leave the build command empty and set the publish directory to `/`.
3. Site configuration → Identity → Enable Identity.
   - Registration: set to **Invite only**.
   - Services → Git Gateway → **Enable**.
4. Identity → Invite users → enter your client's email (and your own).
5. Your client clicks the email invite, sets a password, and lands on `/admin`.
   They can log in there at any time after that.

## How editing works
The client changes text in the editor and clicks **Publish**. The editor saves the change to GitHub,
and Netlify redeploys automatically, usually within about a minute.

Formatting the client can use in text boxes: `*italic*`, `**bold**`, and Enter for a new line.

## Before going live
- Fill in **8. RSVP → Email address RSVPs are sent to**.
  In the current live site this address is blank, so RSVP emails open with no recipient.
