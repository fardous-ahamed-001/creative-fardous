# Creative Fardous — Cursor Project Guide

এই ফাইল Cursor AI-কে প্রজেক্ট সম্পর্কে বুঝতে সাহায্য করে। নতুন ফিচার, বাগ ফিক্স, বা রিফ্যাক্টর করার সময় এই গাইড অনুসরণ করুন।

## Project Overview

**Creative Fardous** — একটি Node.js ভিত্তিক ক্রিয়েটিভ ওয়েব প্রজেক্ট। **Next.js** ফ্রেমওয়ার্ক ও **TypeScript** দিয়ে বানানো হবে। এই রিপোজিটরিতে সোর্স কোড, অ্যাসেট, এবং ডকুমেন্টেশন থাকবে।

## Goals

- পরিষ্কার, রিডেবল, এবং মেইনটেইনেবল কোড লেখা
- ছোট, ফোকাসড পরিবর্তন — অপ্রয়োজনীয় রিফ্যাক্টর এড়িয়ে চলা
- বিদ্যমান কনভেনশন ও প্যাটার্ন মেনে চলা

## Working with Cursor

যখন এই প্রজেক্টে কাজ করবেন:

1. **প্রথমে কোডবেস বুঝুন** — নতুন ফাইল বা প্যাটার্ন যোগ করার আগে আশেপাশের কোড পড়ুন
2. **স্কোপ ছোট রাখুন** — শুধু যা চাওয়া হয়েছে সেটাই পরিবর্তন করুন
3. **কমেন্ট** — শুধু জটিল বা non-obvious লজিকে কমেন্ট দিন
4. **টেস্ট** — শুধু তখনই টেস্ট যোগ করুন যখন ম meaningful coverage দরকার

## Tech Stack

| Layer        | Technology                          |
| ------------ | ----------------------------------- |
| Runtime      | Node.js                             |
| Language     | TypeScript                          |
| Framework    | Next.js (App Router)                |
| UI           | React                               |
| Styling      | TBD (e.g. Tailwind CSS)             |
| Package Mgr  | npm                                 |
| Database     | TBD                                 |
| Deployment   | TBD (e.g. Vercel)                   |

## Folder Structure

Next.js App Router কনভেনশন অনুযায়ী:

```
creative-fardous/
├── cursor.md
├── package.json
├── tsconfig.json
├── next.config.ts
├── public/                 # Static assets (images, fonts, etc.)
├── src/
│   ├── app/                # Routes, layouts, pages (App Router)
│   │   ├── layout.tsx
│   │   ├── page.tsx
│   │   └── globals.css
│   ├── components/         # Reusable React components
│   ├── lib/                # Utilities, helpers, shared logic
│   └── types/              # Shared TypeScript types
└── .env.local              # Environment variables (commit করবেন না)
```

## Coding Conventions

- **TypeScript** — strict mode; `any` এড়িয়ে চলুন; shared types `src/types/` এ রাখুন
- **Next.js** — App Router (`src/app/`) ব্যবহার করুন; server/client component পার্থক্য মেনে চলুন
- **React** — functional components; reusable logic custom hooks-এ extract করুন
- **Imports** — `@/` path alias (e.g. `@/components/...`) ব্যবহার করুন
- বিদ্যমান naming style, import style, এবং file structure অনুসরণ করুন
- নতুন abstraction শুধু তখনই যোগ করুন যখন সত্যিই দরকার
- `.env.local` বা credential ফাইল commit করবেন না

## Commands

```bash
npm install          # Dependencies ইনস্টল
npm run dev          # Development server (http://localhost:3000)
npm run build        # Production build
npm run start        # Production server চালান
npm run lint         # ESLint চালান
```

## Notes

- Commit শুধু তখনই করুন যখন স্পষ্টভাবে বলা হয়
- PR তৈরি করতে `gh` CLI ব্যবহার করুন (যদি GitHub repo থাকে)

---

*শেষ আপডেট: Jun 2026*
