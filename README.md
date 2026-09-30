<div align="center">

# 🏠 Marsa — Booking System

### Real Estate Rental Platform for the Egyptian Market

Chalets · Villas · Apartments · Studios · Hotels — book directly, or through brokers and owners

![Flutter](https://img.shields.io/badge/Mobile-Flutter-02569B?logo=flutter&logoColor=white)
![.NET](https://img.shields.io/badge/Backend-ASP.NET_Core-512BD4?logo=dotnet&logoColor=white)
![Architecture](https://img.shields.io/badge/Architecture-Onion-blue)
![Auth](https://img.shields.io/badge/Auth-JWT_%2B_Google-success)
![Status](https://img.shields.io/badge/Status-Active_Development-orange)

[📱 Download APK](../../releases/latest) · [✨ Features](#-features) · [📸 Screenshots](#-Screenshots) · [🏗 Architecture](#-architecture) · [🗺 Roadmap](#-roadmap)

</div>

---

## 📖 Overview

**Marsa** is a rental booking platform built for the Egyptian real estate market. It connects **tenants**, **owners**, and **brokers** in one system and handles every real-world booking scenario, including the ones that happen offline.

Most platforms only support self-service online bookings. In Egypt, a large share of rentals go through brokers or are arranged by phone. The platform treats these as first-class flows: owners can record them manually, track broker commissions, and keep every tenant and broker in the database for future reuse.

---

## 📱 Download

The Android app is available for testing as a GitHub Release.

**👉 [Download the latest APK](../../releases/latest)**

> 🚀 **Coming soon:** Marsa will be published on **Google Play** and the **Apple App Store**.

---

## ✨ Features

### 🔐 Authentication

- User registration and login
- Form validation and password confirmation validation
- Secure token storage and persistent authentication session
- API error handling
- Loading, success, and failure states

### 🏠 Home & Discovery

The home screen provides multiple sections to help users find available units:

- All Units
- Featured Units
- Units Under 1000 EGP
- Quick category filtering (Chalet, Villa, and other unit types)
- Search
- Responsive unit cards
- Skeleton and shimmer loading states

### 🏡 Unit Details

Each unit has a dedicated details screen with everything a guest needs before reserving:

- Unit images, name, and location
- Description and amenities
- Category and capacity
- Price per night
- Rating and reviews count
- Booking action

### 📅 Booking Flow

Marsa provides a 4-step booking experience:

1. **Date Selection:** choose check-in and check-out dates against the availability calendar.
2. **Booking Summary:** review the unit, dates, number of nights, price details, coupon information, and final price.
3. **Payment:** pay manually through **InstaPay** or **wallet transfer**, and upload the transfer receipt as part of the booking.
4. **Booking Confirmation:** review the booking and payment information and track the current booking status.

### ❤️ Favorites

- Add / remove favorites
- Dedicated favorites screen with synchronized favorite state
- Empty, loading, and failure/retry states
- Pull-to-refresh

### 📋 My Appointments

Users manage their reservations organized by booking status. Each booking shows the unit, location, dates, status, final price, booking ID, and details.

### 👤 Profile

- View and update profile information
- Light / Dark theme switching
- Arabic / English localization
- Logout

### 🧑‍💼 Owner & Broker Workflows (Platform)

Beyond self-service bookings, the platform supports the way rentals actually happen in Egypt:

| Scenario | How it works |
|---|---|
| **Self-service** | The tenant books in the app and the system handles the whole process. |
| **Broker / offline booking** | The owner creates the booking manually, enters the tenant's data, and sets the broker's commission percentage. The calendar is blocked immediately. |
| **Broker with an account** | The broker either notifies the owner or submits the booking data, and the owner **approves** it after verification. |
| **Customer & broker reuse** | Manual tenants and brokers are stored in the database, so repeat customers are never re-entered and can later be invited to create their own accounts. |

Each booking receives a human-readable reference in the format `BK-YYYY-MM-NNNN`.

### 💳 Payments & Discounts

- **Currency:** Egyptian Pound (EGP) only
- **Current:** manual verification for InstaPay and e-wallets. The payment starts as `Pending`, and the owner or admin confirms it after checking the transfer and receipt (`Pending → Confirmed / Succeeded`).
- **Planned:** card payments through a payment gateway and automated verification.
- **Discounts:** coupon codes with percentage-based discounts.

---

# 📸 Screenshots

> Screenshots showcase the main application flows, UI states, booking experience, and user features.

## 🔐 Authentication

| Login | Register |
|:---:|:---:|
| <img src="Docs/Screenshots/login_light.png" width="250"> | <img src="Docs/Screenshots/register_light.png" width="250"> |

---

## 🏠 Home & Discovery

| Loading | Home | Units |
|:---:|:---:|:---:|
| <img src="Docs/Screenshots/home_loading_light.png" width="250"> | <img src="Docs/Screenshots/home4_light.png" width="250"> | <img src="Docs/Screenshots/home3_light.png" width="250"> |

### 🔎 Filtering

<p>
  <img src="Docs/Screenshots/filter1_light.png" width="250">
  <img src="Docs/Screenshots/filter_dark.png" width="250">
  <img src="Docs/Screenshots/filter3_light.png" width="250">
</p>

---

## 🏡 Unit Details

<p>
  <img src="Docs/Screenshots/details1_dark.png" width="250">
  <img src="Docs/Screenshots/details2_dark.png" width="250">
  <img src="Docs/Screenshots/details3_light.png" width="250">
</p>

---

## 📅 Booking Flow

| Date Selection | Date Selection | Booking Summary |
|:---:|:---:|:---:|
| <img src="Docs/Screenshots/date_step_light.png" width="250"> | <img src="Docs/Screenshots/date_step2_dark.png" width="250"> | <img src="Docs/Screenshots/summary_step_dark.png" width="250"> |

| Payment | Confirmation | Booking Status |
|:---:|:---:|:---:|
| <img src="Docs/Screenshots/payment_step2_dark.png" width="250"> | <img src="Docs/Screenshots/appointment_done_light.png" width="250"> | <img src="Docs/Screenshots/appointment_done2_dark.png" width="250"> |

---

## 👤 User Features

### ❤️ Favorites

| Empty State | Loading State | Favorites List |
|:---:|:---:|:---:|
| <img src="Docs/Screenshots/fav_empty.png" width="250"> | <img src="Docs/Screenshots/fav_loading.png" width="250"> | <img src="Docs/Screenshots/fav_dark.png" width="250"> |

---

### 📋 My Appointments

| All Appointments | Completed | Cancelled |
|:---:|:---:|:---:|
| <img src="Docs/Screenshots/all_appointments_dark.png" width="250"> | <img src="Docs/Screenshots/my_appointments_completed_dark.png" width="250"> | <img src="Docs/Screenshots/my_appointments_canceld_light.png" width="250"> |

---

### 👤 Profile

| Profile | Edit Profile | Theme |
|:---:|:---:|:---:|
| <img src="Docs/Screenshots/profile_light.png" width="250"> | <img src="Docs/Screenshots/edit_profile_light.png" width="250"> | <img src="Docs/Screenshots/theme_light.png" width="250"> |

---

## 🏗 Architecture

The backend is built with **ASP.NET Core** using **Onion Architecture**:

```
┌───────────────────────────────────────────┐
│                  API Layer                │  Controllers, Middleware, DI
├───────────────────────────────────────────┤
│               Service Layer               │  Business logic, DTOs, AutoMapper
├───────────────────────────────────────────┤
│             Repository Layer              │  EF Core, UnitOfWork, Specifications
├───────────────────────────────────────────┤
│                Core Layer                 │  Entities, Interfaces, Enums
└───────────────────────────────────────────┘
        Dependencies point inward ➜ Core
```

### Key Patterns

- **Repository + Unit of Work** with a generic `Repository<T>`
- **Specification pattern** for queries
- **Soft delete** and auto-managed `CreatedAt` / `UpdatedAt`
- **Global exception middleware** with consistent API response models
- **JWT + refresh tokens**, Google Sign-In, OTP flows, and adaptive login protection

### Hosting & Media Storage

- **Current:** the backend is deployed on a Monster hosting server, and unit images are uploaded to and served from that server.
- **Planned:** migration to **Azure**, with **Azure Blob Storage** for images.

---

## 🛠 Tech Stack

| Area | Technology |
|---|---|
| Mobile | Flutter (Android now, iOS planned), Shorebird for code push updates |
| Backend | .NET / ASP.NET Core Web API, Onion Architecture |
| ORM | Entity Framework Core |
| Auth | ASP.NET Core Identity, JWT, Refresh Tokens, Google OAuth |
| Email | MailKit |
| Mapping | AutoMapper |
| Hosting | Monster hosting (current), Azure (planned) |

---

## 🗺 Roadmap

| Completed | Planned |
|:---|:---|
| ✅ Authentication | 🔜 Push notifications |
| ✅ Home & unit discovery | 🔜 Additional payment integrations (cards, automated verification) |
| ✅ Unit details | 🔜 Monthly and yearly rentals |
| ✅ Favorites | 🔜 Bed-level rentals (roommates / shared worker housing) |
| ✅ Multi-step booking flow | 🔜 Owner & broker web dashboard |
| ✅ Payment receipt upload | 🔜 Apple Sign-In |
| ✅ Booking status tracking | 🔜 Azure deployment with Blob Storage |
| ✅ Profile management | 🔜 Further performance improvements |
| ✅ Arabic / English localization | 🔜 Google Play release |
| ✅ Light / Dark theme | 🔜 Apple App Store release |
| ✅ Skeleton & shimmer loading | |
| ✅ Shorebird integration | |

### Upcoming Rental Models

| Model | Description |
|---|---|
| **Daily** (current) | Short stays: chalets, villas, hotels, and similar units. |
| **Monthly / Yearly** (planned) | Long-term residential rentals. |
| **Per bed** (planned) | Shared accommodation such as roommate housing or shared workers' housing. Each bed is independently bookable and priced inside a unit. |

---



Swagger UI will be available at https://booker.runasp.net/.


---

## 📁 Project Structure

```
BookingSystem/
├── Core/          # Entities, interfaces, enums
├── Repository/    # EF Core, DbContext, UnitOfWork, repositories
├── Service/       # Business logic, DTOs, mapping profiles
└── API/           # Controllers, middleware, configuration
```

---

## 👨‍💻 Author

**Ibrahem Elkhatib**

Backend Developer (.NET)

<p align="center">
  <a href="https://github.com/Elkhateb639">
    <img src="https://img.shields.io/badge/GitHub-Elkhateb639-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub">
  </a>
  <a href="https://www.linkedin.com/in/ibrahem-elkhatib">
    <img src="https://img.shields.io/badge/LinkedIn-Ibrahem%20Elkhatib-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
  </a>
  <a href="mailto:ebrahemtamer639@gmail.com">
    <img src="https://img.shields.io/badge/Email-ebrahemtamer639%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email">
  </a>
</p>



---

