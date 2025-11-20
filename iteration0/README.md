# IlmQuest (iteration0)

IlmQuest is a web app for schools that blends class management with gamified missions, grades, and resources. Iteration0 is the current working snapshot built on Node/Express and MongoDB; future iterations will build on this structure.

## Prerequisites
- Node.js 18+ and npm
- MongoDB URI (Atlas or local)
- Cloudinary account (for media uploads)

## Quick start
```bash
cd iteration0
npm install
# copy env template, then fill values
cp config/.env.example config/.env  # if you prefer, create config/.env manually
npm start
```

## Environment
Create `config/.env` with:
```
PORT=2121            # or any open port
DB_STRING=your-mongodb-uri
CLOUD_NAME=your-cloudinary-cloud-name
API_KEY=your-cloudinary-api-key
API_SECRET=your-cloudinary-api-secret
```

## Scripts
- `npm start` — runs the server with nodemon on the configured port.

## Project structure
- `controllers/` — route handlers for auth, home, posts, etc.
- `models/` — Mongoose schemas (users, classes, missions, grades, reflections, communications, verses, posts).
- `routes/` — Express routes for main app and posts.
- `middleware/` — auth, multer uploads, cloudinary config.
- `views/` — EJS templates for admin, teacher, student, parent layouts.
- `public/` — static assets (CSS, images).
- `seed.js`, `seedHadith.js` — optional seed scripts to populate sample data (run with `node seed.js` after env and DB are configured).

## Iteration plan
This folder is iteration0. Iteration1–Iteration4 are reserved for future updates; keep new work in the next numbered iteration to preserve history.
