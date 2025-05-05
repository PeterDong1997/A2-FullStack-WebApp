# IFN582 - Assignment 2: Full-Stack Web Application (Team Project)

This repository contains the collaborative development of our Flask + MySQL web application for **Assignment 2** of QUT’s IFN582 unit.

Note: This repo will hold different versions and prototypes contributed by team members. The final template and structure will be confirmed by **Week 11** after team-wide review.

---

## Project Overview

We are building a full-stack web application using:
- Flask (Python backend)
- MySQL (Database)
- HTML/CSS with Bootstrap (Frontend)

The application includes user-facing functionality such as:
- Product browsing
- Basket management
- Checkout
- Admin access control

---

## Tech Stack

| Component     | Tool/Framework        |
|---------------|-----------------------|
| Backend       | Flask (Python)        |
| Database      | MySQL / Flask-MySQLdb |
| Frontend      | HTML, CSS, Bootstrap 5|
| Forms         | Flask-WTF / WTForms   |
| Deployment    | Localhost (in development phase) |

---

## Repository Structure

```
your-repo/
│
├── app.py # Main Flask app
├── templates/ # Jinja2 HTML templates
│ ├── index.html # Landing/search page
│ ├── product_details.html # Item detail & add to basket
│ ├── delivery_request.html # Delivery method selection
│ └── checkout.html # Final checkout page
├── static/ # CSS, JS, images
│ └── style.css
├── sample_data/ # For mock product or user data
│ └── products.csv
├── database/ # Future: MySQL schema & seed data
│ └── schema.sql
├── tasks.md # Task and contribution tracker
└── README.md
```

---

## Functional Pages Overview

| Page                   | Purpose                                                        |
|------------------------|----------------------------------------------------------------|
| index.html             | Main landing page; includes product listing, filtering, search |
| product_details.html   | Shows product info (image, price, description); add to basket  |
| delivery_request.html  | User selects delivery method (click & collect, express, eco)   |
| checkout.html          | Final order summary; collects user information                 |

These pages will later be dynamically rendered using Flask routes and MySQL database queries.

---

## Database Integration Plan

We will integrate MySQL with Flask-MySQLdb and design the following database schema:

- users  
  Fields: user_id, name, email, password_hash, is_admin

- products  
  Fields: product_id, name, category, price, stock, image_url

- orders  
  Fields: order_id, user_id, delivery_type, timestamp

- order_items  
  Fields: order_item_id, order_id, product_id, quantity

Sample data will be stored in `.csv` or `.sql` files under `/sample_data`.  
A full schema initialization script will be provided as `schema.sql`.

---

## Next Steps

- [ ] Share Flask base structure (in progress – due Week 10)
- [ ] Confirm shared template and assign key features (by Week 11)
- [ ] Begin MySQL integration and testing (Week 11–12)
- [ ] Prepare for Week 13 live demonstration

---

## Contribution Notes

Team members are encouraged to:
- Use meaningful commit messages
- Document updates clearly in `tasks.md`
- Pull regularly from `main` to avoid merge conflicts
- Ask questions openly in the group chat or GitHub issues
