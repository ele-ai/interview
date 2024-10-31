# Interview
---

Q1.Explain the page routing mechanism in Next.js.

A1:Next.js uses a file-based routing system. Each file in the pages directory automatically becomes a route. Dynamic routes are created using brackets in the file name (e.g., [id].js).
What are getStaticProps and getServerSideProps?
---

Q2.What are getStaticProps and getServerSideProps?

A2:getStaticProps is used to fetch data at build time to generate static pages, suitable for data that doesn't change often. getServerSideProps fetches data on each request, suitable for content that needs to be updated in real-time.

---

Q3:What are API routes, and how do you use them in Next.js?

A3:API routes allow you to create API endpoints in the pages/api directory. Each file exports a handler function to process HTTP requests.

---
# Coding Test: Build a Simple E-commerce Product Page

**Objective:** Create a simple e-commerce product page that includes user authentication, product listings, and the ability to add items to a shopping cart.

## Requirements:

1. **Create a New Next.js Project:**
   - Set up a new Next.js project using `create-next-app`.

2. **Product Data:**
   - Create a static list of products. Each product should have an `id`, `name`, `description`, `price`, and `imageUrl`.
   - Example data structure:
     ```javascript
     const products = [
       { id: 1, name: 'Product 1', description: 'Description of Product 1', price: 29.99, imageUrl: '/images/product1.jpg' },
       { id: 2, name: 'Product 2', description: 'Description of Product 2', price: 49.99, imageUrl: '/images/product2.jpg' },
       { id: 3, name: 'Product 3', description: 'Description of Product 3', price: 19.99, imageUrl: '/images/product3.jpg' },
     ];
     ```

3. **User Authentication:**
   - Implement a simple authentication system (you can use mock authentication).
   - Create a login page (`/login`) that allows users to log in with a username and password (no backend required; just mock the login).

4. **Product Listings:**
   - Create a homepage (`/`) that displays a grid of product cards.
   - Each product card should show the product name, price, and an "Add to Cart" button.

5. **Shopping Cart:**
   - Implement a shopping cart that allows users to add products.
   - Create a cart icon that shows the number of items in the cart.
   - Create a cart page (`/cart`) that lists all items added to the cart with their details and a total price.

6. **API Routes:**
   - Use Next.js API routes to manage the cart state. Create an API route (`/api/cart`) that allows adding and removing products from the cart.
   - Use local storage or session storage to persist the cart state.

7. **Styling:**
   - Use CSS modules for styling the product cards, login form, and cart page.

8. **Navigation:**
   - Ensure that users can navigate between the homepage, login page, and cart page seamlessly.
