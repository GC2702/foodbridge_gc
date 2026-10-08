# 🍲 FoodBridge — Campus Surplus Food Redistribution Network

FoodBridge is a real-time campus surplus food rescue platform designed to connect mess halls, food courts, and campus event organizers with students to eliminate campus food waste.

---

## 🔗 Project Links

- **Live Application**: https://foodbridge-gc-j7db.vercel.app/
- **GitHub Repository**: https://github.com/GC2702/foodbridge_gc
- **Backend API**: https://foodbridge-c5zw.onrender.com

---

## 🚀 Key Features

- **Instant Surplus Listing**: Mess staff or event coordinators can publish surplus food specifying title, portion quantity, pickup point, and a dynamic best-before time.
- **Real-Time Expiration & Claim Locking**: Post countdown timers automatically disable claims the second a listing expires, switching status to `POST CLOSED`.
- **Portion Allocation & Reg No Tracking**: Students can claim portions using their registration number, with real-time stock reduction preventing overclaiming.
- **Live Impact Dashboard**:
  - **Servings Rescued**: Live counter of all successfully claimed portions.
  - **Servings Expired**: Accurately accounts for any portions left unclaimed once a listing passes its deadline.
- **One-Click State Reset**: Built-in test endpoint and UI button to reset the in-memory store for evaluation cycles.

---

## 🛠 Tech Stack

- **Frontend**: React (Vite), Modern CSS, HTML5
- **Backend**: Node.js, Express.js, CORS
- **Deployment**: 
  - Frontend: **Vercel**
  - Backend: **Render**

---

## 📡 API Endpoints

| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `GET` | `/api/posts` | Returns all active and closed listings ordered by best-before time |
| `POST` | `/api/posts` | Creates a new surplus food listing |
| `POST` | `/api/posts/:id/claims` | Claims a portion quantity against a listing |
| `GET` | `/api/stats` | Returns aggregated metrics (`servingsSaved`, `servingsMissed`) |
| `POST` | `/api/reset` | Resets all in-memory posts, claims, and metrics |

---

## 💻 Local Setup & Execution

### 1. Clone the repository
```bash
git clone [https://github.com/GC2702/foodbridge_gc.git](https://github.com/GC2702/foodbridge_gc.git)
cd foodbridge_gc
