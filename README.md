# dpin-uptime

## Overview
`dpin-uptime` is a decentralized uptime monitoring service. It allows for monitoring of website availability and performance, leveraging a network of validators to perform checks and record uptime data.

## Stack Used
This project is a monorepo managed with **Turborepo** and uses **Bun** as its package manager.

*   **Frontend**: Built with **Next.js**, **React**, and **TypeScript**.
*   **Backend (API)**: Developed using **Node.js**, **Express.js**, and **TypeScript**.
*   **Database**: **PostgreSQL**, managed with **Prisma ORM**.
*   **UI Components**: Custom components are developed within the `packages/ui` workspace.

## Installation

To set up the project locally, follow these steps:

1.  **Clone the repository**:
    ```bash
    git clone https://github.com/your-repo/dpin-uptime.git
    cd dpin-uptime
    ```

2.  **Install dependencies**:
    This project uses `bun` as its package manager.
    ```bash
    bun install
    ```

3.  **Database Setup**:
    Ensure you have a PostgreSQL database running and set the `DATABASE_URL` environment variable in a `.env` file at the root of the project.
    Example `.env` file:
    ```
    DATABASE_URL="postgresql://user:password@localhost:5432/dpin_uptime_db"
    ```
    Then, apply Prisma migrations to set up your database schema:
    ```bash
    bun prisma migrate dev
    ```

4.  **Run the development servers**:
    ```bash
    bun run dev
    ```
    This command will start both the frontend and API development servers.

## Documentation
For a detailed understanding of the project architecture, data flow, and component breakdown, please refer to the [Documentation](documentation.md).