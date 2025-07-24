# E-commerce Backend Product API

## Deployed API

- **Base URL:** [https://e-commerce-6b67.onrender.com](https://e-commerce-6b67.onrender.com)

---

## Tech Stack
- **Node.js**
- **Express.js**
- **MongoDB (Atlas) with Mongoose**
- **Cloudinary (for image uploads)**

---

## How to Run the Project Locally

1. Clone the repository:
   ```sh
   git clone https://github.com/ShreyaKumari13/E-commerce.git
   cd E-commerce
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Set up your `.env` file with the following variables:
   ```env
   MONGO_URI=your_mongodb_connection_string
   CLOUDINARY_NAME=your_cloudinary_name
   CLOUDINARY_API_KEY=your_cloudinary_api_key
   CLOUDINARY_API_SECRET=your_cloudinary_api_secret
   ```
4. Start the server:
   ```sh
   npm start
   ```
5. The API will be available at `http://localhost:4000` by default.

---

## API Documentation

### Base URL
- Local: `http://localhost:4000/api/v1`
- Deployed: `https://e-commerce-6b67.onrender.com/api/v1`

### Endpoints

#### 1. Get All Products
- **GET** `/products`
- **Description:** Returns a list of all products.
- **Example:**
  ```sh
  curl https://e-commerce-6b67.onrender.com/api/v1/products
  ```

#### 2. Get Product by ID
- **GET** `/products/:id`
- **Description:** Returns a single product by its ID.
- **Example:**
  ```sh
  curl https://e-commerce-6b67.onrender.com/api/v1/products/<product_id>
  ```

#### 3. Filter Products by Category
- **GET** `/products?category=Apparel`
- **Description:** Returns products filtered by category.
- **Example:**
  ```sh
  curl "https://e-commerce-6b67.onrender.com/api/v1/products?category=Apparel"
  ```

#### 4. Add a New Product
- **POST** `/products`
- **Description:** Adds a new product (data validation required).
- **Example (curl):**
  ```sh
  curl -X POST https://e-commerce-6b67.onrender.com/api/v1/products \
    -H "Content-Type: application/json" \
    -d '{
      "name": "Sneakers",
      "category": "Footwear",
      "price": 49.99,
      "cuttedPrice": 59.99,
      "description": "Lightweight and comfortable running sneakers.",
      "images": ["https://images.pexels.com/photos/2529148/pexels-photo-2529148.jpeg"],
      "brandname": "RunnerPro",
      "logo": "https://images.pexels.com/photos/936094/pexels-photo-936094.jpeg",
      "specifications": [
        "{\"title\":\"Material\",\"description\":\"Mesh and Rubber\"}",
        "{\"title\":\"Color\",\"description\":\"Black/White\"}"
      ]
    }'
  ```

---

## Brief Note

- **Tech Stack:** Node.js, Express.js, MongoDB (Atlas), Mongoose, Cloudinary
- **How to Run:** Clone the repo, install dependencies, set up your `.env`, and run `npm start`.
- **API Documentation:** See above for endpoints and sample requests. The API is also deployed at [https://e-commerce-6b67.onrender.com](https://e-commerce-6b67.onrender.com).
