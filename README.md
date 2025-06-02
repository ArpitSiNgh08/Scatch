# Scatch

A Node.js + Express e-commerce backend project with authentication, product management, cart, and admin features. Uses MongoDB (via Mongoose), EJS templating, and JWT-based authentication.

---

## Features

- **User Authentication** (JWT, sessions, flash messages)
- **Product Management** (CRUD, image upload with Multer)
- **Shopping Cart** (add to cart, cart view, price breakdown)
- **Admin Panel** (owners routes)
- **EJS Templating** (dynamic views)
- **MongoDB Integration** (Mongoose models)
- **Session & Cookie Management**
- **Flash Messages** for notifications

---

## Setup

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd Scatch
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Configure environment variables**

   Create a `.env` file in the root with:
   ```
   MONGODB_URI=your_mongodb_connection_string
   JWT_KEY=your_jwt_secret
   EXPRESS_SESSION_SECRET=your_session_secret
   ```

4. **Run the server**
   ```bash
   node app.js
   ```
   The app runs on [http://localhost:3000](http://localhost:3000)

---

## Project Structure

```
Scatch/
│
├── app.js
├── config/
│   └── mongoose-connection.js
├── models/
│   ├── product-model.js
│   └── user-model.js
├── routes/
│   ├── index.js
│   ├── ownersRouter.js
│   ├── productsRouter.js
│   └── usersRouter.js
├── middlewares/
│   └── isLoggedIn.js
├── views/
│   ├── cart.ejs
│   ├── shop.ejs
│   ├── index.ejs
│   └── partials/
│       ├── header.ejs
│       └── footer.ejs
└── public/
    └── ...static files...
```

---

## Notes

- **Image Uploads:** Product images are stored as binary in MongoDB and rendered as base64 in EJS.
- **Authentication:** Uses JWT in cookies and session middleware.
- **Flash Messages:** Used for error/success notifications.
- **Cart:** Each user has a cart (array of product ObjectIds).

---

## License

MIT
