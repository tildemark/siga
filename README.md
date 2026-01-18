## 📂 S.I.G.A. (Synchronized Interface for Gadget Automation)

**S.I.G.A.** is a high-performance, cross-platform management interface for **BSD61+ Smart Plugs** and Tuya-compatible devices. Built with a modern web stack and optimized for local-first control.

### 🛠 The Stack

* **Framework:** Next.js 15 (App Router) + Turborepo
* **Database:** Postgres & Prisma ORM
* **Speed:** Redis for real-time state synchronization
* **Desktop:** Tauri (Windows System Tray integration)
* **Mobile:** PWA (Progressive Web App)
* **Deployment:** OCI Ampere Always Free (Ubuntu)

### 🚀 Key Features

* **Instant Toggle:** Sub-second response times using `tuyapi` local protocol.
* **Tray Access:** Quick-control your home directly from the Windows Taskbar.
* **Unified Dashboard:** One codebase powering your Web, Android, and Desktop experience.

---

### Your First Move in the Repo

Since you're using **Turborepo** and **pnpm**, I recommend initializing the project with this structure:

1. `apps/web`: Your Next.js core.
2. `apps/desktop`: Your Tauri wrapper.
3. `packages/database`: Shared Prisma schema.
4. `packages/iot-logic`: Shared `tuyapi` connection utilities.

