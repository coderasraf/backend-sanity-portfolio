# Sanity Portfolio Studio (Backend)

A Sanity Studio that serves as the headless CMS for a personal developer portfolio. It defines the content types the React front end is meant to display.

![Sanity](https://img.shields.io/badge/Sanity_Studio-v2-F03E2F?logo=sanity&logoColor=white)
![React](https://img.shields.io/badge/React-17-61DAFB?logo=react&logoColor=white)

## About

Built in 2022 as a learning project alongside the [sanity-frontend-react](https://github.com/coderasraf/sanity-frontend-react) portfolio front end. Content is edited here and stored in Sanity's hosted `production` dataset.

## Content Schemas

| Schema | Fields |
| --- | --- |
| `works` | title, description, projectLink, codeLink, imgUrl (image with hotspot), tags |
| `skills` | name, bgColor, icon |
| `experiences` | year, works (array of workExperience entries) |
| `workExperience` | name, company, desc |
| `testimonials` | name, company, imgurl, feedback |
| `brands` | imgUrl, name |
| `abouts` | title, description, imgUrl |
| `contact` | name, email, message |

## Features

- Custom document schemas for every portfolio section (projects, skills, work history, testimonials, client brands, about cards, contact messages)
- Image fields with hotspot cropping for project thumbnails
- Vision plugin enabled in development for testing GROQ queries
- Sanity ESLint config

## Tech Stack

- Sanity Studio v2 (`@sanity/base`, `@sanity/desk-tool`, `@sanity/vision`)
- React 17
- styled-components

## Getting Started

Prerequisites: Node.js, npm and the Sanity CLI v2 (`npm install -g @sanity/cli`), plus access to a Sanity project.

```bash
git clone https://github.com/coderasraf/backend-sanity-portfolio.git
cd backend-sanity-portfolio
npm install
npm start        # runs `sanity start` (Studio at http://localhost:3333)
npm run build    # runs `sanity build`
```

To use your own Sanity project, update `api.projectId` and `api.dataset` in `sanity.json`.

## Project Structure

```text
├── sanity.json         # Studio config (project, dataset, plugins)
├── schemas/
│   ├── schema.js       # Registers all document types
│   ├── works.js
│   ├── skills.js
│   ├── experiences.js
│   ├── workExperience.js
│   ├── testimonials.js
│   ├── brands.js
│   ├── abouts.js
│   └── contact.js
├── config/             # Sanity plugin configs
└── static/
```

## Author

Built by **Ashraf Siddik**, Shopify developer & CRO specialist.
- Website: [ashraf-siddik.com](https://ashraf-siddik.com)
- GitHub: [@coderasraf](https://github.com/coderasraf)
