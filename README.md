# Cornerstone Coffee Co.
### A B2B Wholesale Coffee Ordering Platform

> Built for the cafes that keep the world running — one bulk order at a time.

---

## What Is This?

Cornerstone Coffee Co. is a fully functional B2B wholesale e-commerce platform built for independent cafes and small coffee shops that purchase specialty-grade coffee in bulk. No Shopify. No backend. No shortcuts. Just HTML, CSS, JavaScript, and localStorage holding it all together.

This is a 16-week solo capstone project. It started as a wireframe and became a 14-page functioning web application with authentication, a live cart, a complete checkout with shipping and payment, real-time order tracking, and a secret admin dashboard that requires a hidden trigger just to access.

---

## Features

| Feature | What It Does |
|---|---|
| Authentication | Sign up, log in, stay logged in across all pages |
| Live Cart | Add items, adjust quantity, badge updates in real time |
| Full Checkout | Shipping address form and simulated payment entry |
| Order History | Every order saves to the customer profile automatically |
| Order Tracking | Visual tracker — Processing, Shipped, Delivered |
| Profile Management | Edit name, email, and cafe info with inline validation |
| Admin Dashboard | Password-protected dashboard with full order management |
| Secret Admin Entry | See below... |

---

## The Secret Admin Trigger

There is no admin login button anywhere on this site. That is intentional.

To access the admin dashboard, go to any page on the site, find the Cornerstone Coffee Co. text in the footer, and click it 5 times within 3 seconds.

You will be redirected to the admin login. Password: `coffeeforlife`

From the admin dashboard you can:
- View all orders across every customer account
- See total revenue, registered users, and cart activity
- Advance any order from Processing to Shipped to Delivered
- Watch the customer profile update in real time when you do

---

## How Order Tracking Works

This was the most technically complex feature to build. Here is the full flow:

1. Customer places an order on `cart.html`
2. The order saves to three localStorage keys simultaneously:
   - `cc_orders` — the master order list the admin reads from
   - `cc_users` — the full user database
   - `cc_user` — the active session copy the profile reads from
3. Customer sees the order in `profile.html` with a visual progress tracker
4. Admin logs in, finds the order, and clicks the advance button
5. All three localStorage keys update at once
6. Customer refreshes their profile — status has changed

The reason all three keys must update simultaneously is that each one serves a different part of the application. If even one falls out of sync, the customer sees the wrong order status. That was the hardest bug to track down on this entire project.

---

## Checkout Experience

The cart page includes a complete checkout flow with two form sections:

**Shipping Address**
- Street Address, City, State, Zip Code
- Saves with every order so the admin knows exactly where to ship

**Payment Information**
- Cardholder Name, Card Number, Expiration Date, CVV
- Card number auto-formats with spaces as you type
- Expiry date auto-formats with the slash
- No real payment processing — simulated for demonstration purposes

**Shipping Cost**
- Orders under $100 — $15 flat rate shipping
- Orders $100 and over — free shipping
- Automatically calculated and added to the order total

---

## Tech Stack

```
HTML5         — structure across 14 pages
CSS3          — custom dark theme, CSS Grid, Flexbox
JavaScript    — all logic, no frameworks
localStorage  — data persistence without a backend
Google Fonts  — Hammersmith One + Space Mono
```

No libraries. No frameworks. No backend. Everything runs in the browser.

---

## Design

- Color palette: near-black backgrounds (#0a0a0a, #141414, #222222) with off-white text (#f5f5f5)
- Typography: Hammersmith One for headings, Space Mono for UI and body text
- Theme: dark, minimal, editorial
- Consistency: same nav, footer, and CSS variables across all 14 pages

---

## Pages

```
index.html                     — Landing page
shop.html                      — Product catalog with search and filter
wholesale.html                 — Wholesale program info and inquiry form
our-story.html                 — Brand story and team section
contact.html                   — Contact form with validation
cart.html                      — Shopping cart, checkout, shipping, and payment
auth.html                      — Sign in and create account
profile.html                   — Order history, tracking, and profile editing
admin.html                     — Password-protected admin dashboard
product-everyday-gold.html     — Product detail page
product-morning-bloom.html     — Product detail page
product-founders-reserve.html  — Product detail page
product-high-road-decaf.html   — Product detail page
product-midnight-press.html    — Product detail page
product-cornerstone-blend.html — Product detail page
```

---

## localStorage Keys

| Key | What Is Stored |
|---|---|
| `cc_cart` | Current cart items array |
| `cc_user` | Currently logged in user session |
| `cc_users` | All registered user accounts |
| `cc_orders` | All orders across all customers |

---

## How To Run It

No installs. No setup. No terminal.

1. Download or clone the repository
2. Open `index.html` in your browser
3. That is it

---

## Project Timeline

| Milestone | Timeline |
|---|---|
| Project Proposal | Week 1 |
| Wireframes and Design System | Weeks 2-3 |
| Core Pages Built | Weeks 4-8 |
| JavaScript Features | Weeks 9-12 |
| Midterm Presentation | Week 8 |
| Shipping, Payment, and Polish | Weeks 13-15 |
| Final Presentation | Week 16 |

---

## Built By

**Lauryn Miller** — Web Development Capstone, 2026

> "I almost just built a landing page. Glad I didn't."

---

*Cornerstone Coffee Co. — Because your cafe deserves better than a spreadsheet order form.*
