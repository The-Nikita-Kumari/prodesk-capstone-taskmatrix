# 🧩 TaskMatrix — Project Management Tool

> **Capstone Project | Frontend Track | Week 13 Planning Document**

---

## 📌 Project Description

**TaskMatrix** is a modern, full-featured project management tool inspired by Jira and Asana, designed specifically for software development teams. It enables teams to plan, track, and collaborate on tasks using an intuitive Kanban board interface — with support for task assignments, priority tagging, due dates and team roles.

This project is built as a **Frontend-only** application using mocked data (via `db.json` + Zustand/LocalStorage) to simulate real backend interactions.

---

## 👤 Intern Details

| Field | Details |
|---|---|
| **Track** | Frontend Development |
| **Project** | TaskMatrix — Project Management Tool |
| **Week** | Week 13 — Capstone Planning |
| **Deliverable** | PRD + Figma Wireframes + State Architecture |

---

## 🛠️ Tech Stack

| Layer | Technology | Reason |
|---|---|---|
| **Framework** | Next.js 15 (App Router) | Required for Frontend track; built-in routing, SSR support |
| **Language** | TypeScript 5 | Type safety, better DX, fewer runtime bugs |
| **Styling** | Tailwind CSS v3 + Shadcn UI | Fast, utility-first styling with accessible components |
| **State Management** | Zustand | Lightweight, simple API, perfect for client-side state |
| **Data Persistence** | LocalStorage + `db.json` (mock) | Simulates backend without a real server |
| **Icons** | Lucide React | Consistent, modern icon set |
| **Drag & Drop** | `@dnd-kit/core` | Accessible, performant DnD for Kanban cards |
| **Date Handling** | date-fns | Lightweight date formatting & calculations |
| **Forms** | React Hook Form + Zod | Validation and form state management |
| **Animations** | Framer Motion | Smooth transitions for cards, modals, sidebar |

---

## 🗂️ Designed Screens

> The following screens have been designed and are ready for implementation.

### 1. 🔐 Login Screen
> Clean, centered card layout with the **TaskMatrix** brand logo, email + password fields with icon buttons, a primary **Login** button, and a secondary **Signup** option separated by an "OR" divider. Built on a light gray background.

<img width="1246" height="811" alt="Login" src="https://github.com/user-attachments/assets/bdf4a006-1c43-4bb2-b1e7-64754a777f20" />

### 2. 📝 Sign Up Screen
> Two-column form layout collecting **First Name**, **Last Name**, **Email**, **Mobile Number**, **Password**, **Confirm Password**, and **Company Name**. Single full-width **Sign up** CTA button at the bottom.

<img width="1248" height="813" alt="Sign Up" src="https://github.com/user-attachments/assets/06cb43eb-0085-4ea2-ae56-f0286e1dd420" />

### 3. 📊 Dashboard Screen
> Analytics-focused overview page featuring:
> - **Task Status Overview** bar chart (Backlog 26%, In Progress 33%, In Review 13%, Done 28%)
> - **Task Completed**, **Pending Tasks**, and **Upcoming Deadlines** stat cards with month-over-month deltas
> - **Status Breakdown** grid showing per-column task counts
> - **Task Calendar** widget with a weekly timeline view of upcoming tasks
> - Left sidebar with Menu (Dashboard, Tasks, Projects), Insights (Notes, Reports, Progress, Goals), Communication (Team, Messages), and System (Dark Mode toggle, Settings, Help)

<img width="1266" height="805" alt="Dashboard" src="https://github.com/user-attachments/assets/d55dc149-82ad-4f39-98dc-a96de7657d17" />

### 4. 📋 Kanban Board (Task Details) Screen
> Full Kanban board view with:
> - **4 columns**: To-do , In Progress , In Review , Completed
> - Task cards showing due date, priority tag (Critical / High / Medium / Low), project name, progress bar, assignee avatars, and attachment/comment counts
> - **At Risk / On Track / Off Track** status badges on cards
> - Top bar with **Sort**, **List**, **Kanban**, **Calendar**, **Timeline** view toggles
> - **Import Task** and **+ Add Task** action buttons

<img width="1242" height="810" alt="Task Details" src="https://github.com/user-attachments/assets/14474484-99ad-4954-871f-4299becadcef" />

---

## 🏗️ Architecture Diagram

The state tree has been finalized and is split into **5 Zustand stores**: `authStore`, `userStore`, `taskStore`, `projectStore`, and `uiStore`.

<img width="1115" height="823" alt="State Tree" src="https://github.com/user-attachments/assets/e3b1f58a-94a3-46ab-8933-0b9652dffcbc" />

---

## ✅ Core Features (MVP — Week 14 Target)

### 🔐 Authentication (Mocked)
- [ ] Login page with email + password *(screen designed ✅)*
- [ ] Sign up page with full registration form *(screen designed ✅)*
- [ ] Role-based access: `Admin`, `Member`, `Viewer`
- [ ] Persisted session via LocalStorage
- [ ] Protected routes (redirect to login if unauthenticated)

### 📋 Kanban Board
- [ ] Columns: **To-do → In Progress → In Review → Completed** *(screen designed ✅)*
- [ ] Drag-and-drop cards between columns (`@dnd-kit`)
- [ ] Add new tasks via modal form (`+ Add Task` button)
- [ ] Import tasks via `Import Task` button
- [ ] Edit and delete tasks
- [ ] Column task count badge
- [ ] View toggle: **List**, **Kanban**, **Calendar**, **Timeline**

### 🗃️ Task Management
- [ ] Task title, description (rich text)
- [ ] Assignee (select from team members)
- [ ] Due date picker
- [ ] Priority tags: `Critical`, `High`, `Medium`, `Low`
- [ ] Status badges: `At Risk`, `On Track`, `Off Track`, `Set Status`
- [ ] Progress bar per task card
- [ ] Labels / Tags (e.g., `bug`, `feature`, `design`)
- [ ] Attachment count and comment count on cards
- [ ] Subtask checklist inside each task

### 👥 Team Management
- [ ] View all team members and their roles
- [ ] Assign/unassign members to tasks
- [ ] Admin can invite (mock) or remove members
- [ ] `+ Add Member` shortcut in top navigation

### 📡 Activity Feed
- [ ] Real-time-style feed showing: task creation, status changes, assignments
- [ ] Timestamps for each activity
- [ ] Filtered by project or user

### 🔍 Filtering & Search
- [ ] Filter tasks by: Assignee, Priority, Due Date, Label
- [ ] Global search bar (searches task titles + descriptions) — `⌘F` shortcut shown in UI

---

## 📊 Dashboard Features (Designed ✅)

- **Task Status Overview** — Bar chart showing status distribution over time
- **Task Completed** — Count with % change from last month
- **Pending Tasks** — Count with % change from last month
- **Upcoming Deadlines** — Count with % change from last month
- **Status Breakdown** — Per-column task counts (To-do, In Progress, In Review, Completed)
- **Task Calendar** — Weekly timeline with task events

---

## 🚀 Extended Features (Week 15–16 Target)

| Feature | Week |
|---|---|
| Dashboard analytics (task count by status, burndown) | Week 15 |
| Dark mode toggle *(toggle visible in sidebar design)* | Week 15 |
| Notifications panel *(bell icon in top nav)* | Week 15 |
| AI-powered task description generator (Claude API) | Week 16 |
| AI-powered priority auto-suggestion | Week 16 |
| Export board as CSV | Week 16 |

---

## 🎯 User Stories

| As a... | I want to... | So that... |
|---|---|---|
| Team Member | See all tasks on a Kanban board | I can understand the project status at a glance |
| Team Member | Drag tasks between columns | I can update status without clicking through menus |
| Team Member | View task details in a modal | I can see full description, assignee, and subtasks |
| Admin | Assign tasks to team members | I can distribute work across the team |
| Admin | Set task priority and due dates | I can communicate urgency clearly |
| Admin | View the activity feed | I can track who changed what and when |
| Any User | Filter tasks by assignee or priority | I can focus only on what's relevant to me |
| Any User | Search for a specific task | I can quickly find tasks without scrolling |
| Any User | See a dashboard with task stats | I can get a quick overview without opening the board |

---

## 📅 Weekly Delivery Plan

| Week | Goal |
|---|---|
| **Week 13** | ✅ PRD, Figma Designs (Login, Signup, Dashboard, Kanban), State Architecture |
| **Week 14** | Build MVP: Auth, Kanban Board, Task CRUD |
| **Week 15** | Full Feature Completion: Filters, Team page, Activity Feed |
| **Week 16** | AI Integration (task description/priority), Polish, Dark Mode |
| **Week 17** | Final Deployment (Vercel), Demo Video, Go Live |

---

## 🔗 Links

| Resource | URL |
|---|---|
| GitHub Repository | https://github.com/The-Nikita-Kumari/prodesk-capstone-taskmatrix |
| Figma Designs | https://www.figma.com/design/4uNVktfrekCKT88AI4NKAS/TaskMatrix-Layouts?node-id=0-1&p=f&t=0CMUi7Gbk05sCimd-0 |
