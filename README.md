#  Cornerstone Coffee Co.
### *A B2B Wholesale Coffee Ordering Platform*

> Built for the cafes that keep the world running — one bulk order at a time.

---

## What Is This?

Cornerstone Coffee Co. is a fully functional B2B wholesale e-commerce platform built for small cafes and restaurants that need to order coffee in bulk. No Shopify. No backend. No shortcuts. Just HTML, CSS, JavaScript, and a whole lot of localStorage holding it all together.

This is my 16-week capstone project. It started as a wireframe and turned into a 14-page functioning web app with authentication, a live cart, order tracking, and a secret admin dashboard.

---

##  Features

| Feature | What It Does |
|---|---|
|  Authentication | Sign up, log in, stay logged in across pages |
|  Live Cart | Add items, adjust quantity, see the badge update in real time |
|  Order Checkout | Place orders with a simulated payment flow |
|  Order History | Every order saves to your profile automatically |
|  Order Tracking | Visual tracker  Processing  Shipped  Delivered |
|  Profile Management | Edit your name, email, cafe info with inline validation |
|  Admin Dashboard | Password-protected dashboard with full order and user management |
|  Secret Admin Entry | *See below...* |

---

##  The Secret Admin Trigger

There is no "Admin Login" button anywhere on the site. That's intentional.

To access the admin dashboard, go to **any page** on the site, find the **Cornerstone Coffee Co.** text in the footer, and **click it 5 times within 3 seconds.**

You'll be redirected to the admin login. Password: `coffeeforlife`

From the admin dashboard you can:
- View all orders across every customer account
- See total revenue, registered users, and cart activity
- Advance any order from Processing  Shipped  Delivered
- Watch the customer's profile update in real time when you do

---

##  How Order Tracking Works

This was the trickiest feature to build. Here's the full flow:

1. Customer places an order on `cart.html`
2. Order saves to **three** localStorage keys simultaneously:
   - `cc_orders`  the master order list the admin reads from
   - `cc_users`  the full user database
   - `cc_user`  the active session copy the profile reads from
3. Customer sees their order in `profile.html` with a visual progress tracker
4. Admin logs in, finds the order, clicks ** Shipped** or ** Delivered**
5. All three localStorage keys update at once
6. Customer refreshes their profile  status has changed

The reason it has to update all three at the same time? If even one falls out of sync, the customer sees the wrong status. That bug took a while to track down.

---

##  Tech Stack

```
HTML5          structure across 14 pages
CSS3           custom dark theme, CSS Grid, Flexbox
JavaScript     all logic, no frameworks
localStorage   data persistence (cart, users, orders)
Google Fonts   Hammersmith One + Space Mono
```

No libraries. No frameworks. No backend. Everything runs in the browser.

---

##  Design

- **Color palette:** Near-black backgrounds (`#0a0a0a`, `#141414`, `#222222`) with off-white text (`#f5f5f5`)
- **Typography:** Hammersmith One for headings, Space Mono for UI elements and body
- **Theme:** Dark, minimal, editorial  think specialty coffee meets luxury brand
- **Consistency:** Same nav, same footer, same CSS variables across all 14 pages

---

##  Pages

```
index.html                   Landing page
shop.html                    Product catalog with search + filter
wholesale.html               Wholesale program info + inquiry form
our-story.html               Brand story + team section
contact.html                 Contact form with validation
cart.html                    Shopping cart + checkout
auth.html                    Sign in / Create account
profile.html                 Order history + tracking + profile edit
admin.html                   Password-protected admin dashboard
product-everyday-gold.html   Product detail page
product-morning-bloom.html   Product detail page
product-dark-matter.html     Product detail page
product-single-origin.html   Product detail page
product-cold-brew.html       Product detail page
product-decaf.html           Product detail page
```

---

##  localStorage Keys

| Key | What's Stored |
|---|---|
| `cc_cart` | Current cart items array |
| `cc_user` | Currently logged in user (session) |
| `cc_users` | All registered user accounts |
| `cc_orders` | All orders across all customers |

---

##  How To Run It

No installs. No setup. No terminal.

1. Download or clone the repository
2. Open `index.html` in your browser
3. That's it

---

##  Project Timeline

| Milestone | Date |
|---|---|
| Project Proposal | Week 1 |
| Wireframes + Design System | Week 2-3 |
| Core Pages Built | Week 4-8 |
| JavaScript Features | Week 9-12 |
| Midterm Presentation | Week 8 |
| Final Presentation | Week 16 |

---

##  Built By

**Lauryn Miller**  Software Development Capstone, 2026

> *"I almost just built a landing page. Glad I didn't."*

---

*Cornerstone Coffee Co.  Because your cafe deserves better than a spreadsheet order form.*
