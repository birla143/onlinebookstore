# Online Bookstore - Java Servlet Project

A full-stack online bookstore application built using Java, Servlets, JDBC, and MySQL. It features separate interfaces for users and administrators for a complete e-commerce experience.

---

## 📋 Table of Contents

1.  [About The Project](#about-the-project)
    * [Key Features](#key-features)
    * [Tech Stack](#tech-stack)
2.  [Getting Started](#getting-started)
    * [Prerequisites](#prerequisites)
    * [Installation](#installation)
3.  [Usage](#usage)
4.  [Screenshots](#screenshots)
5.  [Contributing](#contributing)

---

## 📖 About The Project

This project is a web-based bookstore designed to showcase the use of Java Servlets and JDBC for back-end development. It provides a platform for users to browse and purchase books, while administrators can manage the store's inventory and view sales data.

![Online Bookstore Homepage](https://user-images-githubusercontent.com/34605595/137615096-8447d32d-bddc-4f13-a8ed-3c0f4dd5e04e.png)

### Key Features

* **User Authentication:** Secure registration and login for users.
* **Product Catalog:** Users can view a list of all available books.
* **Shopping Cart:** Users can add books, specify quantities, and proceed to checkout.
* **Admin Dashboard:** A separate interface for administrators to manage the store.
* **Inventory Management:** Admins can add new books, update stock, change prices, and remove books.
* **Sales History:** Admins can track all transactions.

### Tech Stack

* **Backend:** Java 8+, Servlets, JDBC
* **Frontend:** HTML, CSS, JavaScript, Bootstrap
* **Database:** MySQL
* **Web Server:** Apache Tomcat 8.0+
* **Build Tool:** Apache Maven

---

## 🚀 Getting Started

Follow these instructions to set up the project on your local machine.

### Prerequisites

You must have the following software installed:
* Git
* Java JDK 8 or higher
* Eclipse IDE for Enterprise Java Developers
* Apache Maven
* Apache Tomcat 8.0 or higher
* MySQL Server

### Installation

1.  **Clone the Repository**
    ```bash
    git clone [https://github.com/birla143/onlinebookstore.git](https://github.com/birla143/onlinebookstore.git)
    ```

2.  **Initialize the Database**
    * Log in to your MySQL instance.
    * Execute the following SQL script to create the database, tables, and insert sample data.
        ```sql
        CREATE DATABASE IF NOT EXISTS onlinebookstore;
        USE onlinebookstore;
        CREATE TABLE IF NOT EXISTS books(barcode VARCHAR(100) PRIMARY KEY, name VARCHAR(100), author VARCHAR(100), price INT, quantity INT);
        CREATE TABLE IF NOT EXISTS users(username VARCHAR(100) PRIMARY KEY,password VARCHAR(100), firstname VARCHAR(100), lastname VARCHAR(100),address TEXT, phone VARCHAR(100),mailid VARCHAR(100),usertype INT);
        INSERT INTO books VALUES('9780134190563','The Go Programming Language','Alan A. A. Donovan and Brian W. Kernighan',400,8),('9780133053036','C++ Primer','Stanley Lippman and Josée Lajoie and Barbara Moo',976,13),('9781718500457','The Rust Programming Language','Steve Klabnik and Carol Nichols',560,12),('9781491910740','Head First Java','Kathy Sierra and Bert Bates and Trisha Gee',754,23);
        INSERT INTO users VALUES('demo','demo','Demo','User','Demo Home','42502216225','demo@gmail.com',2),('Admin','Admin','Mr.','Admin','Haldia WB','9584552224521','admin@gmail.com',1),('shashi','shashi','Shashi','Raj','Bihar','1236547089','shashi@gmail.com',2);
        COMMIT;
        ```

3.  **Configure in Eclipse**
    * Import the cloned repository as a Maven project into Eclipse (`File > Import > Maven > Existing Maven Projects`).
    * Update the database connection details in `src/main/resources/application.properties`.
    * Build the project using Maven: Right-click project > `Run As` > `Maven build...` > Goals: `clean install`.
    * Add the project to your configured Tomcat server.

---

## ▶️ Usage

1.  Start the Tomcat server from within Eclipse.
2.  Open a web browser and navigate to `http://localhost:8083/onlinebookstore/` (or the port you configured).
3.  **Default Credentials**:
    * **Admin**:
        * Username: `Admin`
        * Password: `Admin`
    * **User**:
        * Username: `shashi`
        * Password: `shashi`

---

## 🖼️ Screenshots

| Admin Dashboard                                                                                                                 | Book Listing Page                                                                                                             |
| ------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| ![Admin Panel](https://user-images-githubusercontent.com/34605595/224770257-e18a3810-0457-4b78-bf46-cf82746708ee.png)            | ![Book Listing](https://user-images-githubusercontent.com/34605595/224769990-f440f74d-41b2-4629-ba1c-a87267f225d9.png)      |
| **Shopping Cart** | **User Profile** |
| ![Shopping Cart](https://user-images-githubusercontent.com/34605595/224770145-5902054f-5943-44ac-b02f-92097c8a6972.png)          | ![User Profile](https://user-images-githubusercontent.com/34605595/224770392-5a5478d2-98cc-44ee-8689-132b6b16af80.png)      |

---

## 🤝 Contributing

Suggestions and contributions are always welcome! Feel free to open an issue or submit a pull request to improve the project.
