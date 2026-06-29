# Creative Fardous

A creative web project built with **Node.js**, **TypeScript**, and **Next.js**.

## About

Creative Fardous is a Node.js–based web application using the Next.js App Router and React. The goal is clean, maintainable code with a focused scope and consistent conventions.

## Tech Stack

| Layer         | Technology              |
| ------------- | ----------------------- |
| Runtime       | Node.js                 |
| Language      | TypeScript              |
| Framework     | Next.js (App Router)    |
| UI            | React                   |
| Package manager | npm                   |
| Styling       | TBD (e.g. Tailwind CSS) |
| Database      | TBD                     |
| Deployment    | TBD (e.g. Vercel)       |

## Prerequisites

- [Node.js](https://nodejs.org/) 18.18 or later (20+ recommended)
- npm (included with Node.js)

## Getting Started

Clone the repository and install dependencies:

```bash
git clone <repository-url>
cd creative-fardous
npm install
```

Once Next.js is scaffolded, use:

```bash
npm run dev      # Start development server at http://localhost:3000
npm run build    # Create a production build
npm run start    # Run the production server
npm run lint     # Run ESLint
```

## Project Structure

```
creative-fardous/
├── README.md
├── cursor.md              # Cursor AI project guide
├── package.json
├── tsconfig.json
├── next.config.ts
├── public/                # Static assets (images, fonts, etc.)
├── src/
│   ├── app/               # Routes, layouts, pages (App Router)
│   ├── components/        # Reusable React components
│   ├── lib/               # Utilities and shared logic
│   └── types/             # Shared TypeScript types
└── .env.local             # Local environment variables (do not commit)
```

## Environment Variables

Copy `.env.example` to `.env.local` and fill in the values when environment configuration is added:

```bash
cp .env.example .env.local
```

Never commit `.env.local` or files containing secrets.

## Development Notes

- Use TypeScript strict mode; avoid `any` where possible
- Prefer the App Router (`src/app/`) and distinguish server vs. client components
- Use functional React components and `@/` path aliases for imports
- See [cursor.md](./cursor.md) for detailed AI and team conventions

## License

ISC
