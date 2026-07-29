# Ayush K — Portfolio

A single self-contained `index.html` — no build step, no dependencies to install. Tailwind and fonts load from CDN; everything else (animations, form logic, section content) is plain JS/CSS in the file.

## Run it locally
Just open `index.html` in a browser. Or serve it: `npx serve .`

## Deploy (pick one, all zero-config)
- **Netlify** — drag the folder onto app.netlify.com/drop, or `netlify deploy --prod`
- **Vercel** — `vercel --prod` from this folder
- **GitHub Pages** — push to a repo, enable Pages on the `main` branch root

## Contact form
Uses [FormSubmit](https://formsubmit.co) pointed at `alex.carter.dev@example.com` — free, no signup, but **the first submission triggers a confirmation email you must click** to activate that address. Swap the email in the form's `action` attribute for your real one, or swap the whole block for EmailJS if you'd rather send from JS with an API key.

## Customize content
All section content (skills, projects, certifications, timeline) lives in plain JS objects near the top of the `<script>` block at the bottom of `index.html` — edit the arrays (`skillGroups`, `projects`, `certifications`, `timelineItems`) rather than hunting through markup. Replace `public/profile.jpg`-style placeholders, resume URL, and social links by searching for `alexcarter.dev`, `example.com`, and `#` in the file.

## Later: porting to React
If you eventually want the full React + TypeScript + Vite version this started from, the section structure and copy here map 1:1 onto components (`Hero`, `About`, `SkillsGrid`, `ProjectCard`, `Timeline`, `ContactForm`) — happy to scaffold that separately when you're ready for it.
