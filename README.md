# NestJS User CRUD API

This is a simple backend application built using **NestJS** and **MongoDB**. It provides RESTful CRUD operations for managing user data.

## 📦 Tech Stack

* **NestJS** (TypeScript)
* **MongoDB** (Local instance)
* **Mongoose** for schema modeling
* **class-validator** and **class-transformer** for request validation

---

## 📋 Features

* Create a new user
* Get all users
* Get a user by ID
* Update a user (partial updates allowed)
* Delete a user

### 👤 User Model

```json
{
  "_id": "string",
  "name": "string",
  "email": "string",
  "age": 25
}
```

---

## 🚀 Getting Started

### Prerequisites

* [Node.js](https://nodejs.org/) (v16 or above)
* [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)
* [MongoDB](https://www.mongodb.com/) (running locally on default port `27017`)

### 🛠 Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/your-username/nestjs-user-api.git
   cd nestjs-user-api
   ```

2. **Install dependencies**

   ```bash
   npm install
   # or
   yarn install
   ```

3. **Ensure MongoDB is running locally**
   By default, the app connects to: `mongodb://localhost:27017/nest_users`

   You can update the URI in `app.module.ts` if needed:

   ```ts
   MongooseModule.forRoot('mongodb://localhost:27017/nest_users')
   ```

4. **Start the application**

   ```bash
   npm run start:dev
   ```

5. **API is live at:**

   ```
   http://localhost:3000
   ```

---

## 📫 API Endpoints

### Create a User

```
POST /users
```

**Request Body:**

```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "age": 30
}
```

### Get All Users

```
GET /users
```

### Get User by ID

```
GET /users/:id
```

### Update User (Partial)

```
PATCH /users/:id
```

**Request Body Example:**

```json
{
  "age": 31
}
```

### Delete User

```
DELETE /users/:id
```

---

## ✅ Validation Rules

* `name`: string (required)
* `email`: valid email (required, unique)
* `age`: integer (required, must be >= 0)

---

## 🐛 Error Handling

Returns appropriate HTTP status codes:

* `400 Bad Request` for validation errors
* `404 Not Found` if user is not found
* `500 Internal Server Error` for unexpected issues

---

## 🧪 Testing API

You can use tools like [Postman](https://www.postman.com/) or [cURL](https://curl.se/) to test the endpoints.

Example:

```bash
curl -X POST http://localhost:3000/users \
  -H 'Content-Type: application/json' \
  -d '{"name": "Jane", "email": "jane@example.com", "age": 28}'
```

---

## 📂 Project Structure

```
src/
├── app.module.ts
├── main.ts
└── users/
    ├── dto/
    │   ├── create-user.dto.ts
    │   └── update-user.dto.ts
    ├── schemas/
    │   └── user.schema.ts
    ├── users.controller.ts
    ├── users.module.ts
    └── users.service.ts
```

---

## 📄 License

MIT

---

## 🙋‍♂️ Questions?

Feel free to reach out if you encounter issues or need enhancements.
