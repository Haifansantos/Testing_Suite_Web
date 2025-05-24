Web Automation Testing Suite
Automated end-to-end testing suite for a demo e-commerce website using Selenium WebDriver and pytest.
This project demonstrates QA automation skills by covering key flows: login, product visibility, add to cart, and checkout.

🛠️ Technologies
Python 3.x

Selenium WebDriver

pytest

webdriver-manager

Google Chrome

🚀 Setup & Run
Clone repository

bash
Copy
Edit
git clone https://github.com/Haifansantos/Web-Automation.git
cd Web-Automation
Install dependencies

bash
Copy
Edit
pip install -r requirements.txt
Run tests

bash
Copy
Edit
pytest
Screenshots on failure saved in /reports/screenshots/

📂 Project Structure
arduino
Copy
Edit
Web-Automation/
├── conftest.py             # pytest fixtures & config
├── requirements.txt        # dependencies
├── tests/
│   ├── test_login.py
│   ├── test_product_visibility.py
│   ├── test_add_to_cart.py
│   └── test_checkout.py
└── utils/
    └── driver_setup.py     # webdriver helper
✔️ Test Coverage
User login

Product visibility on inventory page

Adding item to shopping cart

Checkout flow with user info and order completion****
