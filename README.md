# 💸 FINOVA – Finance Management Platform
A powerful full-stack **Finance Management Platform** to help users seamlessly manage their **income**, **expenses**, and **financial goals** in real-time with clean visuals and secure access. FINOVA is built using **Next.js**, **Prisma**, **Supabase**, **Clerk**, **Inngest**, **Arcjet**, and styled beautifully with **Tailwind CSS** and **Shadcn UI**.


---

## 📌 Table of Contents

- [✨ Features](#-features)
- [🧰 Tech Stack](#-tech-stack)
- [📦 Prerequisites](#-prerequisites)
- [⚙️ Getting Started](#️-getting-started)
- [🧪 Tool Installations & Setup](#-tool-installations--setup)
  - [Prisma](#1-prisma)
  - [Supabase](#2-supabase)
  - [Clerk](#3-clerk)
  - [Inngest](#4-inngest)
  - [Arcjet](#5-arcjet)
  - [Shadcn UI](#6-shadcn-ui)
- [🔐 Environment Variables](#-environment-variables)
- [📁 Folder Structure](#-folder-structure)
- [🚀 Running the Project](#-running-the-project)
- [🛠️ Future Enhancements](#️-future-enhancements)

---
## ✨ Features

- 🔐 Secure user authentication via Clerk
- 📊 Real-time income and expense tracking
- 📁 Database management with Prisma and Supabase
- 🔄 Background job processing using Inngest
- 🛡️ Security enhancement with Arcjet API protection
- 🌈 Responsive design using Tailwind CSS and Shadcn UI
- ⚡ Fast, scalable Next.js frontend

---

## 🧰 Tech Stack

| Tool/Tech     | Description                                |
|---------------|--------------------------------------------|
| **Next.js**   | Full-stack React framework                 |
| **Prisma**    | Type-safe ORM for database access          |
| **Supabase**  | Open-source Firebase alternative           |
| **Clerk**     | Plug-and-play authentication               |
| **Inngest**   | Event-driven functions & background jobs   |
| **Arcjet**    | API security and rate limiting             |
| **Shadcn UI** | Accessible component library (Tailwind)    |
| **Tailwind CSS** | Utility-first CSS framework             |
| **JavaScript/HTML** | Core languages                       |

---


###  a `.env` file with following variables -

```
DATABASE_URL=
DIRECT_URL=

NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=
NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL=/onboarding
NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL=/onboarding

GEMINI_API_KEY=

RESEND_API_KEY=

ARCJET_KEY=
```
