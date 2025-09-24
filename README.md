# TalentFlow

A modern, full-stack talent management platform built with **React**, **TypeScript**, and **Vite**. TalentFlow provides comprehensive tools for HR teams to manage job postings, candidate assessments, and recruitment workflows with efficiency and scalability.

Other UI/UX and Brand Design of the product:- https://www.figma.com/design/0i4mcs6iHnwaMrMTLqTPp4/TalentFlow?node-id=0-1&t=AXRXNsMhKwdmaCqd-1
BrandGuidelines:- https://drive.google.com/drive/folders/1ZK-qyuTlvUIkAMjQKiS9cqkA-PfdkS3Q?usp=sharing
---

## Features

### Core Functionality

* **Job Management**: Create, edit, and manage job postings with detailed requirements.
* **Candidate Management**: Track and manage candidate profiles and applications.
* **Assessment Builder**: Create multi-section assessments with various question types.
* **Assessment Preview**: Real-time preview of assessments before publishing.
* **Assessment Results**: View and analyze candidate responses.
* **Dashboard Analytics**: Comprehensive HR dashboard with key metrics.

### Question Types

* Single Choice
* Multiple Choice
* Short Text
* Long Text
* Numeric Input
* File Upload

### Advanced Features

* **Conditional Logic**: Dynamically show or hide questions based on previous answers.
* **Real-time Validation**: Client-side validation with customizable rules.
* **Responsive Design**: Mobile-first layout with Tailwind CSS.
* **Mock API**: Complete mock backend with MSW (Mock Service Worker).
* **Persistent Storage**: IndexedDB integration via Dexie.

---

## Tech Stack

### Frontend

* React 19.1.1 – UI library with the latest features
* TypeScript 5.8.3 – Type-safe JavaScript
* Vite 7.1.2 – Fast build tool and development server
* React Router DOM 7.9.0 – Client-side routing
* Tailwind CSS 4.1.13 – Utility-first CSS framework

### State Management & Data

* Dexie 4.2.0 – IndexedDB wrapper for local storage
* MSW 2.11.2 – Mock Service Worker for API mocking
* Axios 1.12.1 – HTTP client for API requests

### UI Components

* Radix UI – Accessible component primitives
* Lucide React – Icon library
* React Hot Toast – Notifications
* Class Variance Authority – Component variant management

### Development Tools

* ESLint – Code linting and formatting
* TypeScript ESLint – TypeScript-specific linting rules
* Faker.js – Fake data generation for development

---

## Project Structure

```
src/
├── components/           # Reusable UI components
│   ├── common/           # Shared components (JobCard, JobSkeleton)
│   ├── HrDashboard/      # HR-specific components
│   ├── Jobs/             # Job-related components
│   ├── layout/           # Layout components (Header, Footer, HrLayout)
│   ├── sections/         # Landing page sections
│   └── ui/               # Base UI components (Button, Card, Logo)
├── pages/                # Page components
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
├── services/             # Business logic and data layer
│   ├── db/               # Database layer (Dexie)
│   ├── mocks/            # Mock API handlers (MSW)
│   └── seed/             # Seed data generation
├── types/                # TypeScript type definitions
├── utils/                # Utility functions
└── main.tsx              # Application entry point
```

---

## Quick Start

### Prerequisites

* Node.js 18+
* npm or yarn

### Installation

```bash
# Clone the repository
git clone <repository-url>
cd talentflow

# Install dependencies
npm install

# Start development server
npm run dev
```

Visit the application in your browser at: localhost

### Available Scripts

```bash
npm run dev      # Start development server
npm run build    # Build for production
npm run preview  # Preview production build
npm run lint     # Run ESLint
```

---

## Architecture

### Frontend

* Component-based modular React architecture
* Full TypeScript coverage for type safety
* Mobile-first responsive design with Tailwind CSS
* Accessibility built-in with Radix UI primitives

### Data Layer

* Mock backend powered by MSW
* IndexedDB persistence via Dexie
* Seed data generation using Faker.js
* Strong typing across all data operations

### Routing

* Client-side navigation with React Router DOM
* Nested routes for dashboards and assessments
* Route protection with automatic redirects for HR login flow

---

## Technical Decisions

**Why React 19?**

* Improved concurrent rendering
* Automatic batching for better performance
* New hooks for enhanced developer experience

**Why Vite over Create React App?**

* Faster builds and hot module replacement
* Built-in TypeScript and CSS support
* Smaller, optimized bundles

**Why Dexie over localStorage?**

* More efficient for large datasets
* SQL-like query capabilities
* Full TypeScript support
* Offline-first capabilities

**Why MSW over JSON Server?**

* Intercepts actual HTTP requests for realistic mocking
* Consistent development and testing environments
* Better debugging with network tab integration
* Easy to implement complex logic

**Why Tailwind CSS?**

* Rapid prototyping with utility-first approach
* Mobile-first responsiveness built-in
* Easily customizable design system
* Purges unused styles for performance

---

## Known Issues & Solutions

1. **SPA Routing on Vercel**

   * Issue: 404 errors when refreshing pages
   * Solution: Added `vercel.json` with rewrite rules to serve `index.html`

2. **MSW Import Errors in Production**

   * Issue: Dynamic MSW imports failing
   * Solution: Fallback logic added to start app without MSW

3. **Hydration Errors with Option Elements**

   * Issue: `<span>` elements inside `<option>` caused React errors
   * Solution: Replaced with text-only option values

4. **Assessment List Not Refreshing**

   * Issue: Newly created assessments not appearing immediately
   * Solution: Added refresh triggers on location change and window focus

---

## Deployment

### Vercel (Recommended)

* Connect the GitHub repository to Vercel
* Automatic detection of Vite configuration
* `vercel.json` handles SPA routing
* Zero-configuration deployment

### Other Platforms

* **Netlify**: Add `_redirects` file with `/* /index.html 200`
* **GitHub Pages**: Use `gh-pages` with proper base path
* **AWS S3 + CloudFront**: Configure error pages to redirect to `index.html`

---

## Future Enhancements

### Planned Features

* User authentication and authorization
* Real-time collaboration on assessments
* Advanced analytics and reporting
* Email notifications and integrations
* Bulk candidate operations
* Assessment templates and library
* API rate limiting and caching
* Progressive Web App (PWA) features

### Technical Improvements

* Comprehensive test coverage
* Error boundaries for reliability
* Performance monitoring tools
* Further bundle size optimization
* Internationalization (i18n) support
* Dark mode theme

---

## Contributing

1. Fork the repository
2. Create a feature branch:

   ```bash
   git checkout -b feature/amazing-feature
   ```
3. Commit your changes:

   ```bash
   git commit -m 'Add amazing feature'
   ```
4. Push to the branch:

   ```bash
   git push origin feature/amazing-feature
   ```
5. Open a Pull Request

---

## Acknowledgments

* React – The UI library
* Vite – The build tool
* Tailwind CSS – The CSS framework
* MSW – The API mocking library
* Dexie – The IndexedDB wrapper
* Radix UI – The component primitives

---

**TalentFlow – Streamlining talent management for modern HR teams.**
