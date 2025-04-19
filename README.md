# 🌸 Requirement Document – Flower Shop Website

## 1. 📋 Summary Requirements

This document outlines what the flower shop website will include in its initial version.

### ✅ Features:

> **Note:** Anything not listed below is considered outside the scope of the project. Adding new
> features beyond this list may affect the overall timeline and cost estimates.

- A homepage with promotional banners and featured flower collections
- A product catalog where visitors can browse various flower types
- Individual product pages with description, image, and price
- A shopping cart to review selected items before checkout
- A checkout process where users can place orders
  > **Note:** The client is responsible for selecting the payment/checkout provider (e.g., Stripe,
  PayPal). The developer will support integration only. Pricing and setup fees are discussed
  separately.
- Email confirmation sent to users after completing an order
- A private area for shop owners to:
    - Manage flower listings (add/edit/delete)
    - View and manage customer orders
- Image support for all flower products
- User registration and login, allowing customers to track their orders

---

## 2. 🚫 Out of Scope

The following features are not included in this version:

- Multi-language or multi-currency support
- Inventory management (This website is a brand presentation site with order functionality, not a
  warehouse or stock control system)
- Promo codes or sales campaigns
- A mobile app version (The site will be responsive on mobile, but this is not a native app)
- Blog or news section
- Advanced reporting or analytics
- **Selecting the payment/checkout provider and handling any business agreements or provider fees**
  – only technical integration is included

---

## 3. 🔗 Linked Services

| Service                                      | Role                                        | Free Tier                           | Key Limitations                                      | Upgrade Cost (Monthly) |
|----------------------------------------------|---------------------------------------------|-------------------------------------|------------------------------------------------------|------------------------|
| [**Vercel**](https://vercel.com/pricing)     | Hosts the website and API endpoints         | 100GB bandwidth, single environment | Cold starts after inactivity, no staging environment | $20                    |
| [**Supabase**](https://supabase.com/pricing) | Stores product, order, user, and image data | 500MB storage, basic access         | Slower access after inactivity, limited file storage | $25                    |
| `T.B.D`                                      | Payment processor                           | T.B.D                               | T.B.D                                                | T.B.D                  |
| [**Resend**](https://resend.com/pricing)     | Sends email confirmations                   | 100 emails per day                  | No branded sending domain unless set up              | $20                    |
| **Domain**                                   | Custom website address                      | Not included                        |                                                      | ~$1/month              |

---

## 4. 📦 Tech Stack Summary

| Layer    | Technology                                           |
|----------|------------------------------------------------------|
| Frontend | Next.js (React), Tailwind CSS, `next/image`          |
| Backend  | Vercel API routes, Supabase database                 |
| Auth     | Supabase Auth (email + password)                     |
| Payments | Stripe Checkout (or other provider chosen by client) |
| Email    | Resend                                               |
| Admin    | Protected routes in Next.js                          |
| Storage  | Supabase Storage (images)                            |

---

## 5. 🗓 Project Timeline & Estimated Working Hours

> **Note:** The following timeline reflects development time only. It does not include design or
> content dependencies. Design work must be completed before development begins and is not part of
> this proposal.

| Task                                         | Estimated Days      | Estimated Billable Hours |
|----------------------------------------------|---------------------|--------------------------|
| Project setup                                | 1 day               | 2 hours                  |
| Homepage                                     | 2 days              | 8 hours                  |
| Product listing & detail                     | 3 days              | 13 hours                 |
| Cart & Checkout flow                         | 3 days              | 13 hours                 |
| Email confirmation                           | 1 day               | 3 hours                  |
| User account (signup/login + order tracking) | 2 days              | 8 hours                  |
| Admin dashboard (product + order management) | 5 days              | 13 hours                 |
| Vercel deployment + environment setup        | 1 day               | 2 hours                  |
| Final polish + responsive UI                 | 2 days              | 5 hours                  |
| **Total**                                    | **20 working days** | **67 hours**             |
