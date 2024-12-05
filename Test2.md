
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






   




