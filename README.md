# Project Overview — Seewee.ai Project description
 Seewee.ai is an AI-powered job application assistant. It allows users to:

* Create tailored resumes for every job description.
* Automatically log each generated resume as an application.
* Manage and track applications inside a dashboard.
* Extend functionality via a Chrome extension on third-party job boards (LinkedIn, Indeed, etc.).

The platform is subscription-based, with Free, Pro, and Career+ tiers. it will 
🎯 Goals

1. Build a production-ready backend (NodeJS + Express + Prisma + PostgreSQL) with authentication, role-based access, billing, and a scalable resume generation service.
2. Deliver a clean and modern web application (Next.js) and Chrome extension that integrate seamlessly with the backend.
3. Launch with subscription plans (Free, Starter, Pro, Career+) and ensure credit/quota enforcement and analytics for Career+ users.
4. Meet non-functional requirements: ≤10s resume generation, 10k concurrent burst handling, GDPR compliance, and 99.9% uptime.

✅ Requirements
Core features

* User onboarding: Sign up / login via email/password and Google OAuth.
* Profiles: Store personal info, work experience, education, skills. Profile health score for Career+ users.
* Job board: Browse jobs from scraped database with filters (keyword, location, salary, remote/hybrid).
* Resume generation: AI tailors resumes per JD, exports PDF/DOCX, stores resume history.
* Applications: Auto-log every generated resume as an application. Dashboard with filters and statuses. Analytics for Career+ users.
* Chrome extension: Inject “Generate Resume” button on job boards, call API, and sync back to dashboard.
* Billing & credits: Stripe integration with Free, Starter, Pro, Career+ tiers. Enforce monthly limits + overage credits.

Roles & permissions

* User: Manage profile, browse jobs, generate resumes (within limits), view application history.
* Career+ User: All above + track application statuses + analytics dashboard.
* Admin: Manage templates, manage subscriptions.
* SUPER_ADMIN: Root privileges (manage admins, billing overrides, system configs).

Non-functional requirements

* Performance: Resume generation ≤ 10 seconds.
* Scalability: Handle 10k concurrent resume generation bursts with queueing.
* Security: Encrypted user data, GDPR-compliant delete/export.
* Availability: 99.9% uptime target.
* Compliance: ATS-friendly resume output (machine-readable, text-first formatting).

