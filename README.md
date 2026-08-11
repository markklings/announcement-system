# Project: Announcement System
---
### Brief Introduction
A centralized, reliable, user-friendly web application where teachers and class officers can post-real time updates, event notices, and urgent alerts, ensuring all students and community members stay informed.

### Core Project Scope & Goals:
### Project Scope
To develop a centralized, reliable, and user-friendly web application where teachers, class officers, and community leaders can post real-time updates, event notices, and urgent alerts, ensuring all students and community members stay informed.
### System Goals
- **Centralized Communication:** Eliminate scattered messaging across multiple system platforms.
- **Role-Based Access Control:** Ensure only authorized users (e.g., Admins/Officers) can post announcements, while general users can view and interact.
- **Real-Time Notifications:** Ensure high-priority announcements (e.g., class cancellations, emergency alerts) reach users immediately.
- **Accessibility & Responsiveness:** Provide a clean, modern UI that works seamlessly on both mobile devices and desktop computers.
---
### Technical Scopes (In-Scope vs. Out-of-Scopes):
| **In-Scopes (Core-Features)** | **Out-of-Scopes (Future Enhancements)** |
| --- | --- |
| **Authentication:** User signup/login, password resetting, JWT/Session handling. |Native mobile app development (iOS/Android native builds).  |
| **Role Management:** Admin (create/edit/delete), Viewer (read/react/comment). | Payment integration for community events. |
| **Announcement Feed:** Categorization (Class, Urgency, Community), search, and tagging. | Complex multi-language localization (AI translation). |
| **Notifications:** In-app notifications or email alerts for high-priority posts. | Voice/Video announcement hosting. |
| **Dashboard:** Admin panel to manage users, posts, and moderation settings. | |
---
#### Resource Allocation & SDLC Phase Breakdown
| **Tool Name** |  **Type** | **Role / Description** |
| --- | --- | --- |
| **VILT:** Vue.js, Inertia.js, Laravel, Tailwind CSS | Frontend | This is the standard level for enterprise-grade laravel applications. |
| **Laravel 11** | Backend | This is where the business logic & security (Router, Business Logic, Security, Database ORM & Notification system). |
| **PostgreSQL, Redis & Cloudinary** | Database  & Cloud Storage| This is where user data, uploaded documents and announcement banners stored.  |
| **Render** | Hosting Service | This is where the system hosted. |
| **Git + GitHub** | CI/CD & Version Control | This is where version control, documentations and source code stored. |
---
#### SDLC Phases & Action Plan
1. **Planning**
    - **Focus:** Define system requirements, scope boundaries, and timeline (Gantt chart or Kanban board).
    - **Deliverable:** Project Charter, Software Requirement Specification (SRS) outline.
2. **Analysis**
    - **Focus:** Define functional/non-functional requirements and target audience personas (Students vs. Admins).
    - **Deliverable:** System Architecture Diagram, Entity Relationship Diagram (ERD), Use Case Diagrams.
3. **Design**
    - **Focus:** Low-fidelity wireframes and high-fidelity UI mockups; RESTful API schema design.
    - **Deliverable:** Figma UI designs, Database Schema, API Endpoint documentation (e.g., Swagger/Postman).
4. **Coding (Implementation)**
    - **Focus:** Frontend component architecture, backend API endpoints, database setup, and RBAC integration.
    - **Deliverable:** Functional codebase managed via Git (GitHub/GitLab repository).
5. **Testing**
    - **Focus:** Unit testing, integration testing (API endpoints), cross-browser compatibility, and User Acceptance Testing (UAT).
    - **Deliverable:** Bug tracking report, test case execution log.
6. **Deployment**
    - **Focus:** CI/CD pipeline set up, environment variable configuration (production vs. development), database migration.
    - **Deliverable:** Live, publicly accessible web application.
7. **Maintenance**
    - **Focus:** Monitoring application health, applying security patches, gathering user feedback, and addressing bug reports.
    - **Deliverable:** System changelogs, user feedback logs.
---
```mermaid
gantt
    Announcement System Project Timeline
    dateFormat  YYYY-MM-DD
    axisFormat  Week %W

    section Planning & Design
    Planning, SRS, UML & Flowchart        :a1, 2026-08-10, 7d

    section Foundation
    DB Design, Migrations, Setup          :a2, after a1, 7d

    section Core Backend
    Core APIs, Auth & RBAC (Roles)        :a3, after a2, 14d

    section Frontend & Features
    Frontend UI, Feed & Notifications     :a4, after a3, 14d

    section Testing & Launch
    Testing (UAT, Bugs) & Deployment      :a5, after a4, 7d

    section Finalization
    Docs, Presentation Prep & Buffer      :a6, after a5, 7d
