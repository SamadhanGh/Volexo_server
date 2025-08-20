
# 🚖 Volexo Server

Volexo_server is the **backend service** for the **Volexo ride-hailing platform**, built with **Java (Spring Boot)**.  
It provides secure REST APIs for authentication, rider and driver management, wallet operations, and ride lifecycle handling.

---

## 🔗 Frontend
Check out the **Volexo Client (Frontend)** here:  
👉 [Volexo_client](https://github.com/SamadhanGh/Volexo_client)

---

## ⚙️ Tech Stack
- **Java** (Spring Boot)
- **Spring Security + JWT** (Authentication & Authorization)
- **Maven** (Build system)
- **REST APIs** for Rider & Driver
- **Database** (configurable: MySQL / PostgreSQL)

---

## 🚀 Getting Started

### Prerequisites
- Install **Java 17+**
- Install **Maven**
- Set up a **database** (MySQL/PostgreSQL)

### Clone the Repository
```bash
git clone https://github.com/SamadhanGh/Volexo_server.git
cd Volexo_server
````

### Run the Server

```bash
mvn spring-boot:run
```

The server will start at:

```
http://localhost:8080
```

---

## 🔐 Authentication APIs

### Rider Signup

```http
POST /auth/signUp
Content-Type: application/json

{
  "name": "mogali",
  "email": "mogali2003@gmail.com",
  "password": "Sama@1234",
  "role": "RIDER"
}
```

### Rider Login

```http
POST /auth/login
Content-Type: application/json

{
  "email": "mogali2003@gmail.com",
  "password": "Sama@1234"
}
```

---

## 👤 Rider APIs

* **PUT** `/rider/wallet/addBalance/{amount}` → Add balance to wallet
* **POST** `/rider/ride/request` → Request a ride
* **PATCH** `/rider/ride/cancel-ride/{rideId}` → Cancel ride
* **GET** `/rider/wallet/getBalance` → Get wallet balance
* **GET** `/rider/wallet/transactionHistory` → Get transaction history
* **GET** `/rider/rides` → Get all rides
* **GET** `/rider/rides/history` → Get ride history
* **GET** `/rider/rides/active-rides` → Get active rides
* **POST** `/rider/driver/rate` → Rate driver
* **GET** `/rider/profile` → Get rider profile

---

## 🚗 Driver APIs

* **POST** `/auth/signUp` → Signup as driver
* **POST** `/auth/login` → Driver login
* **PUT** `/driver/wallet/addBalance/{amount}` → Add balance to wallet
* **POST** `/driver/ride/{rideRequestId}/accept` → Accept ride request
* **POST** `/driver/ride/{rideId}/start` → Start ride with OTP
* **POST** `/driver/ride/{rideId}/end` → End ride
* **POST** `/driver/ride/{rideId}/cancel` → Cancel ride
* **POST** `/driver/rating/rider` → Rate rider
* **GET** `/driver/wallet/getBalance` → Get wallet balance
* **GET** `/driver/wallet/transactionHistory` → Get transaction history
* **GET** `/driver/rides/history` → Get ride history
* **GET** `/driver/ride/requests` → View new ride requests
* **GET** `/driver/ride/active-ride` → Get active ride
* **GET** `/driver/profile` → Get driver profile

---

## 📌 Example: Add Balance to Wallet (Rider)

```http
PUT /rider/wallet/addBalance/100
Authorization: Bearer <JWT_TOKEN>
```

---

## 📄 License

This project is licensed under the **MIT License**.

---

## ✨ Author

Developed by [Samadhan Ghorpade](https://github.com/SamadhanGh) 🚀

