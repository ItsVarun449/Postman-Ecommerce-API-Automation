# Ecommerce API Testing Project using Postman

This project demonstrates API testing using Postman on DummyJSON E-commerce APIs.

## Features

- User Authentication API Testing
- Bearer Token Authorization
- Environment Variables
- Dynamic Data Handling
- Product API Testing
- Cart API Testing
- Automated Test Scripts using JavaScript
- API Response Validation

---

## APIs Covered

### 1. Login API
POST `/auth/login`

- Generates access token
- Stores token in environment variables

### 2. Get User Profile
GET `/auth/me`

- Uses Bearer Token authentication
- Validates status code

### 3. Get Products
GET `/products`

- Fetches products list
- Dynamically stores product ID

### 4. Single Product API
GET `/products/{{product_id}}`

- Retrieves single product details

### 5. Cart API
GET `/carts/28`

- Validates cart total
- Uses assertions in Postman scripts

---

## Technologies Used

- Postman
- JavaScript
- REST API Testing
- DummyJSON API

---

## Test Validations Used

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

```javascript
pm.expect(jsonData.total).to.be.above(0);
```

---

## Environment Variables Used

| Variable | Purpose |
|----------|----------|
| dummy_json | Base URL |
| Token | Authentication Token |
| product_id | Dynamic Product ID |
| cart_id | Cart Identifier |

---

## Author

Varun Rana
