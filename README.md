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
- 📧 Transactional email integration using Resend API
- 🧠 AI-powered financial assistant via Google Gemini
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

---

## 📦 Prerequisites

Before running the project, ensure you have the following installed:

- [Node.js (v18+)](https://nodejs.org/)
- [npm or yarn](https://www.npmjs.com/)
- [Git](https://git-scm.com/)
- A Supabase project
- A Clerk account
- Arcjet & Inngest accounts (free plans are enough)

---

---

## ⚙️ Getting Started

### 1. Clone the Repo

```bash
git clone https://github.com/Dikshav07/Finance-Management-Platform.git
cd Finance-Management-Platform
```
### 2. Install Dependencies
```bash
npm install
```
---
---
## 🧪 Tool Installations & Setup
### 1. Prisma
Prisma is used to connect to and query your Supabase PostgreSQL database.

#### 🔧 Installation
```base
npm install prisma --save-dev
npx prisma init
```
This will generate 
```base
/prisma/schema.prisma
```

#### ⚙️ Usage
- Define your database schema in ```base prisma/schema.prisma ```
- Run the following to generate and apply migrations:
```base
npx prisma migrate dev --name init
npx prisma generate
```

### 2. Supabase
Supabase is used as the backend database (PostgreSQL) and auth (optionally).

- Go to https://supabase.com/ and create a project.
- Copy the project URL and anon/public key for use in your environment variables.

### 3. Clerk
Clerk handles user registration, login, and sessions.

#### 🔧 Installation
```base
npm install @clerk/clerk-react
```
- Go to https://clerk.dev/ and create an app.
- Get your Publishable Key and Secret Key from the Clerk dashboard.

### 4. Inngest
Used for background jobs and event-driven processing.
#### 🔧 Installation
```base
npm install inngest @inngest/next
```
#### ⚙️ Usage
- Create an account at https://www.inngest.com/
- Copy your Inngest Signing Key and add it to your ```.env``` file.

### 5. Arcjet
Arcjet helps protect your API and prevent abuse.

#### 🔧 Installation
```base
npm install arcjet
```
Visit https://arcjet.com/ and generate your ARCJET_API_KEY.

### 6. Shadcn UI
Used for beautifully styled, accessible UI components.
#### 🔧 Installation
```base
npx shadcn-ui@latest init
```
- You’ll be prompted to configure Tailwind CSS and React.
- After setup, a ```components/ui/``` folder will be created.

#### ⚙️ Usage
You can now import UI components like:
```js
import { Button } from "@/components/ui/button"
```

### 7. 🔑 GEMINI_API_KEY
#### 📌 What It Is:
This is your API key for Google Gemini — a generative AI platform by Google (formerly part of Bard / PaLM 2). You use this to send prompts and receive AI-generated responses.

#### 📦 Usage Example:
If you're using Gemini via Google’s @google/generative-ai Node.js SDK:

```base
npm install @google/generative-ai
```
```js
import { GoogleGenerativeAI } from "@google/generative-ai";

const genAI = new GoogleGenerativeAI(process.env.GEMINI_API_KEY);

const model = genAI.getGenerativeModel({ model: "gemini-pro" });

const result = await model.generateContent("How do I manage my finances?");
```
#### 📄 How to Get It:
1. Go to Google AI Studio.
2. Click Get API Key from the settings or top right corner.
3. Paste it into your ```.env```:
```
GEMINI_API_KEY=your_google_gemini_api_key_here
```
### 8. 🔑 RESEND_API_KEY
#### 📌 What It Is:
This is your API key for Resend — an email API platform for sending transactional or marketing emails via server-side apps.

#### 📦 Usage Example:
```bash
npm install resend
```
```js
import { Resend } from 'resend';

const resend = new Resend(process.env.RESEND_API_KEY);

await resend.emails.send({
  from: 'finance@finova.com',
  to: 'diksha@example.com',
  subject: 'Your Monthly Report',
  html: '<p>Your budget is on point!</p>',
});
```
#### 📄 How to Get It:
1. Go to https://resend.com/
2. Sign up → Go to Dashboard → API Keys → Generate Key.
3. Add to your ```.env```:
```
RESEND_API_KEY=your_resend_api_key_here
```
---
---
## 🔐 Environment Variables
Create a ```.env``` file in the root of your project and add the following:

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
---
---
## 📁 Folder Structure
```text

Finance-Management-Platform/
├── app/                  # Next.js app routes
├── components/           # Reusable components
├── data/                 # Static/shared content
├── hooks/                # Custom React hooks
├── lib/                  # Utilities and helpers
├── prisma/               # Prisma DB schema
├── public/               # Static assets
├── styles/               # Tailwind & global styles
├── .env.example          # Sample env file
└── README.md             # Project documentation
```
---
---
## 🚀 Running the Project
Once you’ve completed all installations and ```.env``` setup:

```bash
npm run dev
```
Open your browser and visit:
```http://localhost:3000```


---
