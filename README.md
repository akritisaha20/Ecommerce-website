# \# Ecommerce-website- (LuXora Essence)

# 

# LuXora Essence is a stylish and user-friendly e-commerce website built with a \*\*Node.js + Express backend\*\* and a \*\*static HTML/CSS/JavaScript frontend\*\*. User accounts are stored locally in a JSON file — no external database required.

# 

# This project is designed to provide a clean, modern shopping experience with:

# 

# \- ⚡ Smooth user navigation

# \- 🛒 Essential features like wishlist, cart, login/register

# \- 🖥 Responsive and accessible UI

# \- 🔐 Secure authentication (bcrypt password hashing)

# 

# \## 🔧 Technologies Used

# 

# \- \*\*Frontend:\*\* HTML, CSS, JavaScript (with Swiper.js for carousels and Flaticon UIcons for icons) — no React is currently used

# \- \*\*Backend:\*\* Node.js \& Express.js

# \- \*\*Data Storage:\*\* Local JSON file (`users.json`) via Node's built-in `fs` module — no external database

# \- \*\*Auth:\*\* bcrypt for password hashing

# \- \*\*Deployment:\*\* Vercel

# 

# \## 📂 Project Structure

# 

# \- `index.html`, `shop.html`, `cart.html`, `wishlist.html`, `login-register.html`, `accounts.html`, `details.html` — Frontend pages

# \- `server.js` — Backend server logic (Express routes for register/login, JSON file storage)

# \- `users.json` — Local user data store (auto-created, not committed to Git)

# \- `assets/` — Static CSS, JS, and image assets

# \- `package.json` / `package-lock.json` — Project metadata \& dependencies

# \- `.gitignore` — Excludes `node\_modules/`, `users.json`, etc. from Git

# 

# \## ⚙️ Setup

# 

# 1\. Clone the repository

# &#x20;  ```bash

# &#x20;  git clone https://github.com/akritisaha20/Ecommerce-website-.git

# &#x20;  cd Ecommerce-website-

# &#x20;  ```

# 

# 2\. Install dependencies

# &#x20;  ```bash

# &#x20;  npm install

# &#x20;  ```

# 

# 3\. Start the server

# &#x20;  ```bash

# &#x20;  node server.js

# &#x20;  ```

# &#x20;  or, for auto-restart during development:

# &#x20;  ```bash

# &#x20;  npx nodemon server.js

# &#x20;  ```

# 

# 4\. Open `index.html` in your browser (or serve the folder with a static server) to view the frontend.

# 

# A `users.json` file will be created automatically the first time someone registers.

# 

# \## 🚀 Deployment

# 

# \- \*\*Live site:\*\* https://ecommerce-website-rho-sable.vercel.app

# \- Also available via GitHub Pages: https://akritisaha20.github.io/Ecommerce-website-/

# 

# \## 🔐 Security Notes

# 

# \- Passwords are hashed with bcrypt before being stored — plain-text passwords are never saved.

# \- `users.json` is excluded from Git via `.gitignore` so real user data never gets pushed to GitHub.

# 

# \## ⚠️ Note on Data Persistence

# 

# Since user data is stored in a local JSON file rather than a cloud database, data will only persist on the machine/server running the app. For a production deployment where data needs to persist across restarts or be shared across multiple servers, a proper database (like MongoDB, PostgreSQL, etc.) would be needed.

# 

# Feel free to explore the code and suggest improvements!

