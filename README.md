# Ecommerce Website (MERN)

A full-stack e-commerce website built with MongoDB, Express, React and Node.js.
Based on the Amazona tutorial project, updated to run on modern Node.js (18+)
and the latest Mongoose.

## Features

- Product listing with search, filters (category, price, rating) and sorting
- Shopping cart, shipping address, payment (PayPal) and order tracking
- User registration, sign in (JWT) and profile page
- Seller and admin dashboards: products, orders, users, sales charts
- Live chat support (Socket.io)

## Tech stack

- React, Redux, React Router, Axios
- Node.js, Express, JWT, Multer, Socket.io
- MongoDB with Mongoose

## Run locally

Requirements: Node.js 18 or newer (20 LTS recommended) and a MongoDB database.

### 1. Setup MongoDB

Either use a free cluster from [MongoDB Atlas](https://cloud.mongodb.com) or a local MongoDB.

For Atlas, copy `.env.example` to `.env` in the root folder and set your own values:

```
MONGODB_URL=mongodb+srv://USER:PASSWORD@cluster0.xxxxx.mongodb.net/amazona?retryWrites=true&w=majority
JWT_SECRET=a-long-random-string
```

With a local MongoDB you do not need a `.env` file (it uses `mongodb://localhost/amazona`).

### 2. Run the backend

```
npm install
npm run dev
```

It should print `Serve at http://localhost:5000` and `MongoDB connected`.
(`npm start` runs the same server without auto-restart, for production.)

### 3. Run the frontend

In a second terminal:

```
cd frontend
npm install
npm start
```

The site opens at http://localhost:3000.

### 4. Seed users and products

Open these two links in the browser, in this order:

- http://localhost:5000/api/users/seed
- http://localhost:5000/api/products/seed

### 5. Sign in

Go to http://localhost:3000/signin

- Admin: `admin@example.com` / `1234`
- User: `user@example.com` / `1234`

## Deployment

Set `MONGODB_URL` and `JWT_SECRET` as environment variables on your host
(for example Render). The seed links are disabled when `NODE_ENV=production`;
set `ALLOW_SEED=true` temporarily if you need to seed a production database.

## Credits

Original tutorial by Basir (Amazona). This version was updated and maintained by Maryam Alkurd.il and password and click signin
