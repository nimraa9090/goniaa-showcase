# Goniaa Showcase

## Pitch
**Goniaa** is a comprehensive, AI-driven e-commerce ecosystem designed to bridge the gap between high-end retail and intelligent brand management. It combines a sleek, user-centric storefront with a powerful administrative suite and a cutting-edge AI Brand Manager to automate growth, optimize operations, and enhance customer engagement.

## Problem/Solution
*   **The Problem:** Traditional e-commerce platforms often suffer from fragmented data, lack of intelligent insights, and poor session persistence, leading to operational inefficiencies and lost sales.
*   **The Solution:** Goniaa provides a unified architecture where a dynamic storefront, a native mobile app, and an AI-powered manager work in tandem. By leveraging persistent state management, dynamic database integration, and AI-driven content scheduling, Goniaa ensures a seamless experience for both customers and brand owners.

## System Overview
The Goniaa ecosystem is composed of four primary pillars:
1.  **Consumer Storefront:** A high-performance web interface for browsing and purchasing.
2.  **Native Mobile Application:** An Expo-powered app featuring advanced capabilities like Virtual Try-on.
3.  **Administrative Dashboard:** A robust command center for managing products, categories, and orders.
4.  **AI Brand Manager:** An intelligent dashboard that handles AI-driven content creation, WhatsApp automation, and predictive analytics.

## Live Links
<!-- TODO: Add your live deployment links below -->
*   **Storefront:** [Link Placeholder]
*   **Brand Manager Demo:** [Link Placeholder]
*   **Mobile App Demo:** [Link Placeholder]

## Tech Stack
| Layer | Technology |
| :--- | :--- |
| **Frontend (Web)** | Next.js, TailwindCSS, Zustand (Persisted) |
| **Mobile App** | Expo (React Native), NativeWind, Drizzle ORM |
| **Backend/Database** | Supabase (PostgreSQL), Auth, Storage |
| **AI Engine** | Google Gemini AI |
| **Infrastructure** | Vercel, GitHub Actions |

## Feature Breakdown

### 🛍️ Storefront & Mobile App
*   **Dynamic Product Catalog:** Real-time synchronization with the admin database.
*   **Virtual Try-on:** (Mobile Exclusive) AI-powered visual testing for products.
*   **Seamless Checkout:** Optimized flow with order tracking and confirmation.
*   **Persistent Cart:** User sessions remain intact across refreshes and devices.

### ⚙️ Administrative Suite
*   **Inventory Management:** Dynamic category creation and product mapping.
*   **Order Fulfillment:** Real-time status updates with optimistic UI feedback.
*   **Reliability Engineering:** Automated data cleaning to prevent database constraint violations.

### 🤖 AI Brand Manager
*   **Content Calendar:** Automated post scheduling for TikTok, Instagram, and Facebook.
*   **WhatsApp Automation:** Intelligent inbound/outbound message handling with quick-reply templates.
*   **AI Analytics:** Predictive scoring for content performance (Algo-Score).

## Technical Highlights
*   **Persistence Layer:** Refactored state management using Zustand middleware to ensure zero session loss on page reloads.
*   **Dynamic Integration:** Replaced hardcoded logic with a fully dynamic database-to-UI pipeline for category management.
*   **Optimistic UI:** Implemented immediate local state updates for administrative actions to provide a "zero-latency" feel.
*   **Asset Pipeline:** Standardized image service for robust handling of product assets and storage bucket routing.

## Note about Private Source Code
The source code for this project is hosted in private repositories. This repository serves as a portfolio showcase featuring documentation, architecture overviews, and visual demonstrations.

<!-- TODO: Add a GIF or screenshot of the overall system here -->
