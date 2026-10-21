# 🍔 Canteen Management System

> A console-based Canteen Management System built in **C** that demonstrates the practical implementation of core **Data Structures and Algorithms (DSA)** and binary file handling.

![C Language](https://img.shields.io/badge/Language-C-blue.svg)
![DSA Project](https://img.shields.io/badge/DSA-Linked%20List%20|%20Queue%20|%20Stack-green.svg)
![Status](https://img.shields.io/badge/Status-Completed-success.svg)

---

## 📌 About the Project

The **Canteen Management System** automates everyday canteen operations—such as menu browsing, food ordering, order fulfillment, inventory management, and tracking cancelled orders. It bridges theoretical computer science concepts (like linear and non-linear data structures) with a real-world application.

---

## 🧠 Data Structures & Algorithms (DSA) Implementation

| Data Structure / Algorithm | How it's Used in the Project | Purpose / Benefit |
| :--- | :--- | :--- |
| **Singly Linked List** | Manages the canteen menu (`Node` & `Food` structs) | Dynamic memory allocation allows items to be added without fixed-size limits. |
| **Queue (FIFO)** | Handles incoming orders (`Queue` struct with front/rear) | Ensures fair, sequential order processing (`serveNextOrder`). |
| **Stack (LIFO)** | Manages cancelled orders (`Stack` struct with top pointer) | Tracks recently cancelled orders and automatically restores stock. |
| **Sorting Algorithms** | Bubble Sort (on arrays extracted from the linked list) | Sorts menu items dynamically by **Price** (low to high) or alphabetically by **Name**. |
| **Searching Algorithm** | Linear Search with case-insensitive substring matching | Allows customers to search for food items by keyword with partial matches (`strstr`). |

---

## ✨ Key Features

### 👤 Customer & Order Management
* **View Menu:** Displays available food items, item IDs, prices, and real-time stock levels.
* **Search & Sort:** Search for specific dishes or sort the menu by price and name.
* **Place Order:** Validates stock, calculates the bill, automatically deducts inventory, generates an **Order Receipt**, and adds the order to the pending queue.
* **Order Cancellation:** Cancel the latest pending order, which immediately restores food stock and logs it into the cancellation stack.

### 🛠️ Admin Panel
* **Menu & Stock Management:** Add new food items or update stock quantities in real time.
* **Order Processing:** View pending orders and serve them sequentially (**FIFO**).
* **Audit & Reports:** View logs of cancelled orders and full completed order history.
* **Canteen Statistics:** High-level dashboard showing total active food items, total stock units, low-stock alerts ($\le 5$ items), inventory valuation, pending orders count, and cancelled orders count.

### 💾 Data Persistence
* Uses binary file operations (`menu.dat` and `orders.dat`) to ensure that menu updates, stock changes, and completed order histories are saved across application sessions.

---

## 🚀 Getting Started

### Prerequisites
You need a C compiler installed on your system (e.g., GCC, Clang, or MSVC).

### Compilation & Execution

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/YOUR_USERNAME/canteen-management-system.git](https://github.com/YOUR_USERNAME/canteen-management-system.git)
   cd canteen-management-system
