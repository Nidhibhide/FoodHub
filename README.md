

# FoodHub  

**FoodHub** is a **MERN Stack** backend application that enables users to browse restaurants, place orders, track delivery, and make payments. This system includes **role-based APIs** for **customers, admin, and restaurant owner**, along with **MongoDB aggregation-based reports** for analytics.  

## Features  

### Customer Features  
- User authentication (Register/Login with JWT)  
- Browse restaurants and food items  
- Place and track orders  
- View order history  
- Provide reviews and ratings  
- Generate spending and order reports  

### Admin Features  
- Manage restaurants and users  
- Track overall sales and revenue  
- View top-selling restaurants and monthly trends  
- Generate business reports using aggregation  

### Restaurant Features  
- Accept and process orders  
- Track restaurant earnings  
- View popular food items  
- Generate restaurant performance reports  

## Tech Stack  

- **Backend:** Node.js, Express.js, TypeScript 
- **Database:** MongoDB 
- **Authentication:** JWT-based authentication  
- **Middleware:** CORS, Helmet  




## API Endpoints  

### Customer APIs (`/api/customers`)  
- `POST /register` → Register a new customer  
- `POST /login` → Login customer  
- `GET /restaurants` → Browse restaurants  
- `POST /order` → Place a new order  
- `GET /orders` → View order history  
- `POST /review` → Submit restaurant review  
- `GET /reports/spending` → View total spent amount & order count  
- `GET /reports/favorite-restaurants` → View top visited restaurants  

### Admin APIs (`/api/admin`)  
- `POST /restaurant` → Add a new restaurant  
- `GET /restaurants` → View all restaurants  
- `DELETE /restaurant/:id` → Remove a restaurant  
- `GET /reports/sales` → View total revenue & order count  
- `GET /reports/top-restaurants` → Get top-selling restaurants  
- `GET /reports/monthly-sales` → View monthly earnings trends  

### Restaurant APIs (`/api/restaurant`)  
- `POST /menu` → Add new food items  
- `GET /orders` → View incoming orders  
- `PUT /order/:id/status` → Update order status  
- `GET /reports/sales` → View restaurant earnings & completed orders  
- `GET /reports/average-order-value` → Calculate average order value  
- `GET /reports/popular-items` → Find most ordered food items  

## Reports (Using MongoDB Aggregation)  

### Customer Reports  
- **Total Spending Report:** Total amount spent on orders  
- **Favorite Restaurants:** Top 3 most ordered-from restaurants  

### Admin Reports  
- **Total Revenue & Sales:** Total income generated by all restaurants  
- **Top Restaurants:** Restaurants with the highest order count  
- **Monthly Sales Trends:** Graph of sales per month  

### Restaurant Reports  
- **Total Earnings Report:** Total revenue generated  
- **Average Order Value:** Average price per order  
- **Popular Food Items:** Most frequently ordered food items  

## Installation  

1. **Clone the repository**  
```sh
git clone https://github.com/your-username/foodhub-backend.git
cd foodhub-backend
```
  
2. **Install dependencies**  
```sh
npm install
```

3. **Set up `.env` file**  
```sh
MONGO_URI=your-mongodb-connection-string
JWT_SECRET=your-secret-key
PORT=5000
```

4. **Start the server**  
```sh
npm start
```

