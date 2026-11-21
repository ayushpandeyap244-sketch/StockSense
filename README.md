# StockSense — Inventory Management

StockSense is a browser-based inventory management app for tracking products, stock levels and stock movements across warehouses and locations. It runs entirely on the front end (plain HTML, CSS and JavaScript) and saves its data in the browser's `localStorage`, so there is nothing to install and no server to set up.

## Features

- **Dashboard** – live overview of stock, low-stock alerts, and open receipts and deliveries (late vs. upcoming).
- **Products** – product catalog with SKU, category, unit of measure, cost and a **reorder point** that powers low-stock warnings.
- **Receipts** – record incoming stock from suppliers.
- **Delivery** – record outgoing stock to customers.
- **Adjustments** – transfer stock between two locations or correct counts after a stock-take.
- **Stock** – current quantity of every product, with the option to edit counts.
- **Move History** – a log of every stock movement.
- **Warehouses & Locations** – manage multiple warehouses and the storage locations inside them.
- **Authentication & roles** – sign up / log in, with an **Inventory Manager** role (full access) and a staff role (Products, Warehouses and Locations are hidden).
- **Password reset** – OTP-style reset flow (simulated on the front end).
- **Built-in help** – guided intro tour, a full in-app Guide, and a context-help button on every screen.

## Getting Started

No build step or dependencies are needed.

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/<your-repo>.git
   cd <your-repo>
   ```
2. Open `index.html` in any modern browser (just double-click the file).

### Demo account

The app is seeded with sample products, warehouses and locations, plus a demo user:

| Login Id | Password   | Role              |
|----------|------------|-------------------|
| `demo`   | `demo1234` | Inventory Manager |

You can also create your own account from the sign-up screen.

## Project Structure

```
.
├── index.html   # Page markup and CSS
├── script.js    # All application logic (data, rendering, auth, modals)
└── README.md
```

## How Data Is Stored

All data lives in your browser under the `localStorage` key `stocksense_db_v2`. This means:

- Data persists across page reloads, but only in that browser on that device.
- Clearing site data resets the app back to its seeded demo state.
- Users, passwords and the password-reset OTP are all stored client-side, so this is a prototype and **not suitable for real or sensitive data**.

## Roadmap

- Django (Python) backend with a proper database to replace `localStorage`.
- Server-side authentication and role-based permissions.
- Move CSS into its own stylesheet.

## Tech Stack

HTML5 · CSS3 · Vanilla JavaScript (no frameworks or external libraries)
