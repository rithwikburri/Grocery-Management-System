# Grocery-Management-System
A comprehensive Grocery Management System designed to streamline inventory management, order tracking, and billing processes for grocery stores.
Features

User Features

User Registration and Login

New users can register with a username, password, and mobile number.

Existing users can log in with their credentials.

Cart Management

View items available in different grocery categories.

Add items to the cart, specifying quantity.

View and edit the cart before checkout.

Order Management

View past orders in the order history.

Place orders from the cart.

Admin Features

Admin Login

Dedicated admin accounts to log in and manage the system.

Grocery Inventory Management

Add new grocery items to existing categories.

Update the quantity and price of items.

View Order History

View order history for all users.

Installation

Prerequisites

Python 3.x

Basic knowledge of running Python scripts.

Steps

Clone or download the project files to your local machine.

Ensure the following JSON files are present in the project directory:

users.json: Stores user data.

admin.json: Stores admin data.

grocery.json: Stores grocery item data.

cart.json: Stores user cart data.

orders.json: Stores user order data.

Install required dependencies (if any).

Usage

Starting the Application

Run the script using the following command:

python main.py

Main Menu

1. Login as User: Allows registered users to log in and access their account.

2. Login as Admin: Allows admins to log in and manage the grocery inventory and order history.

3. Register: Enables new users to create an account.

4. Exit: Exits the application.

JSON File Structure

users.json

Stores user information:

[
    {
        "username": "user1",
        "password": "password1",
        "mobile": "1234567890"
    }
]

admin.json

Stores admin information:

[
    {
        "username": "admin1",
        "password": "adminpassword"
    }
]

grocery.json

Stores grocery items categorized by type:

{
    "Fruits": [
        {"id": 1001, "name": "Apple", "quantity": 10, "price": 100},
        {"id": 1002, "name": "Banana", "quantity": 20, "price": 50}
    ],
    "Vegetables": [
        {"id": 2001, "name": "Tomato", "quantity": 15, "price": 30}
    ]
}

cart.json

Stores cart data for each user:

[
    {
        "username": "user1",
        "orders": [
            {
                "type": "Fruits",
                "name": "Apple",
                "quantity": 2,
                "price": 200
            }
        ]
    }
]

orders.json

Stores completed orders:

[
    {
        "username": "user1",
        "items": [
            {
                "item_id": 1001,
                "item_name": "Apple",
                "item_quantity": 2,
                "item_price": 200
            }
        ],
        "total_price": 200
    }
]

Key Functions

loadusers(), loadcart(), loadadmin(), loadgroceries()

Load data from respective JSON files.

Handle missing or malformed files by returning default values.

savegrocery(), saveusers(), savecart()

Save updated data to respective JSON files.

User-Related Functions

login(): Handles user login.

register(): Registers a new user.

usermenu(): Displays the user menu with options for cart and order management.

Admin-Related Functions

loginadmin(): Handles admin login.

adminmenu(): Displays the admin menu for grocery and order management.

Cart Management

addtocart(): Allows users to add items to their cart.

showcart(): Displays the user's cart and allows editing or proceeding to checkout.

Order History

orderhistory(username): Displays order history for a specific user.

adminorderhistory(): Allows admin to view order history for any user.

Inventory Management

addgrocery(): Adds new items to the inventory or updates existing items.

Future Enhancements

Implement a graphical user interface (GUI).

Add user authentication with hashed passwords.

Integrate a database for better scalability.

Enhance reporting features for admins.

Contributing

Contributions are welcome! If you'd like to contribute, please:

Fork the repository.

Create a feature branch.

Submit a pull request with a detailed description of the changes.

