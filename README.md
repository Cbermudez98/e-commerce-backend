# E-commerce platform

## Description
This project aims to develop an e-commerce platform using technologies such as Express.js, MongoDB, PostgreSQL, Redis, and Docker. The platform allows users to purchase a variety of products. Users can register, manage their shopping carts by adding and removing items.

## Key Components
1. **Image Microservice**:
   - Create a microservice responsible for storing images and providing URLs for serving images.

2. **Log Microservice**:
   - Develop a microservice that registers and stores logs from all other microservices. Log data will be stored in a NoSQL database, such as MongoDB.

3. **Mail Microservice**:
   - Create a microservice for sending emails and implement a queue to manage email delivery.

4. **User Microservice**:
   - This microservice is responsible for user management. It allows users to register, update their personal data, and handles user authentication manage two roles admin and user. User data,including authentication details, will be stored in a SQL database, such as PostgreSQL or MySQL. Additionally, email validation is implemented to prevent users from logging in until their email is verified.

5. **Products Microservice**:
   - This microservice handles product management. Administrators can add products, while any user can retrieve a paginated list of available products. Product data will be stored in a SQL database, such as Mysql or Postgress.

6. **Cache Microservice**:
   - Implement a microservice that manages data caching using Redis. The cache will store a list of 10 products currently in stock, with a 20% discount, for a duration of 24 hours.
   - Users can add and remove items from their shopping carts, access cart details, and, once payment is made, the cart will be cleared from the cache.

7. **Cart Microservice**:
   - This microservice allows users to interact with their shopping carts. It cross-references information on products with discounts and the contents of the user's cart. When the user decides to pay for the cart, the transaction data will be securely stored in a SQL database to ensure data integrity and transactions. This microservice will maintain a relation table to save the products with discounts associated with the purchase. It will also send an email to the user with details of the purchased products and the total amount. Additionally, an email notification will be sent when the cart has been successfully purchased, listing the items in the cart.

# Extras
- All microservices will be equipped with unit tests and thorough documentation to ensure the reliability and maintainability of the system.
