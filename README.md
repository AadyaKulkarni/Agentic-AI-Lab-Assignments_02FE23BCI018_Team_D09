Agentic AI Systems — All 14 Labs & Assignments

# CareerPilot — Placement Readiness & Career Intelligence Portal

An AI-powered placement preparation and career intelligence platform designed to help students assess their job readiness, identify skill gaps, discover relevant opportunities, and prepare for technical recruitment processes.

CareerPilot brings together career guidance, resume analysis, skill assessment, job discovery, coding performance insights, and interview preparation within a unified platform. It aims to make placement preparation more structured and data-driven by combining AI-assisted analysis with practical career tools.

## Table of Contents
- Project Overview
- Key Features
- Platform Modules
- System Architecture
- Technology Stack
- Repository Structure
- Getting Started
- Running the Application
- Implementation Notes
- Future Scope

## Project Overview

The transition from academic learning to professional employment can be challenging for students. Identifying suitable job opportunities, understanding industry expectations, evaluating technical skills, and preparing for recruitment processes often require using multiple disconnected platforms.

CareerPilot addresses this challenge through an integrated placement-readiness portal that brings these activities together.

The platform focuses on:
- Evaluating resumes and identifying areas for improvement.
- Comparing existing skills with job-specific requirements.
- Discovering relevant job opportunities based on candidate profiles.
- Tracking coding performance and identifying improvement areas.
- Supporting technical interview preparation.
- Providing AI-assisted career insights to guide preparation decisions.

## Key Features

- **AI-Powered Resume Analysis:** Evaluates resume content and provides suggestions to improve relevance, clarity, and presentation.
- **Skill Gap Analysis:** Identifies differences between a candidate's existing skill set and the skills expected for selected roles.
- **Job Matching:** Helps users discover relevant job opportunities by comparing candidate profiles with job requirements.
- **Coding Analytics:** Provides insights into coding performance and areas that may require further practice.
- **Interview Preparation:** Supports preparation for technical interviews through AI-assisted guidance.
- **Company Exploration:** Provides a dedicated interface for exploring companies and placement-related opportunities.
- **Career Intelligence:** Combines different assessment and discovery modules to help students make more informed preparation decisions.

## Platform Modules

| Module | Description |
|---|---|
| Resume Analysis | Reviews resume content and generates improvement suggestions. |
| Skill Gap Analysis | Compares candidate skills against role-specific requirements. |
| Job Matching | Uses profile and job information to identify relevant opportunities. |
| Coding Analytics | Analyzes coding-related performance and highlights improvement areas. |
| Interview Preparation | Provides AI-assisted technical interview preparation. |
| Company Portal | Offers a dedicated interface for exploring companies and opportunities. |

## System Architecture

CareerPilot follows a full-stack application architecture with separate frontend and backend components.

**Frontend**
- Provides the user interface and interactive placement-readiness modules.
- Built using React and TypeScript.
- Handles user interactions, navigation, and presentation of results.

**Backend**
- Built using Python and FastAPI.
- Exposes API endpoints for application functionality.
- Organizes application logic into API routes and service modules.
- Integrates AI-assisted functionality and external job-search services.

**Data and Infrastructure**
- PostgreSQL serves as the relational database.
- Redis supports application-level caching and related operations.
- Docker and Docker Compose support containerization and application setup.

## Technology Stack

| Category | Technologies |
|---|---|
| Programming Languages | Python, TypeScript |
| Frontend | React |
| Backend | FastAPI |
| Database | PostgreSQL |
| Caching | Redis |
| AI Integration | Gemini / OpenAI integrations, depending on configuration |
| Job Data | Remotive API |
| Containerization | Docker, Docker Compose |
| Matching Techniques | TF-IDF, Cosine Similarity |
| Testing | Python-based backend tests |

## Repository Structure

The project is organized into separate frontend and backend components.

```text
CareerPilot/
└── placement_portal/
    ├── backend/
    │   ├── app/
    │   │   ├── api/
    │   │   │   └── agents.py
    │   │   └── services/
    │   │       └── job_search.py
    │   └── tests/
    │       └── test_live_job_search.py
    │
    ├── frontend/
    │   └── src/
    │       └── pages/
    │           └── Companies.tsx
    │
    └── README.md
```

*Note: This is a representative structure highlighting selected files. Additional application modules, configuration files, and components may be present in the repository.*

## Getting Started

### Prerequisites

- Python 3.10 or later.
- Node.js and npm.
- PostgreSQL.
- Redis.
- Docker and Docker Compose (if using the containerized setup).
- Visual Studio Code or another code editor.

### Setup

1. Clone the repository.

```bash
git clone https://github.com/YOUR-USERNAME/CareerPilot.git
```

2. Navigate to the project directory.

```bash
cd CareerPilot/placement_portal
```

3. Configure the backend environment and install the dependencies specified in the backend requirements file.

4. Configure the required environment variables, including database credentials and AI service API keys.

5. Install frontend dependencies.

```bash
cd frontend
npm install
```

6. Configure and start PostgreSQL and Redis.

## Running the Application

### Backend

From the backend directory, activate your Python environment and start the FastAPI application.

```bash
uvicorn app.main:app --reload
```

The API documentation can generally be accessed through:

```text
http://127.0.0.1:8000/docs
```

### Frontend

From the frontend directory:

```bash
npm run dev
```

Open the local development URL displayed in the terminal.

### Docker

If the repository includes a Docker Compose configuration, the application can be started using:

```bash
docker compose up --build
```

Refer to the project's configuration and environment files for the exact service setup.

## Implementation Notes

- **Modular architecture:** Frontend and backend responsibilities are separated to support independent development and maintenance.
- **AI-assisted functionality:** AI integrations support selected career guidance and assessment workflows. Their availability depends on the configured providers and API credentials.
- **Job discovery:** External job-search data is integrated through the Remotive API.
- **Matching approach:** TF-IDF and cosine similarity can be used to compare candidate profiles and job-related information.
- **Data management:** PostgreSQL provides relational data storage, while Redis supports caching-related functionality.
- **Containerization:** Docker-based configuration supports consistent development and deployment environments.
- **Testing:** Backend test scripts support validation of application functionality, including job-search workflows.

## Future Scope

- Integration with additional job portals and recruitment platforms.
- More advanced resume parsing and role-specific recommendations.
- Personalized learning roadmaps based on identified skill gaps.
- Expanded coding assessments and performance tracking.
- Mock interview simulations with detailed feedback.
- Recruitment trend analysis and company-specific preparation insights.
- Improved analytics dashboards for tracking placement readiness.
- Deployment and scalability improvements for wider institutional use.

---

**CareerPilot — Prepare Smarter. Identify Gaps. Navigate Your Career.**
