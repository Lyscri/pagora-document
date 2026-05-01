# 💳 Pagora — Payment Gateway from Scratch

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)

> A complete, step-by-step guide and implementation of a payment gateway built from the ground up using Node.js and Express.

---

## 📖 About

**Pagora** is a full educational project that walks you through building a payment gateway from scratch. Whether you're a developer looking to understand how online payments work under the hood, or someone building their first e-commerce integration, Pagora covers the full cycle — from setting up your server to processing and confirming transactions securely.

📄 **Full documentation:** [https://lyscri.github.io/pagora-document/](https://lyscri.github.io/pagora-document/)

---

## ✨ Features

- 🔐 Secure payment flow design
- 🧾 Transaction processing and lifecycle management
- 🔁 Webhook handling for payment confirmation
- 🛡️ Input validation and error handling
- 📦 RESTful API built with Express
- 🧪 Ready-to-test endpoints and examples

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| **Node.js** | Runtime environment |
| **Express** | Web framework and API routing |
| **dotenv** | Environment variable management |

---

## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/) v16 or higher
- npm (comes with Node.js)

### Installation

1. **Clone the repository**

```bash
git clone https://github.com/lyscri/pagora.git
cd pagora
```

2. **Install dependencies**

```bash
npm install
```

3. **Set up environment variables**

Create a `.env` file in the root of the project:

```env
PORT=3000
PAYMENT_API_KEY=your_payment_provider_api_key
WEBHOOK_SECRET=your_webhook_secret
```

4. **Start the server**

```bash
npm start
```

The server will be running at `http://localhost:3000`.

---

## 📡 API Overview

### Create a Payment

```http
POST /api/payments
```

```json
{
  "amount": 5000,
  "currency": "USD",
  "description": "Order #1234",
  "customer_email": "user@example.com"
}
```

### Check Payment Status

```http
GET /api/payments/:id
```

### Webhook Listener

```http
POST /api/webhooks
```

Handles real-time payment status updates from the payment provider.

> 📘 For the full API reference and detailed explanation of each endpoint, visit the [documentation site](https://lyscri.github.io/pagora-document/).

---

## 📂 Project Structure

```
pagora/
├── src/
│   ├── routes/         # Express route definitions
│   ├── controllers/    # Business logic per route
│   ├── middlewares/    # Auth, error handling, validation
│   └── services/       # Payment provider integrations
├── .env.example
├── package.json
└── README.md
```

---

## 🧪 Testing

Run the test suite with:

```bash
npm test
```

You can use tools like [Postman](https://www.postman.com/) or [cURL](https://curl.se/) to test the API endpoints manually.

---

## 📚 Documentation

The complete guide — including architecture decisions, flow diagrams, and code walkthroughs — is available here:

🔗 [https://lyscri.github.io/pagora-document/](https://lyscri.github.io/pagora-document/)

---

## 🤝 Contributing

Contributions are welcome! If you'd like to improve this project:

1. Fork the repository
2. Create a new branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m 'Add your feature'`
4. Push to the branch: `git push origin feature/your-feature`
5. Open a Pull Request

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 👤 Author

Made with ❤️ by [@lyscri](https://github.com/lyscri)
