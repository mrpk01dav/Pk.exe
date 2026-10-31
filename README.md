# PK.exe — Prince Kumar's portfolio
React + Vite + vanilla CSS. No other runtime dependencies.

## Run
npm install && npm run dev    # local
npm run build                 # outputs dist/

## Edit content
All content is in `src/data/` (profile, skills, projects, journey). Fields marked TODO need your real info.
Resume: put the PDF in `public/` and set `resume: '/your-file.pdf'` in `profile.js`.
Contact form: create a form at formspree.io, copy `.env.example` to `.env`, set `VITE_FORM_ENDPOINT`. Add the same variable in Vercel > Settings > Environment Variables.
Set the real domain in `index.html` (canonical) and add `public/og-image.png`, then add an og:image tag.

## Deploy (GitHub + Vercel)
1. Create an empty GitHub repo; `git init && git add . && git commit -m "init" && git remote add origin <url> && git push -u origin main`
2. vercel.com > Add New > Project > import the repo. Framework: Vite, build `npm run build`, output `dist`, install `npm install`.
3. Add VITE_FORM_ENDPOINT, deploy, then test the live URL. Future commits to main redeploy automatically.
