# emilyhopefilm.com

The website for *Emily Hope*, a documentary by Ben Garvin and Lindsey Seavert (Tiny Window Pictures).

It is a plain static site: HTML files, one CSS file, and images. No frameworks, no build step, no database. GitHub Pages publishes whatever is in this repository about a minute after any change.

## How to make a change

**On github.com (no software needed):** open the file, click the pencil icon, edit, then click "Commit changes." The live site updates in about a minute.

**With an AI assistant (Claude, ChatGPT/Codex, etc.):** connect it to this GitHub repository and describe the change in plain English, e.g. "Add a screening on March 7, 2027 at 7 pm at the Riverview Theater in Minneapolis, tickets at [link]." Point it to this README first.

## Where things are

| Page | File |
|---|---|
| Home | `index.html` |
| The Film (synopsis, opening scene, statement, filmmakers, credits) | `film/index.html` |
| Screenings | `screenings/index.html` |
| Press & Festivals (loglines, specs, stills, contacts) | `press/index.html` |
| Support | `support/index.html` |
| Page-not-found | `404.html` |
| All colors, fonts and spacing | `css/style.css` (colors are at the top) |
| Web-sized photos | `img/stills/` (each in 800, 1600 and 2400 px wide) |
| Full-resolution press photos | `press/stills/` |
| Press photo zip | `press/emily-hope-press-stills.zip` |

The header and footer are repeated in every page. If you change a link, an email address or the footer text, change it in all six HTML files.

## Common tasks

**Add a screening.** In `screenings/index.html`, find the comment that starts `TO ADD A SCREENING`. Copy the block between `START` and `END`, paste it inside `<ul class="screenings">`, and edit the date, event, venue and link. Delete the "No public screenings are scheduled yet" item once there is a real screening. Soonest first.

**Add a festival selection or award.** In `screenings/index.html`, find the `FESTIVAL LAURELS` comment, remove the `<!--` and `-->` around it, and edit.

**Update specs (running time, aspect ratio, sound).** `press/index.html`, the table under "Specifications." Copy a `<tr>` row to add one.

**Change a photo caption.** Captions appear in `<figcaption>` tags. The same caption may appear on the Press page and on another page; search all files for the old text.

**Add or replace a photo.** Save three copies, 800, 1600 and 2400 pixels wide, in `img/stills/` using the naming pattern already there, and update the `<img>` tag. Add the original to `press/stills/` if it should be downloadable. Never alter photographs beyond resizing and cropping.

**Swap in the email signup form.** Each page with "Stay in touch" has a comment `EMAIL SIGNUP`. Replace the button under it with the embed code from Kit (or Buttondown).

## Rules for editors (people and AI)

- Keep it simple: no animation, carousels, pop-ups or trackers. The film is quiet; the site should be too.
- Every page keeps exactly one `<h1>`, a unique `<title>` and a unique `<meta name="description">`.
- Every image needs meaningful `alt` text.
- Photographs are journalism: resize or crop only. No retouching and no AI-generated or AI-altered images, ever.
- Use relative links (`../press/`), not `/press/`, except in `404.html`.
- When adding or removing a page, update `sitemap.xml`.
- Names: Emily Hope Hofher (on first reference), then Emily. Her husband is Rob Raub; her daughter is Ruby.

## Hosting

- Hosted free on GitHub Pages from the `main` branch.
- Domain `emilyhopefilm.com` is registered at GoDaddy; its DNS points to GitHub Pages.
- Donations go through fiscal sponsor FilmNorth: https://filmnorth.org/fiscally-sponsored-projects/emily-hope/
- Festival submissions: https://filmfreeway.com/projects/4390738
