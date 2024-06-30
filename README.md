![Screenshot (8)(1)](https://github.com/PRINCEMISHRAJI/Botcoin/assets/50262987/da881cae-8e99-4e4c-a293-0e504859760c)

Author : Ankit Mishra


Botcoin
Botcoin is a React-based web application that displays points and energy levels with a dynamic, interactive UI. Users can click on the main coin image to earn points, and the application visually displays the energy consumption and point increments with animations.
Available to use at : https://botcoin-boxx.onrender.com or https://t.me/MineBotcoin_Bot/mine


Features
Interactive Clicks: Users can click on the main coin to earn points.
Animated Points: Points added by clicks are displayed with animations.
Energy Management: Energy decreases with clicks and regenerates over time.
Responsive UI: Adaptable and visually appealing UI using Tailwind CSS.
Technologies Used
React: JavaScript library for building user interfaces.
Vite: Next-generation front-end tooling.
Tailwind CSS: Utility-first CSS framework for rapid UI development.
Getting Started
Prerequisites
Make sure you have the following installed:

Node.js (v14 or later)
npm (v6 or later) or yarn
Installation
Clone the repository:
bash
Copy code
git clone https://github.com/PRINCEMISHRAJI/Botcoin.git
cd Botcoin
Install dependencies:
bash
Copy code
npm install
or

bash
Copy code
yarn install
Development
To run the application in development mode, use:

bash
Copy code
npm run dev
or

bash
Copy code
yarn dev
Open http://localhost:5173 to view it in the browser.

Production
To build the application for production, use:

bash
Copy code
npm run build
or

bash
Copy code
yarn build
This will create an optimized build in the dist folder.

To serve the production build, use:

bash
Copy code
npm run serve
or

bash
Copy code
yarn serve
Deployment
The application is designed to be deployed on Render. Here are the necessary configurations:

Render Configuration
Create a render.yaml file:
yaml
Copy code
services:
  - type: web
    name: botcoin-app
    env: node
    plan: free
    buildCommand: npm install && npm run build
    startCommand: npm run serve
    envVars:
      - key: NODE_ENV
        value: production
Set the PORT environment variable in Render's environment settings (usually set automatically).
Vite Configuration
Ensure your vite.config.js binds to 0.0.0.0:

js
Copy code
import { defineConfig } from 'vite';

export default defineConfig({
  server: {
    host: '0.0.0.0',
    port: process.env.PORT || 5173,
  }
});
Contributing
Contributions are welcome! Please open an issue or submit a pull request for any changes or improvements.

Contact
For any questions or suggestions, feel free to contact the repository owner.
