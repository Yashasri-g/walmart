# Walmart Companion AI — Unified Smart Retail Assistant

---

## ✅ PROJECT NAME
**Walmart Companion AI** — Unified Smart Retail Assistant

---

## ✅ OVERALL FLOW

1. **Login Page** → 2. **Role-Based Dashboard** → 3. **Role-Specific Tabs**

- Users land on **Login Page**
- Select role: **Admin/Store Manager** or **Customer/Shopper**
- On successful login, route to role dashboard
- Each dashboard shows relevant tabs only

---

## ✅ MAIN PAGES & WHAT HAPPENS

### 🗂️ 1. Login Page

**Purpose:**
- Authenticate & set user type
- Store role in session

**Components:**
- Email & password (mock)
- Role selector: Admin or Customer
- Route to `/admin` or `/customer` after login

**Tech:** React + Context for role, no real backend auth needed.

---

### 🗂️ 2. Admin Dashboard

**URL:** `/admin`

**Tabs:**
- 📊 **Demand Forecast**
- 📑 **Reports**
- 📦 **Inventory Planner**

#### ✅ Tab: Demand Forecast

**What’s Here:**
- Interactive charts for predicted sales by Dept
- Data source: Prophet JSON
- Filters for date ranges, depts

**ML / Data:**
- Prophet forecast output displayed with Chart.js/Recharts

**Purpose:**
- Visualize future demand → help plan stock

---

#### ✅ Tab: Reports

**What’s Here:**
- Past sales vs forecast comparison
- Holiday sales trends
- Option to download CSV/PDF

**ML / Data:**
- Historical dataset + Prophet results

**Purpose:**
- Analyze prediction accuracy → adjust promotions, staff

---

#### ✅ Tab: Inventory Planner

**What’s Here:**
- Highlight Depts at risk of stockout (low stock + high forecasted sales)
- Smart reorder recommendations
- Mock ‘Reorder Now’ or ‘Send to Supplier’ button

**ML / Data:**
- Prophet forecast + simple stock rules

**Purpose:**
- Connect demand insight → actionable supply chain decision

---

### 🗂️ 3. Customer Dashboard

**URL:** `/customer`

**Tabs:**
- 🛍️ **Smart Recommendations**
- ⚡ **Express Checkout**
- 🧭 **Smart Guide**
- 🚚 **Delivery Status**

#### ✅ Tab: Smart Recommendations

**What’s Here:**
- “You may like” product carousel
- Mock upsell bundles, substitutes
- Click → Add to Cart

**ML / Data:**
- (Optional) Small content-based filter (Python + JSON)
- Or static mock recs for demo

**Purpose:**
- Show how personalized suggestions boost convenience & basket size

---

#### ✅ Tab: Express Checkout

**What’s Here:**
- Cart summary
- Quick pay mock (pretend card/UPI)
- QR code for in-store self-checkout

**ML / Data:**
- No ML, just flow

**Purpose:**
- Proves frictionless checkout concept → reduced lines

---

#### ✅ Tab: Smart Guide

**What’s Here:**
- In-cart micro tips: “Try this healthy substitute”
- Budget-friendly switch suggestions
- Eco-friendly label tags

**ML / Data:**
- Small rule-based tags OR static JSON

**Purpose:**
- Educates cost-conscious shoppers → trust + loyalty

---

#### ✅ Tab: Delivery Status

**What’s Here:**
- Order status page
- Mock real-time ETA
- Notifications like “Out for Delivery”

**ML / Data:**
- Frontend-only dummy updates

**Purpose:**
- Makes post-checkout experience clear → no frustration

---

## ✅ HOW THE TECH CONNECTS

| Page                | Frontend                  | Backend / Model              |
|---------------------|--------------------------|------------------------------|
| Login               | React                    | Context or LocalStorage for role |
| Admin: Demand Forecast | React + Chart.js      | Prophet JSON                 |
| Admin: Reports      | React tables & charts    | Prophet JSON + uploaded CSV  |
| Admin: Inventory Planner | React + simple logic | Forecast + rules in Python, output JSON |
| Customer: Smart Recs| React carousel           | Mock recsys JSON             |
| Customer: Express Checkout | React            | Static flow                  |
| Customer: Smart Guide | React tips             | Static JSON                  |
| Customer: Delivery Status | React              | Dummy ETA logic              |

---

## ✅ FOLDER STRUCTURE

```
/walmart-companion-ai
│
├── /public
├── /src
│   ├── /components
│   │   ├── Login.jsx
│   │   ├── AdminDashboard.jsx
│   │   ├── CustomerDashboard.jsx
│   │   ├── DemandForecast.jsx
│   │   ├── Reports.jsx
│   │   ├── InventoryPlanner.jsx
│   │   ├── SmartRecs.jsx
│   │   ├── ExpressCheckout.jsx
│   │   ├── SmartGuide.jsx
│   │   ├── DeliveryStatus.jsx
│   ├── /data
│   │   ├── forecast.json
│   │   ├── recs.json
│   │   ├── guide.json
│   ├── App.jsx
│   ├── routes.jsx
└── package.json
```

---
````
