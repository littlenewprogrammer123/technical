Laravel Developer Interview Task
This project contains solutions to a series of tasks designed for assessing Laravel development skills. Each task focuses on different aspects of Laravel development, including frontend design, backend development, database management, and API integration.

Table of Contents
Task 1: UI/UX - Web Design & Development
Task 2: Laravel Blade & Backend Development
Task 3: MySQL Database Knowledge
Task 4: API Integration Knowledge
Task 1: UI/UX - Web Design & Development
Objective: Create a simple blog page using Bootstrap or Tailwind CSS for responsive design and good UI/UX principles. Additionally, implement a dark mode toggle and a comment section using AJAX.

Key Features:

Responsive design with Bootstrap/Tailwind CSS.
Blog posts with title, image, short description, and a "Read More" button.
Dark mode toggle to switch between light and dark modes.
Comment section implemented with AJAX (no page reload).
How to Use:

Open the project in your browser and navigate to the blog page to see the responsive layout and functionality.
Click the dark mode toggle button to switch between light and dark modes.
Add comments to the posts, which will be submitted using AJAX.
Task 2: Laravel Blade & Backend Development
Objective: Create a simple User Management system with registration, login, and role-based authentication (Admin & User).

Key Features:

Admin can create, update, and delete users.
Users can register, log in, and log out.
Admin can assign roles to users (admin or user).
Blade templates are used for front-end views.
How to Use:

Navigate to the /admin/users route to see the user management interface.
The Admin user can perform CRUD operations on users.
Use Laravel's built-in authentication to log in, register, and manage users.
Routes:

admin.users.index: List all users.
admin.users.create: Create a new user.
admin.users.edit: Edit an existing user.
admin.users.destroy: Delete a user.
Task 3: MySQL Database Knowledge
Objective: Create a database schema for an e-commerce system with the required tables and relationships. Implement the necessary MySQL queries for fetching data, updating stock, etc.

Key Features:

Database schema for Users, Products, Orders, and Order Items.
Queries to:
Fetch all products with more than 10 in stock.
Fetch all orders placed by a specific user.
Update product stock after an order is placed.
Eloquent relationships between models (User, Order, Product, and OrderItem).
How to Use:

Run the schema creation routes to generate the required database tables.
Use the admin/products-in-stock, admin/user-orders/{userId}, and admin/update-product-stock routes to interact with the data.
Use the Eloquent relationships to interact with models and retrieve associated data.
Routes:

admin/products-in-stock: Fetch all products with more than 10 in stock.
admin/user-orders/{userId}: Fetch orders by a specific user.
admin/update-product-stock: Update the stock of products after an order.
Task 4: API Integration Knowledge
Objective: Integrate a third-party API (https://jsonplaceholder.typicode.com/users) into the Laravel application and display the data. Add a search bar to filter users, handle errors, and store data in the database.

Key Features:

Fetch user data from the external API (jsonplaceholder.typicode.com).
Display a list of users with their name, email, and address in a Blade view.
Implement a search bar to filter users by name.
Store the fetched data in the database.
Bonus: Update the data periodically using Laravel Scheduler.
How to Use:

Visit the admin/users/api route to fetch user data from the external API and store it in your local database.
Use the admin/users/search route to search for users by name.
Optionally, use admin/users/scheduler to trigger a scheduler that fetches and updates the data periodically.
Routes:

admin/users/api: Fetch and store user data from the external API.
admin/users/search: Search for users by name.
admin/users/scheduler: Trigger the periodic data update using Laravel Scheduler.
Prerequisites
Laravel 8 or higher
Composer
PHP 7.4 or higher
MySQL (or any other supported database)
Installation
Clone the Repository:

bash
Copy
git clone <repository_url>
Install Dependencies: Navigate to the project directory and run:

bash
Copy
composer install
Set up Environment Variables: Create a .env file by copying .env.example:

bash
Copy
cp .env.example .env
Generate Application Key: Run the following command to generate the application key:

bash
Copy
php artisan key:generate
Set up the Database: Configure your database in the .env file and run the migrations:

bash
Copy
php artisan migrate
Run the Application: Start the Laravel development server:

bash
Copy
php artisan serve
Visit http://localhost:8000 to access the application.

Bonus
Scheduler: To update the data periodically, add the following cron job to your server:

bash
Copy
* * * * * php /path_to_your_project/artisan schedule:run >> /dev/null 2>&1
Testing: You can write tests for each task using Laravel's built-in testing features.
