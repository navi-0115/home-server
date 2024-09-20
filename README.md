# Home Server

[Home Server](https://amazingsafari.haidar.dev) is a online store for home server products

Table of Contents:

- [Home Server](#home-server)
  - [Links](#links)
  - [Features](#features)
  - [UI Designs](#ui-designs)
    - [Home Page](#home-page)

## Links

- Website/Frontend: <https://homeserver.navinrgh.site>
  - Backend: <https://homeserver-backend.navinrgh.site>
- Repositories:
  - General: <https://github.com/mhaidarhanif/amazingsafari>
  - Backend: <https://github.com/mhaidarhanif/amazingsafari-backend>
  - Frontend: <https://github.com/mhaidarhanif/amazingsafari-frontend>

Inspirations:

- <https://servermall.com/>
- <https://bambino.budigunawan.com>
- <https://stlzoo.org/services/gift-shops/zoo-merchandise>

## Features

- Home page
  - Hero section
  - Products catalogue. Example: <https://bambino.budigunawan.com>
- Product page
  - Image
  - SKU (stock keeping unit)
  - Name
  - Price
  - Description
  - Add to cart form: quantity input & add to cart button
- Shopping cart page
  - Product items to buy
    - Image, name, price, quantity, total (price x quantity)
    - Remove item
  - Link: continue shopping, go to products catalogue
  - Link: checkout
- Checkout page
  - Order summary
    - Product items to buy
    - Grand total of all product items to buy

## UI Designs

- Figma: <https://www.figma.com/design/vH4MyTnT20CLf9MKW7dKLO/Home-Server-E-Commerce?node-id=0-1&t=ZqHwyYDMnEjdAEgU-1>

### Home Page

<img alt="Home Page" src="./designs/home.jpg" width="400" />

## Entity Relationship Diagram (ERD)

![ERD](./diagrams/erd.svg)

## REST API Endpoints

- Production: `https://amazingsafari.haidar.dev`
- Local: `http://localhost:3000`

| Endpoint         | HTTP     | Description               |
| ---------------- | -------- | ------------------------- |
| `/products`      | `GET`    | Get all products          |
| `/products/:id`  | `GET`    | Get product by id         |
| `/products/seed` | `POST`   | Seed all initial products |
| `/products`      | `POST`   | Add new product           |
| `/products`      | `DELETE` | Delete all products       |
| `/products/:id`  | `DELETE` | Delete product by id      |
| `/products/:id`  | `PUT`    | Update product by id      |

### Product

```json
{
  "id": "abc123",
  "name": "Panda Plush",
  "price": 120000
}
```

### Add New Product

Request Body:

```json
{
  "name": "Panda Plush",
  "price": 120000,
  "color": "white"
}
```

Response Body:

```json
{
  "id": "abc123",
  "name": "Panda Plush",
  "price": 120000,
  "colors": ["white"]
}
```
