# NestJS User CRUD API

This is a simple backend application built using **NestJS** and **MongoDB**. It provides RESTful CRUD operations for managing user data.

## 📦 Tech Stack

* **NestJS** (TypeScript)
* **MongoDB** (Local instance)
* **Mongoose** for schema modeling
* **class-validator** and **class-transformer** for request validation

## 📋 Features

* Create a new user
* Get all users
* Get a user by ID
* Update a user (partial updates allowed)
* Delete a user


## 🚀 Getting Started

1. **Clone the repository**

   ```bash
   git clone https://github.com/your-username/nestjs-user-api.git
   cd nestjs-user-api
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Ensure MongoDB is running locally**
   By default, the app connects to: `mongodb://localhost:27017/users_db`

   You can update the URI in `app.module.ts` if needed:

   ```ts
   MongooseModule.forRoot('mongodb://localhost:27017/users_db')
   ```

4. **Start the application**

   ```bash
   npm run start:dev
   ```

5. **API is live at:**

   ```
   http://localhost:3000
   ```

## 📫 API Endpoints

```
POST /users
PATCH /users/:id
GET /users
GET /users/:id
DELETE /users/:id
```

## 🧪 Testing API
Import the following Postman collection for easy testing:
[Postman-collection.json](https://github.com/user-attachments/files/21264752/Postman-collection.json)
