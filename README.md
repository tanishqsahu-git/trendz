# Trendz


## About the Project

Trendz is a full-stack app with features like AI-moderation, realtime, infinite-scroll, Auth, image-upload, posts, comments, likes, follows, uploads, stories, profiles and more. This project is built using Typescript, React, Express, React Query, PostgreSQL and so on. We will be implementing the features with Context APIs to maintain simplicity as much as possible so that anyone can understand the process.


## How to navigate the Project ?

The project consists of two folders `client` and `server`. Both are responsible for handling frontend and backend features respectively. Below are the details on how the client and server folders are structured to better understand the architecture of the application.

### Frontend folder structure:

Here's an overview of the project's frontend folder structure:

```
📂client/
    ├── public/             # Public assets and HTML template
    ├── src/
    │   ├── assets/         # Assets / files used in the application
    │   ├── assets/         # All configs for endpoints
    │   ├── components/     # Reusable React components
    │   ├── hooks/          # Reusable custom hooks
    │   ├── context/        # React context apis
    |   |   |
    |   │   ├── darkModeContext.tsx   # Handles toggle for dark mode
    |   │   └── authContext.tsx       # Handles authentication (Login)
    |   |
    │   ├── pages/          # Top-level application pages
    |   ├── types/          # Custom and global types defined
    │   ├── utils/          # Utility functions and constants
    │   ├── App.css         # Styles for App.tsx
    │   ├── App.tsx         # Main client-side application file
    │   ├── index.css       # Global css file
    │   └── main.tsx        # All Routes & protected routes are handled here
    └── index.html          # Root html file
    └── package.json        # Dependencies for the client-side
    └── tsconfig.json       # Typescript configuration
    └── ...
```

### Backend folder structure:

Here's an overview of the project's backend folder structure:

```
📂server/
    ├── src/
    │   ├── __tests__/      # All test cases
    │   ├── config/         # All endpoint configurations
    │   ├── controllers/    # Controllers consists of logic for routes
    │   ├── db/             # Database configuration and setup
    │   ├── middlewares/    # Middleware configs and setup
    │   ├── routes/         # Routes for all features
    │   ├── utils/          # Utility files
    │   ├── validations/    # Zod validations
    │   └── main.ts         # root file for server
    │
    └── .eslintrc           # eslint config
    └── .prettierrc         # prettier config
    └── .env                # environment variables
    └── package.json        # Dependencies for the server-side
    └── tsconfig.json       # Typescript configuration
    └── ...
```

## Features ✨

-   **User Authentication**: Users can create accounts, log in, and securely access their personalized profiles. We have used JWT for user authentication feature.
-   **Infinite-scroll**: Using react-query, user will now be able to experience infinite scroll features on posts.
-   **Responsive Design**: Enjoy a consistent and visually appealing experience across various devices.
-   **User Profile**: User can manage their profile info and edit them.
-   **Upload Posts**: User can post their thoughts or memories with or without images attached. File upload managed through AWS S3 and Cloudfront.
-   **Comments**: User can comment on the posts made by their followers.
-   **Likes**: User can like any post.
-   **Activities**: Get realtime activity of users posting or commenting.
-   **Moderator**: This uses an AI-powered moderator to ban users related on content.
-   **Follow**: Users can follow others to view their posts.
-   **Stories**: Add weekly stories to your profile for other users to view. This will be auto-deleted post 1 week.
-   **Image Upload**: Images are supported upto 20MB for any uploads.
-   **Ban System**: This is directly connected to moderator. Once detected user will be added to banned records.
-   **Realtime**: This feature displays all the online friends available at the moment in realtime.

## Installation 💻

To make the whole application run locally on your computer, you have to run both `client` and `server` separately in the terminal simultaneously. You will also need to setup your own AWS S3, .env file and configure the endpoints in both client and server using `config/config.ts` file.

### Project setup:

Follow the steps below to setup the project locally:

1. Clone the repository:

    ```bash
    git clone https://github.com/tanishqsahu-git/trendz
    ```

2. Navigate to the project directory:

    ```bash
    cd trendz
    ```

> You can use `npm / yarn / pnpm`. Just replace `pnpm` with `npm` or `yarn` for all the commands.

### Frontend setup:

To run the client locally, follow the below steps:

1. Navigate to the client directory:

    ```bash
    cd client
    ```

2. Install the dependencies using pnpm / npm (make sure you have pnpm installed):

    ```bash
    pnpm install
    ```

3. Start the development server for frontend:

    ```bash
    pnpm start
    ```

4. Open your browser and visit `http://localhost:5173/` to access the frontend of LinkX application.

### Backend setup:

Setting up the server is similar to frontend setup given above. Follow the below steps:

1. Navigate to the api directory:

    ```bash
    cd server
    ```

2. Install the dependencies using npm:

    ```bash
    npm install
    ```

3. Start the development server for backend:

    ```bash
    npm start
    ```

4. Open your browser and visit `http://localhost:3000/` to access the backend of LinkX application.

> **Note**
> Make sure both client and server are running locally for the fullstack features to work.

### Testing:

Testing your code if it runs as expected can be done using the below command for server.
Integration and Unit tests cover almost all the functionalities that are critical for the application.
Make sure to follow `.env.example` file to get all the test cases working.

1. Navigate to server:

    ```bash
    cd server
    ```

2. Run all test cases:

    ```bash
    npm test
    ```

3. Run individual test cases based on the describe names:

    ```bash
    jest -t "<Any test case describe title here>"
    ```

## Technologies Used 🔧

### Frontend technologies:

-   **Vite**: Latest version of Vite is used for react frontend.
-   **Typescript**: TypeScript checks a program for errors before execution, ensures better developer experience.
-   **React**: JavaScript library for building user interfaces.
-   **Axios**: Promise-based HTTP client for making API requests.
-   **SCSS**: Sass is a preprocessor scripting language that is interpreted or compiled into Cascading Style Sheets.
-   **React Router**: react-router-dom V6 is used for the application routing.
-   **React Query**: Also knows as Tanstack query for better data fetching.
-   **Context-API**: Manage states across components with ease.
-   **Themes**: Both dark and light themes are included in the application using SCSS.

### Backend technologies:

-   **NodeJS**: NodeJS for backend is a pretty popular choice.
-   **Typescript**: TypeScript checks a program for errors before execution.
-   **Zod**: Zod for consistent input validation, data structuring, and error handling.
-   **ExpressJS**: NodeJS framework for backend.
-   **JWT**: Authentication management.
-   **PostgreSQL**: Supabase is used to manage our postgres database.
-   **AI Moderator**: AI detects any unsafe images uploaded and bans the user based on results.
-   **Realtime**: Manages realtime updates using websockets.



