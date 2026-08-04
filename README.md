# 🛍️ LuXora Essence — E-Commerce Website

LuXora Essence is a stylish, modern e-commerce website with a working authentication backend. Built with a Node.js + Express server and a static HTML/CSS/JS frontend.

**Live site:** https://ecommerce-website-rho-sable.vercel.app
**GitHub Pages (frontend only, no backend):** https://akritisaha20.github.io/Ecommerce-website-/

---

## ✨ Features

- Homepage with hero banner and "Shop the Latest Trends" section
- Popular Categories carousel (Swiper.js)
- Product listings with ratings, pricing, wishlist and cart icons
- Wishlist and Cart pages
- Login / Sign Up pages with real backend authentication
- My Account page
- Fully responsive, styled UI

---

## 🧱 Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML, CSS, JavaScript (Swiper.js, Flaticon UIcons) |
| Backend | Node.js + Express.js |
| Data Storage | Local `users.json` file (via Node's `fs` module) |
| Auth | bcrypt password hashing |
| Deployment | Vercel |

> **Note:** This project does not use React or a cloud database — it's a Node + Express backend with a static frontend and file-based user storage. This keeps the project simple and dependency-free, with no external database setup required.

---

## 📂 Project Structure

```
Ecommerce-website-/
├── index.html            # Homepage
├── shop.html              # Product listing page
├── cart.html               # Shopping cart
├── wishlist.html           # Wishlist page
├── login-register.html     # Auth pages
├── accounts.html           # My Account page
├── details.html            # Product detail page
├── assets/
│   ├── css/styles.css
│   └── img/                 # Product images, icons, banners
├── server.js               # Express backend (serves frontend + API)
├── users.json               # Auto-created; stores registered users (gitignored)
├── vercel.json              # Deployment config (includes static assets)
├── package.json
├── package-lock.json
└── .gitignore
```

---

## 🔌 Backend API

| Method | Route | Description |
|---|---|---|
| POST | `/api/register` | Creates a new user (username, email, password). Password is hashed with bcrypt before saving to `users.json`. |
| POST | `/api/login` | Validates email and password against stored users. |
| GET | `/` | Serves the homepage and other static frontend files. |

---

## ⚙️ Setup

1. Clone the repository
   ```bash
   git clone https://github.com/akritisaha20/Ecommerce-website-.git
   cd Ecommerce-website-
   ```

2. Install dependencies
   ```bash
   npm install
   ```

3. Start the server
   ```bash
   node server.js
   ```
   or, for auto-restart during development:
   ```bash
   npx nodemon server.js
   ```

4. Open your browser to
   ```
   http://localhost:5000
   ```

A `users.json` file will be created automatically the first time someone registers.

---

## 🚀 Deployment

Deployed on [Vercel](https://vercel.com) as a Node.js serverless function. A `vercel.json` config file ensures static assets (`assets/`, `.html` files) are correctly included in the deployment, since Vercel's zero-config Node.js builds don't automatically bundle static files alongside a server entry point.

Any push to the `main` branch triggers an automatic redeploy.

---

## 🔐 Security Notes

- Passwords are hashed with bcrypt before being stored — plain-text passwords are never saved.
- `users.json` is excluded from Git via `.gitignore`, so real user data never gets pushed to GitHub.
- This project previously used MongoDB Atlas; it was removed in favor of local file storage to eliminate external dependencies and credential management.

---

## ⚠️ Known Limitation

Since user data is stored in a local JSON file rather than a persistent cloud database, data may reset when Vercel's serverless function restarts or redeploys (serverless environments don't guarantee persistent file writes across invocations). This setup is well-suited for demos and portfolios; for production use with permanent data storage, a real database (MongoDB, PostgreSQL, Supabase, etc.) would be the next step.

---

Feel free to explore the code and suggest improvements!