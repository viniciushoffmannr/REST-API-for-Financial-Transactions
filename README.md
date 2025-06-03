# 💰 REST API for Financial Transactions

A high-performance Node.js REST API for managing financial transactions built with Fastify, Knex, and SQLite.

## ✨ Features

- ✅ Create new transactions (credit/debit)
- ✅ List all transactions
- ✅ Get account summary
- ✅ View specific transaction details
- ✅ Session-based user identification

## 📋 Business Rules

- ✅ Transactions can be credit (adds to total) or debit (subtracts from total)
- ✅ User identification across requests via cookies
- ✅ Users can only view transactions they created

## 🛠️ Technologies

- **⚡ Fastify**: High-performance web framework
- **🔄 Knex**: SQL query builder
- **🗃️ SQLite**: Database
- **📘 TypeScript**: Type safety
- **✓ Zod**: Schema validation
- **🧪 Vitest**: Testing framework

## 🚀 Getting Started

### Prerequisites

- Node.js >= 18

### Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/transactions-api.git
cd transactions-api
```

2. Install dependencies
```bash
npm install
```

3. Create environment file
```bash
cp .env.example .env
```

### Running the Application

1. Run database migrations
```bash
npm run knex -- migrate:latest
```

2. Start the development server
```bash
npm run dev
```

The server will be running at http://localhost:3333 🚀

## 🔌 API Endpoints

### Create Transaction
```
POST /transactions
```
Body:
```json
{
  "title": "Salary",
  "amount": 5000,
  "type": "credit"
}
```

### List All Transactions
```
GET /transactions
```

### Get Account Summary
```
GET /transactions/summary
```

### Get Specific Transaction
```
GET /transactions/:id
```

## 🧪 Testing

Run the test suite:
```bash
npm test
```

## 🏗️ Building for Production

```bash
npm run build
```

The compiled files will be available in the `build` directory.


