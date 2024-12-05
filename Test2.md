
# Feature: User Registration in APP

## Scenario: User registers successfully

### Given:
The user is on the registration page.

### When:
The user enters valid information (name, email, password).

### Then:
The user should be successfully registered.  
The user should be redirected to the login page.

## Chai.js Code:
```javascript
const chai = require('chai');
const expect = chai.expect;
const registrationPage = require('../pages/registrationPage');

describe('User Registration', function() {
  it('should register user successfully', function() {
    registrationPage.open();
    registrationPage.fillRegistrationForm('Jane Doe', 'jane@example.com', 'securePassword123');
    registrationPage.submitForm();
    expect(registrationPage.getSuccessMessage()).to.equal('Registration successful');
    expect(browser.getUrl()).to.include('/login');
  });
});
```

# Feature: User Login

## Scenario: User logs in with valid credentials

### Given:


The user is on the login page.

### When:
The user enters valid credentials (email, password).

### Then:
The user should be successfully logged in.  
The user should be redirected to the dashboard.

## Chai.js Code:
```javascript
const chai = require('chai');
const expect = chai.expect;
const loginPage = require('../pages/loginPage');

describe('User Login', function() {
  it('should login user successfully', function() {
    loginPage.open();
    loginPage.enterCredentials('jane@example.com', 'securePassword123');
    loginPage.submitLogin();
    expect(loginPage.getWelcomeMessage()).to.include('Welcome, Jane Doe');
    expect(browser.getUrl()).to.include('/dashboard');
  });
});
```

# Feature: Product Catalog Browsing

## Scenario: User browses products successfully

### Given:
The user is on the product catalog page.

### When:
The user searches for a product category (e.g., "shoes").

### Then:
Relevant products should be displayed based on the search criteria.

### Chai.js Code:
```javascript
const chai = require('chai');
const expect = chai.expect;
const productPage = require('../pages/productPage');

describe('Product Catalog Browsing', function() {
  it('should display products based on search', function() {
    productPage.open();
    productPage.searchProduct('shoes');
    expect(productPage.getSearchResults()).to.not.be.empty;
    expect(productPage.getSearchResultsTitles()).to.include('Running Shoes');
  });
});
```

# Feature: Shopping Cart Management
## Scenario: User adds a product to the cart
### Given:
The user is on a product detail page.

### When:
The user clicks "Add to Cart".

### Then:
The product should be added to the shopping cart.

### Chai.js Code:
```javascript
const chai = require('chai');
const expect = chai.expect;
const productPage = require('../pages/productPage');
const cartPage = require('../pages/cartPage');

describe('Shopping Cart Management', function() {
  it('should add product to the cart', function() {
    productPage.openProduct('123'); // Assume '123' is the product ID
    productPage.addToCart();
    cartPage.open();
    expect(cartPage.getCartItems()).to.include('Running Shoes');
  });
});
```

# Feature: Order Placement
## Scenario: User places an order successfully
### Given:
The user has products in the shopping cart.

### When:
The user proceeds to checkout and completes payment.

### Then:
The order should be placed successfully, and a confirmation message displayed.

### Chai.js Code:
```javascript
const chai = require('chai');
const expect = chai.expect;
const checkoutPage = require('../pages/checkoutPage');

describe('Order Placement', function() {
  it('should place an order successfully', function() {
    checkoutPage.open();
    checkoutPage.enterShippingDetails('123 Main St', 'City', '123456');
    checkoutPage.selectPaymentMethod('Credit Card');
    checkoutPage.submitOrder();
    expect(checkoutPage.getConfirmationMessage()).to.equal('Order placed successfully');
  });
});
```


# Feature: Order Tracking
## Scenario: User checks the status of an order
### Given:
The user has placed an order.

### When:
The user navigates to the order tracking page.

### Then:
The current order status should be displayed.

### Chai.js Code:
```javascript
const chai = require('chai');
const expect = chai.expect;
const trackingPage = require('../pages/trackingPage');

describe('Order Tracking', function() {
  it('should display the correct order status', function() {
    trackingPage.open();
    trackingPage.enterOrderID('ORD123456');
    expect(trackingPage.getOrderStatus()).to.equal('Shipped');
  });
});
```

# Feature: User Profile Management
## Scenario: User updates profile information
### Given:
The user is logged in.

### When:
The user navigates to the profile page and updates their information.

### Then:
The profile should be updated successfully.

### Chai.js Code:
```javascript
const chai = require('chai');
const expect = chai.expect;
const profilePage = require('../pages/profilePage');

describe('User Profile Management', function() {
  it('should update user profile successfully', function() {
    profilePage.open();
    profilePage.updateProfile('Jane Updated', 'janeupdated@example.com');
    expect(profilePage.getSuccessMessage()).to.equal('Profile updated successfully');
  });
});
```


   




