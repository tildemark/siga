# S.I.G.A. 🚀

### **S**ynchronized **I**nterface for **G**adget **Automation**

**S.I.G.A.** (Cebuano: *Siga* - "to light up / power on") is a professional-grade, local-first management system for **BSD61+ Smart Plugs** and Tuya-compatible IoT devices. It provides a unified, low-latency interface across Web, Android, and Windows Tray.

---

## 🏗 System Architecture

S.I.G.A. is built on a "Brain-and-Bridge" architecture to ensure sub-second response times:

* **The Brain (Next.js):** Acts as the central command, managing the database, authentication, and the PWA frontend.
* **The Synchronizer (Redis):** Maintains real-time device states, ensuring the UI reflects the physical plug state instantly.
* **The Bridge (Tauri):** A lightweight Rust wrapper that brings S.I.G.A. to the Windows System Tray for instant access without opening a browser.
* **The Local Link (Tuyapi):** Communicates directly with devices on the LAN, bypassing the cloud for maximum speed.

---

## 🛠 Tech Stack

| Layer | Technology |
| --- | --- |
| **Monorepo** | [Turborepo](https://turbo.build/) + `pnpm` |
| **Frontend** | [Next.js 15](https://nextjs.org/) (App Router), Tailwind CSS |
| **Backend** | Node.js, [Prisma ORM](https://www.prisma.io/) |
| **Database** | PostgreSQL |
| **Caching/Real-time** | Redis |
| **Desktop** | [Tauri](https://tauri.app/) (Rust-based wrapper) |
| **Infrastructure** | OCI Always Free Ampere Instance (Ubuntu) |

---

## 🚀 Key Features

* **Low-Latency Toggling:** Uses local IP control to eliminate cloud-roundtrip lag.
* **Windows Tray Integration:** Minimize to tray; toggle your plugs with a single click from the taskbar.
* **Mobile-First PWA:** "Install" S.I.G.A. on Android for a native-like smart home app experience.
* **Smart State Sync:** Redis-backed state management ensures your dashboard is never out of sync with reality.
* **Developer Friendly:** Built with TypeScript and a modular monorepo structure.

---

## 📋 Getting Started

### Prerequisites

* Node.js (v20+)
* pnpm
* Docker (for local Postgres/Redis)
* Rust (for Tauri development)

### Installation

1. **Clone the repo:**
```bash
git clone https://github.com/tildemark/SIGA.git
cd SIGA

```


2. **Install dependencies:**
```bash
pnpm install

```


3. **Environment Setup:**
Copy `.env.example` to `.env` and fill in your Tuya API credentials and OCI database strings.
4. **Run Development Mode:**
```bash
pnpm dev

```



---

## 🚢 Deployment

S.I.G.A. is optimized for **Oracle Cloud Infrastructure (OCI)**.

* **Production Host:** Always Free Ampere Instance (ARM64).
* **Process Management:** PM2 or Docker Compose.
* **PWA:** Served via Next.js with `@serwist/next`.

---

## 🤝 Contributing


This is a personal project by **[tildemark](https://www.google.com/search?q=https://github.com/tildemark)**, focusing on the Cebu/CDO tech ecosystem. Feel free to fork, submit PRs, or report issues.

**License:** MIT

