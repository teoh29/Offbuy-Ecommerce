# OffBuy — E-Commerce Mobile UI/UX Design Case Study

<p align="center">
  <img src="assets/home.png" alt="OffBuy Banner" width="260"/>
</p>

<p align="center">
  <b>A minimalist, human-centered mobile commerce design focused on decluttering the buyer journey, eliminating hidden checkout friction, and streamlining navigation.</b>
</p>

<p align="center">
  <a href="https://drive.google.com/file/d/1jh1Xe4WQP0wJvdOJRtxNez3QX66S0m_d/view?usp=sharing">
    <img src="https://img.shields.io/badge/Demo%20Video-Google%20Drive-blue?style=for-the-badge&logo=google-drive" alt="Watch Presentation"/>
  </a>
  <img src="https://img.shields.io/badge/Design%20Type-Mobile%20UI%2FUX-success?style=for-the-badge" alt="Design Type"/>
  <img src="https://img.shields.io/badge/Context-Academic%20Project-orange?style=for-the-badge" alt="Context"/>
</p>

---

## 📌 Table of Contents
- [Executive Overview](#-executive-overview)
- [Problem Statement](#-problem-statement)
- [Competitive UX Audit](#-competitive-ux-audit)
- [Application Logical Flow](#-application-logical-flow)
- [High-Fidelity Interface Mock-ups](#-high-fidelity-interface-mock-ups)
- [Target Audience & Market Segments](#-target-audience--market-segments)
- [Monetization Strategy](#-monetization-strategy)
- [Proposed Technical Architecture (Java GUI)](#-proposed-technical-architecture-java-gui)
- [Project Presentation](#-project-presentation)
- [Contributors](#-contributors)

---

## 🔍 Executive Overview

During and after the COVID-19 pandemic, consumer reliance on e-commerce escalated drastically. However, many legacy online shopping applications became visually overwhelming—burdened by aggressive advertising banners, nested menus, cluttered product pages, and ambiguous pricing structures.

**OffBuy** is a mobile shopping concept built to bridge these usability gaps. It focuses on:
- **Clean Visual Hierarchy:** Eliminating promotional clutter from core transaction pages.
- **Frictionless Navigation:** A persistent tab structure and predictable path to checkout.
- **Transparent Pricing:** Clear itemized breakdowns of merchandise, shipping costs, discounts, and coin redemptions to combat cart abandonment.

---

## ⚠️ Problem Statement

Modern mobile shoppers encounter friction across four primary touchpoints:

1. **Complex Navigation & Information Clutter:** Multi-layered menus and dense banners obscure core categories and search utilities.
2. **Layout Inconsistencies:** Discrepancies across buttons, typographies, and responsive layouts introduce cognitive fatigue.
3. **Flawed Search & Empty States:** Inadequate filtering and zero-result search errors mislead customers into thinking inventory is unavailable.
4. **Checkout & Payment Anxiety:** Lack of alternative payment methods and ambiguous fees lead to hesitation over data privacy and unexpected totals.

---

## 📊 Competitive UX Audit

Before designing OffBuy, our team audited three dominant market platforms:

| Platform | Strengths Identified | Key UX Bottlenecks & Limitations |
| :--- | :--- | :--- |
| **Shopee** | • Effective white space on home screen<br>• Robust seller rating system<br>• Convenient "Buy Again" shortcut | • Individual product pages are cluttered with redundant shipping/voucher blocks<br>• Small font sizes for discounts and prices |
| **Lazada** | • Prominent bold discount badges<br>• Pre-checked cart functionality<br>• Structured product listing filters | • Inconspicuous in-app wallet icon during time-sensitive checkouts<br>• Transaction history buried beneath promotional banners |
| **SHEIN** | • Strong category taxonomy via information-foraging theory<br>• Integrated shoe "Fit Finder" reducing return rates | • Overwhelming information density<br>• Over-engineered search filter menus causing visual fatigue |

---

## 🧭 Application Logical Flow

The diagram below maps the complete user architecture, from authentication to order fulfillment:

```mermaid
graph TD
    A[Log In / Register] --> B[Home Page]

    B --> C[Notifications]
    B --> D[Discover]
    B --> E[Search & Filters]
    B --> F[Shopping Cart]
    B --> G[Profile]

    C --> C1[Order Updates]
    C --> C2[Promotions]

    D --> H[Product Suggestions]
    E --> H
    H --> I[Product Selection & Detail View]

    I --> F

    F --> J[Checkout Process]
    J --> K[Secure Payment Processing]
    K --> L[Order Confirmation & Tracking]

    G --> M[Me / Personal Details]
    G --> N[Become a Seller]
    G --> O[Customer Support & Feedback]
    G --> P[Purchase History]
    G --> Q[Account Settings]

    M --> M1[Account Info]
    M --> M2[Wishlist]
    M --> M3[Following Shops]
    M --> M4[Recently Viewed]

    P --> P1[Order Tracking]
