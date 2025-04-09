﻿# Credit-Bee
#!/bin/bash

cat << 'EOF' > README.md
# 🐝 BeeTrail Field Logger

BeeTrail is a field-logging backend system for managing beehives and crop data. It supports role-based access control (beekeeper/admin), geo-filtered crop search, CSV exports, sync token for offline support, and a Swagger API for documentation.

---

## 🌐 Live API Endpoints

| Feature           | Endpoint                          | Method | Auth Required | Description                           |
|------------------|-----------------------------------|--------|----------------|---------------------------------------|
| Add Hive          | `/api/hives`                      | POST   | ✅             | Add a new hive                        |
| Get All Hives     | `/api/hives`                      | GET    | ✅             | Fetch all hives                       |
| Export CSV        | `/api/hives/export`               | GET    | ✅             | Download hive data as CSV             |
| Add Crop          | `/api/crops`                      | POST   | ✅             | Add new crop                          |
| Get Nearby Crops  | `/api/crops/nearby`               | GET    | ✅             | Get crops by geo + date filter        |
| Get Sync Token    | `/api/sync-token`                 | GET    | ✅             | Get a sync token for offline support  |
| Admin Dashboard   | `/admin`                          | GET    | ❌             | Basic HTML dashboard with data stats  |
| Swagger Docs      | `/api-docs`                       | GET    | ❌             | Swagger UI for API testing            |

---

## 🔐 Authentication

All protected routes require a **Bearer Token** in the `Authorization` header:


How to Run Locally
Clone this repository:

bash
Copy code
git clone https://github.com/your-username/beetrail-field-logger.git
cd beetrail-field-logger


Install dependencies:
npm install


Create a .env file:
PORT=5000
MONGO_URI=mongodb://localhost:27017/beetrail
JWT_SECRET=yourSecretKey

Start the server:
npm start

