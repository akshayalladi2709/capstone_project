# BStackDemo E-Commerce Testing Project

## Overview
This project is an automated testing framework for the BStackDemo e-commerce website (https://bstackdemo.com/). It uses Selenium WebDriver with Cucumber for behavior-driven development (BDD) testing. The tests cover various user scenarios including login, shopping, checkout, and handling different user account types.

## Project Structure
```
├── src
│   ├── main
│   │   ├── java
│   │   └── resources
│   └── test
│       ├── java
│       │   └── StepDefinition
│       │       ├── BStackDemo.java
│       │       ├── DemouserSteps.java
│       │       ├── ExistingOrdersUserSteps.java
│       │       ├── FavUserSteps.java
│       │       ├── ImageUserSteps.java
│       │       ├── LockedUserSteps.java
│       │       ├── PageClass.java
│       │       └── TestRunner.java
│       └── resources
│           └── features
│               ├── 1Loginnormaluser.feature
│               ├── 2demousershopping.feature
│               ├── 3ImagenotloadingUser.feature
│               ├── 4FavUserlogin.feature
│               ├── 5ordereduserscart.feature
│               └── 6LockedaccUser.feature
```

## Features
The project tests the following scenarios:

1. **Normal User Login and Shopping Flow** - Complete end-to-end shopping journey with login, product search, cart management, checkout, and order receipt download.

2. **Demo User Shopping** - Testing shopping flow for demo users including search functionality, filters (low to high, high to low), and privacy policy verification.

3. **Image Not Loading User** - Testing behavior when images don't load for specific users.

4. **Favorite User Login** - Testing functionality for users with favorite products.

5. **Existing Orders User** - Testing cart functionality for users with existing orders.

6. **Locked Account User** - Validating error messages for locked user accounts.

## Technologies Used
- Java
- Selenium WebDriver 4.22.0
- Cucumber 7.27.2
- JUnit 4.13.2
- Maven
- WebDriverManager 6.2.0
- Apache POI 5.2.5 (for Excel operations)

## Prerequisites
- Java JDK 8 or higher
- Maven
- Chrome browser

## How to Run Tests

### Using Maven
```bash
mvn clean test
```

### Using TestRunner
Run the `TestRunner.java` class as a JUnit test from your IDE.

## Test Reports
After test execution, reports are generated in the following formats:

- HTML Report: `target/HTML/htmlreport.html`
- JSON Report: `target/JSON/jsonreport`
- JUnit Report: `target/JUNIT/junitreport`

## Page Object Model
The project follows the Page Object Model design pattern:

- `PageClass.java` contains all the web elements and methods to interact with the web pages
- Step definition classes implement the Cucumber steps and use the PageClass methods

## Test Scenarios

### Normal User Login
Tests a complete shopping journey with login, adding products to cart, checkout, and order receipt download.

### Demo User Shopping
Tests shopping functionality for demo users including search, filters, and privacy policy verification.

### Locked User Account
Validates error messages when attempting to log in with a locked user account.

## Contributing
To contribute to this project:

1. Fork the repository
2. Create a feature branch
3. Add your tests
4. Submit a pull request

