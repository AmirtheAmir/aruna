# Aruna

<<<<<<< HEAD
Aruna is a collectible toy e-commerce website built for the Aruna collection. The site presents premium collectible products through a clean storefront experience with collection browsing, product detail pages, search, cart, checkout, account management, newsletter signup, and policy pages.
=======

[Live Demo](https://arunacollection.vercel.app)

## Overview

Aruna helps collectors explore toy and model collections, inspect product details and availability, and organize items for purchase. Collection pages, searchable inventory, and product galleries connect catalog browsing with cart management.

Supabase provides catalog data, product images, authentication, profiles, saved addresses, newsletter subscriptions, and policy content. Checkout presents address and payment forms with calculated totals; payment processing and order creation are not implemented, and the orders tab displays an empty state.

<<<<<<< HEAD
Aruna was built to turn a collectible toy catalog into a complete online shopping experience. Instead of showing products as a static gallery, the project gives collectors a practical way to browse, compare, search, and prepare purchases from one responsive interface.
=======
## Key Features
>>>>>>> 7272dd0 (updated readme files)

- **Collections and Product Details:** Browse Classics, Modern, Batman, Speed Racer, and Ferrari collections, with image galleries, descriptions, pricing, and sold-out states.
- **Search and Filtering:** Search product names and tags, preview matching products and tag suggestions, filter results by availability and price range, and sort by price.
- **Session Cart:** Add products, adjust quantities, remove items, and review totals, with cart contents retained in sessionStorage and synchronized cart counts.
- **Checkout Preview:** Enter shipping and billing details or select saved addresses, apply predefined discount codes, and view shipping estimates for Finland or Australia with estimated tax.
- **Authentication and Accounts:** Sign up or sign in using Supabase email OTP, edit profile details, and add, edit, or delete up to four addresses with a default address selection.
- **Currency Selection:** Search available countries and currencies and convert displayed catalog prices using fixed client-side exchange rates.
- **Newsletter and Policies:** Submit newsletter subscriptions with email validation and duplicate handling, and read database-backed refund, privacy, shipping, terms, and cookie policies.

## Tech Stack

- **Core:** Next.js App Router, React, TypeScript
- **Styling & Animation:** Tailwind CSS, CSS Modules, Motion
- **Backend & Services:** Supabase Database, Supabase Auth, Supabase Storage, Next.js Route Handlers
- **Data Fetching:** Axios, Fetch API
- **Tooling:** npm, ESLint, PostCSS, SVGR, React Compiler
- **Analytics:** Vercel Analytics

## Technical Highlights

- **Server and Client Data Flow:** Server components query Supabase for home, collection, and product pages. Route handlers expose products and policies and accept newsletter subscriptions, while a shared typed mapper normalizes product rows for the UI.

![Search page screenshot](./public/screenshots/desktop_searchPage.png)

- **Reusable Component Architecture:** Atoms, molecules, and organisms compose shared product cards, filter controls, navigation, account modals, and checkout sections. A common policy page renders database sections ordered by their section index.

![Policies page screenshot](./public/screenshots/policies.png)

- **Cart Synchronization:** Shared helpers persist cart items in sessionStorage and dispatch a custom cart-updated event, which cart views, checkout, and navigation subscribe to for updates.
- **Client-Side Catalog Processing:** Memoized transformations match names and tags, deduplicate search suggestions, calculate availability counts, and apply price ranges and sorting to fetched catalog data.

## Getting Started

### Clone Repository

```bash
git clone https://github.com/AmirtheAmir/aruna.git
cd aruna
```

### Install Dependencies

```bash
npm install
```
