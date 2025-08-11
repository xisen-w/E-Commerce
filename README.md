# JoyMart E-Commerce Website

A fully responsive e-commerce website built with HTML, CSS, and JavaScript. With product listings, shopping cart functionality, and open for Facebook Pixel integration for event tracking.

## Table of Contents

- [Features](#features)
- [Setup Instructions](#setup-instructions)
- [Running Locally](#running-locally)
- [Website Components](#website-components)
- [Monitoring Events in Facebook Events Manager](#monitoring-events-in-facebook-events-manager)
- [API Integration](#api-integration)
- [Screenshots](#screenshots)

## Features

- Integrated with Faker.js and mockapi.io for dynamic data generation
- Responsive layout for all device sizes
- Shopping cart with add, remove, and quantity adjustment
- Product details page with ratings and description
- Order confirmation flow
- Need to implement - Facebook Pixel event tracking

## Setup Instructions

1. **Clone the repository**
   ```
   bash
   git clone https://github.com/yourusername/E-CommerceWebsite.git
   cd E-CommerceWebsite
   ```

2. **Project Structure**
   The project has the following structure:
   ```
   E-CommerceWebsite/
   ├── index.html              # Main entry point
   ├── header.html             # Navigation header
   ├── footer.html             # Footer section
   ├── content.html            # Product listings page
   ├── contentDetails.html     # Product details page
   ├── cart.html               # Shopping cart page
   ├── orderPlaced.html        # Order confirmation page
   ├── css/                    # CSS stylesheets
   │   ├── header.css
   │   ├── footer.css
   │   ├── content.css
   │   ├── contentDetails.css
   │   ├── cart.css
   │   └── orderPlaced.css
   ├── js/                     # JavaScript libraries
   │   └── jQuery3.4.1.js
   ├── content.js              # Product listing functionality
   ├── contentDetails.js       # Product details functionality
   ├── cart.js                 # Shopping cart functionality
   └── orderPlaced.js          # Order confirmation functionality
   ```

3. **Facebook Pixel Setup** #TODO
   - The website needs to be configured with Facebook Pixel for event tracking.
     - Create a Facebook Pixel in your Facebook Business Manager
     - Integrated the Facebook Pixel code into the website's multiple pages to track user interactions across standard events for e-commerce websites.

## Running Locally

Since the website uses XMLHttpRequest to load components, you need to serve it through a web server rather than opening the HTML files directly. Here are three ways to run it locally:

### 1. Using Python (Recommended)

Python comes with a built-in HTTP server that's perfect for local development:

**For Python 3:**
```bash
cd /path/to/E-CommerceWebsite
python -m http.server 8000
```

**For Python 2:**
```bash
cd /path/to/E-CommerceWebsite
python -m SimpleHTTPServer 8000
```

Then open your browser and navigate to: `http://localhost:8000`

### 2. Using VS Code Live Server

If you're using Visual Studio Code:
1. Install the "Live Server" extension
2. Right-click on index.html and select "Open with Live Server"

## Website Components

### 1. Header (header.html, header.css)
- Colorful JoyMart navigation bar
- Logo and search functionality
- Account and cart links
- Category navigation

### 2. Product Listing (content.html, content.js, content.css)
- Hero banner
- Category cards
- Product grid with:
  - Product images
  - Titles and descriptions
  - Ratings and reviews
  - Pricing with consistent 2-decimal formatting
  - Prime badges
  - "Add to Cart" buttons

### 3. Product Details (contentDetails.html, contentDetails.js)
- Product images
- Title, category, and description
- Price information
- Star ratings and review count
- "Add to Cart" and "Buy Now" buttons

### 4. Shopping Cart (cart.html, cart.js)
- List of added products
- Quantity adjustment controls
- Remove item functionality
- Total price calculation
- "Place Order" button

### 5. Order Confirmation (orderPlaced.html, orderPlaced.js)
- Order success message
- Order summary
- Total amount and item count

### 6. Footer (footer.html, footer.css)
- Multiple information sections
- Links to various site sections
- Copyright information
- "Back to top" button


## API Integration

The website uses [FakeStore API](https://fakestoreapi.com/) to fetch product data:

- Product listings: https://fakestoreapi.com/products
- Product details: https://fakestoreapi.com/products/{id}

All prices from the API are consistently formatted to display with 2 decimal places using `Number(price).toFixed(2)`.

## Acknowledgments

- Original design created for JoyMart
- Product data provided by [FakeStore API](https://fakestoreapi.com/)
