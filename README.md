# HAMUSSMANEL — Ultra-Premium Animated Full-Stack Digital Subscription Marketplace

An award-winning, luxury tech e-commerce platform and wholesale digital subscription marketplace built specifically for the Pakistani market (inspired by the business model of subscription.pk), featuring real database persistence, local payment integration (JazzCash, Easypaisa, Raast, Bank Transfer), prepaid reseller wallets, digital credential vaults, and an enterprise administration control panel.

---

## 🌟 Brand Identity & Visual Language

- **Brand:** **HAMUSSMANEL** (`hamussmpanel.online`)
- **Tagline:** Everything Premium. One Smart Destination.
- **Support Helpline / WhatsApp:** **03057482488**
- **Support Email:** **info@Hamussmpanel.online**
- **Color Palette:**
  - **Primary Dark:** `#080B14`
  - **Secondary Dark:** `#111827`
  - **Primary Accent:** `#7567FF`
  - **Secondary Accent:** `#38BDF8`
  - **Muted Slate:** `#94A3B8`
  - **Success Green:** `#16A34A`
  - **Borders:** Subtle slate tones (`#1E293B`)

---

## 🚀 Key Features

### 1. Animated Storefront & Sections
- **Top Announcement Bar:** Configurable promo deal strip with direct WhatsApp contact: `03057482488`.
- **Cinematic Animated Hero:** Floating 3D-inspired glassmorphic subscription cards (ChatGPT Plus, Netflix UHD 4K, Canva Pro, YouTube Premium) with staggered reveals.
- **Trust Indicators (Section C):** 4 core trust pillars (Convenient Digital Ordering, Secure Checkout, Clear Subscription Details, 24/7 Dedicated Support).
- **Category Explorer (Section D):** 6 distinctive category cards (AI Tools, Entertainment, Study & Productivity, VPN & Privacy, IPTV & Live TV, Design & Developer).
- **Featured Subscriptions (Section E):** High-demand subscriptions with multi-plan tiers, discount badges, and instant Add to Cart.
- **Promotional Campaign Banner (Section F):** Annual bundle savings highlight.
- **AI & Productivity Showcase (Section G):** Dedicated collection for ChatGPT Plus, Claude 3.5, and Midjourney.
- **Bestsellers (Section H):** Real database-ranked bestsellers.
- **How It Works (Section I):** 3-step transparent ordering and delivery workflow.
- **Moderated Customer Reviews (Section J):** Verified customer feedback with star ratings and live submission form.
- **Accessible FAQ Accordion (Section K):** Animated accordion answering payment, delivery, and warranty questions.
- **Working Newsletter (Section L):** Connected to database with email validation and deduplication.
- **Luxury Multi-Column Footer (Section M):** Complete contact info, categories, legal policies, and payment badges.

### 2. Shopping Experience & Checkout
- **Filterable Shop (`/shop`):** Real-time search, category filters, price range slider, sort options, and empty states.
- **Interactive Product Detail (`/product/[slug]`):** Plan switcher, dynamic pricing calculation, features checklist, warranty details, customer reviews, related products, and direct WhatsApp ordering.
- **Persistent Cart & Slide-Over Drawer:** LocalStorage sync, quantity adjustments, item deletion, coupon system (`HAMUSS10` for 10% off), subtotal, discount, and total calculation.
- **Pakistani Local Checkout (`/checkout`):**
  - JazzCash (`03057482488` - HAMUSSMANEL OFFICIAL)
  - Easypaisa (`03057482488` - HAMUSSMANEL OFFICIAL)
  - Meezan Bank / Raast IBFT
  - Reseller Prepaid Wallet Balance
  - Transaction ID (Trx ID) verification & customer notes
- **Order Success (`/order-success/[orderId]`):** Order confirmation with direct WhatsApp verification button and credentials vault.

### 3. Wholesale Reseller Portal (`/reseller`)
- Wholesale discounted catalog for agencies and campus sellers.
- Prepaid wallet balance management.
- Deposit request form with JazzCash/Easypaisa/Bank transfer.
- Transaction history ledger with PENDING, APPROVED, and REJECTED statuses.
- Concurrency-safe atomic wallet debit at checkout.

### 4. Enterprise Admin Dashboard (`/admin`)
- **Dashboard Overview (`/admin`):** Database-driven Total Revenue, Total Orders, Active Customers, Pending Fulfillment, and Recent Orders table.
- **Order Administration (`/admin/orders`):** Search, status filtering, payment verification (PENDING -> PAID), fulfillment dispatch (UNFULFILLED -> FULFILLED), and confidential delivery credentials assignment.
- **Product & Plan Management (`/admin/products`):** Create new subscription products, configure multi-tier plans and durations, set starting & original prices, and manage features.
- **Category Administration (`/admin/categories`):** Add/edit categories, slugs, and badges.
- **Reseller Deposit Management (`/admin/resellers`):** 1-click atomic deposit approval that increments reseller wallet balances.
- **Customer Accounts (`/admin/customers`):** View registered users, roles, order counts, and spent totals.
- **Storefront Customization (`/admin/settings`):** Update phone `03057482488`, email `info@Hamussmpanel.online`, announcement bar, and payment receiving accounts.
- **Technical SEO Audit (`/admin/seo`):** Real-time diagnostic tool verifying meta titles, descriptions, image alt tags, canonicals, and sitemap coverage.

### 5. Technical SEO & Legal Compliance
- Dynamic XML Sitemap (`/sitemap.xml`)
- Dynamic Robots.txt (`/robots.txt`)
- Schema.org JSON-LD Structured Data (`Product`, `AggregateOffer`, `OnlineStore`, `Article`)
- Legal pages: Terms (`/terms`), Privacy (`/privacy`), Refund & Warranty (`/refund-policy`), Delivery (`/delivery-policy`), Contact (`/contact`).

---

## 🔐 Demo & Testing Credentials

| Role | Email | Password | Access Area |
|------|-------|----------|-------------|
| **Super Admin** | `admin@hamussmanel.online` | `admin1234` | Full `/admin` Console |
| **Wholesale Reseller** | `reseller@hamussmanel.online` | `reseller1234` | `/reseller` Portal (Preloaded with Rs. 25,000) |
| **Customer** | `customer@hamussmanel.online` | `customer1234` | `/account` Customer Dashboard |

> **Promo Code:** Use coupon code `HAMUSS10` during cart or checkout for an instant **10% discount**.

---

## 🛠️ Stack & Architecture

- **Framework:** Next.js 14 (App Router)
- **Language:** TypeScript 5
- **Styling:** Tailwind CSS 3
- **Icons:** Lucide React
- **Animations:** Custom CSS keyframes, micro-interactions, responsive transitions
- **Database ORM:** Prisma Client 5.22
- **Database:** SQLite (persisted locally at `prisma/dev.db` with seamless PostgreSQL migration compatibility)
- **Authentication:** JWT tokens stored in HTTP-Only cookies with bcrypt password hashing

---

## 🏃‍♂️ How to Run

1. **Install Dependencies:**
   ```bash
   npm install
   ```

2. **Database Push & Seed:**
   ```bash
   npx prisma db push
   node scripts/seed.js
   ```

3. **Start Development Server:**
   ```bash
   npm run dev
   ```
   Open `http://localhost:3000` in your browser.

4. **Production Build & Start:**
   ```bash
   npm run build
   npm run start
   ```

5. **Run Automated Test Suite:**
   ```bash
   node scripts/test-workflows.js
   ```
