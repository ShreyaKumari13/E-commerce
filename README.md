# E-commerce Backend Product API

## Backend Developer Test Implementation

This project implements a RESTful Product API as part of the backend developer test. The API is built using Node.js, Express, and MongoDB (via Mongoose), and is fully integrated into the existing project structure.

---

## Product API Endpoints

| Method | Endpoint                | Description                                 |
|--------|------------------------|---------------------------------------------|
| GET    | `/api/v1/products`     | List all products (supports filtering)      |
| GET    | `/api/v1/products/:id` | Get a single product by ID                  |
| GET    | `/api/v1/products?category=Apparel` | Filter products by category      |
| POST   | `/api/v1/products`     | Add a new product (validation included)     |

### Example: Add a Product (POST `/api/v1/products`)
```json
{
  "name": "T-Shirt",
  "category": "Apparel",
  "price": 19.99,
  "description": "Comfortable cotton t-shirt.",
  "images": ["<image_url>"],
  "brandname": "BrandX",
  "logo": "<logo_url>",
  "specifications": ["{\"title\":\"Material\",\"description\":\"Cotton\"}"]
}
```

---

## Database
- The API uses MongoDB for data storage.
- Set your connection string in `.env` as:
  ```
  MONGO_URI=mongodb+srv://<username>:<password>@<cluster-url>/<dbname>?retryWrites=true&w=majority
  ```

---

## How to Run

1. Install dependencies:
   ```sh
   npm install
   ```
2. Set up your `.env` file with your MongoDB URI.
3. Start the server:
   ```sh
   npm start
   ```
4. Use Postman or curl to test the endpoints above.

---

## Notes
- All endpoints are implemented in `api/controllers/productController.js` and registered in `api/routes/productRoute.js`.
- The API is fully integrated with the existing project and follows best practices for structure and validation.
