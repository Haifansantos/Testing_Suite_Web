Web Automation Testing Suite
Overview
This project contains an automated testing suite for a simple e-commerce web application using Selenium WebDriver and Python. The goal is to demonstrate practical skills in Quality Assurance (QA) engineering by implementing end-to-end tests covering core functionalities such as login, product visibility, add to cart, and checkout.

Features
Automated browser testing using Selenium WebDriver

Test cases covering:

User login

Product visibility verification

Adding product to cart

Checkout process

Reusable WebDriver setup with pytest fixtures

Automatic screenshot capture on test failures

Structured tests split across multiple files for maintainability

Compatible with Chrome via WebDriver Manager

Technologies Used
Python 3.x

Selenium WebDriver

pytest

webdriver-manager

Google Chrome browser

Getting Started
Prerequisites
Python 3.x installed on your machine

Google Chrome browser installed

Git installed (optional, for cloning the repo)

Installation
Clone the repository:

bash
Copy
Edit
git clone https://github.com/Haifansantos/Web-Automation.git
cd Web-Automation
Install required Python packages:

bash
Copy
Edit
pip install -r requirements.txt
Note: Make sure requirements.txt includes selenium, pytest, and webdriver-manager.

Running Tests
To execute the full test suite, run:

bash
Copy
Edit
pytest
Tests will launch Chrome browser sessions and run through defined test scenarios. On failures, screenshots will be saved in the reports/screenshots directory.

Project Structure
Copy
Edit
Web-Automation/
│
├── tests/
│   ├── test_login.py
│   ├── test_product_visibility.py
│   ├── test_add_to_cart.py
│   └── test_checkout.py
│
├── utils/
│   └── driver_setup.py
│
├── conftest.py
├── requirements.txt
└── README.md
