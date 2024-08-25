# Objective: 
Develop a single-page Telegram Mini app/Web app named "TapMe" where users can earn coins by tapping a button like TapSwap (https://t.me/tapswap_bot). Functionality is a simple CRUD operation. Ensure the app includes basic tap animations to enhance the user experience. The implementation should be done in TypeScript. 


# Requirements:
* Frontend: Use React.js with TypeScript for the web app interface.
* Backend: Use Node.js with TypeScript and GraphQL-Yoga for the GraphQL server.
* Database: Use Supabase to store user information and game data.
* Telegram Integration: Use Telegram's Bot API to handle user interactions.
* Design: Ensure the application is responsive,  optimized for mobile screen and includes basic tap animations.
* Features:
   Clicker Game:
    * Users can tap a button to earn coins.
    * Display the user's total coin balance on the tap page.
    * Implement basic tap animations for better user experience (check out Tap UX of reference games below by checking them out)
    * Ensure real-time updates for the coin balance (feel free to use your own strategy to update user balance on remote supabase database to avoid too many requests)
* Telegram Bot:
* Create a Telegram bot to handle user interactions and commands.
* Use commands like /start to interact with the game.

# Step-by-Step Implementation:

Step 1: Setup Telegram Bot (30 minutes)
* Create a Telegram bot using BotFather:
* Follow the BotFather instructions to create a new bot and obtain the bot token.
  (https://t.me/botfather)
* Set up the bot to handle commands for the clicker game:
* Create a simple /start command to interact with the game.
(Reference - https://github.com/revenkroz/telegram-web-app-bot-example)

Step 2: Frontend Development (3 hours)
* Set up a React.js project with TypeScript for the web app:
* Create a new React.js project using Create React App with TypeScript template or a similar tool.
* Develop the clicker game interface:
  * Create a button for users to tap and earn coins. (Feel free to take Tap button inspiration from reference Tap games screenshots below)
  * Implement basic tap animations to enhance the user experience.
  * Display the user's total coin balance on the tap page.
  * Ensure real-time updates for the coin balance (based on your chosen read/write strategy)
  * Host the web app:
  * Deploy the React.js app on a quick and easy hosting service like Vercel or Netlify (FREE version).

Step 3: Backend Development (2 hours)
* Set up a Node.js project with TypeScript for the backend:
* Create a new Node.js project and set up the necessary dependencies (e.g., GraphQL-Yoga, TypeScript).
* Set up Supabase to store user information and game data:
* Create a simple table for users and their coin balances in Supabase.
* Use Supabase's API to interact with the database (FREE version)
* Implement GraphQL schema and resolvers:
* Define a simple schema to support queries and mutations for retrieving and updating coin balances.

Step 4: Integration (1-2 hours)
* Integrate the Telegram bot with the backend:
* Insert new users in the db when they interact with our bot using /start command
* Integrate the frontend web app with the GraphQL server:
* Use Apollo Client to connect the React app to the GraphQL server.
* Ensure seamless communication between the frontend and backend for displaying coins.



# Tools and Technologies:
* Frontend: React.js, TypeScript
* Backend: Node.js, TypeScript, GraphQL-Yoga
* Database: Supabase
* Telegram: Bot API 
* Deployment: Vercel, Netlify (or similar hosting service)
* Deliverables:
* A fully functional mini clicker game "TapMe" as a Telegram Mini app/Web app.


# How will users(reviewers) use this game?
* Users open their telegram mobile app.
* They go to the "GameTabBot" bot
* They click  /start command
* Mini app (game) should launch (in full screen mode)
* Users should be able to Tap the main Tap button (use any fancy button/image you like)
* Users can see their coins updating in real-time with each Tap (these coin balance is persisted in Supabase database so that users can see their updated balance every time they open the TapMe game)
