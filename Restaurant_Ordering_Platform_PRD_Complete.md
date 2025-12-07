# 📘 Product Requirements Document (PRD)
## Restaurant Ordering Platform - Complete Specification

---

## 📑 Document Control

| **Item** | **Details** |
|----------|-------------|
| **Project Name** | Restaurant Ordering Platform |
| **Document Type** | Product Requirements Document (PRD) |
| **Document Version** | 2.0 - Complete |
| **Date** | December 2024 |
| **Prepared By** | Development Team - King Saud University |
| **Supervisor** | Dr. Iehab AL Rassan |
| **Document Status** | Final - Ready for Implementation |
| **Target Platform** | iOS Mobile Application (Flutter Framework) |
| **Backend** | Firebase (Firestore, Auth, Cloud Functions, FCM, Storage) |
| **Approval Status** | Pending Review |

---

# Table of Contents

1. [Executive Summary](#1-executive-summary)
2. [Product Scope](#2-product-scope)
3. [Stakeholders & User Roles](#3-stakeholders--user-roles)
4. [User Personas](#4-user-personas)
5. [Technical Architecture](#5-technical-architecture)
6. [Functional Requirements](#6-functional-requirements)
7. [Error Handling Strategy](#7-error-handling-strategy)
8. [Performance Requirements](#8-performance-requirements)
9. [Security & Privacy](#9-security--privacy)
10. [Release Strategy](#10-release-strategy)
11. [Testing Strategy](#11-testing-strategy)
12. [Screen Inventory](#12-screen-inventory)
13. [User Journeys](#13-user-journeys)
14. [Component Library](#14-component-library)
15. [Animations & Interactions](#15-animations--interactions)
16. [Data Requirements](#16-data-requirements)
17. [Prototype Specifications](#17-prototype-specifications)
18. [Success Criteria](#18-success-criteria)
19. [Assumptions & Constraints](#19-assumptions--constraints)
20. [Appendix](#20-appendix)

---

# 1. Executive Summary

## 1.1 Product Overview
Restaurant Ordering Platform is a comprehensive, cross-role mobile application that revolutionizes food delivery by unifying **Customers**, **Restaurants**, and **Drivers** in a single ecosystem. Built with Flutter and Firebase, the platform addresses critical market gaps through innovative features like Family Wallets, Group Orders with Bill Splitting, and real-time order synchronization.

## 1.2 Product Vision
To become the leading food delivery platform in Saudi Arabia by providing:
- **For Customers:** Seamless ordering with advanced payment options
- **For Restaurants:** Powerful management tools and promotional capabilities
- **For Drivers:** Efficient delivery workflow with clear navigation

## 1.3 Business Objectives

| **Objective** | **Metric** | **Target** | **Timeline** |
|--------------|-----------|-----------|--------------|
| User Acquisition | Active users | 10,000 users | 6 months |
| Order Volume | Orders/day | 500+ orders | 3 months |
| Customer Satisfaction | App rating | 4.5+ stars | Ongoing |
| Restaurant Partners | Onboarded restaurants | 100+ restaurants | 6 months |
| Driver Network | Active drivers | 200+ drivers | 4 months |
| Revenue | Monthly GMV | SAR 500,000+ | 6 months |
| Order Completion | Success rate | 95%+ | 3 months |

## 1.4 Success Metrics

### Primary KPIs:
- ✅ **Customer Retention:** 80% month-over-month
- ✅ **Order Completion Rate:** 95%+
- ✅ **Average Delivery Time:** < 35 minutes
- ✅ **Order Cancellation Rate:** < 2%
- ✅ **On-Time Delivery:** 90%+
- ✅ **App Crash Rate:** < 0.1%

### Secondary KPIs:
- Average order value: SAR 60+
- Repeat order rate: 60%+
- Family Wallet adoption: 20% of users
- Group Order usage: 15% of orders
- Restaurant satisfaction: 4.0+ stars
- Driver satisfaction: 4.0+ stars

## 1.5 Target Market

| **Aspect** | **Details** |
|-----------|-------------|
| **Primary Market** | Saudi Arabia (Riyadh initial launch) |
| **Expansion Plan** | Jeddah, Dammam (Phase 2) |
| **Demographics** | Ages 18-45, tech-savvy, middle to upper-middle income |
| **Market Size** | 5M+ potential users in Riyadh |
| **TAM** | SAR 2.5B+ annual food delivery market |
| **Competitive Advantage** | Family Wallet + Group Order features |

## 1.6 Product Differentiators

| **Feature** | **Competitors** | **Our Platform** | **Impact** |
|------------|----------------|------------------|-----------|
| **Family Wallet** | ❌ Not available | ✅ Full featured | High |
| **Group Order + Split Bill** | ⚠️ Limited | ✅ Advanced | High |
| **Scheduled Orders** | ⚠️ Some have | ✅ Full support | Medium |
| **Real-time Tracking** | ✅ Standard | ✅ Enhanced | Medium |
| **Driver Chat/Call** | ⚠️ Limited | ✅ Full featured | Medium |
| **Multi-payment Options** | ✅ Standard | ✅ Advanced | Medium |

---

# 2. Product Scope

## 2.1 In Scope - Phase 1 (MVP)

### **Authentication & User Management:**
✅ Multi-role registration (Customer/Restaurant/Driver)  
✅ Phone number + OTP authentication  
✅ Google Sign-In  
✅ Apple Sign-In (iOS)  
✅ Profile management  
✅ Document verification (Restaurant/Driver)  

### **Customer Features:**
✅ Restaurant discovery with filters  
✅ Advanced search functionality  
✅ Menu browsing & item customization  
✅ Shopping cart management  
✅ Multiple payment methods  
✅ **Family Wallet** ⭐ (Unique)  
✅ **Group Orders with Bill Splitting** ⭐ (Unique)  
✅ Scheduled ordering  
✅ Real-time order tracking  
✅ Order history & reorder  
✅ Chat and call with driver  
✅ Rating & review system  
✅ Address management  
✅ Application wallet  

### **Restaurant Features:**
✅ Order management dashboard  
✅ Real-time order notifications  
✅ Dynamic menu management  
✅ Promotion creation & management  
✅ Operating hours control  
✅ Order status updates  
✅ Restaurant profile management  
✅ Analytics (basic)  

### **Driver Features:**
✅ Delivery request system  
✅ Accept/reject orders  
✅ Google Maps navigation integration  
✅ Order pickup & delivery workflow  
✅ Customer communication (chat/call)  
✅ Earnings tracker  
✅ Delivery history  
✅ Availability toggle  

### **Shared Features:**
✅ Push notifications (FCM)  
✅ Bilingual support (Arabic/English)  
✅ In-app chat system  
✅ Real-time data synchronization  
✅ Image upload & storage  

### **Technical Implementation:**
✅ Interactive Figma prototype (~160 screens)  
✅ Flutter mobile application (iOS primary)  
✅ Firebase backend (Firestore, Auth, Functions, Storage)  
✅ Google Maps API integration  
✅ Payment gateway mock (Hyperpay/Stripe ready)  
✅ SMS service integration (OTP)  

---

## 2.2 Out of Scope - Future Phases

### **Phase 2 Features (6-12 months):**
❌ AI-powered restaurant recommendations  
❌ Voice ordering  
❌ Live chat with restaurant  
❌ Multi-stop deliveries  
❌ Grocery and pharmacy ordering  
❌ Loyalty points program  
❌ Subscription plans (unlimited delivery)  
❌ Advanced analytics dashboards  
❌ Restaurant web portal  

### **Phase 3 Features (12-18 months):**
❌ Table reservations  
❌ Meal planning & recurring orders  
❌ Corporate accounts  
❌ Catering orders  
❌ Virtual restaurants (cloud kitchens)  
❌ Drone delivery integration  
❌ Augmented reality menu preview  
❌ Desktop/web versions  

### **Never in Scope:**
❌ Restaurant POS system  
❌ Food preparation management  
❌ Inventory management  
❌ Accounting software integration  

---

# 3. Stakeholders & User Roles

## 3.1 Internal Stakeholders

| **Role** | **Responsibility** | **Involvement Level** | **Decision Authority** |
|----------|-------------------|---------------------|---------------------|
| **Product Owner** | Define vision, prioritize features, accept deliverables | Daily | High |
| **Project Manager** | Timeline, resources, coordination, risk management | Daily | Medium |
| **UI/UX Designer** | Prototype design, user experience, design system | Daily (Phase 1) | Medium |
| **Frontend Developer** | Flutter app development, UI implementation | Daily (Phase 2+) | Low |
| **Backend Developer** | Firebase setup, APIs, cloud functions, database | Daily (Phase 2+) | Low |
| **QA Engineer** | Testing strategy, test execution, quality assurance | Daily (Phase 3+) | Low |
| **DevOps Engineer** | CI/CD, deployment, monitoring, infrastructure | Weekly | Low |
| **Security Specialist** | Security audit, penetration testing, compliance | As needed | Medium |

## 3.2 External Stakeholders

| **Role** | **Interest** | **Impact Level** | **Engagement** |
|----------|-------------|----------------|---------------|
| **End Customers** | Easy ordering, payment options, fast delivery | Critical | High (feedback) |
| **Restaurant Owners** | Order management, revenue growth, customer reach | Critical | High (onboarding) |
| **Delivery Drivers** | Clear workflow, earnings, flexible schedule | Critical | Medium (support) |
| **Payment Gateway** | Transaction processing, compliance | High | Medium (integration) |
| **Google Maps** | Navigation services, API usage | High | Low (integration) |
| **SMS Provider** | OTP delivery | Medium | Low (integration) |
| **App Store (Apple)** | Distribution platform, compliance | High | Low (review process) |
| **Investors/Advisors** | Project success, ROI, growth metrics | Medium | Medium (reporting) |
| **Regulatory Bodies** | Compliance (food safety, data privacy) | Medium | Low (as required) |

---

# 4. User Personas

## 👤 Persona 1: Sarah Al-Otaibi - The Busy Professional (Customer)

### **Demographics**
- **Age:** 28 years old
- **Gender:** Female
- **Location:** Riyadh, Al Olaya District
- **Occupation:** Marketing Manager at tech startup
- **Income:** SAR 15,000/month
- **Education:** Bachelor's in Business Administration
- **Family Status:** Married, 1 child (3 years old), lives with extended family

### **Technology Profile**
- **Tech Savviness:** High - early adopter, uses 20+ apps daily
- **Devices:** iPhone 14 Pro, iPad Pro, MacBook
- **Internet Usage:** 8+ hours/day
- **Preferred Apps:** Instagram, WhatsApp, Snapchat, Amazon, Careem
- **Digital Payment:** Comfortable with all methods

### **Daily Routine**
- **Weekdays:**
  - 7:00 AM: Wake up, prepare child for nursery
  - 8:30 AM: Office arrival
  - 1:00 PM: Quick lunch (often orders delivery)
  - 6:00 PM: Leave office
  - 8:00 PM: Family dinner (orders 3-4x/week)
- **Weekends:**
  - Family time, social gatherings
  - Hosts guests (orders for groups)

### **Pain Points**
1. **Time Constraints:**
   - Too busy to cook daily
   - Needs quick meal solutions
   - Wants to schedule orders in advance

2. **Budget Management:**
   - Multiple family members using delivery apps
   - Hard to track overall food spending
   - Needs to control household food budget

3. **Group Ordering Challenges:**
   - Coordinating office lunch orders is chaotic
   - Collecting money from colleagues is awkward
   - WhatsApp groups for orders get messy

4. **Current App Limitations:**
   - No family spending control
   - Can't split bills easily
   - Too many steps to reorder favorites

### **Goals & Motivations**
- ✅ **Primary Goal:** Save time while maintaining budget control
- ✅ **Secondary Goals:**
  - Control family's food delivery spending
  - Simplify group lunch ordering at work
  - Discover new restaurants easily
  - Track all food expenses in one place

### **Frustrations with Existing Apps**
- "I wish I could set spending limits for my siblings"
- "Group ordering with colleagues is always complicated"
- "Why can't I schedule breakfast for tomorrow morning?"
- "I never know how much my family spent on food this month"

### **Feature Priorities**
1. **Family Wallet** ⭐⭐⭐⭐⭐ (Critical)
2. **Group Order + Split Bill** ⭐⭐⭐⭐⭐ (Critical)
3. **Scheduled Orders** ⭐⭐⭐⭐ (High)
4. **Quick Reorder** ⭐⭐⭐⭐ (High)
5. **Favorites & History** ⭐⭐⭐ (Medium)

### **User Story**
> "As a busy professional managing a household, I want to control my family's food delivery spending through a family wallet and easily coordinate group lunch orders at work, so that I can stay within budget while enjoying convenient meal solutions without the hassle of manual money collection."

### **Behavioral Traits**
- **Decision Making:** Quick, data-driven
- **Risk Tolerance:** Medium - tries new apps but expects quality
- **Social Influence:** High - shares experiences on social media
- **Brand Loyalty:** Low - switches apps for better features/deals
- **Price Sensitivity:** Medium - values convenience over small savings

---

## 🍽️ Persona 2: Ahmed Al-Malki - The Restaurant Owner (Restaurant)

### **Demographics**
- **Age:** 42 years old
- **Gender:** Male
- **Location:** Riyadh, owns "Mama's Kitchen" in Al Malqa
- **Occupation:** Restaurant Owner & Manager
- **Business Size:** 1 location, 15 employees, 50 seats
- **Experience:** 8 years in restaurant business
- **Education:** High school + culinary courses

### **Business Profile**
- **Cuisine:** Traditional Saudi (Kabsa, Mandi, Machboos)
- **Revenue:** SAR 80,000/month
  - 60% Dine-in
  - 40% Delivery (wants to increase to 60%)
- **Operating Hours:** 11 AM - 11 PM (7 days/week)
- **Peak Hours:** 1-3 PM (lunch), 7-10 PM (dinner)
- **Current Delivery Platforms:** Using 3 platforms (Jahez, HungerStation, Mrsool)

### **Technology Profile**
- **Tech Savviness:** Medium - uses WhatsApp, basic apps, Excel for accounting
- **Devices:** Samsung Galaxy S22, laptop for admin work
- **Learning Style:** Prefers video tutorials, needs simple interfaces
- **Digital Adoption:** Hesitant but willing if it helps business

### **Daily Routine**
- **Morning (8-11 AM):**
  - Food prep, inventory check
  - Staff coordination
  - Review yesterday's orders

- **Peak Hours (11 AM - 3 PM, 7-10 PM):**
  - Manage kitchen operations
  - Handle delivery orders (chaotic)
  - Customer service (dine-in + phone orders)

- **Off-Peak:**
  - Planning, menu updates
  - Dealing with delivery apps (manual process)
  - Accounting, expense tracking

### **Pain Points**

1. **Order Management Chaos:**
   - Phone ringing constantly for orders
   - Managing 3 different delivery tablets simultaneously
   - Orders get missed or delayed
   - No unified system to track everything

2. **High Commission Fees:**
   - Paying 20-30% commission to delivery platforms
   - Eating into profit margins
   - Cannot afford to increase prices

3. **Menu Update Difficulty:**
   - Item out of stock? Must update on 3 platforms
   - Promotion running? Manual setup everywhere
   - Time-consuming and error-prone

4. **Limited Customer Insight:**
   - Doesn't know who repeat customers are
   - Cannot target promotions effectively
   - No direct communication with customers

5. **Peak Hour Pressure:**
   - Orders flood in simultaneously
   - Hard to prioritize and manage
   - Staff overwhelmed
   - Quality suffers

### **Goals & Motivations**
- ✅ **Primary Goal:** Increase delivery orders by 50% while reducing chaos
- ✅ **Secondary Goals:**
  - Reduce commission costs
  - Streamline operations
  - Better customer relationships
  - Effective promotions during slow hours
  - Build brand loyalty

### **Frustrations with Current System**
- "I'm paying 25% commission and still doing all the work!"
- "By the time I update the menu on all apps, lunch rush is over"
- "Orders arrive with no warning, kitchen can't keep up"
- "I wish I could offer discounts during slow hours to attract customers"

### **Feature Priorities**
1. **Real-time Order Notifications** ⭐⭐⭐⭐⭐ (Critical)
2. **Easy Menu Management** ⭐⭐⭐⭐⭐ (Critical)
3. **Promotion Tools** ⭐⭐⭐⭐ (High)
4. **Operating Hours Control** ⭐⭐⭐⭐ (High)
5. **Order Status Updates** ⭐⭐⭐⭐ (High)
6. **Analytics** ⭐⭐⭐ (Medium)

### **User Story**
> "As a restaurant owner, I want to manage all my delivery orders, menu items, and promotions from a single mobile app with instant notifications, so that I can increase delivery revenue without the chaos of juggling multiple platforms and reduce operational stress on my team."

### **Success Criteria**
- Can update menu in < 2 minutes
- Receive orders instantly (< 10 seconds)
- Prepare orders efficiently (no missed orders)
- Run effective promotions (increase slow-hour orders by 30%)
- Reduce manual coordination time by 60%

### **Behavioral Traits**
- **Decision Making:** Practical - "Will this help my business?"
- **Risk Tolerance:** Low - needs to see clear benefits
- **Tech Adoption:** Gradual - prefers simple, proven solutions
- **Communication Style:** Direct, prefers Arabic
- **Learning Preference:** Hands-on practice, visual guides

---

## 🚗 Persona 3: Khalid Al-Harthi - The Part-Time Driver (Driver)

### **Demographics**
- **Age:** 25 years old
- **Gender:** Male
- **Location:** Riyadh, Al Naseem District
- **Occupation:** University student + Part-time delivery driver
- **Education:** Bachelor's student (Computer Science, final year)
- **Income:** SAR 4,000-6,000/month from deliveries
- **Vehicle:** Motorcycle (more efficient in traffic)

### **Technology Profile**
- **Tech Savviness:** Medium-High - comfortable with apps, troubleshoots issues
- **Devices:** iPhone 12, uses Google Maps extensively
- **App Usage:** Delivery apps, maps, messaging, banking
- **Digital Payment:** Prefers digital transfers

### **Schedule & Availability**
- **Weekdays:**
  - Morning: University classes (8 AM - 2 PM)
  - Afternoon: Study/rest (2-5 PM)
  - **Evening: Deliveries (5-11 PM)** ← Peak earning time
  - Target: 15-20 deliveries/day

- **Weekends:**
  - **All day available (10 AM - 11 PM)**
  - Target: 25-30 deliveries/day
  - Maximum earnings

- **Flexibility:** Key motivation - works around study schedule

### **Earnings Breakdown**
- **Base Rate:** SAR 10-15 per delivery
- **Distance Bonus:** SAR 2-5 for longer trips
- **Tips:** SAR 0-20 (varies)
- **Peak Hour Bonus:** +30% during rush hours
- **Daily Goal:** SAR 200+ (weekdays), SAR 300+ (weekends)
- **Monthly Goal:** SAR 5,000+

### **Pain Points**

1. **Navigation Challenges:**
   - Incorrect or incomplete addresses
   - Hard to find buildings in new areas
   - Traffic delays not accounted for
   - Wastes time searching for locations

2. **Communication Issues:**
   - Customers don't answer calls
   - Cannot send messages on some apps
   - Language barriers with expatriates
   - Awkward phone calls

3. **Order Information Gaps:**
   - Unclear pickup instructions
   - Missing apartment/floor numbers
   - Special delivery instructions hidden
   - Cannot contact restaurant easily

4. **App Reliability:**
   - Apps crash during busy hours
   - GPS inaccurate
   - Slow to load maps
   - Battery drain

5. **Payment & Earnings:**
   - Payment delays (weekly instead of daily)
   - Unclear earning breakdowns
   - Disputes over delivery completion
   - No transparency

### **Goals & Motivations**
- ✅ **Primary Goal:** Maximize earnings in limited time
- ✅ **Secondary Goals:**
  - Complete deliveries efficiently (15+ per day)
  - Maintain 5-star rating
  - Build regular income stream
  - Save for graduation/post-university plans
  - Flexible work fitting study schedule

### **Motivations for Choosing This Work**
- **Flexibility:** Work when free from classes
- **Independence:** Be own boss
- **Active:** Prefers outdoor work to desk jobs
- **Fast Money:** Daily/weekly payouts
- **Low Barrier:** No special qualifications needed

### **Frustrations with Current Apps**
- "Why can't customers just message instead of expecting calls?"
- "I waste 10 minutes searching for buildings because addresses are incomplete"
- "Apps crash when I need them most during dinner rush"
- "I want to see my earnings in real-time, not wait till end of week"

### **Feature Priorities**
1. **Clear Navigation** ⭐⭐⭐⭐⭐ (Critical)
2. **Customer Chat/Call** ⭐⭐⭐⭐⭐ (Critical)
3. **Quick Status Updates** ⭐⭐⭐⭐ (High)
4. **Order Details Clarity** ⭐⭐⭐⭐ (High)
5. **Earnings Tracker** ⭐⭐⭐⭐ (High)
6. **Delivery History** ⭐⭐⭐ (Medium)

### **User Story**
> "As a part-time delivery driver, I want clear navigation to customer locations with the ability to easily chat or call them, so that I can complete more deliveries efficiently during my limited available hours and maximize my earnings while maintaining a high rating."

### **Success Criteria**
- Complete 15+ deliveries/day (weekdays)
- Maintain 4.8+ star rating
- < 5% delivery delays
- < 5 minutes average time to find locations
- Earn SAR 200+ daily (weekdays)

### **Behavioral Traits**
- **Decision Making:** Efficiency-focused - "Will this save me time?"
- **Risk Tolerance:** Medium - willing to try new platforms for better pay
- **Tech Adoption:** Fast - adopts apps that make work easier
- **Communication Style:** Brief, prefers text over calls
- **Work Ethic:** Hustler mentality, goal-oriented

### **Device/App Requirements**
- **Must-Have:** Fast loading, works offline (maps), low battery drain
- **Nice-to-Have:** Dark mode, voice navigation, earnings predictions

---

# 5. Technical Architecture

## 5.1 System Architecture Overview

```
┌─────────────────────────────────────────────────────────────────┐
│                      PRESENTATION LAYER                          │
│                                                                  │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐         │
│  │   Customer   │  │  Restaurant  │  │    Driver    │         │
│  │     App      │  │     App      │  │     App      │         │
│  │   (Flutter)  │  │   (Flutter)  │  │   (Flutter)  │         │
│  │              │  │              │  │              │         │
│  │  iOS/Android │  │  iOS/Android │  │  iOS/Android │         │
│  └──────┬───────┘  └──────┬───────┘  └──────┬───────┘         │
└─────────┼──────────────────┼──────────────────┼────────────────┘
          │                  │                  │
          └──────────────────┴──────────────────┘
                             │
          ┌──────────────────▼──────────────────┐
          │         API GATEWAY LAYER           │
          │      (Firebase Cloud Functions)      │
          │                                      │
          │  ┌────────────────────────────────┐ │
          │  │  Authentication Middleware     │ │
          │  │  - Token Verification          │ │
          │  │  - Role Authorization          │ │
          │  │  - Rate Limiting               │ │
          │  └────────────────────────────────┘ │
          │                                      │
          │  ┌────────────────────────────────┐ │
          │  │  Business Logic Layer          │ │
          │  │  - Input Validation            │ │
          │  │  - Data Transformation         │ │
          │  │  - Error Handling              │ │
          │  └────────────────────────────────┘ │
          └──────────────────┬──────────────────┘
                             │
          ┌──────────────────▼──────────────────┐
          │     CORE BUSINESS SERVICES           │
          │                                      │
          │  ┌────────────┐  ┌────────────┐    │
          │  │   Order    │  │  Payment   │    │
          │  │ Management │  │ Processing │    │
          │  │  Service   │  │  Service   │    │
          │  └────────────┘  └────────────┘    │
          │                                      │
          │  ┌────────────┐  ┌────────────┐    │
          │  │   Driver   │  │Notification│    │
          │  │ Assignment │  │  Service   │    │
          │  │  Service   │  │   (FCM)    │    │
          │  └────────────┘  └────────────┘    │
          │                                      │
          │  ┌────────────┐  ┌────────────┐    │
          │  │   Search   │  │  Analytics │    │
          │  │  Service   │  │  Service   │    │
          │  └────────────┘  └────────────┘    │
          └──────────────────┬──────────────────┘
                             │
          ┌──────────────────▼──────────────────┐
          │        DATA PERSISTENCE LAYER        │
          │           (Firebase)                 │
          │                                      │
          │  ┌────────────┐  ┌────────────┐    │
          │  │  Firestore │  │  Firebase  │    │
          │  │  Database  │  │    Auth    │    │
          │  │  (NoSQL)   │  │            │    │
          │  └────────────┘  └────────────┘    │
          │                                      │
          │  ┌────────────┐  ┌────────────┐    │
          │  │   Cloud    │  │  Firebase  │    │
          │  │  Storage   │  │  Realtime  │    │
          │  │ (Files)    │  │  Database  │    │
          │  └────────────┘  └────────────┘    │
          └──────────────────┬──────────────────┘
                             │
          ┌──────────────────▼──────────────────┐
          │      EXTERNAL SERVICES LAYER         │
          │                                      │
          │  ┌────────────┐  ┌────────────┐    │
          │  │   Google   │  │   Payment  │    │
          │  │  Maps API  │  │  Gateway   │    │
          │  │  - Places  │  │ (Hyperpay) │    │
          │  │  - Directions│ │           │    │
          │  │  - Geocoding│  │           │    │
          │  └────────────┘  └────────────┘    │
          │                                      │
          │  ┌────────────┐  ┌────────────┐    │
          │  │    SMS     │  │   Email    │    │
          │  │  Service   │  │  Service   │    │
          │  │ (Twilio/   │  │ (SendGrid) │    │
          │  │  Unifonic) │  │            │    │
          │  └────────────┘  └────────────┘    │
          └──────────────────────────────────────┘
```

---

## 5.2 Technology Stack

### **Frontend (Mobile App)**

| **Component** | **Technology** | **Version** | **Justification** |
|--------------|---------------|------------|------------------|
| **Framework** | Flutter | 3.16+ | • Cross-platform (iOS/Android)<br>• Hot reload for fast development<br>• Native-like performance<br>• Rich widget library<br>• Strong community support |
| **Language** | Dart | 3.2+ | • Flutter's native language<br>• Strong typing<br>• Async/await support<br>• Null safety |
| **State Management** | Riverpod | 2.4+ | • Reactive programming<br>• Testable<br>• Scalable<br>• Compile-safe<br>• No BuildContext required |
| **Navigation** | Go Router | 12.0+ | • Declarative routing<br>• Deep linking support<br>• URL-based navigation<br>• Type-safe routes |
| **Local Storage** | Hive | 2.2+ | • Fast NoSQL database<br>• Offline support<br>• Lazy loading<br>• Encryption support |
| **Secure Storage** | Flutter Secure Storage | 9.0+ | • Keychain (iOS) / Keystore (Android)<br>• Token storage<br>• Biometric integration |
| **Network** | Dio | 5.4+ | • HTTP client<br>• Interceptors<br>• Request/response logging<br>• Error handling |
| **Maps** | Google Maps Flutter | 2.5+ | • Native map integration<br>• Markers, polylines<br>• Location services |
| **Notifications** | Firebase Messaging | 14.7+ | • Push notifications<br>• Topic subscription<br>• Background handling |
| **Image Handling** | Cached Network Image | 3.3+ | • Efficient caching<br>• Progressive loading<br>• Placeholder support |
| **Image Picker** | Image Picker | 1.0+ | • Camera/gallery access<br>• Multiple selection<br>• Compression |
| **Localization** | Flutter Intl | 0.18+ | • i18n support<br>• RTL/LTR switching<br>• Date/number formatting |
| **Permission Handling** | Permission Handler | 11.0+ | • Runtime permissions<br>• Status checking<br>• Settings redirect |
| **URL Launcher** | URL Launcher | 6.2+ | • Open external URLs<br>• Phone dialer<br>• Email client |
| **Share** | Share Plus | 7.2+ | • Native share sheet<br>• Text/file sharing<br>• Social media integration |

### **Backend (Cloud Services)**

| **Component** | **Technology** | **Purpose** | **Features Used** |
|--------------|---------------|------------|------------------|
| **Database** | Firebase Firestore | • Real-time NoSQL database<br>• Document-based | • Real-time listeners<br>• Offline persistence<br>• Transactions<br>• Batch writes<br>• Security rules |
| **Authentication** | Firebase Auth | • User authentication | • Phone auth (OTP)<br>• Google Sign-In<br>• Apple Sign-In<br>• Custom tokens<br>• Email/password |
| **Storage** | Firebase Cloud Storage | • File storage | • Image/document upload<br>• Public/private buckets<br>• CDN integration<br>• Access control |
| **Functions** | Cloud Functions for Firebase | • Serverless backend logic | • HTTP triggers<br>• Firestore triggers<br>• Auth triggers<br>• Scheduled functions<br>• Pub/Sub |
| **Hosting** | Firebase Hosting | • Web app hosting (admin panel) | • Fast CDN<br>• SSL certificates<br>• Custom domains |
| **Analytics** | Firebase Analytics | • User behavior tracking | • Event logging<br>• User properties<br>• Conversion tracking |
| **Crash Reporting** | Firebase Crashlytics | • Error monitoring | • Crash reports<br>• Non-fatal errors<br>• Custom logs |
| **Performance** | Firebase Performance | • App performance monitoring | • Network monitoring<br>• Screen rendering<br>• Custom traces |
| **Remote Config** | Firebase Remote Config | • Feature flags | • A/B testing<br>• Dynamic configuration<br>• Gradual rollouts |
| **Messaging** | Firebase Cloud Messaging (FCM) | • Push notifications | • Topic messaging<br>• Direct messaging<br>• Data/notification payloads |

### **Third-Party Integrations**

| **Service** | **Provider** | **Purpose** | **Usage** |
|------------|-------------|-----------|-----------|
| **Maps & Navigation** | Google Maps Platform | Location services | • Maps SDK<br>• Places API<br>• Directions API<br>• Geocoding API<br>• Distance Matrix API |
| **Payment Gateway** | Hyperpay (Primary)<br>Stripe (Backup) | Payment processing | • Card payments<br>• Apple Pay<br>• Tokenization<br>• 3D Secure<br>• Webhooks |
| **SMS Service** | Unifonic (Primary)<br>Twilio (Backup) | OTP delivery | • SMS API<br>• Delivery reports<br>• Number verification |
| **Email Service** | SendGrid | Transactional emails | • Welcome emails<br>• Password reset<br>• Order confirmations<br>• Receipts |

### **Development Tools**

| **Tool** | **Purpose** | **Platform** |
|---------|-----------|-------------|
| **IDE** | VS Code / Android Studio | Development |
| **Version Control** | Git + GitHub | Code repository |
| **Design** | Figma | UI/UX design, prototyping |
| **API Testing** | Postman | API endpoint testing |
| **CI/CD** | GitHub Actions / Codemagic | Automated builds, testing, deployment |
| **App Distribution** | Firebase App Distribution | Beta testing |
| **Code Quality** | SonarQube / CodeMagic | Static analysis, code coverage |
| **Monitoring** | Sentry (optional) | Error tracking |
| **Documentation** | Swagger / Postman | API documentation |

---

## 5.3 Database Design (Firestore)

### **Collection Structure**

```
root/
│
├── users/
│   └── {userId}/
│       ├── addresses/ (subcollection)
│       ├── paymentMethods/ (subcollection)
│       ├── wallet/ (subcollection)
│       └── familyWallets/ (subcollection)
│
├── restaurants/
│   └── {restaurantId}/
│       ├── menu/
│       │   └── {categoryId}/
│       │       └── items/ (subcollection)
│       └── promotions/ (subcollection)
│
├── orders/
│   └── {orderId}/
│       ├── statusHistory/ (subcollection)
│       └── chat/ (subcollection)
│
├── groupOrders/
│   └── {groupOrderId}/
│
├── drivers/
│   └── {driverId}/
│
├── notifications/
│   └── {notificationId}/
│
└── chats/
    └── {chatId}/
        └── messages/ (subcollection)
```

### **Detailed Schema**

#### **users/ Collection**

```typescript
interface User {
  // Basic Info
  userId: string;          // Firebase Auth UID
  role: 'customer' | 'restaurant' | 'driver';
  name: string;
  email: string;
  phoneNumber: string;     // +966501234567
  profilePhoto: string;    // Storage URL
  language: 'en' | 'ar';
  
  // Metadata
  createdAt: Timestamp;
  updatedAt: Timestamp;
  lastLoginAt: Timestamp;
  
  // Settings
  notificationSettings: {
    orderUpdates: boolean;
    promotions: boolean;
    chat: boolean;
    email: boolean;
  };
  
  // Stats (for customers)
  stats?: {
    totalOrders: number;
    totalSpent: number;
    favoriteRestaurants: string[];  // restaurantIds
  };
  
  // Restaurant-specific
  restaurantInfo?: {
    restaurantId: string;
    businessName: string;
    commercialLicense: string;
    verificationStatus: 'pending' | 'approved' | 'rejected';
    documents: {
      license: string;    // Storage URL
      menu: string[];     // Storage URLs
    };
  };
  
  // Driver-specific
  driverInfo?: {
    driverId: string;
    nationalId: string;
    vehicleType: 'motorcycle' | 'car';
    vehicleModel: string;
    plateNumber: string;
    licenseNumber: string;
    verificationStatus: 'pending' | 'approved' | 'rejected';
    rating: number;
    totalDeliveries: number;
    isAvailable: boolean;
    currentLocation: GeoPoint;
    documents: {
      license: string;
      insurance: string;
      vehicleRegistration: string;
    };
  };
}
```

#### **users/{userId}/addresses/ Subcollection**

```typescript
interface Address {
  addressId: string;
  label: string;           // 'Home', 'Work', 'Other'
  district: string;
  street: string;
  buildingNumber: string;
  apartmentNumber?: string;
  floor?: string;
  additionalDirections?: string;
  location: GeoPoint;      // lat, lng
  phoneNumber: string;
  isDefault: boolean;
  createdAt: Timestamp;
}
```

#### **users/{userId}/paymentMethods/ Subcollection**

```typescript
interface PaymentMethod {
  paymentMethodId: string;
  type: 'card' | 'applePay';
  
  // Card details (tokenized)
  cardToken?: string;      // From payment gateway
  cardLast4?: string;      // 1234
  cardBrand?: string;      // 'Visa', 'Mastercard', 'Mada'
  expiryMonth?: string;    // 12
  expiryYear?: string;     // 2025
  cardholderName?: string;
  
  isDefault: boolean;
  createdAt: Timestamp;
}
```

#### **users/{userId}/wallet/ Subcollection**

```typescript
interface WalletTransaction {
  transactionId: string;
  type: 'credit' | 'debit';
  amount: number;
  balance: number;         // Balance after transaction
  description: string;     // 'Order payment', 'Refund', 'Top-up'
  orderId?: string;
  paymentMethodId?: string;
  status: 'pending' | 'completed' | 'failed';
  createdAt: Timestamp;
}

// Also store current balance in user document
interface User {
  wallet: {
    balance: number;
    currency: 'SAR';
  };
}
```

#### **users/{userId}/familyWallets/ Subcollection**

```typescript
interface FamilyWallet {
  familyWalletId: string;
  name: string;            // 'Al-Otaibi Family'
  ownerId: string;         // userId
  totalBalance: number;
  currency: 'SAR';
  
  members: {
    userId: string;
    name: string;
    avatar: string;
    role: 'owner' | 'member';
    spendingLimits: {
      daily?: number;
      weekly?: number;
      monthly?: number;
      perOrder?: number;
    };
    currentSpent: {
      daily: number;
      weekly: number;
      monthly: number;
      lastResetDaily: Timestamp;
      lastResetWeekly: Timestamp;
      lastResetMonthly: Timestamp;
    };
    status: 'active' | 'paused' | 'pending';
    joinedAt: Timestamp;
  }[];
  
  // Transactions stored in subcollection
  createdAt: Timestamp;
  updatedAt: Timestamp;
}
```

#### **restaurants/ Collection**

```typescript
interface Restaurant {
  restaurantId: string;
  ownerId: string;         // userId
  
  // Basic Info
  name: string;
  description: string;
  logo: string;            // Storage URL
  coverImage: string;
  
  // Classification
  cuisineType: string[];   // ['Traditional Saudi', 'BBQ']
  categories: string[];    // ['Lunch', 'Dinner', 'Breakfast']
  
  // Rating & Reviews
  rating: number;          // 4.7
  totalReviews: number;
  
  // Delivery Info
  deliveryFee: number;
  minimumOrder: number;    // 30 SAR
  estimatedDeliveryTime: string;  // '25-35 min'
  
  // Status
  isOpen: boolean;
  isPaused: boolean;       // Temporarily paused by owner
  isVerified: boolean;
  
  // Operating Hours
  operatingHours: {
    monday: { open: string; close: string; isClosed: boolean; };
    tuesday: { open: string; close: string; isClosed: boolean; };
    // ... for each day
    sunday: { open: string; close: string; isClosed: boolean; };
  };
  
  // Location
  location: GeoPoint;
  address: {
    district: string;
    street: string;
    buildingNumber: string;
    city: string;
  };
  
  // Contact
  phoneNumber: string;
  email: string;
  
  // Stats
  stats: {
    totalOrders: number;
    totalRevenue: number;
    avgOrderValue: number;
  };
  
  // Metadata
  createdAt: Timestamp;
  updatedAt: Timestamp;
}
```

#### **restaurants/{restaurantId}/menu/{categoryId}/ Subcollection**

```typescript
interface MenuCategory {
  categoryId: string;
  name: string;            // 'Appetizers', 'Mains', etc.
  name_ar: string;
  order: number;           // Display order
  isActive: boolean;
  createdAt: Timestamp;
}
```

#### **restaurants/{restaurantId}/menu/{categoryId}/items/ Subcollection**

```typescript
interface MenuItem {
  itemId: string;
  name: string;
  name_ar: string;
  description: string;
  description_ar: string;
  price: number;
  images: string[];        // Storage URLs
  categoryId: string;
  
  // Availability
  isAvailable: boolean;
  isPopular: boolean;
  
  // Customization Options
  customizations?: {
    sizes?: {
      name: string;        // 'Small', 'Medium', 'Large'
      name_ar: string;
      priceModifier: number;  // +0, +5, +10
    }[];
    addOns?: {
      name: string;
      name_ar: string;
      price: number;
    }[];
    removableIngredients?: string[];
  };
  
  // Nutrition (optional)
  nutrition?: {
    calories: number;
    protein: number;
    carbs: number;
    fat: number;
  };
  
  // Stats
  rating?: number;
  reviewCount?: number;
  orderCount: number;
  
  createdAt: Timestamp;
  updatedAt: Timestamp;
}
```

#### **restaurants/{restaurantId}/promotions/ Subcollection**

```typescript
interface Promotion {
  promotionId: string;
  title: string;
  title_ar: string;
  description: string;
  description_ar: string;
  
  // Discount
  discountType: 'percentage' | 'fixed' | 'buyXgetY';
  discountValue: number;   // 20 (for 20% or 20 SAR)
  
  // Buy X Get Y
  buyQuantity?: number;    // Buy 2
  getQuantity?: number;    // Get 1 free
  
  // Validity
  startDate: Timestamp;
  endDate: Timestamp;
  
  // Conditions
  minimumOrderValue?: number;
  applicableItems?: string[];  // itemIds, if empty = all items
  applicableCategories?: string[];
  maxUsagePerCustomer?: number;
  totalUsageLimit?: number;
  
  // Status
  isActive: boolean;
  currentUsageCount: number;
  
  createdAt: Timestamp;
  updatedAt: Timestamp;
}
```

#### **orders/ Collection**

```typescript
interface Order {
  orderId: string;
  orderNumber: string;     // Human-readable: 'ORD-12345'
  
  // Parties
  customerId: string;
  restaurantId: string;
  driverId: string | null;
  
  // Status
  status: 'placed' | 'accepted' | 'preparing' | 'ready' | 
          'driverAssigned' | 'pickedUp' | 'onTheWay' | 
          'delivered' | 'cancelled';
  cancelReason?: string;
  cancelledBy?: 'customer' | 'restaurant' | 'driver' | 'system';
  
  // Items
  items: {
    itemId: string;
    name: string;
    price: number;
    quantity: number;
    customizations?: {
      size?: string;
      addOns?: string[];
      removedIngredients?: string[];
    };
    specialInstructions?: string;
    itemTotal: number;   // price * quantity + customizations
  }[];
  
  // Pricing
  subtotal: number;
  deliveryFee: number;
  discount: number;
  discountCode?: string;
  vat: number;             // 15%
  total: number;
  
  // Payment
  paymentMethod: 'familyWallet' | 'applicationWallet' | 'card' | 'applePay';
  paymentDetails: {
    familyWalletId?: string;
    memberId?: string;
    cardLast4?: string;
    transactionId?: string;
  };
  paymentStatus: 'pending' | 'completed' | 'failed' | 'refunded';
  
  // Delivery
  deliveryAddress: {
    label: string;
    fullAddress: string;
    location: GeoPoint;
    phoneNumber: string;
    additionalDirections?: string;
  };
  
  // Timing
  scheduledTime: Timestamp | null;  // null = deliver now
  estimatedDeliveryTime: Timestamp;
  actualDeliveryTime: Timestamp | null;
  preparationTime: number | null;   // minutes set by restaurant
  
  // Group Order
  isGroupOrder: boolean;
  groupOrderId: string | null;
  
  // Special Instructions
  specialInstructions?: string;
  
  // Ratings
  customerRating?: {
    restaurant: number;    // 1-5
    driver: number;
    restaurantReview?: string;
    driverReview?: string;
    ratedAt: Timestamp;
  };
  
  // Metadata
  createdAt: Timestamp;
  updatedAt: Timestamp;
}
```

#### **orders/{orderId}/statusHistory/ Subcollection**

```typescript
interface OrderStatusHistory {
  statusId: string;
  status: string;
  timestamp: Timestamp;
  updatedBy: string;       // userId or 'system'
  updatedByRole: 'customer' | 'restaurant' | 'driver' | 'system';
  notes?: string;
}
```

#### **groupOrders/ Collection**

```typescript
interface GroupOrder {
  groupOrderId: string;
  hostId: string;
  restaurantId: string;
  
  // Info
  name: string;            // 'Office Lunch'
  joinCode: string;        // 'ABC123'
  joinLink: string;        // 'https://app.com/join/ABC123'
  
  // Timing
  deadline: Timestamp;
  createdAt: Timestamp;
  
  // Delivery
  deliveryAddress: {
    label: string;
    fullAddress: string;
    location: GeoPoint;
    phoneNumber: string;
  };
  
  // Status
  status: 'open' | 'closed' | 'paying' | 'confirmed' | 'cancelled';
  
  // Participants
  participants: {
    userId: string;
    name: string;
    avatar: string;
    isHost: boolean;
    items: {
      itemId: string;
      name: string;
      price: number;
      quantity: number;
      customizations?: any;
      itemTotal: number;
    }[];
    subtotal: number;
    amountToPay: number;   // After split
    paymentStatus: 'pending' | 'paid' | 'failed';
    paymentMethod?: string;
    paidAt?: Timestamp;
    joinedAt: Timestamp;
  }[];
  
  // Pricing
  totalSubtotal: number;
  deliveryFee: number;
  vat: number;
  totalAmount: number;
  
  // Split Method
  splitMethod: 'equal' | 'byItems' | 'custom';
  
  // Linked Order
  orderId: string | null;
  
  updatedAt: Timestamp;
}
```

#### **drivers/ Collection**

```typescript
interface Driver {
  driverId: string;
  userId: string;
  
  // Personal Info
  fullName: string;
  nationalId: string;
  phoneNumber: string;
  profilePhoto: string;
  
  // Vehicle
  vehicleType: 'motorcycle' | 'car' | 'bicycle';
  vehicleModel: string;
  vehicleColor: string;
  plateNumber: string;
  licenseNumber: string;
  
  // Documents
  documents: {
    driverLicense: string;   // Storage URL
    vehicleRegistration: string;
    insurance: string;
    profilePhoto: string;
  };
  
  // Verification
  verificationStatus: 'pending' | 'approved' | 'rejected';
  verificationNotes?: string;
  verifiedAt?: Timestamp;
  
  // Status
  isAvailable: boolean;
  isOnline: boolean;
  
  // Location (updated in real-time)
  currentLocation: GeoPoint;
  lastLocationUpdate: Timestamp;
  
  // Stats
  rating: number;
  totalRatings: number;
  totalDeliveries: number;
  completionRate: number;  // %
  avgDeliveryTime: number; // minutes
  
  // Earnings (calculated)
  earnings: {
    today: number;
    thisWeek: number;
    thisMonth: number;
    total: number;
  };
  
  // Current Active Delivery
  activeOrderId: string | null;
  
  createdAt: Timestamp;
  updatedAt: Timestamp;
}
```

#### **notifications/ Collection**

```typescript
interface Notification {
  notificationId: string;
  userId: string;
  
  // Content
  type: 'order' | 'payment' | 'promotion' | 'familyWallet' | 
        'groupOrder' | 'driver' | 'system';
  title: string;
  title_ar: string;
  body: string;
  body_ar: string;
  
  // Data
  data: {
    orderId?: string;
    restaurantId?: string;
    groupOrderId?: string;
    familyWalletId?: string;
    [key: string]: any;
  };
  
  // Status
  isRead: boolean;
  readAt?: Timestamp;
  
  // Navigation
  actionUrl?: string;      // Deep link
  
  createdAt: Timestamp;
  expiresAt?: Timestamp;   // Auto-delete after
}
```

#### **chats/ Collection**

```typescript
interface Chat {
  chatId: string;
  orderId: string;
  
  // Participants
  participants: {
    customerId: string;
    driverId: string;
  };
  
  // Status
  status: 'active' | 'closed';
  
  // Last Message
  lastMessage: string;
  lastMessageSenderId: string;
  lastMessageTime: Timestamp;
  
  // Unread Count
  unreadCount: {
    [userId: string]: number;
  };
  
  createdAt: Timestamp;
  updatedAt: Timestamp;
}
```

#### **chats/{chatId}/messages/ Subcollection**

```typescript
interface ChatMessage {
  messageId: string;
  senderId: string;
  senderRole: 'customer' | 'driver';
  
  // Content
  type: 'text' | 'image' | 'location';
  text?: string;
  imageUrl?: string;
  location?: GeoPoint;
  
  // Status
  isRead: boolean;
  readAt?: Timestamp;
  
  timestamp: Timestamp;
}
```

---

### **Indexes (Firestore Composite Indexes)**

```javascript
// Required composite indexes for efficient queries

// 1. Restaurants by location and rating
{
  collection: 'restaurants',
  fields: [
    { fieldPath: 'location', order: 'ASCENDING' },
    { fieldPath: 'rating', order: 'DESCENDING' }
  ]
}

// 2. Orders by customer and status
{
  collection: 'orders',
  fields: [
    { fieldPath: 'customerId', order: 'ASCENDING' },
    { fieldPath: 'status', order: 'ASCENDING' },
    { fieldPath: 'createdAt', order: 'DESCENDING' }
  ]
}

// 3. Orders by restaurant and status
{
  collection: 'orders',
  fields: [
    { fieldPath: 'restaurantId', order: 'ASCENDING' },
    { fieldPath: 'status', order: 'ASCENDING' },
    { fieldPath: 'createdAt', order: 'DESCENDING' }
  ]
}

// 4. Orders by driver
{
  collection: 'orders',
  fields: [
    { fieldPath: 'driverId', order: 'ASCENDING' },
    { fieldPath: 'createdAt', order: 'DESCENDING' }
  ]
}

// 5. Available drivers near location
{
  collection: 'drivers',
  fields: [
    { fieldPath: 'isAvailable', order: 'ASCENDING' },
    { fieldPath: 'currentLocation', order: 'ASCENDING' }
  ]
}

// 6. Notifications by user
{
  collection: 'notifications',
  fields: [
    { fieldPath: 'userId', order: 'ASCENDING' },
    { fieldPath: 'isRead', order: 'ASCENDING' },
    { fieldPath: 'createdAt', order: 'DESCENDING' }
  ]
}
```

---

### **Security Rules (Firestore)**

```javascript
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    
    // Helper functions
    function isAuthenticated() {
      return request.auth != null;
    }
    
    function isOwner(userId) {
      return isAuthenticated() && request.auth.uid == userId;
    }
    
    function hasRole(role) {
      return isAuthenticated() && 
             request.auth.token.role == role;
    }
    
    // Users collection
    match /users/{userId} {
      allow read: if isOwner(userId);
      allow create: if isAuthenticated();
      allow update: if isOwner(userId);
      allow delete: if false; // Prevent deletion
      
      // Addresses subcollection
      match /addresses/{addressId} {
        allow read, write: if isOwner(userId);
      }
      
      // Payment methods subcollection
      match /paymentMethods/{paymentMethodId} {
        allow read, write: if isOwner(userId);
      }
      
      // Wallet subcollection
      match /wallet/{transactionId} {
        allow read: if isOwner(userId);
        allow create: if isOwner(userId);
        allow update, delete: if false; // Prevent modification
      }
      
      // Family wallets subcollection
      match /familyWallets/{familyWalletId} {
        allow read: if isOwner(userId) || 
                       resource.data.members[request.auth.uid] != null;
        allow create, update: if isOwner(userId);
        allow delete: if false;
      }
    }
    
    // Restaurants collection
    match /restaurants/{restaurantId} {
      allow read: if true; // Public read
      allow create: if hasRole('restaurant');
      allow update: if isAuthenticated() && 
                       request.auth.token.restaurantId == restaurantId;
      allow delete: if false;
      
      // Menu subcollection
      match /menu/{categoryId} {
        allow read: if true; // Public read
        allow write: if isAuthenticated() && 
                        request.auth.token.restaurantId == restaurantId;
        
        match /items/{itemId} {
          allow read: if true;
          allow write: if isAuthenticated() && 
                         request.auth.token.restaurantId == restaurantId;
        }
      }
      
      // Promotions subcollection
      match /promotions/{promotionId} {
        allow read: if true;
        allow write: if isAuthenticated() && 
                        request.auth.token.restaurantId == restaurantId;
      }
    }
    
    // Orders collection
    match /orders/{orderId} {
      allow read: if isAuthenticated() && (
        request.auth.uid == resource.data.customerId ||
        request.auth.uid == resource.data.driverId ||
        request.auth.token.restaurantId == resource.data.restaurantId
      );
      
      allow create: if hasRole('customer');
      
      allow update: if isAuthenticated() && (
        hasRole('restaurant') ||
        hasRole('driver') ||
        request.auth.uid == resource.data.customerId
      );
      
      allow delete: if false;
      
      // Status history subcollection
      match /statusHistory/{statusId} {
        allow read: if isAuthenticated();
        allow create: if isAuthenticated();
        allow update, delete: if false;
      }
      
      // Chat subcollection
      match /chat/{messageId} {
        allow read, create: if isAuthenticated() && (
          request.auth.uid == get(/databases/$(database)/documents/orders/$(orderId)).data.customerId ||
          request.auth.uid == get(/databases/$(database)/documents/orders/$(orderId)).data.driverId
        );
        allow update, delete: if false;
      }
    }
    
    // Group orders collection
    match /groupOrders/{groupOrderId} {
      allow read: if isAuthenticated() &&
                     resource.data.participants[request.auth.uid] != null;
      allow create: if hasRole('customer');
      allow update: if isAuthenticated() && (
        request.auth.uid == resource.data.hostId ||
        resource.data.participants[request.auth.uid] != null
      );
      allow delete: if isAuthenticated() && 
                       request.auth.uid == resource.data.hostId;
    }
    
    // Drivers collection
    match /drivers/{driverId} {
      allow read: if isAuthenticated();
      allow create: if hasRole('driver');
      allow update: if isAuthenticated() && 
                       request.auth.uid == resource.data.userId;
      allow delete: if false;
    }
    
    // Notifications collection
    match /notifications/{notificationId} {
      allow read, update: if isAuthenticated() && 
                             request.auth.uid == resource.data.userId;
      allow create: if isAuthenticated(); // Cloud function creates
      allow delete: if isOwner(resource.data.userId);
    }
    
    // Chats collection
    match /chats/{chatId} {
      allow read, create: if isAuthenticated() &&
                             request.auth.uid in resource.data.participants;
      allow update: if isAuthenticated() &&
                       request.auth.uid in resource.data.participants;
      allow delete: if false;
      
      // Messages subcollection
      match /messages/{messageId} {
        allow read, create: if isAuthenticated() &&
                               request.auth.uid in get(/databases/$(database)/documents/chats/$(chatId)).data.participants;
        allow update: if isAuthenticated() &&
                         request.auth.uid == resource.data.senderId;
        allow delete: if false;
      }
    }
  }
}
```

---

## 5.4 API Specifications (Cloud Functions)

### **Base URL**
```
https://us-central1-restaurant-platform.cloudfunctions.net/api
```

### **Authentication**
All API requests require Firebase Auth token in header:
```
Authorization: Bearer <firebase_auth_token>
```

---

### **Authentication APIs**

#### **1. Send OTP**
```http
POST /auth/sendOTP
Content-Type: application/json

Request:
{
  "phoneNumber": "+966501234567",
  "role": "customer"
}

Response (200 OK):
{
  "success": true,
  "message": "OTP sent successfully",
  "expiresIn": 300
}

Errors:
400: { "error": "Invalid phone number format" }
429: { "error": "Too many requests. Try again in 15 minutes" }
500: { "error": "Failed to send OTP" }
```

#### **2. Verify OTP**
```http
POST /auth/verifyOTP
Content-Type: application/json

Request:
{
  "phoneNumber": "+966501234567",
  "otp": "123456",
  "role": "customer"
}

Response (200 OK):
{
  "success": true,
  "token": "eyJhbGciOiJIUzI1NiIs...",
  "refreshToken": "eyJhbGciOiJIUzI1NiIs...",
  "userId": "abc123xyz",
  "isNewUser": false,
  "user": {
    "userId": "abc123xyz",
    "name": "Sarah Al-Otaibi",
    "email": "sarah@example.com",
    "role": "customer"
  }
}

Errors:
400: { "error": "Invalid OTP" }
401: { "error": "OTP expired" }
404: { "error": "User not found" }
```

---

### **Order Management APIs**

#### **3. Create Order**
```http
POST /orders/create
Authorization: Bearer <token>
Content-Type: application/json

Request:
{
  "restaurantId": "rest123",
  "items": [
    {
      "itemId": "item456",
      "quantity": 2,
      "customizations": {
        "size": "Large",
        "addOns": ["extra cheese"],
        "removedIngredients": ["onions"]
      },
      "specialInstructions": "Well done"
    }
  ],
  "deliveryAddress": {
    "addressId": "addr789",
    "label": "Home",
    "district": "Al Olaya",
    "street": "King Fahd Road",
    "buildingNumber": "15",
    "apartmentNumber": "3A",
    "location": {
      "lat": 24.7136,
      "lng": 46.6753
    },
    "phoneNumber": "+966501234567",
    "additionalDirections": "Ring doorbell twice"
  },
  "paymentMethod": "familyWallet",
  "paymentDetails": {
    "familyWalletId": "fw123",
    "memberId": "user789"
  },
  "scheduledTime": null,
  "specialInstructions": "Please call before arriving",
  "couponCode": "SAVE20"
}

Response (200 OK):
{
  "success": true,
  "order": {
    "orderId": "order789",
    "orderNumber": "ORD-12345",
    "estimatedDelivery": "2024-12-25T14:30:00Z",
    "subtotal": 70.00,
    "deliveryFee": 15.00,
    "discount": 14.00,
    "vat": 10.65,
    "total": 81.65
  }
}

Errors:
400: { "error": "Invalid items or address" }
402: { "error": "Payment failed", "details": "Insufficient balance" }
404: { "error": "Restaurant not found" }
409: { "error": "Restaurant is currently closed" }
422: { "error": "Minimum order not met", "minimumRequired": 30.00 }
```

#### **4. Update Order Status**
```http
PATCH /orders/{orderId}/status
Authorization: Bearer <token>
Content-Type: application/json

Request:
{
  "status": "preparing",
  "estimatedPrepTime": 25
}

Response (200 OK):
{
  "success": true,
  "order": {
    "orderId": "order789",
    "status": "preparing",
    "estimatedDelivery": "2024-12-25T14:30:00Z",
    "updatedAt": "2024-12-25T13:45:00Z"
  }
}

// Automatically triggers:
// - FCM notification to customer
// - Status history update
// - Driver assignment (if status = 'ready')

Errors:
403: { "error": "Not authorized to update this order" }
404: { "error": "Order not found" }
409: { "error": "Cannot update order in current status" }
```

#### **5. Cancel Order**
```http
POST /orders/{orderId}/cancel
Authorization: Bearer <token>
Content-Type: application/json

Request:
{
  "reason": "Changed my mind",
  "cancelledBy": "customer"
}

Response (200 OK):
{
  "success": true,
  "order": {
    "orderId": "order789",
    "status": "cancelled",
    "refundAmount": 81.65,
    "refundStatus": "processing"
  }
}

// Automatically triggers:
// - Payment refund
// - Notifications to restaurant/driver
// - Order status update

Errors:
403: { "error": "Cannot cancel order after driver picked up" }
404: { "error": "Order not found" }
```

---

### **Group Order APIs**

#### **6. Create Group Order**
```http
POST /groupOrders/create
Authorization: Bearer <token>
Content-Type: application/json

Request:
{
  "restaurantId": "rest123",
  "name": "Office Lunch",
  "deadline": "2024-12-25T13:00:00Z",
  "deliveryAddress": {
    "label": "Office",
    "fullAddress": "Al Olaya, King Fahd Road, Building 10",
    "location": { "lat": 24.7136, "lng": 46.6753 },
    "phoneNumber": "+966501234567"
  }
}

Response (200 OK):
{
  "success": true,
  "groupOrder": {
    "groupOrderId": "grp456",
    "joinCode": "ABC123",
    "joinLink": "https://app.com/join/ABC123",
    "qrCodeUrl": "https://storage.../qr/ABC123.png",
    "expiresAt": "2024-12-25T13:00:00Z"
  }
}

Errors:
400: { "error": "Invalid restaurant or address" }
422: { "error": "Deadline must be at least 15 minutes from now" }
```

#### **7. Join Group Order**
```http
POST /groupOrders/{groupOrderId}/join
Authorization: Bearer <token>
Content-Type: application/json

Request:
{
  "joinCode": "ABC123"
}

Response (200 OK):
{
  "success": true,
  "groupOrder": {
    "groupOrderId": "grp456",
    "name": "Office Lunch",
    "restaurant": {
      "restaurantId": "rest123",
      "name": "Mama's Kitchen",
      "logo": "https://..."
    },
    "host": {
      "userId": "user123",
      "name": "Sarah"
    },
    "deadline": "2024-12-25T13:00:00Z",
    "participants": [
      { "userId": "user123", "name": "Sarah", "itemCount": 2 },
      { "userId": "user456", "name": "Ahmed", "itemCount": 1 }
    ]
  }
}

Errors:
404: { "error": "Group order not found" }
409: { "error": "Group order has closed" }
410: { "error": "Join code expired" }
```

#### **8. Add Item to Group Order**
```http
POST /groupOrders/{groupOrderId}/items
Authorization: Bearer <token>
Content-Type: application/json

Request:
{
  "itemId": "item789",
  "quantity": 1,
  "customizations": {
    "size": "Medium",
    "addOns": ["extra sauce"]
  }
}

Response (200 OK):
{
  "success": true,
  "groupOrder": {
    "groupOrderId": "grp456",
    "yourItems": [...],
    "yourSubtotal": 35.00,
    "totalAmount": 147.00
  }
}

// Real-time update pushed to all participants via Firestore listener

Errors:
403: { "error": "Group order is closed" }
404: { "error": "Group order or item not found" }
```

#### **9. Close Group Order & Split Bill**
```http
POST /groupOrders/{groupOrderId}/close
Authorization: Bearer <token>
Content-Type: application/json

Request:
{
  "splitMethod": "byItems"
}

Response (200 OK):
{
  "success": true,
  "groupOrder": {
    "groupOrderId": "grp456",
    "status": "closed",
    "participants": [
      {
        "userId": "user123",
        "name": "Sarah",
        "subtotal": 55.00,
        "deliveryShare": 5.00,
        "vatShare": 9.00,
        "amountToPay": 69.00,
        "paymentStatus": "pending"
      },
      {
        "userId": "user456",
        "name": "Ahmed",
        "subtotal": 52.00,
        "deliveryShare": 5.00,
        "vatShare": 8.55,
        "amountToPay": 65.55,
        "paymentStatus": "pending"
      }
    ],
    "totalAmount": 134.55
  }
}

// Sends payment request notification to all participants

Errors:
403: { "error": "Only host can close group order" }
409: { "error": "Group order already closed" }
```

#### **10. Pay Group Order Share**
```http
POST /groupOrders/{groupOrderId}/pay
Authorization: Bearer <token>
Content-Type: application/json

Request:
{
  "paymentMethod": "card",
  "paymentDetails": {
    "cardToken": "tok_visa1234"
  }
}

Response (200 OK):
{
  "success": true,
  "payment": {
    "transactionId": "txn_abc123",
    "amount": 69.00,
    "status": "completed"
  },
  "groupOrder": {
    "yourPaymentStatus": "paid",
    "pendingParticipants": 1
  }
}

// When all participants paid:
// - Creates single order to restaurant
// - Sends confirmation to all participants

Errors:
402: { "error": "Payment failed", "details": "Card declined" }
409: { "error": "You have already paid" }
```

---

### **Payment APIs**

#### **11. Process Payment**
```http
POST /payments/charge
Authorization: Bearer <token>
Content-Type: application/json

Request:
{
  "orderId": "order789",
  "amount": 81.65,
  "currency": "SAR",
  "paymentMethod": {
    "type": "card",
    "token": "tok_visa1234"
  }
}

Response (200 OK):
{
  "success": true,
  "transaction": {
    "transactionId": "txn_abc123",
    "status": "succeeded",
    "amount": 81.65,
    "currency": "SAR",
    "receipt": "https://storage.../receipts/txn_abc123.pdf"
  }
}

Errors:
402: { "error": "Payment declined", "declineCode": "insufficient_funds" }
500: { "error": "Payment gateway error" }
```

#### **12. Family Wallet Deduct**
```http
POST /familyWallet/deduct
Authorization: Bearer <token>
Content-Type: application/json

Request:
{
  "familyWalletId": "fw123",
  "memberId": "user789",
  "amount": 45.00,
  "orderId": "order789"
}

Response (200 OK):
{
  "success": true,
  "wallet": {
    "remainingBalance": 805.00,
    "memberRemainingLimit": {
      "daily": 155.00,
      "monthly": 755.00
    }
  },
  "transaction": {
    "transactionId": "txn_wallet456",
    "timestamp": "2024-12-25T14:00:00Z"
  }
}

// Triggers notification to family owner

Errors:
400: { "error": "Insufficient wallet balance" }
403: { "error": "Member spending limit exceeded" }
404: { "error": "Family wallet not found" }
```

#### **13. Top Up Application Wallet**
```http
POST /wallet/topup
Authorization: Bearer <token>
Content-Type: application/json

Request:
{
  "amount": 100.00,
  "paymentMethod": {
    "type": "card",
    "token": "tok_visa1234"
  }
}

Response (200 OK):
{
  "success": true,
  "wallet": {
    "balance": 220.00
  },
  "transaction": {
    "transactionId": "txn_topup789",
    "amount": 100.00,
    "timestamp": "2024-12-25T14:00:00Z"
  }
}

Errors:
402: { "error": "Top-up payment failed" }
422: { "error": "Amount must be between 10 and 1000 SAR" }
```

---

### **Driver Assignment API (Cloud Function - Internal)**

#### **14. Assign Driver to Order**
```javascript
// Triggered automatically when order status = 'ready'
// Cloud Function: onOrderReady

exports.assignDriver = functions.firestore
  .document('orders/{orderId}')
  .onUpdate(async (change, context) => {
    const newStatus = change.after.data().status;
    const oldStatus = change.before.data().status;
    
    if (oldStatus !== 'ready' && newStatus === 'ready') {
      const orderId = context.params.orderId;
      const order = change.after.data();
      
      // Algorithm:
      // 1. Query available drivers within 5km radius
      const nearbyDrivers = await findNearbyDrivers(
        order.restaurant.location,
        5000 // 5km
      );
      
      // 2. Sort by: rating > distance > completion rate
      const sortedDrivers = nearbyDrivers.sort((a, b) => {
        if (a.rating !== b.rating) return b.rating - a.rating;
        if (a.distance !== b.distance) return a.distance - b.distance;
        return b.completionRate - a.completionRate;
      });
      
      // 3. Send request to top driver
      for (const driver of sortedDrivers) {
        const accepted = await sendDeliveryRequest(driver.driverId, orderId);
        
        if (accepted) {
          await assignDriverToOrder(orderId, driver.driverId);
          return;
        }
        
        // If no response in 30 seconds, try next driver
        await wait(30000);
      }
      
      // If no driver accepts, notify customer
      await notifyCustomer(order.customerId, 'No driver available');
    }
  });
```

---

### **Notification APIs**

#### **15. Send Push Notification**
```http
POST /notifications/send
Authorization: Bearer <token>
Content-Type: application/json

Request:
{
  "userId": "user123",
  "type": "order",
  "title": "Order Update",
  "title_ar": "تحديث الطلب",
  "body": "Your order is being prepared",
  "body_ar": "يتم تحضير طلبك",
  "data": {
    "orderId": "order789",
    "status": "preparing"
  },
  "actionUrl": "/orders/order789"
}

Response (200 OK):
{
  "success": true,
  "notificationId": "notif456",
  "sentAt": "2024-12-25T14:00:00Z"
}

// FCM automatically handles:
// - Device token lookup
// - Push delivery
// - Badge count update
```

---

### **Search & Discovery APIs**

#### **16. Search Restaurants**
```http
GET /restaurants/search?q=pizza&lat=24.7136&lng=46.6753&radius=5000
Authorization: Bearer <token>

Response (200 OK):
{
  "success": true,
  "results": [
    {
      "restaurantId": "rest123",
      "name": "Pizza Paradise",
      "logo": "https://...",
      "cuisineType": ["Italian"],
      "rating": 4.5,
      "deliveryFee": 10.00,
      "estimatedDeliveryTime": "30-40 min",
      "distance": 1.2,
      "isOpen": true
    }
  ],
  "total": 5
}
```

#### **17. Get Restaurant Menu**
```http
GET /restaurants/{restaurantId}/menu
Authorization: Bearer <token>

Response (200 OK):
{
  "success": true,
  "restaurant": {
    "restaurantId": "rest123",
    "name": "Mama's Kitchen",
    ...
  },
  "categories": [
    {
      "categoryId": "cat1",
      "name": "Appetizers",
      "items": [
        {
          "itemId": "item1",
          "name": "Hummus",
          "price": 12.00,
          "image": "https://...",
          "isAvailable": true
        }
      ]
    }
  ]
}
```

---

## 5.5 Data Flow Diagrams

### **5.5.1 Customer Order Flow**

```
┌─────────────┐      ┌──────────────┐      ┌──────────────┐      ┌────────────┐
│  Customer   │      │    Cloud     │      │  Firestore   │      │ Restaurant │
│     App     │      │  Functions   │      │   Database   │      │    App     │
└──────┬──────┘      └──────┬───────┘      └──────┬───────┘      └─────┬──────┘
       │                    │                     │                    │
       │ 1. Place Order     │                     │                    │
       │─────────────────────>                     │                    │
       │                    │                     │                    │
       │                    │ 2. Validate Data    │                    │
       │                    │──────────────────────>                    │
       │                    │                     │                    │
       │                    │ 3. Process Payment  │                    │
       │                    │──────────────────────>                    │
       │                    │                     │                    │
       │                    │ 4. Create Order Doc │                    │
       │                    │──────────────────────>                    │
       │                    │                     │                    │
       │ 5. Order Confirmed │                     │ 6. New Order       │
       │<─────────────────────                     │─────────────────────>
       │                    │                     │                    │
       │                    │                     │ 7. Accept Order    │
       │                    │                     │<─────────────────────
       │                    │                     │                    │
       │ 8. FCM: Accepted   │                     │                    │
       │<─────────────────────<─────────────────────                    │
       │                    │                     │                    │
```

### **5.5.2 Driver Assignment Flow**

```
┌──────────────┐      ┌──────────────┐      ┌──────────────┐      ┌────────────┐
│  Restaurant  │      │    Cloud     │      │  Firestore   │      │   Driver   │
│     App      │      │  Functions   │      │   Database   │      │    App     │
└──────┬───────┘      └──────┬───────┘      └──────┬───────┘      └─────┬──────┘
       │                    │                     │                    │
       │ 1. Mark Ready      │                     │                    │
       │─────────────────────>                     │                    │
       │                    │                     │                    │
       │                    │ 2. Trigger          │                    │
       │                    │ assignDriver()      │                    │
       │                    │ (Cloud Function)    │                    │
       │                    │                     │                    │
       │                    │ 3. Query Available  │                    │
       │                    │    Drivers (5km)    │                    │
       │                    │──────────────────────>                    │
       │                    │                     │                    │
       │                    │ 4. Driver List      │                    │
       │                    │<──────────────────────                    │
       │                    │                     │                    │
       │                    │ 5. Send FCM         │                    │
       │                    │ Delivery Request    │                    │
       │                    │─────────────────────────────────────────>│
       │                    │                     │                    │
       │                    │                     │ 6. Accept          │
       │                    │                     │<─────────────────────
       │                    │                     │                    │
       │                    │ 7. Update Order     │                    │
       │                    │ (assign driver)     │                    │
       │                    │──────────────────────>                    │
       │                    │                     │                    │
       │ 8. Driver Assigned │                     │                    │
       │<─────────────────────                     │                    │
       │                    │                     │                    │
```

### **5.5.3 Real-Time Order Tracking**

```
┌─────────────┐      ┌──────────────┐      ┌────────────┐
│  Customer   │      │  Firestore   │      │   Driver   │
│     App     │      │   Database   │      │    App     │
└──────┬──────┘      └──────┬───────┘      └─────┬──────┘
       │                    │                    │
       │ 1. Open Order      │                    │
       │    Tracking        │                    │
       │                    │                    │
       │ 2. Subscribe to    │                    │
       │    Order Document  │                    │
       │─────────────────────>                    │
       │                    │                    │
       │ 3. Real-time       │                    │
       │    Listener Active │                    │
       │<─────────────────────                    │
       │                    │                    │
       │                    │ 4. Update Status   │
       │                    │<─────────────────────
       │                    │                    │
       │ 5. Snapshot Update │                    │
       │<─────────────────────                    │
       │                    │                    │
       │ 6. UI Updates      │                    │
       │    Automatically   │                    │
       │                    │                    │
       │                    │ 7. Update Location │
       │                    │<─────────────────────
       │                    │    (every 10 sec)  │
       │                    │                    │
       │ 8. Location Update │                    │
       │<─────────────────────                    │
       │                    │                    │
```

---

## 5.6 Security Architecture

### **Authentication Flow**

```
┌──────────────┐      ┌──────────────┐      ┌──────────────┐
│     User     │      │    Mobile    │      │   Firebase   │
│              │      │     App      │      │     Auth     │
└──────┬───────┘      └──────┬───────┘      └──────┬───────┘
       │                    │                     │
       │ 1. Enter Phone     │                     │
       │─────────────────────>                     │
       │                    │                     │
       │                    │ 2. Request OTP      │
       │                    │──────────────────────>
       │                    │                     │
       │                    │ 3. Send SMS via     │
       │                    │    Twilio/Unifonic  │
       │                    │<──────────────────────
       │                    │                     │
       │ 4. Receive SMS     │                     │
       │<────────────────────                     │
       │                    │                     │
       │ 5. Enter OTP       │                     │
       │─────────────────────>                     │
       │                    │                     │
       │                    │ 6. Verify OTP       │
       │                    │──────────────────────>
       │                    │                     │
       │                    │ 7. Generate Token   │
       │                    │<──────────────────────
       │                    │                     │
       │                    │ 8. Store Token      │
       │                    │    Securely         │
       │                    │    (Keychain/       │
       │                    │     Keystore)       │
       │                    │                     │
       │ 9. Authenticated   │                     │
       │<─────────────────────                     │
       │                    │                     │
```

### **Authorization & Role-Based Access Control**

```javascript
// Custom Claims in Firebase Auth Token
{
  "uid": "abc123xyz",
  "role": "customer",        // customer | restaurant | driver
  "restaurantId": null,      // populated if role = restaurant
  "driverId": null,          // populated if role = driver
  "verificationStatus": "approved",
  "iat": 1703520000,
  "exp": 1703606400
}

// Middleware to check authorization
async function authorizeRequest(req, res, next) {
  try {
    // 1. Extract token from header
    const token = req.headers.authorization?.split('Bearer ')[1];
    
    if (!token) {
      return res.status(401).json({ error: 'No token provided' });
    }
    
    // 2. Verify token
    const decodedToken = await admin.auth().verifyIdToken(token);
    
    // 3. Check role
    const requiredRole = req.route.meta?.role;
    if (requiredRole && decodedToken.role !== requiredRole) {
      return res.status(403).json({ error: 'Insufficient permissions' });
    }
    
    // 4. Attach user to request
    req.user = decodedToken;
    next();
    
  } catch (error) {
    return res.status(401).json({ error: 'Invalid token' });
  }
}
```

### **Data Encryption**

| **Data Type** | **Encryption Method** | **Key Storage** |
|--------------|---------------------|----------------|
| **Auth Tokens** | AES-256 | Keychain (iOS) / Keystore (Android) |
| **Payment Tokens** | Payment Gateway Tokenization | Payment provider's vault |
| **User Passwords** | bcrypt (if email/password) | Firebase Auth (managed) |
| **Sensitive Documents** | AES-256 at rest | Firebase Storage (automatic) |
| **Database** | Encrypted at rest | Firebase (automatic) |
| **Network Traffic** | TLS 1.3 | N/A (HTTPS) |

### **Security Best Practices Implemented**

1. **Authentication:**
   - ✅ Multi-factor authentication (phone + OTP)
   - ✅ Session management with token refresh
   - ✅ Biometric authentication option
   - ✅ Account lockout after failed attempts

2. **Authorization:**
   - ✅ Role-based access control (RBAC)
   - ✅ Firestore security rules
   - ✅ Cloud Function middleware
   - ✅ Principle of least privilege

3. **Data Protection:**
   - ✅ Encryption at rest and in transit
   - ✅ Tokenization of payment data
   - ✅ Secure key storage
   - ✅ Regular security audits

4. **API Security:**
   - ✅ Rate limiting (100 requests/min per user)
   - ✅ Input validation and sanitization
   - ✅ SQL injection prevention (NoSQL)
   - ✅ XSS protection
   - ✅ CORS configuration

5. **App Security:**
   - ✅ Certificate pinning
   - ✅ Jailbreak/root detection
   - ✅ Code obfuscation
   - ✅ No sensitive data in logs

---

## 5.7 Scalability Considerations

### **Current Setup (MVP)**

| **Component** | **Capacity** | **Cost (Est.)** |
|--------------|-------------|----------------|
| **Firestore Reads** | 1M reads/month | Free tier |
| **Firestore Writes** | 500K writes/month | Free tier |
| **Cloud Storage** | 5GB | Free tier |
| **Cloud Functions** | 2M invocations/month | Free tier |
| **FCM** | Unlimited | Free |
| **Google Maps API** | 28,000 requests/month | Free tier |

### **Scaling Strategy**

#### **Phase 1: 0-10K Users (Months 1-6)**
- ✅ Firebase free tier sufficient
- ✅ Single region (us-central1)
- ✅ No caching needed
- **Estimated Cost:** $0-50/month

#### **Phase 2: 10K-100K Users (Months 7-12)**
- 🔄 Implement Cloud CDN for images
- 🔄 Add Redis cache (via Cloud Memorystore)
- 🔄 Optimize Firestore queries
- 🔄 Enable Firebase Performance Monitoring
- **Estimated Cost:** $200-500/month

#### **Phase 3: 100K+ Users (Year 2+)**
- 🔄 Multi-region deployment
- 🔄 Load balancer (Cloud Load Balancing)
- 🔄 Auto-scaling Cloud Functions
- 🔄 Database sharding by region
- 🔄 CDN for static assets
- 🔄 Microservices architecture
- **Estimated Cost:** $2,000-5,000/month

### **Performance Optimizations**

| **Optimization** | **Implementation** | **Impact** |
|-----------------|-------------------|-----------|
| **Image Compression** | Compress images to WebP format | -60% bandwidth |
| **Lazy Loading** | Load images on demand | -40% initial load time |
| **Pagination** | 10 items per page | -80% data transfer |
| **Caching** | Cache restaurant list for 5 minutes | -70% database reads |
| **Indexing** | Composite indexes on common queries | -90% query time |
| **CDN** | Serve static assets from CDN | -50% latency |

---

# 6. Functional Requirements

## 6.1 Authentication & User Management

### FR-001: Multi-Role User Registration

| **ID** | **FR-001** |
|--------|-----------|
| **Feature** | Multi-role User Registration |
| **Priority** | **P0 - Critical** |
| **User Story** | As a new user, I want to register using my phone number or social accounts so that I can access the platform based on my role |

**Detailed Requirements:**

1. **Phone Number Registration:**
   - User enters phone number with country code (+966)
   - System validates format using regex: `^(\+966|966|05)[0-9]{8}$`
   - Send 6-digit OTP via SMS (expires in 5 minutes)
   - Allow 3 OTP resend attempts (with 60-second cooldown)
   - After 3 failed verification attempts, lock for 15 minutes
   - After 5 failed attempts in 1 hour, lock for 24 hours

2. **Social Sign-In:**
   - **Google Sign-In:**
     - Use Firebase Auth Google provider
     - Request: email, name, profile photo
     - Auto-populate profile fields
   - **Apple Sign-In (iOS):**
     - Use Firebase Auth Apple provider
     - Support "Hide My Email" feature
     - Handle anonymous email forwarding
   - Link social account to phone number (required)

3. **Role Selection:**
   - Display 3 role cards with icons:
     - 🛒 Customer: "Order food from restaurants"
     - 🍽️ Restaurant: "Manage your restaurant"
     - 🚗 Driver: "Deliver orders and earn"
   - User taps one card to select role
   - Role determines:
     - Subsequent onboarding screens
     - App permissions
     - UI/features available
     - Firebase custom claims
   - **Cannot change role after registration** without contacting support

4. **Customer Onboarding (5 screens):**
   - **Screen 1:** Role confirmed
   - **Screen 2:** Profile Setup
     - Name (required): Text input, 2-50 characters
     - Email (required): Email validation
     - Profile Photo (optional): Upload or capture
   - **Screen 3:** Location Permission
     - Request: "Allow location access for nearby restaurants"
     - Options: Allow / Don't Allow (can skip)
   - **Screen 4:** Notification Permission
     - Request: "Get updates on your orders"
     - Options: Allow / Don't Allow (can skip)
   - **Screen 5:** Success
     - "Welcome to [App Name]!"
     - "Start Ordering" button → Home screen

5. **Restaurant Onboarding (8 screens):**
   - **Screen 1:** Role confirmed
   - **Screen 2:** Basic Info
     - Restaurant Name (required): 3-50 characters
     - Owner Name (required): 3-50 characters
     - Email (required): Email validation
   - **Screen 3:** Business Details
     - Commercial License Number (required): Alphanumeric, 10-15 chars
     - Phone Number (required): +966 format
     - Restaurant Type: Dropdown (Dine-in, Delivery, Both)
   - **Screen 4:** Address
     - District: Dropdown
     - Street: Text input
     - Building Number: Text input
     - Map picker: Drag pin to exact location
   - **Screen 5:** Document Upload
     - Commercial License: PDF/Image, max 5MB
       - File picker or camera
       - Preview uploaded file
     - Menu Samples: Multiple images, max 10MB total
       - Gallery picker (max 5 images)
       - Swipe to preview
   - **Screen 6:** Restaurant Logo
     - Upload logo: PNG/JPG, max 2MB, square (1:1 ratio)
     - Crop tool
     - Preview
   - **Screen 7:** Review & Submit
     - Summary of all entered info
     - "Edit" buttons for each section
     - "Submit for Approval" button
   - **Screen 8:** Pending Approval
     - Status: "Under Review"
     - Message: "We'll review your application within 24-48 hours"
     - "You'll receive a notification once approved"
     - "OK" button → Close app or logout

6. **Driver Onboarding (10 screens):**
   - **Screen 1:** Role confirmed
   - **Screen 2:** Personal Info
     - Full Name (required): 3-50 characters
     - Email (required)
     - Date of Birth (required): Date picker, must be 18+
   - **Screen 3:** National ID
     - National ID Number (required): 10 digits
     - Upload ID (front & back): 2 images, max 5MB each
   - **Screen 4:** Driver's License
     - License Number (required): Alphanumeric
     - Expiry Date (required): Must be valid for 6+ months
     - Upload License (front & back): 2 images
   - **Screen 5:** Vehicle Info
     - Vehicle Type (required): Dropdown (Motorcycle, Car, Bicycle)
     - Make: Text input (e.g., "Honda", "Toyota")
     - Model: Text input (e.g., "Civic", "Corolla")
     - Year: Number picker (1990-2024)
     - Color: Text input
     - Plate Number (required): Alphanumeric, Arabic or English
   - **Screen 6:** Vehicle Documents
     - Registration (Istimara): PDF/Image, max 5MB
       - Must show valid expiry
     - Insurance: PDF/Image, max 5MB
       - Must be valid
   - **Screen 7:** Profile Photo
     - Upload clear face photo: Max 2MB
     - Guidelines: "Good lighting, no sunglasses, no hat"
     - Camera or gallery
   - **Screen 8:** Bank Account (for payouts)
     - Bank Name: Dropdown (Saudi banks)
     - IBAN: 24-character validation (SA...)
     - Account Holder Name: Must match driver name
   - **Screen 9:** Review & Submit
     - All info summary
     - Checklist of documents:
       - ✅ National ID
       - ✅ Driver's License
       - ✅ Vehicle Registration
       - ✅ Insurance
       - ✅ Profile Photo
     - "Submit for Approval" button
   - **Screen 10:** Pending Approval
     - Status: "Under Review"
     - Message: "Background check & document verification may take 48-72 hours"
     - "We'll notify you once approved"
     - "OK" button → Close app or logout

7. **Post-Approval Process:**
   - **Restaurant:**
     - Admin reviews documents in admin panel
     - Checks: License validity, menu appropriateness
     - Approval actions:
       - ✅ Approve: Send FCM notification "Your restaurant is approved!"
         - User can now login and access restaurant dashboard
       - ❌ Reject: Send notification with reason
         - User can resubmit after fixing issues
   
   - **Driver:**
     - Admin reviews all documents
     - Background check (optional integration with 3rd party service)
     - Approval actions:
       - ✅ Approve: Send FCM notification "You're approved to start delivering!"
         - User can now login and start accepting orders
       - ❌ Reject: Send notification with reason
         - User can resubmit

**Acceptance Criteria:**
- ✅ User can register with phone + OTP in < 2 minutes
- ✅ Social sign-in completes in < 30 seconds
- ✅ OTP delivery within 10 seconds (95% of the time)
- ✅ Document upload supports PDF, JPG, PNG formats
- ✅ File size validation prevents uploads >5MB
- ✅ Image compression applied automatically
- ✅ Restaurant/Driver see "Pending Approval" status after registration
- ✅ Customers can start using app immediately (no approval needed)
- ✅ All forms support Arabic and English
- ✅ Form validation shows real-time error messages
- ✅ "Back" button allows editing previous steps without losing data
- ✅ Progress indicator shows current step (e.g., "Step 3 of 5")

**Error Handling:**

| **Error** | **Message** | **Resolution** |
|-----------|------------|---------------|
| Invalid phone format | "Please enter a valid Saudi phone number" | Show format example: +966501234567 |
| OTP not received | "Didn't receive code? Resend in 60s" | Countdown timer, then enable "Resend" |
| Invalid OTP | "Incorrect code. 2 attempts remaining" | Show remaining attempts |
| Account locked | "Too many failed attempts. Try again in 15 minutes" | Show countdown |
| File too large | "File must be less than 5MB" | Show file size |
| Invalid file type | "Please upload PDF, JPG, or PNG" | Show supported formats |
| Network error | "Connection lost. Please try again" | Retry button |
| Email already exists | "This email is already registered" | "Login instead" button |
| Phone already exists | "This number is already registered" | "Login instead" button |

**Wireframe Screens:**

**Common Screens (All Roles):**
1. Welcome Screen (role selection)
2. Phone Number Entry
3. OTP Verification
4. Social Sign-In Options

**Customer Screens:**
5. Customer Profile Setup
6. Location Permission
7. Notification Permission
8. Registration Success

**Restaurant Screens:**
9. Restaurant Basic Info
10. Business Details
11. Address & Location
12. Document Upload (License)
13. Document Upload (Menu)
14. Logo Upload
15. Review & Submit
16. Pending Approval

**Driver Screens:**
17. Driver Personal Info
18. National ID Upload
19. Driver's License Upload
20. Vehicle Info
21. Vehicle Documents Upload
22. Profile Photo Upload
23. Bank Account Info
24. Review & Submit
25. Pending Approval

**Technical Notes:**
- Store user data in Firestore: `/users/{userId}`
- Store documents in Cloud Storage: `/uploads/{role}/{userId}/{documentType}/{filename}`
- Use Cloud Function to compress images after upload
- Set custom claims after approval: `role`, `restaurantId`/`driverId`, `verificationStatus`
- Send SMS via Twilio/Unifonic API
- Implement rate limiting: max 5 OTP requests per hour per phone number
- Log all registration attempts for security audit

---

### FR-002: Secure Login

| **ID** | **FR-002** |
|--------|-----------|
| **Feature** | Secure Login with Multiple Options |
| **Priority** | **P0 - Critical** |
| **User Story** | As a returning user, I want to login quickly and securely using my preferred method |

**Detailed Requirements:**

1. **Phone + OTP Login:**
   - Same OTP flow as registration
   - User enters phone number
   - System checks if user exists in Firestore
   - If new phone: Show "No account found. Sign up instead?"
   - If exists: Send OTP
   - After OTP verification:
     - Generate Firebase Auth token
     - Store token securely in Keychain/Keystore
     - Navigate to appropriate dashboard (Customer/Restaurant/Driver)

2. **Social Login:**
   - **"Continue with Google":**
     - Trigger Google Sign-In flow
     - Firebase Auth handles OAuth
     - If account exists: Login immediately
     - If new account: Prompt to link phone number (required)
   - **"Continue with Apple" (iOS only):**
     - Trigger Apple Sign-In
     - Handle "Hide My Email" scenarios
     - Same linking flow as Google

3. **Remember Me:**
   - Checkbox: "Keep me logged in"
   - If checked:
     - Token valid for 30 days
     - Auto-refresh token before expiry
     - User stays logged in across app launches
   - If unchecked:
     - Token valid for session only
     - User must re-login after closing app

4. **Biometric Login (Post-First Login):**
   - **Face ID (iPhone X+):**
     - After first successful login, prompt: "Enable Face ID for quick login?"
     - If enabled:
       - Store encrypted token in Keychain with biometric protection
       - Next login: Show Face ID prompt immediately
       - Fallback to phone/OTP if Face ID fails
   - **Touch ID (older iPhones):**
     - Same flow as Face ID

5. **Auto-Login:**
   - On app launch:
     - Check if valid token exists
     - If yes: Verify token with Firebase
     - If valid: Auto-login to last role's dashboard
     - If expired: Prompt to login

6. **Session Management:**
   - Token expiry: 30 days (if "Remember Me" checked)
   - Auto-refresh: 7 days before expiry
   - Force logout scenarios:
     - User logs out manually
     - User changes password
     - Admin force-logout (security)
     - Token revoked

7. **Logout:**
   - User taps "Logout" in settings
   - Confirmation modal: "Are you sure you want to logout?"
   - Actions: "Cancel", "Logout"
   - On logout:
     - Delete auth token from local storage
     - Clear all cached data
     - Clear Firestore persistence
     - Revoke FCM token
     - Navigate to Welcome screen

**Acceptance Criteria:**
- ✅ Login completes in < 30 seconds (excluding OTP wait time)
- ✅ Biometric login available after first successful login
- ✅ Token auto-refreshes silently in background
- ✅ Graceful handling of network errors (offline mode)
- ✅ User can switch between phone/social login methods
- ✅ Session persists across app restarts (if "Remember Me" enabled)
- ✅ Clear error messages for all failure scenarios
- ✅ No sensitive data (password, token) stored in plain text

**Error Handling:**

| **Error** | **Message** | **Resolution** |
|-----------|------------|---------------|
| Invalid OTP | "Incorrect code. Please try again" | Allow 3 attempts, then resend |
| Expired OTP | "Code expired. Request a new one" | "Resend Code" button |
| Account not found | "No account found. Sign up instead?" | "Sign Up" button |
| Account locked | "Account temporarily locked. Contact support" | Support contact button |
| Network error | "No internet connection. Try again" | Retry button |
| Biometric failed | "Face ID failed. Try again or use passcode" | Fallback to phone login |
| Token expired | "Session expired. Please login again" | Auto-redirect to login |
| Social login failed | "Google Sign-In failed. Try again" | Retry or use phone login |

**Wireframe Screens:**
1. Login Screen (phone + social options)
2. OTP Input Screen
3. Biometric Prompt (Face ID/Touch ID)
4. Loading/Authenticating Screen
5. Error Screen (with retry button)

**Technical Implementation:**

```dart
// Example: Biometric Login
Future<bool> loginWithBiometrics() async {
  final LocalAuthentication auth = LocalAuthentication();
  
  // Check if biometrics available
  final bool canAuthenticate = await auth.canCheckBiometrics;
  if (!canAuthenticate) return false;
  
  try {
    // Prompt biometric authentication
    final bool authenticated = await auth.authenticate(
      localizedReason: 'Authenticate to login',
      options: const AuthenticationOptions(
        biometricOnly: true,
        stickyAuth: true,
      ),
    );
    
    if (authenticated) {
      // Retrieve stored token from secure storage
      final secureStorage = FlutterSecureStorage();
      final token = await secureStorage.read(key: 'auth_token');
      
      if (token != null) {
        // Verify token with Firebase
        final user = await FirebaseAuth.instance.signInWithCustomToken(token);
        return true;
      }
    }
    
    return false;
    
  } catch (e) {
    print('Biometric authentication failed: $e');
    return false;
  }
}
```

---


## 6.2 Customer Features

### FR-003: Restaurant Discovery & Filtering

| **ID** | **FR-003** |
|--------|-----------|
| **Feature** | Browse, Search, Filter, and Sort Restaurants |
| **Priority** | **P0 - Critical** |

**Key Features:**
- Display 10 restaurants per page (infinite scroll)
- Each card shows: image, name, cuisine, rating, delivery time, fee, status
- Default sort: Nearest first
- Search: Restaurant name, dish name, cuisine type
- **Filters:**
  - Cuisine (multi-select)
  - Price range (slider: 0-200 SAR)
  - Distance (slider: 0-10km)
  - Delivery time (< 30min, 30-45min, 45-60min)
  - Rating (4+, 4.5+)
  - Offers available, Open now
- **Sort:** Nearest, Highest rated, Lowest fee, Fastest
- **Quick Filters:** Favorites, New, Trending, Free Delivery

**Acceptance Criteria:**
- ✅ List loads in < 2 seconds
- ✅ Search returns results in < 1 second
- ✅ Filters apply immediately
- ✅ Skeleton loading during fetch
- ✅ Pull-to-refresh updates list

---

### FR-004: Menu Browsing & Item Customization

| **ID** | **FR-004** |
|--------|-----------|
| **Priority** | **P0 - Critical** |

**Key Features:**
- Restaurant header: Cover image, logo, name, rating, delivery info
- Menu categories (sticky tabs): Appetizers, Mains, Desserts, Drinks
- Item cards: image, name, description, price, availability
- Item detail modal:
  - Full image, name, description, base price
  - Size selection (Small, Medium, Large + price)
  - Add-ons (checkboxes with prices)
  - Remove ingredients (checkboxes)
  - Special instructions (text area, 200 chars)
  - Quantity selector (1-20)
  - Subtotal calculation
  - "Add to Cart" button
- Floating cart button with badge

**Acceptance Criteria:**
- ✅ Menu loads in < 1.5 seconds
- ✅ Images load progressively
- ✅ Price updates in real-time
- ✅ Out-of-stock items disabled
- ✅ Add to cart shows success feedback

---

### FR-005: Shopping Cart Management

| **ID** | **FR-005** |
|--------|-----------|
| **Priority** | **P0 - Critical** |

**Key Features:**
- Cart list: All items with customizations, prices, quantity
- Edit item: Opens detail modal with pre-filled selections
- Remove item: Confirmation modal
- Price breakdown: Subtotal, delivery fee, discount, VAT (15%), total
- Coupon entry: Input field, apply button, validation
- Minimum order warning (if below threshold)
- "Clear Cart" button
- "Proceed to Checkout" button

**Acceptance Criteria:**
- ✅ Cart updates instantly
- ✅ Calculations accurate
- ✅ Coupon validates in < 1 second
- ✅ Cart persists across sessions (Hive storage)
- ✅ Cart clears after successful order

---

### FR-006: Checkout & Payment

| **ID** | **FR-006** |
|--------|-----------|
| **Priority** | **P0 - Critical** |

**Sections:**

1. **Delivery Address:**
   - Select from saved addresses
   - Add new address (with map picker)
   - Edit/delete addresses
   - Mark default

2. **Delivery Time:**
   - Deliver Now (default)
   - Schedule Order (date/time picker, min: 2 hours ahead, max: 7 days)

3. **Payment Method:**
   - Family Wallet (shows balance, select member)
   - Credit/Debit Card (mock UI: card number, expiry, CVV)
   - Apple Pay (mock UI)
   - Application Wallet (shows balance, top-up option)

4. **Order Summary:**
   - Items, subtotal, fees, discount, total

5. **Special Instructions:**
   - Text area (300 chars)

6. **Place Order Button:**
   - Validation checks (address, payment)
   - Loading state
   - Success → Order Tracking
   - Failure → Error modal

**Acceptance Criteria:**
- ✅ Checkout loads in < 1 second
- ✅ Address can be added via map
- ✅ Scheduled orders validate restaurant hours
- ✅ Payment validates before order placement
- ✅ Clear error messages

---

### FR-007: Family Wallet ⭐

| **ID** | **FR-007** |
|--------|-----------|
| **Priority** | **P1 - High (Unique Feature)** |

**Key Features:**

1. **Create Family Wallet:**
   - Enter family name
   - Set initial balance (min: 100 SAR)
   - Add members (phone/email)
   - Set spending limits per member (daily/monthly)
   - Send invitations

2. **Manage Family:**
   - View all members with balances
   - Edit spending limits
   - Remove members
   - Top-up wallet balance
   - View transaction history

3. **Invitation Flow:**
   - Invitee receives push notification
   - Shows: Family name, owner name, spending limit
   - Actions: Accept / Decline
   - After acceptance: Wallet appears in payment options

4. **Payment with Family Wallet:**
   - During checkout, select family wallet
   - Owner: Choose which member pays
   - Member: Auto-select self
   - Shows remaining balance/limit
   - Deducts from wallet on order placement

5. **Transaction History:**
   - List of all transactions
   - Filter by member, date, amount
   - Export to PDF/Excel

**Acceptance Criteria:**
- ✅ Family wallet created in < 2 minutes
- ✅ Invitations deliver within 10 seconds
- ✅ Spending limits enforce correctly
- ✅ Balance updates in real-time
- ✅ Only owner can add/remove members

---

### FR-008: Group Order ⭐

| **ID** | **FR-008** |
|--------|-----------|
| **Priority** | **P1 - High (Unique Feature)** |

**Key Features:**

1. **Start Group Order:**
   - Select restaurant
   - Enter group name
   - Set deadline (10min, 20min, 30min, 1 hour, custom)
   - Set delivery address
   - Generate join code & link
   - Share via QR, WhatsApp, SMS, link

2. **Join Group Order:**
   - Open join link/scan QR
   - Shows: Host name, restaurant, deadline countdown
   - "Join Order" button
   - Browse menu and add items

3. **Group Cart:**
   - View modes: "By Person" / "All Items"
   - Shows each participant's items and subtotal
   - Real-time updates when anyone adds/removes items
   - Countdown timer to deadline
   - Host can remove participants/items

4. **Split Bill Options:**
   - **Equal Split:** Total ÷ participants
   - **Pay Own Items:** Each pays their items + equal share of delivery fee
   - **Custom Split:** Manual amounts

5. **Payment Collection:**
   - Payment status tracker (shows who paid)
   - Each participant receives notification
   - Pay their share via their preferred method
   - Timeout: 10-minute reminder, 30-minute host action (remove or cancel)

6. **Order Placement:**
   - When all paid: Host confirms & places single order
   - All participants can track order
   - Shared delivery to one address

**Acceptance Criteria:**
- ✅ Group order created in < 30 seconds
- ✅ Join link opens correctly
- ✅ Real-time updates appear within 1 second
- ✅ Split calculations accurate
- ✅ All participants notified at key milestones
- ✅ Order placed only after all payments

---

### FR-009: Order Tracking

| **ID** | **FR-009** |
|--------|-----------|
| **Priority** | **P0 - Critical** |

**Status Steps:**
1. Order Placed
2. Restaurant Accepted
3. Preparing
4. Ready for Pickup
5. Driver Assigned
6. Driver Picked Up
7. On the Way
8. Delivered

**Features:**
- Visual progress indicator
- Estimated delivery time countdown
- Driver info: Name, photo, rating, vehicle
- Live map (simplified UI - mock)
- Contact driver: Chat/Call buttons
- Cancel order (if allowed - before driver picks up)
- Push notifications on status change

**Acceptance Criteria:**
- ✅ Status updates in real-time
- ✅ Map shows driver location (mock movement for prototype)
- ✅ Chat/Call buttons functional
- ✅ Cancel only available before "Driver Picked Up"

---

### FR-010: Order History & Reorder

| **ID** | **FR-010** |
|--------|-----------|
| **Priority** | **P2 - Medium** |

**Features:**
- List past orders (date, restaurant, total, status)
- Filter: All, Completed, Cancelled
- Order details: Items, address, payment, receipt
- **"Reorder" button:** Adds same items to cart (checks availability)
- Rate order: Restaurant (1-5 stars) + Driver (1-5 stars) + optional review
- Report issue

**Acceptance Criteria:**
- ✅ History loads in < 2 seconds
- ✅ Reorder checks item availability
- ✅ Rating submits successfully

---

### FR-011: Communication (Chat & Call)

| **ID** | **FR-011** |
|--------|-----------|
| **Priority** | **P2 - Medium** |

**Chat:**
- Simple in-app chat interface
- Text messages only
- Timestamp, online/offline status
- Unread badge

**Call:**
- "Call Driver" button
- Opens native phone dialer
- Masked number (optional - for privacy)

**Acceptance Criteria:**
- ✅ Messages deliver within 2 seconds
- ✅ Call button opens dialer correctly
- ✅ Chat history saved

---

### FR-012: User Profile & Settings

| **ID** | **FR-012** |
|--------|-----------|
| **Priority** | **P2 - Medium** |

**Sections:**
- **Profile:** Edit name, email, photo
- **Addresses:** Manage saved addresses
- **Payment Methods:** Manage cards, wallets
- **Wallet:** View balance, transaction history, add funds
- **Language:** Switch English/Arabic
- **Notifications:** Toggle order updates, promotions, chat
- **Help & Support:** FAQ, contact form
- **Logout**

**Acceptance Criteria:**
- ✅ Profile updates save successfully
- ✅ Language switch applies immediately (app restart)
- ✅ Logout clears all cached data

---

## 6.3 Restaurant Features

### FR-013: Restaurant Dashboard

| **ID** | **FR-013** |
|--------|-----------|
| **Priority** | **P0 - Critical** |

**Features:**
- Stats cards: Today's orders, revenue, avg rating
- Quick actions: New orders, menu, promotions
- Toggle: Open/Closed status
- Order notifications (sound + badge)

---

### FR-014: Order Management

| **ID** | **FR-014** |
|--------|-----------|
| **Priority** | **P0 - Critical** |

**Features:**
- New order notification (sound + visual)
- Order details: Items, customer, address, payment
- Actions: Accept (set prep time) / Reject (reason)
- Update status: Preparing → Ready for Pickup
- Filter: New, In Progress, Completed

**Acceptance Criteria:**
- ✅ Notifications arrive within 10 seconds
- ✅ Accept/Reject updates customer immediately
- ✅ Status changes trigger driver assignment

---

### FR-015: Menu Management

| **ID** | **FR-015** |
|--------|-----------|
| **Priority** | **P1 - High** |

**Features:**
- View all menu items by category
- Add item: Name, description, price, image, category, customizations
- Edit item: Update any field
- Delete item: Confirmation required
- Toggle availability: In stock / Out of stock
- Manage categories: Add, edit, delete, reorder
- Drag & drop to reorder items

**Acceptance Criteria:**
- ✅ Menu updates reflect to customers within 1 minute
- ✅ Images upload successfully (max 2MB)
- ✅ Drag & drop works smoothly

---

### FR-016: Promotions & Offers

| **ID** | **FR-016** |
|--------|-----------|
| **Priority** | **P2 - Medium** |

**Features:**
- Create promotion:
  - Title, description
  - Discount: % / Fixed amount / Buy-X-Get-Y
  - Start/end date & time
  - Applicable items/categories
  - Minimum order value
- Active/Inactive promotions list
- Edit/Delete promotion
- Schedule future promotions

**Acceptance Criteria:**
- ✅ Promotion goes live at scheduled time
- ✅ Customers see "OFFER" badge on restaurant card
- ✅ Discount applies correctly at checkout

---

### FR-017: Operating Hours

| **ID** | **FR-017** |
|--------|-----------|
| **Priority** | **P2 - Medium** |

**Features:**
- Set hours for each day of week
- Add multiple time slots per day (e.g., lunch & dinner)
- Mark holidays/closed days
- Temporary hours override

**Acceptance Criteria:**
- ✅ Restaurant shows "Closed" when outside operating hours
- ✅ Scheduled orders validate against hours

---

### FR-018: Restaurant Profile

| **ID** | **FR-018** |
|--------|-----------|
| **Priority** | **P3 - Low** |

**Features:**
- Edit: Name, logo, cover image, description
- Update contact info
- View reviews & ratings (read-only)

---

## 6.4 Driver Features

### FR-019: Driver Dashboard

| **ID** | **FR-019** |
|--------|-----------|
| **Priority** | **P0 - Critical** |

**Features:**
- Toggle: Available / Unavailable
- Stats: Today's deliveries, earnings
- Active delivery card (if any)
- Delivery request notifications

---

### FR-020: Delivery Request Handling

| **ID** | **FR-020** |
|--------|-----------|
| **Priority** | **P0 - Critical** |

**Features:**
- New request notification (sound + vibration)
- Request details: Restaurant, customer location, distance, payment
- Actions: Accept / Reject (with 30-second timer)
- Auto-reassign if timeout

**Acceptance Criteria:**
- ✅ Notification arrives within 5 seconds
- ✅ 30-second countdown visible
- ✅ Accept updates order status immediately

---

### FR-021: Active Delivery Workflow

| **ID** | **FR-021** |
|--------|-----------|
| **Priority** | **P0 - Critical** |

**Features:**
- Order details: Items, customer info, addresses
- **Navigate to Restaurant:** Button opens Google Maps
- Update status: Heading to Restaurant → Arrived → Picked Up
- **Navigate to Customer:** Button opens Google Maps
- Update status: On the Way → Delivered
- Contact customer: Chat/Call buttons
- Mark as delivered: Confirmation (optional: delivery code)

**Acceptance Criteria:**
- ✅ Navigate buttons open Google Maps
- ✅ Status updates notify customer
- ✅ Delivery completes workflow

---

### FR-022: Delivery History

| **ID** | **FR-022** |
|--------|-----------|
| **Priority** | **P3 - Low** |

**Features:**
- List past deliveries
- Earnings summary (today, week, month)

---

### FR-023: Driver Profile

| **ID** | **FR-023** |
|--------|-----------|
| **Priority** | **P2 - Medium** |

**Features:**
- View profile: Name, photo, rating, total deliveries
- Update vehicle info
- View/update documents (license, insurance, registration)
- Settings: Notifications, availability preferences

---

## 6.5 Shared Features

### FR-024: Push Notifications

| **ID** | **FR-024** |
|--------|-----------|
| **Priority** | **P0 - Critical** |

**Notification Types:**
- Order status updates
- New delivery requests (driver)
- Family wallet invitations
- Group order invites
- Promotions (opt-in)
- Payment confirmations
- Rating requests

**Features:**
- In-app notification center
- Badge counts
- Mark as read
- Clear all
- Deep links to relevant screens

---

### FR-025: Search

| **ID** | **FR-025** |
|--------|-----------|
| **Priority** | **P2 - Medium** |

**Features:**
- Search bar: "Search restaurants or dishes..."
- Autocomplete suggestions (after 2 characters)
- Recent searches (last 5)
- Popular searches
- Clear history

---

### FR-026: Ratings & Reviews

| **ID** | **FR-026** |
|--------|-----------|
| **Priority** | **P2 - Medium** |

**Features:**
- Rate restaurant: 1-5 stars + optional review (after delivery)
- Rate driver: 1-5 stars + optional review
- View restaurant reviews (list with filters: Recent, Highest, Lowest)

---

### FR-027: Help & Support

| **ID** | **FR-027** |
|--------|-----------|
| **Priority** | **P3 - Low** |

**Features:**
- FAQ section (categories: Orders, Payment, Account, etc.)
- Contact support form (name, email, message, screenshot upload)
- Live chat (mock UI - shows "Agent will respond soon")

---

# 7. Error Handling Strategy

## 7.1 Error Categories & Resolution

### **Network Errors**

| **Error** | **User Message** | **Technical Action** | **UI Treatment** |
|-----------|-----------------|---------------------|------------------|
| No Internet | "No internet connection. Please check your network" | Queue API calls, retry when online | Full-screen error with "Retry" button |
| Timeout | "Request timed out. Please try again" | Retry request (max 3 attempts) | Toast notification + Retry button |
| Server Error (500) | "Something went wrong. We're fixing it" | Log error, notify team | Error dialog with "Contact Support" |
| API Unavailable (503) | "Service temporarily unavailable" | Exponential backoff retry | Banner notification |

### **Authentication Errors**

| **Error** | **User Message** | **Action** |
|-----------|-----------------|-----------|
| Token Expired | "Session expired. Please login again" | Clear token, redirect to login |
| Invalid Token | "Authentication failed. Please login" | Force logout |
| Account Locked | "Account locked due to suspicious activity" | Show support contact |
| Unverified Account | "Please verify your email/phone" | Show verification screen |

### **Validation Errors**

| **Error** | **User Message** | **UI Treatment** |
|-----------|-----------------|------------------|
| Empty Required Field | "This field is required" | Red border + error text below field |
| Invalid Format | "Please enter a valid [email/phone/etc.]" | Red border + format hint |
| Min/Max Length | "[Field] must be between X-Y characters" | Character counter (red when invalid) |
| File Size Exceeded | "File must be less than 5MB" | File size display + Clear button |
| Invalid File Type | "Only PDF, JPG, PNG files allowed" | Supported formats list |

### **Business Logic Errors**

| **Error** | **User Message** | **Action** |
|-----------|-----------------|-----------|
| Restaurant Closed | "This restaurant is currently closed" | Show opening hours + Schedule option |
| Item Unavailable | "This item is no longer available" | Remove from cart, suggest alternatives |
| Minimum Order Not Met | "Add [X] SAR more to meet minimum order" | Highlight minimum, link to menu |
| Payment Failed | "Payment unsuccessful. Try another method" | Show payment options |
| Insufficient Balance | "Insufficient wallet balance" | Show "Top Up" button |
| Spending Limit Exceeded | "You've reached your spending limit" | Show limit details + "Contact Admin" |
| Order Cannot Be Cancelled | "Order cannot be cancelled after driver pickup" | Show order status |

### **Payment Errors**

| **Error** | **User Message** | **Action** |
|-----------|-----------------|-----------|
| Card Declined | "Card was declined. Try another card" | Show saved cards + Add new |
| Insufficient Funds | "Insufficient funds on card" | Suggest wallet or another card |
| Invalid Card | "Invalid card details. Please check" | Highlight invalid fields |
| 3D Secure Failed | "3D Secure verification failed" | Retry or use another method |
| Payment Gateway Error | "Payment service unavailable. Try again" | Retry button + Support contact |

---

## 7.2 Error Handling Best Practices

### **User-Facing Errors:**
1. **Clear & Concise:** Avoid technical jargon
2. **Actionable:** Provide next steps ("Try again", "Contact support")
3. **Empathetic:** "We're sorry for the inconvenience"
4. **Localized:** Show in user's language (Arabic/English)

### **Developer Error Logging:**
```dart
// Example: Sentry error logging
try {
  await placeOrder(order);
} catch (error, stackTrace) {
  // Log to Sentry
  await Sentry.captureException(
    error,
    stackTrace: stackTrace,
    hint: {
      'orderId': order.id,
      'userId': currentUser.id,
      'restaurantId': order.restaurantId,
    },
  );
  
  // Show user-friendly message
  showErrorDialog(
    context,
    'Failed to place order',
    'Please try again or contact support',
  );
}
```

### **Retry Strategies:**

| **Scenario** | **Strategy** |
|--------------|-------------|
| Network Request | Exponential backoff (1s, 2s, 4s), max 3 attempts |
| Image Upload | Retry immediately once, then queue for background |
| Payment | Show retry button, don't auto-retry |
| Order Placement | Retry once automatically, then manual |

---

# 8. Performance Requirements

## 8.1 Performance Metrics & Targets

| **Metric** | **Target** | **Measurement Method** |
|-----------|-----------|---------------------|
| **App Launch Time** | < 2 seconds | Cold start to first interactive screen |
| **Screen Transition** | < 300ms | Navigate between screens |
| **API Response Time** | < 1 second | From request to response |
| **Image Load Time** | < 2 seconds | From request to display (progressive) |
| **Search Results** | < 1 second | From input to results display |
| **Real-time Updates** | < 1 second | Firestore listener to UI update |
| **App Size** | < 50MB | Download size on App Store |
| **Memory Usage** | < 100MB | Average during active use |
| **Battery Drain** | < 5% per hour | Active use |
| **Crash Rate** | < 0.1% | Crashes per session |

---

## 8.2 Optimization Techniques

### **Frontend Optimizations:**

1. **Image Optimization:**
   - Compress to WebP format (60-80% quality)
   - Progressive loading (blur-up technique)
   - Lazy loading (load images as they enter viewport)
   - CDN caching (Firebase Storage CDN)
   - Thumbnail generation (3 sizes: small, medium, large)

2. **List Performance:**
   - Pagination (10 items per page)
   - ListView.builder with recycling
   - Debounce search input (300ms delay)
   - Skeleton loading during fetch

3. **State Management:**
   - Riverpod for reactive state
   - Avoid unnecessary rebuilds
   - Memoization of computed values
   - Dispose controllers properly

4. **Local Storage:**
   - Hive for fast NoSQL storage
   - Cache restaurant list (5-minute expiry)
   - Cache images (7-day expiry)
   - Secure storage for tokens

### **Backend Optimizations:**

1. **Database:**
   - Composite indexes on common queries
   - Pagination (limit 10-20 documents per query)
   - Query only required fields
   - Use subcollections for large datasets

2. **Cloud Functions:**
   - Min instances for critical functions (avoid cold starts)
   - Timeout: 60 seconds (avoid long-running functions)
   - Batch operations where possible
   - Async processing for non-critical tasks

3. **Caching:**
   - CDN for static assets
   - Redis cache for frequent queries (future enhancement)
   - Client-side caching (Hive)

### **Network Optimizations:**

1. **API Calls:**
   - Combine multiple requests where possible
   - Use Dio interceptors for retry logic
   - Gzip compression for responses
   - HTTP/2 support

2. **Real-Time Data:**
   - Firestore listeners only for active screens
   - Unsubscribe when screen disposed
   - Limit listener updates (throttle to 1 second)

---

## 8.3 Performance Monitoring

**Tools:**
- Firebase Performance Monitoring
- Firebase Crashlytics
- Sentry (optional)
- Custom analytics events

**Key Metrics to Track:**
- Screen rendering time
- Network request duration
- Slow API calls (>3 seconds)
- App crashes with stack traces
- Memory leaks
- Battery usage

---

# 9. Security & Privacy

## 9.1 Data Protection

### **Sensitive Data Encryption:**

| **Data Type** | **Encryption** | **Storage** |
|--------------|---------------|-----------|
| Auth Tokens | AES-256 | Keychain (iOS) / Keystore (Android) |
| Payment Tokens | Tokenization (PCI-compliant) | Payment gateway vault |
| User Passwords | bcrypt hash | Firebase Auth |
| Documents | AES-256 at rest | Firebase Storage |
| Database | Encrypted at rest | Firestore (automatic) |

### **Data Transmission:**
- All network traffic over HTTPS (TLS 1.3)
- Certificate pinning (prevent MITM attacks)
- API request signing (HMAC)

---

## 9.2 Authentication & Authorization

### **Security Measures:**
1. **Phone + OTP:** 6-digit OTP, 5-minute expiry
2. **Rate Limiting:**
   - OTP: Max 5 requests per hour per phone
   - Login: Max 10 attempts per hour per account
   - API: Max 100 requests per minute per user
3. **Session Management:**
   - Token expiry: 30 days
   - Auto-refresh: 7 days before expiry
   - Force logout on suspicious activity
4. **Biometric Authentication:**
   - Face ID / Touch ID support
   - Fallback to phone + OTP

### **Role-Based Access Control (RBAC):**
- Customer: Can only access own orders, profile
- Restaurant: Can only access own restaurant data, orders
- Driver: Can only access assigned deliveries
- Admin: Full access (via admin panel - future)

---

## 9.3 Privacy Compliance

### **Data Collection:**
**What we collect:**
- Name, email, phone number
- Location (for delivery, with permission)
- Order history
- Payment information (tokenized)
- Device information (for analytics)

**What we don't collect:**
- Exact real-time location (only during active delivery)
- Contacts list
- Photos/videos (except uploaded by user)
- Microphone/camera (except for uploads)

### **User Rights:**
- **Right to Access:** View all personal data (export to JSON/PDF)
- **Right to Delete:** Delete account & all data
- **Right to Portability:** Export data in machine-readable format
- **Right to Opt-Out:** Disable notifications, marketing, analytics

### **GDPR/Saudi DPA Compliance:**
- Privacy Policy clearly displayed during registration
- Consent checkboxes for data processing
- Cookie/tracking consent (if web version)
- Data retention: 2 years after last activity, then auto-delete

---

## 9.4 Security Best Practices

### **Code Security:**
1. **Code Obfuscation:**
   - Flutter build with `--obfuscate`
   - ProGuard rules for Android
2. **Secret Management:**
   - API keys in environment variables (not hardcoded)
   - Firebase config in secure storage
3. **Dependency Scanning:**
   - Regular updates for Flutter packages
   - Vulnerability scanning (GitHub Dependabot)

### **Runtime Security:**
1. **Jailbreak/Root Detection:**
   - Detect compromised devices
   - Show warning (don't block - can be bypassed)
2. **SSL Pinning:**
   - Pin Firebase and API certificates
3. **Debugging Detection:**
   - Disable in production builds

### **Incident Response Plan:**
1. **Data Breach:**
   - Notify affected users within 72 hours
   - Force password reset
   - Investigate and patch vulnerability
2. **Suspicious Activity:**
   - Automated account lockout
   - Email/SMS notification to user
   - Manual review by security team

---

# 10. Release Strategy

## 10.1 Release Phases

### **Phase 1: Prototype Development (Weeks 1-6)**

**Deliverables:**
- ✅ Complete Figma prototype (160 screens)
- ✅ Interactive flows (6 user journeys)
- ✅ Design system & component library
- ✅ Annotations for developers
- ✅ PRD finalization

**Milestones:**
- Week 1: Components & Design System
- Week 2: Customer screens (Auth, Browse, Cart)
- Week 3: Customer screens (Checkout, Orders, Family Wallet, Group Order)
- Week 4: Restaurant & Driver screens
- Week 5: Interactivity & animations
- Week 6: Review, polish, handoff

---

### **Phase 2: MVP Development (Weeks 7-16)**

**Deliverables:**
- ✅ Flutter app (iOS primary)
- ✅ Firebase backend setup
- ✅ Core features:
  - Authentication (Phone, Google, Apple)
  - Customer: Browse, Order, Track
  - Restaurant: Orders, Menu
  - Driver: Delivery workflow
  - Family Wallet
  - Group Order
- ✅ Payment gateway integration (Hyperpay)
- ✅ Google Maps integration
- ✅ Push notifications
- ✅ Bilingual support (Arabic/English)

**Milestones:**
- Week 7-8: Project setup, authentication
- Week 9-10: Customer features
- Week 11-12: Restaurant features
- Week 13-14: Driver features
- Week 15: Integration testing
- Week 16: Bug fixes & polish

---

### **Phase 3: Beta Testing (Weeks 17-20)**

**Deliverables:**
- ✅ TestFlight/Firebase App Distribution
- ✅ Closed beta (50 users):
  - 30 customers
  - 10 restaurants
  - 10 drivers
- ✅ Feedback collection & iteration
- ✅ Performance optimization
- ✅ Bug fixes

**Success Criteria:**
- < 5 critical bugs
- 90% task completion rate
- 4.0+ star feedback
- < 1 second avg API response time
- < 0.5% crash rate

---

### **Phase 4: Production Launch (Week 21)**

**Pre-Launch Checklist:**
- ✅ App Store submission (iOS)
- ✅ App Store Optimization (ASO):
  - Title, subtitle, keywords
  - Screenshots (6-8 images)
  - Preview video (30 seconds)
  - Description (Arabic & English)
- ✅ Privacy Policy & Terms of Service
- ✅ Customer support setup (email, chat)
- ✅ Marketing materials ready
- ✅ Backend monitoring setup (Sentry, Firebase)
- ✅ Load testing (simulate 1,000 concurrent users)

**Launch Day:**
- Soft launch: Riyadh only (geo-restricted)
- Monitor: Crashes, errors, API performance
- Support: 24/7 response team
- Marketing: Social media, influencers, ads

---

### **Phase 5: Post-Launch (Weeks 22-26)**

**Focus:**
- User acquisition campaigns
- Onboard restaurants (target: 50 in first month)
- Onboard drivers (target: 100 in first month)
- Daily monitoring & bug fixes
- Iterate based on user feedback
- Weekly release cycle (bug fixes)

---

## 10.2 Rollback Plan

**If critical issues arise:**
1. **Disable feature via Firebase Remote Config**
2. **Rollback to previous version (if needed)**
3. **Notify users via in-app banner**
4. **Fix issue in hotfix branch**
5. **Deploy hotfix within 24 hours**

---

# 11. Testing Strategy

## 11.1 Testing Types

### **1. Unit Testing**

**Coverage Target:** 80%+

**What to test:**
- Business logic functions
- Data models & validation
- State management logic
- Utility functions

**Tools:**
- Flutter test package
- Mockito (for mocking)
- Coverage report (lcov)

**Example:**
```dart
test('Calculate order total correctly', () {
  final order = Order(
    subtotal: 100,
    deliveryFee: 15,
    discount: 20,
    vat: 0.15,
  );
  
  expect(order.calculateTotal(), 108.75); // (100 - 20 + 15) * 1.15
});
```

---

### **2. Widget Testing**

**Coverage Target:** 60%+

**What to test:**
- UI components render correctly
- User interactions (tap, swipe, input)
- State updates reflect in UI
- Navigation flows

**Example:**
```dart
testWidgets('Add to cart button works', (WidgetTester tester) async {
  await tester.pumpWidget(MyApp());
  
  // Find button
  final addButton = find.byKey(Key('addToCartButton'));
  expect(addButton, findsOneWidget);
  
  // Tap button
  await tester.tap(addButton);
  await tester.pump();
  
  // Verify cart updated
  expect(find.text('Cart (1)'), findsOneWidget);
});
```

---

### **3. Integration Testing**

**What to test:**
- End-to-end user flows
- API integration
- Firebase integration
- Payment gateway integration
- Maps integration

**Key Flows:**
1. **Customer Journey:**
   - Register → Browse → Add to cart → Checkout → Pay → Track order
2. **Restaurant Journey:**
   - Register → Pending approval → Login → Receive order → Update status
3. **Driver Journey:**
   - Register → Pending approval → Login → Accept delivery → Navigate → Complete

**Tools:**
- Flutter integration_test package
- Firebase Test Lab

---

### **4. Performance Testing**

**What to test:**
- App launch time
- Screen transition time
- List scrolling performance (60fps)
- Memory usage
- Battery drain
- Network usage

**Tools:**
- Flutter DevTools
- Firebase Performance Monitoring
- Xcode Instruments (iOS)

---

### **5. Stress Testing**

**Scenarios:**
- 1,000 concurrent users placing orders
- 100 restaurants updating menus simultaneously
- 500 drivers going online at once
- 10,000 push notifications sent at once

**Tools:**
- Apache JMeter (API load testing)
- Firebase Test Lab (device testing)

---

### **6. User Acceptance Testing (UAT)**

**Participants:**
- 5 customers
- 2 restaurant owners
- 2 drivers
- 1 product owner

**Duration:** 2 weeks

**Test Cases:**
- Can complete registration in < 5 minutes?
- Can find and order from restaurant in < 3 minutes?
- Is checkout process clear and easy?
- Are error messages helpful?
- Is navigation intuitive?
- Any confusing UI elements?

**Success Criteria:**
- 90% task completion rate
- 4.0+ average satisfaction score
- < 3 critical usability issues

---

## 11.2 Test Cases (Sample)

### **Test Case 1: Customer Registration**

| **Field** | **Value** |
|-----------|-----------|
| **Test ID** | TC-001 |
| **Feature** | User Registration |
| **Priority** | High |
| **Precondition** | User does not have an account |
| **Steps** | 1. Open app<br>2. Tap "Get Started"<br>3. Select "Customer"<br>4. Enter phone: +966501234567<br>5. Tap "Continue"<br>6. Enter OTP: 123456<br>7. Enter name: "Test User"<br>8. Enter email: test@example.com<br>9. Tap "Complete Registration" |
| **Expected Result** | • OTP received within 10 seconds<br>• Registration completes successfully<br>• User redirected to home screen<br>• Welcome notification sent |
| **Actual Result** | (Fill after testing) |
| **Status** | ✅ Pass / ❌ Fail |
| **Notes** | |

### **Test Case 2: Place Order**

| **Field** | **Value** |
|-----------|-----------|
| **Test ID** | TC-002 |
| **Feature** | Place Order |
| **Priority** | Critical |
| **Precondition** | User logged in, restaurant open, cart has items |
| **Steps** | 1. Add items to cart<br>2. Tap "Checkout"<br>3. Select delivery address<br>4. Select payment method: Credit Card<br>5. Enter card: 4111 1111 1111 1111<br>6. Tap "Place Order" |
| **Expected Result** | • Payment processes successfully<br>• Order created in Firestore<br>• Order number displayed: ORD-XXXXX<br>• Customer & restaurant receive notifications<br>• Redirected to order tracking |
| **Actual Result** | |
| **Status** | ✅ Pass / ❌ Fail |
| **Notes** | |

### **Test Case 3: Family Wallet Payment**

| **Field** | **Value** |
|-----------|-----------|
| **Test ID** | TC-003 |
| **Feature** | Family Wallet Payment |
| **Priority** | High |
| **Precondition** | Family wallet exists, balance > order total, member within limit |
| **Steps** | 1. Proceed to checkout<br>2. Select "Family Wallet"<br>3. Select member: "Ahmed"<br>4. Review amount: 45 SAR<br>5. Tap "Pay Now" |
| **Expected Result** | • Payment deducts from family wallet<br>• Member's spent amount increases<br>• Remaining balance/limit updates<br>• Family owner receives notification<br>• Order placed successfully |
| **Actual Result** | |
| **Status** | ✅ Pass / ❌ Fail |
| **Notes** | |

---

# 12. Screen Inventory

## Complete List: ~160 Screens

### **Authentication & Onboarding (25 screens)**

1. Splash Screen
2-4. Onboarding Slides (3 screens)
5. Welcome Screen
6. Role Selection
7. Phone Number Entry
8. OTP Verification
9. Social Sign-In Options
10. Customer Profile Setup
11. Location Permission
12. Notification Permission
13. Customer Success
14-20. Restaurant Onboarding (7 screens: Info, Details, Address, Documents, Logo, Review, Pending)
21-25. Driver Onboarding (5 screens: Personal Info, National ID, License, Vehicle, Documents, Bank, Profile Photo, Review, Pending)

### **Customer - Home & Discovery (15 screens)**

26. Home Screen (Restaurant List)
27. Filters Bottom Sheet
28. Sort Options
29. Search Screen
30. Search Results
31. Restaurant Categories (Horizontal Scroll)
32. Empty State (No Restaurants)
33. Loading State (Skeleton)
34. Restaurant Detail Page
35. Menu Categories (Sticky Tabs)
36. Item Grid/List
37. Item Detail Modal
38. Customization Options (Size, Add-ons, Remove)
39. Quantity Selector
40. Cart Preview (Bottom Sheet)

### **Customer - Cart & Checkout (20 screens)**

41. Cart Screen (With Items)
42. Cart Empty State
43. Edit Item Modal
44. Remove Item Confirmation
45. Coupon Entry Modal
46. Coupon Applied Success
47. Minimum Order Warning
48. Checkout Screen
49. Address Selection
50. Add New Address (Map Picker)
51. Edit Address
52. Delete Address Confirmation
53. Schedule Order Picker (Date + Time)
54. Payment Method Selection
55. Family Wallet Selection (Member Chooser)
56. Credit Card Form (Mock)
57. Apple Pay Sheet (Mock)
58. Application Wallet Balance
59. Top-Up Wallet
60. Processing Payment (Loading)
61. Payment Success
62. Payment Failed
63. Order Confirmation

### **Customer - Family Wallet (12 screens)**

64. Family Wallet Dashboard
65. Create Family Wallet (Step 1: Info)
66. Create Family Wallet (Step 2: Add Members)
67. Create Family Wallet (Step 3: Confirmation)
68. Add Member Screen
69. Invitation Sent Confirmation
70. Invitation Notification (Push)
71. Accept/Reject Invitation Modal
72. Member List Management
73. Edit Member (Spending Limit)
74. Remove Member Confirmation
75. Transaction History
76. Top-Up Family Wallet

### **Customer - Group Order (10 screens)**

77. Start Group Order (Setup)
78. Share Invitation (QR + Link + Options)
79. Join Group Order (Invitation Screen)
80. Group Cart (By Person View)
81. Group Cart (All Items View)
82. Participant List
83. Split Bill Options
84. Payment Status Tracker
85. Individual Payment Screen
86. Group Order Confirmation

### **Customer - Orders & Tracking (12 screens)**

87. Order Tracking Screen
88. Live Map View (Mock)
89. Driver Profile Card
90. Cancel Order Confirmation
91. Order Cancelled Screen
92. Order History List
93. Order Details
94. Reorder Confirmation
95. Rating Modal (Restaurant + Driver)
96. Review Submitted Success
97. Report Issue
98. Empty Order History

### **Customer - Profile & Settings (10 screens)**

99. Profile Screen
100. Edit Profile
101. Saved Addresses List
102. Payment Methods List
103. Add Payment Method
104. Application Wallet
105. Settings Screen
106. Language Switcher
107. Notification Settings
108. Help & Support

### **Restaurant - Dashboard & Orders (15 screens)**

109. Restaurant Login
110. Restaurant Dashboard
111. Incoming Order Notification
112. Order Details
113. Accept Order Modal (Prep Time Input)
114. Reject Order Modal (Reason)
115. Update Order Status Buttons
116. Order Management List (Filters: New, In Progress, Completed)
117. Active Orders
118. Completed Orders
119. Order Detail View (Read-only)
120. Stats & Analytics
121. Notifications List
122. Restaurant Profile
123. Edit Restaurant Info

### **Restaurant - Menu Management (12 screens)**

124. Menu Management List (Categories + Items)
125. Add New Category
126. Edit Category
127. Delete Category Confirmation
128. Add New Item Form
129. Edit Item Form
130. Delete Item Confirmation
131. Image Upload Interface
132. Item Availability Toggle
133. Reorder Items (Drag & Drop)
134. Menu Preview (Customer View)
135. Bulk Upload (Future - optional)

### **Restaurant - Promotions (8 screens)**

136. Promotions List
137. Create Promotion Form (Step 1: Basic Info)
138. Create Promotion Form (Step 2: Conditions)
139. Create Promotion Form (Step 3: Schedule)
140. Promotion Preview
141. Edit Promotion
142. Delete Promotion Confirmation
143. Activate/Deactivate Promotion

### **Restaurant - Settings (5 screens)**

144. Operating Hours Manager
145. Time Picker (Start/End)
146. Holiday/Closed Days
147. Restaurant Settings
148. Help & Support (Restaurant)

### **Driver - Dashboard & Deliveries (20 screens)**

149. Driver Login
150. Driver Dashboard
151. Toggle Availability (Available/Unavailable)
152. Delivery Request Notification
153. Request Details
154. Accept Request Confirmation
155. Reject Request
156. Active Delivery Screen
157. Order Details (Items, Customer Info)
158. Navigate to Restaurant (Confirmation)
159. Update Status: Heading to Restaurant
160. Update Status: Arrived at Restaurant
161. Pickup Confirmation
162. Navigate to Customer (Confirmation)
163. Customer Location on Map
164. Update Status: On the Way
165. Delivery Confirmation Modal
166. Delivery Completed
167. Delivery History List
168. Delivery Details (Past)
169. Earnings Summary

### **Driver - Profile (5 screens)**

170. Driver Profile
171. Edit Driver Profile
172. Vehicle Info
173. Driver Documents
174. Driver Settings

### **Shared Screens (10 screens)**

175. Notification Center
176. Notification Detail
177. Global Search
178. Search Results (Mixed)
179. Language Switcher Modal
180. Loading State (Generic)
181. Error State (Generic)
182. Success Toast
183. Confirmation Dialog (Generic)
184. Chat Interface (Customer ↔ Driver)

### **Optional Error Screens (5 screens)**

185. Restaurant Closed
186. Order Failed
187. No Internet Connection
188. Item Unavailable
189. Location Access Denied

---

**Total Screens: ~189** (Core MVP: 160, Optional: 29)

---

# 13. User Journeys (Detailed)

## Journey 1: First-Time Customer Orders Food

**Actor:** Sarah (New Customer)  
**Goal:** Register, find a restaurant, order food, track delivery  
**Duration:** ~10 minutes

| **Step** | **Screen** | **Action** | **System Response** |
|----------|-----------|-----------|---------------------|
| 1 | Splash | App loads | Shows logo animation (2s) |
| 2 | Onboarding 1 | Swipe right | Next slide |
| 3 | Onboarding 2 | Swipe right | Next slide |
| 4 | Onboarding 3 | Tap "Get Started" | Navigate to Welcome |
| 5 | Welcome | Tap "Get Started" | Navigate to Role Selection |
| 6 | Role Selection | Tap "Customer" card | Navigate to Phone Entry |
| 7 | Phone Entry | Enter +966501234567 → Tap "Continue" | Send OTP via SMS |
| 8 | OTP Verification | Enter 123456 → Tap "Verify" | Verify OTP, navigate to Profile Setup |
| 9 | Profile Setup | Enter name "Sarah", email → Tap "Continue" | Save profile |
| 10 | Location Permission | Tap "Allow" | Grant location access |
| 11 | Notification Permission | Tap "Allow" | Grant notification access |
| 12 | Success | Tap "Start Ordering" | Navigate to Home |
| 13 | Home | See 10 restaurants listed | Load restaurants from Firestore |
| 14 | Home | Tap "Mama's Kitchen" | Navigate to Restaurant Detail |
| 15 | Restaurant Detail | Browse menu, tap "Chicken Kabsa" | Open Item Detail Modal |
| 16 | Item Detail | Select Size "Large", add "Extra Rice", Quantity 1 → Tap "Add to Cart" | Add to cart, show toast "Item added!" |
| 17 | Restaurant Detail | Tap Cart icon (badge shows "1") | Open Cart Preview |
| 18 | Cart | Review item → Tap "Checkout" | Navigate to Checkout |
| 19 | Checkout | Tap "Add Delivery Address" | Navigate to Add Address |
| 20 | Add Address | Drag map pin, enter details → Tap "Save" | Save address, return to Checkout |
| 21 | Checkout | Select payment method "Credit Card" | Show Card Form |
| 22 | Card Form | Enter card details (mock) → Tap "Pay Now" | Process payment (mock) |
| 23 | Processing | Show loading spinner "Placing order..." | Create order in Firestore |
| 24 | Success | Show "Order Placed! ORD-12345" | Clear cart, send notifications |
| 25 | Order Tracking | Watch status: "Accepted" → "Preparing" | Real-time Firestore updates |
| 26 | Order Tracking | Status: "Driver Assigned" - See driver info | Driver assigned by Cloud Function |
| 27 | Order Tracking | Status: "On the Way" - See live map | Driver location updates |
| 28 | Order Tracking | Status: "Delivered" | Show rating prompt |
| 29 | Rating | Rate restaurant 5 stars, driver 5 stars → Tap "Submit" | Save ratings |
| 30 | Home | Navigate back to home | Order complete! |

**Unique Features Showcased:** None in first order - basic flow

---

## Journey 2: Family Wallet Creation & Usage

**Actor:** Sarah (Customer) + Ahmed (Son)  
**Goal:** Create family wallet, invite son, son uses wallet to order

| **Step** | **Actor** | **Screen** | **Action** | **Result** |
|----------|----------|-----------|-----------|------------|
| 1 | Sarah | Profile | Tap "Wallet" | Navigate to Wallet Dashboard |
| 2 | Sarah | Wallet Dashboard | Tap "Create Family Wallet" | Navigate to Create Flow |
| 3 | Sarah | Create Step 1 | Enter "Al-Otaibi Family", Balance 1000 SAR → Next | Save info |
| 4 | Sarah | Create Step 2 | Tap "Add Member" | Open Add Member form |
| 5 | Sarah | Add Member | Enter Ahmed's phone +966509876543, Limit 200 SAR → Send | Send invitation via FCM + SMS |
| 6 | **Ahmed** | **Push Notification** | **Receive "Sarah invited you..."** | **Open app** |
| 7 | **Ahmed** | **Invitation Modal** | **See: "Join Al-Otaibi Family Wallet? Limit: 200 SAR"** | **Show Accept/Decline** |
| 8 | **Ahmed** | **Invitation Modal** | **Tap "Accept"** | **Update member status to "Active"** |
| 9 | Sarah | Member List | See "Ahmed - Active" | Notification: "Ahmed joined!" |
| 10 | **Ahmed** | **Home** | **Browse restaurants, add items to cart** | **Cart total: 45 SAR** |
| 11 | **Ahmed** | **Checkout** | **Select payment: "Family Wallet"** | **Show: "Al-Otaibi Family - 1000 SAR available"** |
| 12 | **Ahmed** | **Family Wallet Payment** | **Auto-selected "Ahmed (Self) - 155 SAR remaining"** | **Show payment details** |
| 13 | **Ahmed** | **Checkout** | **Tap "Place Order"** | **Deduct 45 SAR from wallet, update Ahmed's spent: 45 SAR** |
| 14 | Sarah | Transaction History | See "Ahmed spent 45 SAR" notification | Show transaction |
| 15 | Sarah | Member List | See Ahmed: "Spent 45, Remaining 155" | Updated in real-time |

**Unique Features Showcased:** ⭐ Family Wallet, Invitation system, Spending limits, Transaction visibility

---

## Journey 3: Group Order with Bill Split

**Actor:** Sarah (Host) + 3 Colleagues  
**Goal:** Order lunch for office, split bill

| **Step** | **Actor** | **Screen** | **Action** | **Result** |
|----------|----------|-----------|-----------|------------|
| 1 | Sarah | Home | Tap "Pizza Paradise" | Navigate to Restaurant |
| 2 | Sarah | Restaurant | Tap "Start Group Order" | Navigate to Setup |
| 3 | Sarah | Group Setup | Enter "Office Lunch", Deadline 20 min, Address "Office" → Create | Generate code "ABC123", link |
| 4 | Sarah | Share Link | Tap "Share via WhatsApp" | Open WhatsApp with message + link |
| 5 | Sarah | WhatsApp | Send to "Office Lunch Group" | 3 colleagues receive link |
| 6 | **Colleague 1** | **WhatsApp** | **Tap link** | **Open app, show Join screen** |
| 7 | **Colleague 1** | **Join Screen** | **Tap "Join Order"** | **Added to participants** |
| 8 | **Colleague 1** | **Restaurant Menu** | **Add "Pepperoni Pizza" → Add to Cart** | **Added to group cart** |
| 9 | Sarah | Group Cart | See real-time: "Colleague 1 added Pepperoni Pizza" | Toast notification |
| 10 | **Colleague 2** | **Join + Add** | **Add "Margherita Pizza"** | **Group cart updates** |
| 11 | **Colleague 3** | **Join + Add** | **Add "Wings"** | **Group cart updates** |
| 12 | Sarah | Group Cart | See all 4 participants with items | Total: 147 SAR |
| 13 | Sarah | Group Cart | Deadline reached, tap "Proceed to Payment" | Navigate to Split Bill |
| 14 | Sarah | Split Bill | Select "Pay for Own Items Only" | Calculate: Sarah 35, C1 40, C2 38, C3 34 (+ delivery split) |
| 15 | All | Payment Status | See: Sarah ✅ Paid, Others ⏳ Pending | Show payment tracker |
| 16 | **Colleague 1** | **Payment Notification** | **Receive "Pay your share: 45 SAR"** | **Open payment** |
| 17 | **Colleague 1** | **Payment** | **Pay via Credit Card** | **Status ✅ Paid** |
| 18 | **Colleagues 2 & 3** | **Payment** | **Pay their shares** | **All ✅ Paid** |
| 19 | Sarah | Payment Status | See "All payments received!" | Show "Confirm Order" button |
| 20 | Sarah | Confirmation | Tap "Place Order" | Single order created, all notified |
| 21 | All | Order Tracking | Track shared order | Same order ID for all |

**Unique Features Showcased:** ⭐ Group Order, Real-time collaboration, Bill splitting, Shared tracking

---

## Journey 4: Restaurant Manages Menu & Accepts Order

**Actor:** Ahmed (Restaurant Owner - Mama's Kitchen)

| **Step** | **Screen** | **Action** | **Result** |
|----------|-----------|-----------|------------|
| 1 | Login | Enter phone + OTP | Login as Restaurant |
| 2 | Dashboard | See: "Today: 15 orders, 850 SAR" | Show stats |
| 3 | Dashboard | Tap "Manage Menu" | Navigate to Menu Management |
| 4 | Menu List | See all items, "Kabsa" shows "Available" | Current menu |
| 5 | Menu List | Toggle "Kabsa" to "Unavailable" | Update Firestore, customers see "Out of Stock" |
| 6 | Menu List | Tap "+" Add Item | Navigate to Add Item |
| 7 | Add Item | Enter: Name "Grilled Chicken", Price 35 SAR, Upload image, Category "Mains" → Save | Item added, visible to customers |
| 8 | Dashboard | Tap "Promotions" | Navigate to Promotions |
| 9 | Promotions | Tap "Create Promotion" | Navigate to Create |
| 10 | Create Promotion | Enter: "20% Off Orders > 100 SAR", Valid today 6-8 PM → Activate | Promotion live at 6 PM |
| 11 | Dashboard | **Receive new order notification** (sound + banner) | Order ORD-12345 from Sarah |
| 12 | Order Details | Review: 2 items, 81 SAR, Address shown | Order waiting |
| 13 | Order Details | Tap "Accept", enter prep time "25 min" | Update status to "Accepted", notify customer |
| 14 | Order Management | See order in "In Progress" | Status: Preparing |
| 15 | Order Management | Tap order → "Mark as Ready" | Update status to "Ready", trigger driver assignment |
| 16 | Order Management | See "Driver Assigned: Khalid" | Cloud Function assigned driver |
| 17 | Order Management | Order moves to "Completed" after delivery | Order lifecycle complete |

**Unique Features Showcased:** Real-time menu updates, Promotion scheduling, Order management workflow

---

## Journey 5: Driver Completes Delivery

**Actor:** Khalid (Driver)

| **Step** | **Screen** | **Action** | **Result** |
|----------|-----------|-----------|------------|
| 1 | Login | Login as Driver | Dashboard |
| 2 | Dashboard | Toggle status to "Available" | Set isAvailable = true |
| 3 | Dashboard | Wait... | Cloud Function queries nearby available drivers |
| 4 | **Notification** | **Receive delivery request** (sound + vibration) | Request from Pizza Paradise, 3.2km, 15 SAR |
| 5 | Request Details | See: Restaurant, customer location, items, pay | 30-second countdown |
| 6 | Request Details | Tap "Accept Delivery" within 20s | Assigned to order, customer notified |
| 7 | Active Delivery | See order details, restaurant address | Order info |
| 8 | Active Delivery | Tap "Navigate to Restaurant" | Open Google Maps with restaurant location |
| 9 | Google Maps | Navigate to restaurant | Driving... |
| 10 | Active Delivery | Arrive at restaurant, tap "Arrived at Restaurant" | Update status, notify customer |
| 11 | Active Delivery | Pick up order, tap "Picked Up Order" | Update status |
| 12 | Active Delivery | Tap "Navigate to Customer" | Open Google Maps with customer address |
| 13 | Google Maps | Navigate to customer | Driving... |
| 14 | Active Delivery | Customer sent message: "Please call when arriving" | Chat notification |
| 15 | Chat | Reply: "Will do" | Send message |
| 16 | Active Delivery | Near customer, tap "Call Customer" | Open phone dialer |
| 17 | Phone | Call customer: "I'm outside" | Customer comes down |
| 18 | Active Delivery | Hand over order, tap "Mark as Delivered" | Confirmation modal |
| 19 | Delivery Confirmation | Confirm delivery | Update status to "Delivered", order complete |
| 20 | Dashboard | See earnings updated: "+15 SAR" | Earnings tracker updated |
| 21 | **Rating** | **Customer rates Khalid 5 stars** | **Driver rating updated** |

**Unique Features Showcased:** Driver workflow, Navigation integration, Chat/Call, Real-time status updates

---

# 14. Component Library

## 14.1 Core Components

### **Buttons**

| **Component** | **Variants** | **Usage** | **Example** |
|--------------|------------|-----------|-------------|
| **Primary Button** | Default, Loading, Disabled | Main CTAs | "Place Order", "Add to Cart" |
| **Secondary Button** | Default, Loading, Disabled | Secondary actions | "Cancel", "Back" |
| **Outline Button** | Default, Disabled | Tertiary actions | "View Menu", "Learn More" |
| **Text Button** | Default, Disabled | Low-emphasis actions | "Skip", "Not now" |
| **Icon Button** | Small, Medium, Large | Icon-only actions | Search, Filter, Share |
| **Floating Action Button (FAB)** | Default, Mini, Extended | Primary screen actions | "+" Add item |

### **Input Fields**

| **Component** | **Types** | **States** | **Usage** |
|--------------|----------|-----------|-----------|
| **Text Field** | Single-line, Multi-line | Default, Focus, Error, Disabled | Name, Email, Address |
| **Number Field** | Integer, Decimal | Default, Focus, Error | Price, Quantity, Phone |
| **Password Field** | With show/hide toggle | Default, Focus, Error | Password (if email/password auth) |
| **Search Bar** | With clear button | Default, Focus, Results | Search restaurants, items |
| **OTP Input** | 6-digit code | Default, Focus, Error | OTP verification |
| **Date Picker** | Calendar view | Default, Selected | Schedule order date |
| **Time Picker** | 12/24 hour | Default, Selected | Schedule order time |

### **Selection Controls**

| **Component** | **Usage** | **Example** |
|--------------|-----------|-------------|
| **Checkbox** | Multi-select | Add-ons, Filters |
| **Radio Button** | Single-select | Payment method, Size |
| **Toggle Switch** | On/Off | Availability, Notifications |
| **Dropdown** | Select from list | Cuisine type, Sort by |
| **Slider** | Range selection | Price range, Distance |
| **Segmented Control** | 2-5 options | View modes, Tabs |

### **Cards**

| **Component** | **Variants** | **Usage** |
|--------------|------------|-----------|
| **Restaurant Card** | Horizontal, Vertical | Restaurant list |
| **Item Card** | Image + Details | Menu items |
| **Order Card** | Status + Details | Order history, Active orders |
| **Notification Card** | Icon + Text | Notification center |
| **Payment Method Card** | Icon + Last 4 digits | Payment selection |

### **Lists**

| **Component** | **Variants** | **Usage** |
|--------------|------------|-----------|
| **Simple List** | Text only | Settings options |
| **Two-line List** | Title + Subtitle | Addresses, Orders |
| **Three-line List** | Title + Subtitle + Metadata | Order details |
| **Avatar List** | Image + Text | Participants, Members |
| **Expandable List** | Collapsible sections | FAQ, Categories |

### **Navigation**

| **Component** | **Variants** | **Usage** |
|--------------|------------|-----------|
| **Top App Bar** | Default, Large Title, Search | Screen header |
| **Bottom Navigation** | 2-5 tabs with icons + labels | Main navigation (Customer, Restaurant, Driver) |
| **Tab Bar** | Scrollable, Fixed | Menu categories, Order filters |
| **Drawer** | Side menu (optional - future) | Settings, Profile |

### **Modals & Dialogs**

| **Component** | **Variants** | **Usage** |
|--------------|------------|-----------|
| **Bottom Sheet** | Half-screen, Full-screen, Scrollable | Filters, Item details, Cart preview |
| **Alert Dialog** | Title + Message + Actions | Confirmations, Errors |
| **Action Sheet** | List of actions | Share options, Report issues |
| **Full Screen Modal** | With close button | Add address, Payment form |

### **Feedback**

| **Component** | **Variants** | **Usage** |
|--------------|------------|-----------|
| **Toast** | Success, Error, Info, Warning | "Item added", "Payment failed" |
| **Snackbar** | With action button | "Item removed" (Undo button) |
| **Progress Bar** | Linear, Circular | Loading states |
| **Skeleton** | Card, List, Text | Loading placeholder |
| **Badge** | Number, Dot | Notification count, Cart count |
| **Chip** | Default, Selected, Removable | Filters, Tags |

### **Media**

| **Component** | **Variants** | **Usage** |
|--------------|------------|-----------|
| **Avatar** | Small (32px), Medium (48px), Large (80px) | User profile, Driver info |
| **Image** | Square, Rectangle (16:9), Circle | Restaurant cover, Item image, Logo |
| **Icon** | 16px, 24px, 32px, 48px | Throughout UI |
| **Illustration** | Empty state, Error state, Success | Placeholder graphics |

---

## 14.2 iOS HIG Specific Components

Following **Apple Human Interface Guidelines:**

- **Navigation Bar:** Large title on home screens, standard title on detail screens
- **Tab Bar:** 5 items max, icons + labels, active state highlighted
- **Segmented Control:** 2-5 segments, pill shape
- **Action Sheet:** Native iOS style for destructive actions
- **Date/Time Picker:** Native iOS wheels
- **Toggle Switch:** iOS native style (green when on)
- **Activity Indicator:** iOS native spinner
- **Page Control:** Dots for onboarding/carousels
- **Safe Area:** Respect notch, home indicator, rounded corners

---

## 14.3 Design Tokens

### **Colors**

**Primary Palette:**
```
Primary:     #FF6B35  (Orange - food/appetite stimulation)
Primary Dark: #E5522E
Primary Light: #FF8F66
```

**Secondary Palette:**
```
Secondary:    #4ECDC4  (Teal - freshness)
Secondary Dark: #3EB5AC
Secondary Light: #7ED9D2
```

**Neutrals:**
```
Black:      #1A1A1A
Dark Gray:  #4A4A4A
Gray:       #9E9E9E
Light Gray: #E0E0E0
White:      #FFFFFF
```

**Semantic Colors:**
```
Success:  #4CAF50  (Green)
Error:    #F44336  (Red)
Warning:  #FF9800  (Amber)
Info:     #2196F3  (Blue)
```

**Status Colors:**
```
Open (Restaurant): #4CAF50
Closed:           #F44336
Preparing:        #FF9800
On the Way:       #2196F3
Delivered:        #4CAF50
```

### **Typography**

**Font Family:** SF Pro (iOS) / System Default

**Font Sizes:**
```
Headline 1:  34px / Bold
Headline 2:  28px / Bold
Headline 3:  22px / Semibold
Body Large:  17px / Regular
Body:        15px / Regular
Body Small:  13px / Regular
Caption:     12px / Regular
Button:      15px / Semibold
```

**Line Height:** 1.4-1.6 (for readability)

### **Spacing**

**8px Grid System:**
```
xs:   4px
sm:   8px
md:   16px
lg:   24px
xl:   32px
xxl:  48px
```

### **Border Radius**

```
Small:   4px  (Buttons, Chips)
Medium:  8px  (Cards, Inputs)
Large:   16px (Modals, Bottom Sheets)
Circle:  50% (Avatars, FAB)
```

### **Shadows**

```
Elevation 1:  0 1px 3px rgba(0,0,0,0.12)
Elevation 2:  0 2px 6px rgba(0,0,0,0.16)
Elevation 3:  0 4px 12px rgba(0,0,0,0.20)
Elevation 4:  0 8px 24px rgba(0,0,0,0.24)
```

---

# 15. Animations & Interactions

## 15.1 Micro-interactions

| **Element** | **Animation** | **Trigger** | **Duration** | **Easing** |
|------------|---------------|-------------|--------------|-----------|
| **Button Press** | Scale 0.95x + opacity 0.8 | Tap down | 100ms | Ease-out |
| **Button Release** | Scale 1.0x + opacity 1.0 | Tap up | 100ms | Ease-in |
| **Add to Cart** | Item flies to cart icon | Tap "Add to Cart" | 400ms | Ease-in-out |
| **Success Checkmark** | Scale from 0 → 1.2 → 1.0 + rotate 360° | Payment success | 500ms | Bounce |
| **Loading Spinner** | Rotate 360° continuously | Any loading state | Infinite | Linear |
| **Pull to Refresh** | Spinner appears, rotates | Pull down gesture | 300ms | Ease-out |
| **Heart (Favorite)** | Scale 1.3x + fill color | Tap heart icon | 300ms | Bounce |
| **Star Rating** | Fill left-to-right + scale | Tap star | 150ms/star | Ease-in |
| **Toast Notification** | Slide up from bottom | Any confirmation | 300ms | Ease-out |
| **Badge Count Update** | Scale 1.2x → 1.0 | Count changes | 200ms | Bounce |
| **Swipe Delete** | Item slides left, reveal delete button | Swipe left | 200ms | Ease-out |
| **Tab Switch** | Cross-fade + slight scale | Tap tab | 200ms | Ease-in-out |

---

## 15.2 Screen Transitions

| **Transition Type** | **Use Case** | **Animation** | **Duration** |
|--------------------|--------------|---------------|--------------|
| **Push (Forward)** | Navigate to detail screen | Slide from right (iOS) | 300ms |
| **Pop (Back)** | Return to previous screen | Slide from left | 300ms |
| **Modal (Bottom Sheet)** | Filters, Item details | Slide up from bottom | 350ms |
| **Modal (Full Screen)** | Add address, Payment | Slide up + fade background | 400ms |
| **Tab Switch** | Bottom navigation | Cross-fade + scale | 250ms |
| **Fade** | Loading → Content | Cross-fade | 200ms |
| **Hero Transition** | Restaurant card → Detail | Shared element transition | 400ms |

---

## 15.3 Gestures

| **Gesture** | **Use Case** | **Action** | **Feedback** |
|------------|--------------|------------|--------------|
| **Tap** | All clickable elements | Navigate/Execute action | Ripple effect (Android) / Highlight (iOS) |
| **Long Press** | Restaurant card | Show quick preview modal | Haptic feedback + modal |
| **Swipe Right** | Order card (driver) | Mark as delivered | Item slides + success icon |
| **Swipe Left** | Cart item, Address | Reveal delete button | Item slides + red background |
| **Pull Down** | Lists (Home, History) | Refresh content | Spinner + reload |
| **Pinch** | Map (mock) | Zoom in/out | Map scales |
| **Drag** | Reorder menu items | Change order | Item lifts + shadow |
| **Double Tap** | Item image | Zoom in | Image scales |

---

## 15.4 Loading States

### **Skeleton Screens (Preferred):**
- Restaurant list: Show 3 skeleton cards while loading
- Menu: Show skeleton grid (2 columns)
- Order tracking: Show skeleton timeline

### **Spinners:**
- Payment processing: Centered spinner + "Processing..."
- API calls: Small spinner next to button
- Image loading: Placeholder → Spinner → Image

### **Progress Bars:**
- File upload: Linear progress bar below file name
- Order status: Progress timeline (visual step indicator)

---

## 15.5 Empty States

| **Screen** | **Illustration** | **Message** | **CTA** |
|-----------|-----------------|------------|---------|
| Empty Cart | Shopping bag icon | "Your cart is empty" | "Browse Restaurants" |
| No Orders | Calendar icon | "No orders yet" | "Start Ordering" |
| No Favorites | Heart icon | "No favorites saved" | "Discover Restaurants" |
| No Results (Search) | Magnifying glass | "No results found" | "Clear Search" |
| No Internet | Cloud with X | "No internet connection" | "Retry" |

---

## 15.6 Success States

| **Action** | **Animation** | **Message** |
|-----------|---------------|------------|
| Order Placed | Green checkmark scale + confetti | "Order placed successfully!" |
| Payment Success | Green checkmark + ping | "Payment successful!" |
| Item Added to Cart | Item flies to cart | "Added to cart" (toast) |
| Rating Submitted | Stars fill + checkmark | "Thanks for your feedback!" |
| Document Uploaded | Progress bar → checkmark | "Document uploaded" |

---

# 16. Data Requirements (Mockup Content)

## 16.1 Restaurants (10 Placeholders)

| **#** | **Name** | **Cuisine** | **Logo** | **Rating** | **Delivery Time** | **Fee** | **Minimum** |
|-------|----------|-------------|----------|-----------|-------------------|---------|-------------|
| 1 | Mama's Kitchen | Traditional Saudi | 🍲 | 4.8 ⭐ | 25-35 min | 15 SAR | 30 SAR |
| 2 | Pizza Paradise | Italian | 🍕 | 4.5 ⭐ | 30-40 min | 10 SAR | 25 SAR |
| 3 | Sushi Master | Japanese | 🍣 | 4.9 ⭐ | 35-45 min | 20 SAR | 50 SAR |
| 4 | Burger Bros | Fast Food | 🍔 | 4.3 ⭐ | 20-30 min | 8 SAR | 20 SAR |
| 5 | Curry House | Indian | 🍛 | 4.6 ⭐ | 30-40 min | 12 SAR | 30 SAR |
| 6 | Taco Fiesta | Mexican | 🌮 | 4.4 ⭐ | 25-35 min | 15 SAR | 25 SAR |
| 7 | Noodle Bar | Asian Fusion | 🍜 | 4.7 ⭐ | 30-40 min | 18 SAR | 35 SAR |
| 8 | Grill Station | BBQ | 🥩 | 4.6 ⭐ | 35-45 min | 12 SAR | 40 SAR |
| 9 | Sweet Treats | Desserts | 🍰 | 4.9 ⭐ | 20-30 min | 5 SAR | 15 SAR |
| 10 | Healthy Bites | Healthy | 🥗 | 4.5 ⭐ | 25-35 min | 10 SAR | 25 SAR |

---

## 16.2 Sample Menu Items

### **Mama's Kitchen (Traditional Saudi):**

**Appetizers:**
1. Hummus with Bread - 12 SAR
2. Arabic Salad - 10 SAR
3. Sambousek (Meat) - 15 SAR

**Main Courses:**
4. Chicken Kabsa - 35 SAR
5. Lamb Mandi - 45 SAR
6. Grilled Chicken - 30 SAR
7. Meat Machboos - 40 SAR
8. Stuffed Vine Leaves - 25 SAR

**Desserts:**
9. Kunafa - 15 SAR
10. Basbousa - 12 SAR

**Drinks:**
11. Fresh Orange Juice - 8 SAR
12. Mint Lemonade - 7 SAR
13. Saudi Coffee - 5 SAR

---

### **Pizza Paradise (Italian):**

**Pizza (Small/Medium/Large):**
1. Margherita - 25/35/45 SAR
2. Pepperoni - 30/40/50 SAR
3. BBQ Chicken - 35/45/55 SAR
4. Veggie Supreme - 28/38/48 SAR

**Sides:**
5. Garlic Bread - 12 SAR
6. Mozzarella Sticks - 18 SAR
7. Caesar Salad - 15 SAR

**Desserts:**
8. Tiramisu - 20 SAR
9. Chocolate Lava Cake - 18 SAR

**Drinks:**
10. Soft Drinks - 5 SAR
11. Juice - 8 SAR

---

## 16.3 User Profiles (Mockup)

### **Customers:**

| **Name** | **Phone** | **Email** | **Location** |
|----------|-----------|-----------|--------------|
| Sarah Al-Otaibi | +966501234567 | sarah@example.com | Al Olaya, Riyadh |
| Ahmed Al-Malki | +966509876543 | ahmed@example.com | Al Malqa, Riyadh |
| Fatima Al-Ghamdi | +966507777777 | fatima@example.com | Al Yasmin, Riyadh |

### **Restaurants:**

| **Name** | **Owner** | **Phone** | **Address** |
|----------|-----------|-----------|-------------|
| Mama's Kitchen | Ahmed Al-Malki | +966501111111 | Al Malqa, Building 15 |
| Pizza Paradise | Omar Al-Saud | +966502222222 | Al Olaya, King Fahd Road |

### **Drivers:**

| **Name** | **Phone** | **Vehicle** | **Rating** |
|----------|-----------|------------|-----------|
| Khalid Al-Harthi | +966508888888 | Motorcycle - Honda | 4.9 ⭐ |
| Nasser Al-Otaibi | +966509999999 | Car - Toyota Corolla | 4.7 ⭐ |

---

## 16.4 Sample Orders

### **Order 1:**

```
Order ID: ORD-12345
Customer: Sarah Al-Otaibi
Restaurant: Mama's Kitchen
Items:
  - Chicken Kabsa (Large, Extra Rice) x1 = 40 SAR
  - Arabic Salad x1 = 10 SAR
  - Fresh Orange Juice x2 = 16 SAR
Subtotal: 66 SAR
Delivery Fee: 15 SAR
VAT (15%): 12.15 SAR
Total: 93.15 SAR
Payment: Family Wallet
Status: Delivered
Driver: Khalid
Rating: 5⭐
```

### **Order 2 (Group Order):**

```
Group Order ID: GRP-456
Name: Office Lunch
Host: Sarah Al-Otaibi
Restaurant: Pizza Paradise
Participants:
  - Sarah: Margherita (Medium) x1 = 35 SAR
  - Ahmed: Pepperoni (Large) x1 = 50 SAR
  - Fatima: Veggie Supreme (Medium) x1 = 38 SAR
  - Khalid: BBQ Chicken (Large) x1 = 55 SAR
Subtotal: 178 SAR
Delivery Fee: 10 SAR (split: 2.50 each)
VAT (15%): 28.20 SAR (split proportionally)
Total: 216.20 SAR
Split Method: Pay Own Items
Status: Delivered
```

---

# 17. Prototype Specifications

## 17.1 Figma Setup

| **Aspect** | **Specification** |
|-----------|------------------|
| **Device Frame** | iPhone 14 Pro (393 x 852 px) |
| **Color Mode** | Light mode (primary), Dark mode (optional - future) |
| **Starting Frame** | Splash Screen |
| **Prototype Type** | Interactive, High-Fidelity |
| **Flow Type** | Multiple flows (6 main user journeys) |
| **Transitions** | Smart Animate (primary), Instant (secondary) |
| **Overlay Settings** | Manual close, Click outside to close (for modals) |

---

## 17.2 Interactivity Checklist

**Every screen must have:**
- ✅ **Clickable elements:** All buttons, links, cards interactive
- ✅ **Back navigation:** Back button/gesture where applicable
- ✅ **Tab navigation:** Bottom tabs functional
- ✅ **Form inputs:** Show focus states
- ✅ **Loading states:** Spinners/skeletons where applicable
- ✅ **Success/Error feedback:** Toasts, checkmarks, error dialogs
- ✅ **Empty states:** For lists with no data
- ✅ **Overflow:** Scroll for long content

---

## 17.3 Annotation Guidelines

**For Developers:**
- Add notes for:
  - API endpoints (e.g., "Call POST /orders/create")
  - Validation rules (e.g., "Phone: +966 format, 10 digits")
  - Conditional logic (e.g., "Show if balance < total")
  - Error handling (e.g., "If payment fails, show error dialog")
  - Real-time updates (e.g., "Firestore listener on orders/{orderId}")
  - Navigation (e.g., "Push to OrderTracking screen")

---

## 17.4 Prototype Handoff

**Deliverables:**
1. **Figma Link:** Shareable prototype link with view access
2. **Design System:** Separate Figma file with components, styles
3. **Assets Export:**
   - Icons (SVG, PDF)
   - Images (PNG @1x, @2x, @3x for iOS)
   - Logos (SVG, PNG)
4. **Documentation:**
   - This PRD (PDF + Markdown)
   - User flow diagrams (exported from Figma)
   - Component library documentation
5. **Developer Notes:**
   - Zeplin/Figma inspect for specs
   - Animation specs (timing, easing)
   - Responsive breakpoints (if web version)

---

# 18. Success Criteria

## 18.1 Prototype Acceptance Criteria

**The prototype is considered complete when:**

### **Functional:**
- ✅ All 160+ screens designed and polished
- ✅ All 6 user journeys are fully interactive
- ✅ All 30 use cases are visually represented
- ✅ Unique features (Family Wallet, Group Order) are clearly showcased
- ✅ All buttons, links, and interactive elements are clickable
- ✅ Navigation flows correctly (back, tabs, modals)
- ✅ Form inputs show appropriate states (default, focus, error)
- ✅ Loading states are present where needed
- ✅ Success and error states are designed
- ✅ Empty states are present for lists

### **Design Quality:**
- ✅ Consistent with iOS HIG
- ✅ Design system documented and reusable
- ✅ Typography hierarchy clear
- ✅ Color palette applied consistently
- ✅ Spacing follows 8px grid
- ✅ Icons consistent (same style/size)
- ✅ Images use appropriate aspect ratios
- ✅ Accessibility considerations (color contrast WCAG AA)

### **Bilingual:**
- ✅ English version complete (primary for prototype)
- ✅ Arabic version screens (representative samples - 20-30 key screens)
- ✅ RTL layout demonstrated
- ✅ Language switcher functional

### **Annotations:**
- ✅ Developer notes added to complex interactions
- ✅ API endpoints specified
- ✅ Validation rules documented
- ✅ Conditional logic explained

---

## 18.2 User Testing Goals (Post-Prototype)

**Validate that users can:**
- ✅ Complete customer registration in < 5 minutes
- ✅ Find and order from a restaurant in < 3 minutes
- ✅ Understand checkout process clearly
- ✅ Comprehend Family Wallet concept immediately
- ✅ Complete Group Order flow intuitively
- ✅ Navigate restaurant management easily
- ✅ Understand driver workflow clearly

**Usability Metrics:**
- Task success rate: 90%+
- Average task time: Within expected range
- User satisfaction: 4.0+ / 5.0
- System Usability Scale (SUS): 70+ (Good)

---

## 18.3 MVP Success Metrics (Post-Launch)

| **Metric** | **Target** | **Timeline** |
|-----------|-----------|--------------|
| **User Acquisition** | 1,000 customers | Month 1 |
| **Restaurants Onboarded** | 50 restaurants | Month 1 |
| **Drivers Onboarded** | 100 drivers | Month 1 |
| **Daily Active Users** | 500+ | Month 2 |
| **Orders per Day** | 100+ | Month 2 |
| **Order Completion Rate** | 95%+ | Month 1 |
| **Customer Retention** | 60%+ | Month 2 |
| **App Rating** | 4.0+ stars | Month 1 |
| **Crash Rate** | < 0.5% | Month 1 |
| **Family Wallet Adoption** | 15% of users | Month 3 |
| **Group Order Usage** | 10% of orders | Month 3 |

---

# 19. Assumptions & Constraints

## 19.1 Assumptions

### **Technical:**
- ✅ Users have iOS devices (iPhone SE or newer)
- ✅ Users have stable 4G/5G or WiFi internet
- ✅ Users grant location permissions (for delivery)
- ✅ Users grant notification permissions (for updates)
- ✅ Firebase free tier sufficient for MVP (0-10K users)
- ✅ Google Maps API free tier sufficient (28K requests/month)
- ✅ Payment gateway (Hyperpay) has test environment

### **Business:**
- ✅ Restaurants have digital menus ready
- ✅ Restaurants willing to onboard with <20% commission (future)
- ✅ Drivers have smartphones and data plans
- ✅ Drivers have valid licenses and vehicle documents
- ✅ Customers comfortable with digital payments
- ✅ Regulatory approval not required for MVP (delivery aggregator)

### **User Behavior:**
- ✅ Customers prefer mobile apps over websites
- ✅ Customers order food 2-3 times per week on average
- ✅ Customers value convenience over small price differences
- ✅ Restaurants willing to learn new software (with training)
- ✅ Drivers motivated by flexible work hours

---

## 19.2 Constraints

### **Prototype Phase:**
- ❌ **No real backend:** Prototype is UI/UX only, no functional APIs
- ❌ **No actual payment processing:** Mock payment flows only
- ❌ **No real maps:** Simplified map UI, not interactive Google Maps
- ❌ **No real-time data:** Simulated real-time updates in prototype
- ❌ **Limited data:** 10 restaurants max, placeholder content
- ❌ **One language primary:** English primary, Arabic samples only

### **MVP Phase:**
- ❌ **iOS only:** Android version deferred to Phase 2
- ❌ **Riyadh only:** Geographic restriction for initial launch
- ❌ **Manual restaurant approval:** No automated verification
- ❌ **Manual driver approval:** No automated background checks
- ❌ **Basic analytics:** No advanced BI/reporting
- ❌ **Limited payment methods:** Card, Apple Pay, Wallets only (no cash on delivery)

### **Budget & Timeline:**
- ❌ **Timeline:** 6 weeks prototype, 10 weeks MVP development
- ❌ **Budget:** Limited (student project - no funding)
- ❌ **Team size:** 5 developers (capstone project team)
- ❌ **Third-party costs:** Must stay within free tiers

---

## 19.3 Out of Scope (Explicitly NOT Included)

### **Phase 1 (MVP):**
- ❌ Android app
- ❌ Web app/admin panel
- ❌ Multi-language (beyond English/Arabic)
- ❌ AI recommendations
- ❌ Voice ordering
- ❌ Cash on delivery
- ❌ Loyalty program
- ❌ Subscription plans
- ❌ Table reservations
- ❌ Grocery/pharmacy ordering
- ❌ Catering orders
- ❌ Corporate accounts
- ❌ Restaurant POS integration
- ❌ Inventory management
- ❌ Advanced analytics dashboard

---

# 20. Appendix

## 20.1 Glossary

| **Term** | **Definition** |
|----------|---------------|
| **PRD** | Product Requirements Document - Specification of product features |
| **BRD** | Business Requirements Document - Business justification and objectives |
| **MVP** | Minimum Viable Product - Core features for initial launch |
| **HIG** | Human Interface Guidelines - Apple's design standards for iOS |
| **OTP** | One-Time Password - 6-digit code for phone verification |
| **RTL** | Right-to-Left - Text direction for Arabic language |
| **LTR** | Left-to-Right - Text direction for English language |
| **SAR** | Saudi Riyal - Currency (1 USD ≈ 3.75 SAR) |
| **FCM** | Firebase Cloud Messaging - Push notification service |
| **API** | Application Programming Interface - Backend endpoints |
| **Firestore** | Firebase's NoSQL cloud database |
| **CDN** | Content Delivery Network - Fast asset delivery |
| **CI/CD** | Continuous Integration/Continuous Deployment - Automated builds |
| **UAT** | User Acceptance Testing - Testing with real users |
| **RBAC** | Role-Based Access Control - Permission system |
| **GDPR** | General Data Protection Regulation - EU privacy law |
| **PCI-DSS** | Payment Card Industry Data Security Standard |

---

## 20.2 Acronyms

| **Acronym** | **Full Form** |
|------------|---------------|
| **UI** | User Interface |
| **UX** | User Experience |
| **QA** | Quality Assurance |
| **DB** | Database |
| **ER** | Entity Relationship |
| **CRUD** | Create, Read, Update, Delete |
| **JSON** | JavaScript Object Notation |
| **HTTP** | Hypertext Transfer Protocol |
| **HTTPS** | HTTP Secure |
| **SSL/TLS** | Secure Sockets Layer / Transport Layer Security |
| **AES** | Advanced Encryption Standard |
| **JWT** | JSON Web Token |
| **HMAC** | Hash-based Message Authentication Code |
| **SQL** | Structured Query Language |
| **NoSQL** | Not Only SQL (document databases) |
| **REST** | Representational State Transfer |
| **SDK** | Software Development Kit |
| **IDE** | Integrated Development Environment |

---

## 20.3 References

1. **iOS Human Interface Guidelines:** https://developer.apple.com/design/human-interface-guidelines/
2. **Flutter Documentation:** https://docs.flutter.dev/
3. **Firebase Documentation:** https://firebase.google.com/docs
4. **Google Maps Platform:** https://developers.google.com/maps
5. **Figma Best Practices:** https://www.figma.com/best-practices/
6. **Material Design (Android reference):** https://material.io/design
7. **WCAG 2.1 Accessibility Guidelines:** https://www.w3.org/WAI/WCAG21/quickref/
8. **Apple App Store Review Guidelines:** https://developer.apple.com/app-store/review/guidelines/
9. **Original Capstone Project Report:** (Attached document)

---

## 20.4 Contact Information

| **Role** | **Name** | **Email** | **Phone** |
|----------|----------|-----------|-----------|
| **Product Owner** | (TBD) | product@example.com | +966 XX XXX XXXX |
| **Project Manager** | (TBD) | pm@example.com | +966 XX XXX XXXX |
| **Lead Designer** | (TBD) | design@example.com | +966 XX XXX XXXX |
| **Lead Developer** | (TBD) | dev@example.com | +966 XX XXX XXXX |
| **Supervisor** | Dr. Iehab AL Rassan | (University email) | (University phone) |

**University:** King Saud University  
**College:** Computer and Information Sciences  
**Department:** Computer Science  
**Course:** CSC 496 - Capstone Project  
**Semester:** First Semester 1447 / Autumn-Spring 2025

---

## 20.5 Document Revision History

| **Version** | **Date** | **Author** | **Changes** |
|------------|----------|-----------|-------------|
| 1.0 | Dec 2024 | Team | Initial PRD draft (Basic structure) |
| 2.0 | Dec 2024 | Claude AI | Complete PRD with all sections, technical architecture, detailed requirements, screen inventory, user journeys, components, animations, data, prototype specs, success criteria |

---

## 20.6 Sign-off

| **Role** | **Name** | **Signature** | **Date** |
|----------|----------|-------------|----------|
| **Product Owner** |  |  |  |
| **Project Manager** |  |  |  |
| **Lead Designer** |  |  |  |
| **Lead Developer** |  |  |  |
| **Supervisor** | Dr. Iehab AL Rassan |  |  |

---

# 📌 Quick Reference Card

**Project:** Restaurant Ordering Platform  
**Document:** Product Requirements Document (PRD) v2.0  
**Total Screens:** ~160 (Core: 130, Optional: 30)  
**User Roles:** Customer, Restaurant, Driver  
**Unique Features:** ⭐ Family Wallet, ⭐ Group Order + Bill Split  
**Tech Stack:** Flutter + Firebase  
**Design System:** iOS HIG  
**Languages:** Arabic + English  
**Timeline:** 6 weeks prototype → 10 weeks MVP  
**Deliverable:** Interactive Figma prototype  

**Key Sections:**
- Section 1-5: Overview, Scope, Personas, Architecture
- Section 6: Functional Requirements (FR-001 to FR-027)
- Section 7-11: Error Handling, Performance, Security, Release, Testing
- Section 12: Screen Inventory (all 160 screens listed)
- Section 13: User Journeys (6 detailed flows)
- Section 14-15: Components, Animations
- Section 16-17: Data Requirements, Prototype Specs
- Section 18-20: Success Criteria, Assumptions, Appendix

---

**End of PRD - Part 2**  
**Total Document Pages: ~200+ (Part 1 + Part 2)**

---