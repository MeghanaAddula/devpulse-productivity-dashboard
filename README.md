# devpulse-productivity-dashboard
Full-stack developer productivity analytics MVP that converts engineering metrics into actionable IC insights and manager summaries using React, Vite, Node.js, and Express.
# DevPulse – Developer Productivity Insights Platform

A focused full-stack MVP built for an internship assignment that transforms raw engineering metrics into actionable developer insights, bottleneck analysis, and practical next steps.

---

## Features

### Individual Contributor Dashboard
- Developer profile view
- Engineering productivity metrics visualization
- AI-assisted bottleneck interpretation
- Actionable recommendations

### Metrics Included
- Lead Time for Changes
- Cycle Time
- Bug Rate
- Deployment Frequency
- PR Throughput

### Manager Summary
- Lightweight team-level productivity summary
- Quick visibility into developer trends and bottlenecks

---

## Tech Stack

### Frontend
- React.js
- Vite

### Backend
- Node.js
- Express.js

### Data Layer
- Excel workbook converted into structured JSON

---

## Project Structure

```text
dev-productivity-mvp/
│
├── client/              React frontend
├── server/              Express backend
├── server/data/         JSON data extracted from workbook
```

---

## Installation & Setup

### Prerequisites
- Node.js v18+
- npm

Check versions:

```bash
node -v
npm -v
```

---

## Run the Project

### Install Dependencies

```bash
npm run install-all
```

### Start Frontend & Backend

```bash
npm run dev
```

Frontend:

```text
http://localhost:5173
```

Backend API:

```text
http://localhost:4000/api
```

---

## Run Separately

### Backend

```bash
cd server
npm install
npm run dev
```

### Frontend

```bash
cd client
npm install
npm run dev
```

---

## API Endpoints

```text
GET /api/health
GET /api/options
GET /api/developers/:developerId?month=2026-04
GET /api/manager-summary?month=2026-04
```

---

## Metric Logic

- Lead Time = Average `lead_time_days` from successful production deployments
- Cycle Time = Average `cycle_time_days` from completed Jira issues
- Bug Rate = Escaped production bugs / completed issues
- Deployment Frequency = Count of successful production deployments
- PR Throughput = Count of merged pull requests

---

## Demo Flow

1. Introduce the productivity problem
2. Open the IC dashboard
3. Select developer and month
4. Explain each productivity metric
5. Show bottleneck interpretation
6. Explain recommended next steps
7. Show manager summary dashboard
8. Discuss responsible AI usage and explainable metric logic

---

## Responsible AI Usage

AI tools were used to assist with project structuring, debugging, and productivity improvements.  
All metric calculations and interpretations remain simple, transparent, and explainable.

---

## Future Improvements

- Team comparison dashboard
- Trend analysis across months
- Authentication & role-based access
- Real-time GitHub/Jira integrations
- AI-generated productivity coaching
