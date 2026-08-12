# Ashar Shahid — Portfolio

A personal portfolio site built with React, Vite, Tailwind CSS, and Framer
Motion. All content (experience, projects, skills, education, contact
details) is sourced directly from the uploaded resume — nothing is invented.

## Run it locally

```bash
npm install
npm run dev
```

Open the printed `localhost` URL in your browser.

## Build for production

```bash
npm run build
```

This outputs a static site to `dist/`. You can preview the production build
locally with:

```bash
npm run preview
```

## Deploy to Vercel (free, no backend, no database)

1. **Create a GitHub repository** and push this project to it:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
2. **Go to [vercel.com](https://vercel.com)** and sign in with your GitHub
   account (no credit card required for hobby/personal projects).
3. Click **"Add New Project"** and select the repository you just pushed.
4. Vercel auto-detects this as a **Vite** project — the default build
   settings (`npm run build`, output directory `dist`) are already correct.
   Just click **Deploy**.
5. In a minute or two you'll get a live public URL like
   `https://your-project-name.vercel.app`.

From then on, every `git push` to `main` triggers an automatic redeploy —
including any new certificates or resume updates.

## Adding certificates

No certificate files were provided when this site was built, so the
Certifications section currently shows an empty state. To add certificates:

1. Drop the certificate image or PDF into the matching folder:
   ```
   public/certificates/manual-and-qa-testing/
   public/certificates/automation-testing/
   public/certificates/programming/
   public/certificates/other/
   ```
   (create a new folder under `public/certificates/` if none of these fit)
2. Add an entry for it in `src/data/certificates.js` — there's a
   commented-out example in that file showing every field.
3. Commit and push. Vercel redeploys automatically and the certificate
   appears on the live site, organized into its category with a working
   click-to-expand viewer.

## Updating other content

Everything the site displays lives in two files:

- `src/data/resumeData.js` — profile, summary, skills, experience,
  projects, education, leadership
- `src/data/certificates.js` — certificates and their categories

Edit those, push to GitHub, and the live site updates automatically. You
generally won't need to touch any component files for routine updates.

## Updating the resume file

Replace `public/resume/Ashar_Shahid_Resume.pdf` with your updated PDF
(keep the same filename, or update the `href`/`download` links in
`src/components/Nav.jsx`, `Hero.jsx`, and `Contact.jsx` if you rename it).

## Tech stack

- [React 19](https://react.dev) + [Vite](https://vitejs.dev)
- [Tailwind CSS v4](https://tailwindcss.com)
- [Framer Motion](https://www.framer.com/motion/) for animation
- [lucide-react](https://lucide.dev) for icons

No backend, no database, no paid services — the entire site is static and
deploys as a single Vercel project alongside its resume and certificate
files.
