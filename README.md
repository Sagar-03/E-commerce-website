# MERN Ecommerce

## Description

A full-featured ecommerce store built using the MERN stack (MongoDB, Express, React, Node.js) with integrations of third-party APIs. This platform facilitates three distinct user flows:

1. **Buyers:** Browse and shop products across various categories, brands, and collections.
2. **Sellers or Merchants:** Manage their own brand and product listings.
3. **Admins:** Oversee and control the entire platform, including users, orders, and products.

### Features:

- **Backend:** Powered by Node.js and Express.js for robust and scalable APIs.
- **Database:** MongoDB with Mongoose for seamless schema modeling and database management.
- **Frontend:** Developed using React for a dynamic and responsive user interface.
- **State Management:** Redux with Redux Thunk for efficient application state handling and asynchronous actions.
- **Authentication & Authorization:** JWT for secure user sessions.

## Demo

Experience the application live:
- [Ecommerce Store Demo](https://mern-store-gold.vercel.app) 😄
- [Admin Dashboard Demo](https://mernstore-bucket.s3.us-east-2.amazonaws.com/admin.mp4)

## Setup Guide

### Docker Guide

To run this project locally using Docker:

1. Clone the repository:
   ```bash
   git clone https://github.com/mohamedsamara/mern-ecommerce.git
   ```

2. Update the `docker-compose.yml` file with appropriate values for:
   - `MONGO_URI`
   - `JWT_SECRET`

3. Build and start the Docker containers:
   ```bash
   docker-compose build
   docker-compose up
   ```

### Database Seed

Initialize the database with an admin user:

1. Use the following command, replacing placeholders with your desired email and password:
   ```bash
   npm run seed:db [email@example.com] [password]
   ```

2. For more details, refer to the [seed script](server/utils/seed.js).

### Local Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/mohamedsamara/mern-ecommerce.git
   ```

2. Navigate to the project directory and install dependencies:
   ```bash
   cd mern-ecommerce
   npm install
   ```

3. Configure the environment variables by creating `.env` files in both `client` and `server` directories. Use these templates for guidance:
   - [Frontend .env](client/.env.example)
   - [Backend .env](server/.env.example)

4. Start the development server:
   ```bash
   npm run dev
   ```

## Deployment

This application is deployed on Vercel for both frontend and backend. To deploy:

1. Set the root directory as `client` or `server` during Vercel configuration.
2. Refer to the deployment settings for [frontend](client/vercel.json) and [backend](server/vercel.json).

## Languages & Tools

- **Backend:**
  - [Node.js](https://nodejs.org/)
  - [Express.js](https://expressjs.com/)
  - [MongoDB](https://www.mongodb.com/)
  - [Mongoose](https://mongoosejs.com/)

- **Frontend:**
  - [React](https://reactjs.org/)
  - [Redux](https://redux.js.org/)
  - [Webpack](https://webpack.js.org/)

## Code Formatting

To maintain code quality and consistency, use Prettier as the code formatter:

1. Create a `.vscode` directory in the project root.
2. Add a `settings.json` file with the following configuration:

   ```json
   {
     "editor.formatOnSave": true,
     "prettier.singleQuote": true,
     "prettier.arrowParens": "avoid",
     "prettier.jsxSingleQuote": true,
     "prettier.trailingComma": "none",
     "javascript.preferences.quoteStyle": "single"
   }
   ```

3. Install the Prettier extension in your editor (e.g., VSCode).

