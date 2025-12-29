
# 📚 API Testing – Simple Books Store API

## 📌 Project Overview

This project demonstrates **API testing** for a **Simple Books Store API** using **Postman**.
The purpose is to verify API functionality, performance, authentication, and data correctness for book-related operations such as **retrieving books, managing clients, and handling orders**.

Automated test scripts are written using **JavaScript** inside Postman, with dynamic data handling via **collection variables**.

---

## 🛠 Tools & Technologies

* **Postman**
* **RESTful APIs**
* **JavaScript (Postman Test Scripts)**
* **JSON**
* **Bearer Token Authentication**

---

## 📂 API Modules Covered

### 1️⃣ Status

Checks whether the API service is running.

**Endpoint**

```
GET /status
```

**Validations**

* Status code `200`

---

### 2️⃣ Books

Retrieve books data and validate response correctness.

#### Get All Books

```
GET /books
```

**Validations**

* Status code `200`
* Response time < 2000 ms

#### Get Book by ID

```
GET /books/{bookId}
```

**Validations**

* Status code `200`
* Book ID and name validation
* Data visualization using Postman Visualizer (HTML table)

---

### 3️⃣ Client (Authentication)

Create a new API client and generate an access token.

**Endpoint**

```
POST /api-clients
```

**Validations**

* Status code `200`
* Response time < 3000 ms
* Extract and store `accessToken` as a collection variable

✔ Token is reused in secured endpoints using **Bearer Authentication**.

---

### 4️⃣ Orders

Full CRUD operations for book orders.

#### Create Order

```
POST /orders
```

**Validations**

* Status code `200`
* Order ID saved dynamically

#### Get All Orders

```
GET /orders
```

**Validations**

* Status code `200`
* Authorized access using Bearer Token

#### Get Specific Order

```
GET /orders/{orderId}
```

#### Update Order

```
PATCH /orders/{orderId}
```

#### Delete Order

```
DELETE /orders/{orderId}
```

**Validations**

* Status code `200`
* Response time < 3000 ms

---

## 🔄 Variables Used

| Variable  | Description         |
| --------- | ------------------- |
| `Books`   | Base URL            |
| `Token`   | Bearer access token |
| `orderid` | Order ID            |

---

## ✅ Test Scenarios Implemented

* API availability checks
* Status code validation
* Response time validation
* Data integrity validation
* Authentication handling
* CRUD operations testing
* Dynamic data chaining using variables
* API response visualization

---

## ▶ How to Run the Tests

1. Import the Postman collection
2. Set the `Books` base URL in collection variables
3. Run requests sequentially **or**
4. Use **Postman Collection Runner** to execute all tests

---

## 📈 Expected Results

* All endpoints return correct HTTP status codes
* Secured endpoints require valid authentication
* Orders lifecycle works correctly
* Performance remains within acceptable limits

---

## 👤 Author

**Ahmed Alashmawy**
API Testing & Quality Assurance Engineer


