# 🪙 Wallet Tracker - Expenditure Tracker with R-N & Express 💸

Welcome to Wallet Tracker, a modern, mobile-first application designed to help you manage your finances with ease. This full-stack project features a secure backend API and an intuitive React Native mobile application, allowing users to track their income and expenses seamlessly.

This project was built from the ground up, covering everything from database design and secure authentication to deployment on modern cloud platforms.

## 📸 Screenshots

Here's a glimpse of the application's user flow and core features.

| Sign Up ✅ | Verify Email 🪄 | Sign In 🔑 |
| :---: | :---: | :---: |
| <img src="https://github.com/itsUdit24/wallet-tracker-rn-app/blob/main/screenshots/signup-screen.jpg?raw=true" alt="Sign Up Screen" width="350"/> | <img src="https://github.com/itsUdit24/wallet-tracker-rn-app/blob/main/screenshots/verify-screen.jpg?raw=true" alt="Verify Email Screen" width="350"/> | <img src="https://github.com/itsUdit24/wallet-tracker-rn-app/blob/main/screenshots/signin-screen.jpg?raw=true" alt="Sign In Screen" width="350"/> |

| Home Screen 🏡 | New Transaction 📝|
| :---: | :---: |
| <img src="https://github.com/itsUdit24/wallet-tracker-rn-app/blob/main/screenshots/home-screen.jpg?raw=true" alt="Home Screen with Transactions" width="350"/> | <img src="https://github.com/itsUdit24/wallet-tracker-rn-app/blob/main/screenshots/create-screen.jpg?raw=true" alt="New Transaction Screen" width="350"/> |


## ✨ Features

- ✅ **Secure User Authentication 🔐:** Full sign-up and sign-in functionality, including email verification, powered by Clerk.
- ✅ **Transaction Management 🪙:** Users can create, view, and delete their income and expense records.
- ✅ **Financial Summary 💵:** A dashboard that provides an at-a-glance view of total balance, total income, and total expenses.
- ✅ **Categorization 📝:** Simple and intuitive category selection for each transaction.
- ✅ **Authenticated API 🧑🏻‍💻:** All API endpoints are protected, ensuring users can only access their own financial data.
- ✅ **Real-time Updates 🔃:** Pull-to-refresh functionality on the home screen to fetch the latest transactions.
- ✅ **Create Screen ➕:** To add income or expense transactions.
- ✅ **Delete transactions 🗑️:** To update balance.
- ✅ **Logout 🚪:** To navigate back to login screen.
  

## 🛠️ Tech Stack

This project utilizes a modern, full-stack JavaScript/TypeScript toolset.

| Area | Technology |
| :--- | :--- |
| **Frontend** | React Native, Expo, Expo Router |
| **Backend** | Node.js, Express.js |
| **Database** | PostgreSQL (hosted on Neon) |
| **Authentication**| Clerk |
| **Deployment** | Render.com (Backend), EAS (Mobile App) |
| **API Tools** | Postman |
| **Rate Limiting**| Upstash Redis |


## 🚀 Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

- Node.js (v18 or later)
- npm
- Git

## Local Development Setup ⚙️

This project is split into two parts: `backend` and `mobile`. You will need to run them in two separate terminals.

1.  Clone the repository (or repositories).
    ```sh
    git clone <your-repo-url>
    cd <your-repo-folder>
    ```

2.  **Set up the Backend:**
    - In your first terminal, navigate to the backend folder.
        ```sh
        cd backend
        ```
    - Install the dependencies.
        ```sh
        npm install
        ```
    - Create a `.env` file in the `backend` folder and add your secret keys (see the `.env.example` section below).
    - Start the backend server.
        ```sh
        npm run dev
        ```
    - The server will be running on `http://localhost:3000`.

3.  **Set up the Frontend (Mobile App):**
    - In a **second, separate terminal**, navigate to the mobile folder.
        ```sh
        cd mobile
        ```
    - Install the dependencies.
        ```sh
        npm install
        ```
    - Create a `.env` file in the `mobile` folder and add your public keys (see the `.env.example` section below).
    - Start the Expo development server.
        ```sh
        npx expo start
        ```
    - Scan the QR code with the Expo Go app on your phone.

### Environment Variables

You will need to create two `.env` files for this project to run.

**`backend/.env.example`**
```env
# Port for the local server
PORT=3000

# Full connection string from your Neon dashboard
DATABASE_URL=<your_neon_postgres_connection_url>

# Keys from your Upstash dashboard for rate limiting
UPSTASH_REDIS_REST_URL=<your_redis_connection_url>
UPSTASH_REDIS_REST_TOKEN=<your_redis_rest_token>

# Secret key from your Clerk dashboard
CLERK_SECRET_KEY=<your_clerk_secret_key>

# URL of your live server (for the cron job to keep it awake)
API_URL=<your_api_connection_url>
