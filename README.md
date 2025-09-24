TalentFlow

A modern, full-stack talent management platform for HR teams

TalentFlow is a React + TypeScript powered application designed to streamline job postings, candidate assessments, and recruitment workflows. With a responsive UI, dynamic assessment tools, and robust local storage, it empowers HR teams to manage the entire hiring process efficiently.

🚀 Features
🔹 Core Functionality

Job Management – Create, edit, and manage job postings with detailed requirements.

Candidate Management – Track and manage candidate applications and profiles.

Assessment Builder – Build multi-section assessments with multiple question types.

Assessment Preview – Real-time assessment previews before publishing.

Assessment Results – View and analyze candidate responses.

HR Dashboard – Monitor hiring metrics and insights.

🔹 Supported Question Types

Single Choice

Multiple Choice

Short Text

Long Text

Numeric Input

File Upload

🔹 Advanced Features

Conditional Logic – Show/hide questions dynamically based on responses.

Real-time Validation – Customizable client-side validation rules.

Responsive Design – Built mobile-first with Tailwind CSS.

Mock Backend – Full API simulation using MSW.

Persistent Storage – IndexedDB support via Dexie.

🛠 Tech Stack
Frontend

React 19.1.1 – UI library with concurrent rendering support.

TypeScript 5.8.3 – Strong typing for maintainable code.

Vite 7.1.2 – Ultra-fast build tool and dev server.

React Router DOM 7.9.0 – Client-side routing.

Tailwind CSS 4.1.13 – Utility-first styling framework.

State & Data

Dexie 4.2.0 – IndexedDB wrapper for structured queries.

MSW 2.11.2 – Mock Service Worker for API simulation.

Axios 1.12.1 – HTTP client for API requests.

UI & Components

Radix UI – Accessible component primitives.

Lucide React – Icon set.

React Hot Toast – Notifications.

Class Variance Authority – Variant-based styling.

Development Tools

ESLint – Code linting.

TypeScript ESLint – TypeScript-specific rules.

Faker.js – Test data generation.

📂 Project Structure
src/
├── components/           # Reusable UI components
│   ├── common/           # Shared (JobCard, JobSkeleton)
│   ├── HrDashboard/      # HR-specific components
│   ├── Jobs/             # Job-related components
│   ├── layout/           # Layout (Header, Footer, HrLayout)
│   ├── sections/         # Landing page sections
│   └── ui/               # Base UI (Button, Card, Logo)
├── pages/                # Page-level components
│   ├── AssessmentBuilder.tsx
│   ├── AssessmentPreview.tsx
│   ├── AssessmentResults.tsx
│   ├── Assessments.tsx
│   ├── CandidateJobs.tsx
│   ├── CandidateProfile.tsx
│   ├── Candidates.tsx
│   ├── HrDashboard.tsx
│   ├── JobDetails.tsx
│   ├── Jobs.tsx
│   └── Landing.tsx
├── services/             # Business logic & data
│   ├── db/               # IndexedDB (Dexie)
│   ├── mocks/            # API mocks (MSW)
│   └── seed/             # Seed data
├── types/                # Type definitions
├── utils/                # Utilities
└── main.tsx              # App entry point

⚡ Quick Start
Prerequisites

Node.js 18+

npm or yarn

Installation
# Clone repository
git clone <repository-url>
cd talentflow

# Install dependencies
npm install

# Start dev server
npm run dev


Open browser at 👉 http://localhost:5173

Available Scripts
npm run dev      # Start dev server
npm run build    # Production build
npm run preview  # Preview production build
npm run lint     # Run ESLint

🏗 Architecture
Frontend

Component-Based – Modular React architecture.

Type-Safe – Full TypeScript support.

Responsive – Mobile-first with Tailwind CSS.

Accessible – Radix UI for a11y compliance.

Data Layer

Mock API – Handled via MSW.

IndexedDB Persistence – Dexie for structured offline storage.

Seed Data – Faker.js for realistic test data.

Routing

Client-Side Routing – Powered by React Router DOM.

Nested Routes – HR dashboard with assessment routes.

Route Protection – Redirects for HR flows.

🔧 Technical Decisions

React 19 – Better concurrency, automatic batching, new hooks.

Vite – Faster builds, smaller bundles, improved DX.

Dexie – Structured, scalable storage beyond localStorage.

MSW – Realistic API mocking over static JSON.

Tailwind CSS – Utility-first, customizable, performant.

🐛 Known Issues

SPA Routing on Vercel – Fixed with vercel.json rewrites.

MSW Import Errors – Handled with dynamic import fallbacks.

Hydration Errors – Fixed by removing HTML inside <option>.

Assessment List Refresh – Resolved by adding refresh triggers.

☁ Deployment

Vercel (Recommended) – Auto-detects Vite config, vercel.json handles SPA routing.

Netlify – Use _redirects file (/* /index.html 200).

GitHub Pages – Deploy with gh-pages.

AWS S3 + CloudFront – Redirect errors to index.html.

🔮 Future Enhancements
Planned Features

Authentication & authorization

Real-time collaboration

Advanced analytics & reporting

Email notifications & integrations

Bulk candidate operations

Assessment templates & library

API rate limiting & caching

PWA support

Technical Improvements

Comprehensive test coverage

Error boundaries

Performance monitoring

Bundle optimization

i18n support

Dark mode

🤝 Contributing
# Fork repo
# Create feature branch
git checkout -b feature/amazing-feature

# Commit changes
git commit -m 'Add amazing feature'

# Push branch
git push origin feature/amazing-feature

# Open Pull Request

📜 License

This project is licensed under the MIT License – see the LICENSE
 file.

🙏 Acknowledgments

React
 – UI library

Vite
 – Build tool

Tailwind CSS
 – Styling framework

MSW
 – Mock API

Dexie
 – IndexedDB wrapper

Radix UI
 – Accessible components

💡 TalentFlow – Streamlining recruitment for modern HR teams.
