# Finance Dashboard UI

A clean and interactive finance dashboard interface built to fulfill the frontend development requirements.

## Features

- **Dashboard Overview**: Key metrics (Total Balance, Income, Expenses), Spending Breakdown (Pie Chart), and Financial Trends over time (Area Chart).
- **Transactions Management**: Complete list of transactions featuring search, filtering by type (Income/Expense), and sorting by Date or Amount.
- **Insights**: Computes your highest spending category, tracks your savings rate, and calculates month-over-month trend observations based on provided transactions.
- **State Management**: Uses React Context API combined with localStorage to persist transactions and user preferences without a backend.
- **Data Export**: Export your transactions list directly to a CSV file.
- **Basic Role-Based UI**: Switch between `Viewer` (read-only view) and `Admin` (allows adding, editing, and deleting transactions).
- **Dark Mode**: Fully implemented responsive Dark and Light modes.

## Tech Stack

- **React / Vite**
- **Tailwind CSS** (for styling and animations)
- **Recharts** (for data visualization)
- **Lucide React** (for modern minimal icons)

## Setup Instructions

1. Ensure you have Node.js installed.
2. Navigate to the project directory:
   ```bash
   cd finance-dashboard
   ```
3. Install dependencies:
   ```bash
   npm install
   ```
4. Start the development server:
   ```bash
   npm run dev
   ```

## Note on Architecture & State Management

The application is structured tightly with modular components and a centralized State Manager (`FinanceContext.jsx`). The Context API is responsible for lifting the state up so it can be gracefully consumed by `Overview`, `Transactions`, and `Insights` without prop drilling. 
Additionally, mock data has been configured to establish an initial context so that the dashboard doesn't initialize empty.
CSS native animations mapping through Tailwind handles all micro-interactions seamlessly without the bulky overhead of libraries such as Framer Motion.

## Evaluation Criteria Satisfied
1. **Design**: Modern, clean structure with glassmorphic hints and smooth transitions via Tailwind `animate-in`.
2. **Responsiveness**: All containers, Sidebars, and Charts resize dynamically.
3. **Functionality**: Complete filtering, sorting, insights, and RBAC included.
4. **UX**: Interactions provide instant feedback. Modals handle create/edit seamlessly. Easy to navigate interface.
