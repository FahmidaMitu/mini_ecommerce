# Mini E-commerce REST API

## Features
- Category API (CRUD)
- Product API with Filtering, Searching, Ordering, Pagination
- Token Authentication (Login API)
- Order API (Authenticated user orders)

## Setup Instructions
1. Clone repository: `git clone <https://github.com/FahmidaMitu/mini_ecommerce.git>`
2. Create virtualenv: `python -m venv venv` and activate it.
3. Install dependencies: `pip install -r requirements.txt`
4. Run migrations: `python manage.py migrate`
5. Run server: `python manage.py runserver`

## API Endpoints
- `POST /api/login/` - Login & get Token
- `GET/POST /api/categories/` - List/Create Categories
- `GET/POST /api/products/` - List/Create Products
  - Filter by category: `/api/products/?category=1`
  - Search by name: `/api/products/?search=phone`
  - Order by price: `/api/products/?ordering=price`
- `GET/POST /api/orders/` - List/Create Orders (Requires Token Header: `Authorization: Token <your_token>`)