### 1. Active Listings & Impact Dashboard
*Live metrics tracking rescued servings alongside active listings with countdown timers:*
# 🍲 FoodBridge — Campus Surplus Food Redistribution Network

FoodBridge is a real-time, campus-wide surplus food redistribution web application designed to connect dining halls, canteens, catering events, and students to prevent edible food from ending up in landfills.

---

## 🔗 Live Links

- **Live Web Application**: [https://foodbridge-gc-j7db.vercel.app/](https://foodbridge-gc-j7db.vercel.app/)
- **GitHub Repository**: [https://github.com/GC2702/foodbridge_gc](https://github.com/GC2702/foodbridge_gc)
- **Backend API Service**: [https://foodbridge-c5zw.onrender.com](https://foodbridge-c5zw.onrender.com)

---

## 📖 What the App Does

FoodBridge allows campus food facilities and event organizers to immediately publish surplus food batches with details such as portion counts, pickup location, and a strict "best before" timestamp. 

Students monitor a live feed, view available portions in real time, and claim servings using their campus registration number. When a food batch reaches its expiry deadline, claiming is automatically locked down, and the system aggregates metrics showing both meals rescued and meals expired.

---

## ✅ Completed Features

- [x] **Surplus Food Publishing**: Form validation for item title, portions, pickup location, and expiration datetime.
- [x] **Real-Time Countdown Badges**: Dynamic client-side countdown timer for each post (`h`, `m`, `s`).
- [x] **Automatic Expiration Locking**: Immediate UI lockdown and server-side validation preventing expired listings from accepting claims (`POST CLOSED`).
- [x] **Safe Portion Claiming**: Registration number-tagged claiming with quantity clamping so users cannot claim more than available stock.
- [x] **Live Impact Metrics Dashboard**:
  - **Servings Rescued**: Real-time count of total portions claimed by students.
  - **Servings Expired**: Automatic tally of portions that went unclaimed past the deadline.
- [x] **One-Click State Reset**: Dedicated reset control to clear in-memory state cleanly between evaluation runs.
- [x] **Cloud Deployment & Sync**: Full-stack separation with the frontend hosted on Vercel and the Express backend hosted on Render.

---

## 📸 Screenshots

### 1. Active Listings & Impact Dashboard
*Live metrics tracking rescued servings alongside active listings with countdown timers:*<img width="1296" height="869" alt="Screenshot 2026-10-08 231418" src="https://github.com/user-attachments/assets/af4429d3-b287-4c54-be8a-d9cdf3c75468" />
---

## 💻 How to Run Locally

### Prerequisites
- Node.js (v16 or higher)
- npm or yarn

### 1. Clone the repository
```bash
git clone [https://github.com/GC2702/foodbridge_gc.git](https://github.com/GC2702/foodbridge_gc.git)
cd foodbridge_gc
How I Used AI
AI Tools Used: Google Gemini

What AI Was Used For:

Debugging Timezone Inconsistencies: Identified that <input type="datetime-local"> outputs un-zoned strings that caused server/client clock mismatches, and resolved it using standardized ISO 8601 UTC timestamp conversions.

State Synchronization Logic: Designed atomic validation on both client and Express routes to lock claims concurrently when isExpired(post) evaluates to true.

Deployment Troubleshooting: Diagnosed and resolved Git remote tracking mismatches across deployment platforms (Vercel frontend build cache and Render web service state).

Documentation & UI Polish: Scaffolded UI components for countdown badges and structured the comprehensive technical documentation.
