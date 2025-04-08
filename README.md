# FRONTEND E-COMMERCE WEB APP 2024


## **Project Overview**
This is a fully responsive, custom-built e-commerce web application created using **HTML**, **CSS**, and **Vanilla JavaScript**. The project showcases essential e-commerce features, including dynamic routing, dynamic components loading, cart functionality, product search & filtering, authentication, and guest login. It highlights advanced JavaScript techniques and modular code structure for scalability and reusability.


## **Features**

  ### 1. Core E-commerce Functionalities:
  - Display product cards dynamically.

  - **Search** functionality.
  - **Category-based product filtering.**
  - **Add to cart** functionality with quantity increment/decrement features.
  - **Product details page:**
      - Display similar products based on category or search query.
  - **Cart Sidebar:**
      - Manage cart items with remove and control features.
      - View summary container for item totals and checkout functionality.

  ### 2. Authentication:
  - **User Login:** Modal for user login and registration.

  - **Guest Login:** Special feature allowing users to log in as "Guest" with temporary session data.

  ### 3. Custom Routing:
  - Dynamic routing using Vanilla JS to create a **Single Page App (SPA)** experience.

  - Seamless navigation between home, product details, cart, about, and contact pages.

  ### 4. Responsive Design:
  - Mobile-first approach for accessibility on all devices.

  - Media queries and CSS Grid/Flexbox used for layout adjustments.

  ### 5. Performance and Modularity:
  - JavaScript functions modularized for scalability. *[Classes are not used]*

  - Future projects can reuse components easily (e.g., modal, cart sidebar).


## **File Structure**

```plaintext
/Frontend-E-commerce-Project-2024
|--JS/
|   |-- App.js                     # Entry point for app logic
|   |-- addToCart_functionality.js # Add to cart logic
|   |-- cart_sidebar_handling_and_management.js # Cart sidebar open/close & item management
|   |-- check_SessionData_of_userLoggedIn.js    # Handles user session data
|   |-- checkout_handling.js       # Checkout functionality logic
|   |-- custom_router.js           # Custom routing implementation
|   |-- filter_products.js         # Product filtering logic
|   |-- handle_product_card_routing_&_productPage.js # Handles product routing logic
|   |-- modal_handler.js           # Logic for user login/register
|   |-- modal_popup.js             # Modal popup open/close functionality
|   |-- search_functionality.js    # Search functionality logic
|--styles/
|   |-- about_page_style.css       # About page styles
|   |-- contact_page_style.css     # Contact page styles
|   |-- modal_style.css            # Modal styling
|   |-- product_page_responsive_media.css # Responsive media for product page
|   |-- responsive_media.css       # General responsive styles
|   |-- sidebar_style.css          # Sidebar styling
|   |-- style.css                  # Main styles for index page
|--templates/                      # HTML files for rendering specific pages via JS routing
|   |-- about.html  
|   |-- contact.html  
|   |-- home_page.html             # Home/index page
|   |-- product.html               # Product details page
|
|--index.html                      # Main HTML file
|--products.json                   # JSON data for product list (fallback for fetch API failure)

```

## Data Flow

### 1. `App Initialization:`
  - On page load, JavaScript fetches product data from a `products.json` file or an API (if available).

  - The app dynamically renders product cards on the homepage using fetched data and DOM manipulation.

### 2. `User Interaction:`
  - **Search Bar:**
      - As the user types a query and clicked on Search Button, the app filters the product list and updates the displayed product cards.

  - **Filter by Category:**
      - The user selects a category, and the app filters products based on the selected criteria. The filtered products are displayed dynamically.

### 3. `Routing:`

  - When the user clicks on a product card 'view button' or product card of CART sidebar, the app updates the URL hash (e.g., `#/product?productId=$`) using a custom router.

  - The router dynamically fetches and displays the relevant page content (e.g., product details, about page) without reloading the page.      

### 4. `Cart Management:`

  - **Add to Cart:**
    
    - When the "Add to Cart" button is clicked, the product's details (ID, name, price, etc.) are added to a cart data array in memory.

    - The cart button of Navbar and cart sidebar updates dynamically to reflect the new item, including the subtotal and quantity.

  - **Modify Cart:**

    - Quantity increment/decrement buttons update the cart data array and refresh the cart UI.

    - Removing a product dynamically updates the cart data and recalculates the total.

    - And if product details page is opened and at same time any changes made will reflect on all areas.

### 5. `Authentication:`

  - **Login/Register:**

    - User clicks the login/register button, triggering the modal popup. Credentials are verified using JavaScript logic.

  - **Guest Login:**

    - Clicking the "I'm a Guest" button creates temporary session data to track the user's state.

### 6. `Checkout Process:`

  - On the checkout page, the app checks for an authenticated user session. If no session is found, the user will se a warning message modal shows "You need to login first".

  - After successful authentication, the checkout logic processes the cart data and displays a confirmation message.

### 7. `Session Data Handling:`

  - User sessions (e.g., login state or cart data) are managed using sessionStorage for persisting the data during the session.

--- 

## **Tech Stack**

  - **Frontend:**
    - HTML
    - CSS
    - Vanilla JavaScript

  - **JSON Data:**
    - Used to manage product information and fallback data.

---

## **Installation and Setup**
To run this project locally, follow these steps:

  **1. Clone the repository:**
  ```Bash
  git clone https://github.com/Ritesh-Kumar-Rai/Frontend-E-commerce-Project-2024.git
  ```

  **2. Navigate to the project directory:**
  ```Bash
  cd Frontend-E-commerce-Project-2024
  ```

  **3. Open `index.html` in your browser:**

  - Use a live server extension (e.g., in VS Code) for the best experience.

  - Alternatively, double-click index.html to open it directly.

---

## **Demo Video**
 Check out the demo video showcasing the project's functionality: [Demo Video Link]('https:www.google.com')

## **Future Enhancements**
  1. Add **lazy loading** for images and other resources to improve performance.

  2. Enhance user authentication and session management using APIs.

  3. Integrate a backend for dynamic product fetching.

  4. Migrate to `React.js` for a fully component-based architecture.

  5. Implement `testing frameworks` like:

  - **Cypress** for end-to-end testing of user flows (e.g., cart functionality, routing).

  - **Jest** for unit testing individual JavaScript functions and components to ensure reliability.

## **Credits**
Created by `Ritesh Kumar Rai`.