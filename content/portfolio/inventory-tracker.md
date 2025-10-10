+++
categories = ["web-dev"]
coders = []
date = 2025-09-12T23:00:00Z
description = "A full stack Inventory Tracker built with Spring Boot and React, deployed on AWS to manage product stock, suppliers, and categories"
image = "https://ik.imagekit.io/ys4gkaixy/warehouse-inventory-stock-merchandise-svgrepo-com.svg?updatedAt=1759688272720"
title = "Inventory Tracker Application"
type = "post"
weight = 1
[[tech]]
name = "Spring Boot"
url = "https://spring.io/projects/spring-boot"
logo = "https://ik.imagekit.io/ys4gkaixy/Spring_Boot.svg?updatedAt=1757549837981"
[[tech]]
logo = "https://ik.imagekit.io/ys4gkaixy/Postgresql_elephant.svg?updatedAt=1760063146108"
name = "PostgreSQL"
url = "https://www.postgresql.org"
[[tech]]
logo = "https://ik.imagekit.io/ys4gkaixy/React-icon.svg?updatedAt=1752785957314"
name = "React"
url = "https://react.dev"
[[tech]]
name = "AWS"
url = "https://aws.amazon.com"
logo = "https://ik.imagekit.io/ys4gkaixy/Skills/Amazon_Web_Services_Logo.svg?updatedAt=1744515846258"
+++

## Project Overview

A full-stack inventory tracking system built with a Spring Boot backend and React frontend. The application allows users to view products, categories, and suppliers, while admins have full CRUD access. The project features secure JWT-based authentication and role-based access control.

---

## Project Links

- **Live Application**: [View App](http://inventory-tracker-frontend-react.s3-website-us-east-1.amazonaws.com/)
- **Frontend Repository**: [GitHub - Frontend](https://github.com/sudeepthi59o/InventoryTracker-SpringBoot-Frontend)
- **Backend Repository**: [GitHub - Backend](https://github.com/sudeepthi59o/InventoryTracker-SpringBoot-Backend)

If you'd like to explore the app with different access levels:

- To try the **admin login**, use:  
  `Username: alice_smith`  
  `Password: alice_smith`

- To try the **user login**, use:  
  `Username: carol_brown`  
  `Password: carol_brown`

## Tech Stack:

- Spring Boot (Spring REST, Spring Security (JWT), Spring Data JPA)
- React
- JavaScript (Axios)
- PostgreSQL
- GitHub Actions
- AWS (EC2, S3, RDS)

---

## Features

### Authentication & Authorization

- Secure login using JWT (JSON Web Tokens) with Spring Security
- Role-based access control:
  - **Admins** can create, update, and delete products, categories, and suppliers
  - **All users** can view products, categories, and suppliers

### Product, Category, and Supplier Management

- Dedicated pages for browsing all categories and all suppliers
- Users can view all products or filter by category and/or supplier
- Admins can add, edit, and delete entries

### Frontend Functionality (React)

- Login functionality to authenticate users
- View all products or filter by supplier and/or category
- Navigation to category and supplier pages
- Logout functionality for authenticated users

---

## Backend Architecture

- Built with **Spring Boot**
- RESTful API endpoints using Spring Web
- Data persistence with **Spring Data JPA** and **PostgreSQL** (hosted on AWS RDS)
- Authentication and authorization with **Spring Security** and **JWT**
- Clean relational data model:
  - One-to-many: Category → Products
  - One-to-many: Supplier → Products

---

## DevOps & Deployment

- Continuous Integration and Deployment to AWS using **GitHub Actions**
- Backend deployed to **AWS EC2**
- Frontend hosted via **AWS S3** static website hosting
- PostgreSQL database hosted on **AWS RDS**

---

## Future Improvements

- Full CRUD for categories and suppliers
