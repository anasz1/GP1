# Restaurant Ordering Platform - UI Design Brief
**For Figma Make AI Design Generation**

---

## 📱 Project Overview

**Product Name:** Restaurant Ordering Platform  
**Platform:** iOS Mobile App (iPhone 14 Pro)  
**Design System:** iOS Human Interface Guidelines (HIG)  
**Languages:** Arabic (RTL) + English (LTR)  
**Total Screens:** ~160 screens  
**User Roles:** Customer, Restaurant, Driver (3 apps in 1)

---

## 🎯 Design Goals

1. **Clean & Modern:** Minimalist iOS-native feel
2. **Intuitive Navigation:** Users complete orders in < 2 minutes
3. **High Contrast:** WCAG 2.1 AA compliant
4. **Smooth Animations:** 60fps transitions, < 300ms duration
5. **Bilingual:** Seamless Arabic/English switching with proper RTL support

---

## 🎨 Design System

### Colors

**Primary Palette:**
```
Primary:    #FF6B35 (Orange - food/appetite)
Secondary:  #2E7D32 (Green - fresh/healthy)
Accent:     #FFC107 (Amber - highlights)
```

**Neutrals:**
```
Background: #FFFFFF (White)
Surface:    #F5F5F5 (Light Gray)
Border:     #E0E0E0 (Gray 300)
Text Primary: #212121 (Almost Black)
Text Secondary: #757575 (Gray 600)
```

**Status Colors:**
```
Success:  #4CAF50 (Green)
Error:    #F44336 (Red)
Warning:  #FF9800 (Orange)
Info:     #2196F3 (Blue)
```

**Semantic:**
```
Open:       #4CAF50 (Green badge)
Closed:     #F44336 (Red badge)
Delivering: #2196F3 (Blue)
Pending:    #FF9800 (Orange)
```

### Typography

**Font Family:** SF Pro (iOS System Font)

**Scale:**
```
H1 - Title Large:     34pt, Bold    (Screen titles)
H2 - Title:           28pt, Bold    (Section headers)
H3 - Headline:        22pt, Semibold (Card titles)
Body Large:           17pt, Regular  (Primary text)
Body:                 15pt, Regular  (Secondary text)
Caption:              13pt, Regular  (Labels, hints)
Button:               17pt, Semibold (CTA text)
```

**Line Height:**
- Headlines: 1.2
- Body: 1.5
- Caption: 1.3

### Spacing & Grid

**Base Unit:** 8px

**Common Spacing:**
```
XXS: 4px   (tight elements)
XS:  8px   (element padding)
S:   12px  (small gaps)
M:   16px  (standard gap)
L:   24px  (section spacing)
XL:  32px  (major sections)
XXL: 48px  (screen padding)
```

**Layout Grid:**
- Columns: 4 (mobile)
- Gutter: 16px
- Margins: 20px (left/right)

### Corner Radius
```
Small:  4px  (badges, tags)
Medium: 8px  (buttons, inputs)
Large:  12px (cards)
XLarge: 16px (modals, sheets)
Round:  50%  (avatars, icons)
```

### Shadows
```
Small:  0 2px 4px rgba(0,0,0,0.08)   (cards)
Medium: 0 4px 8px rgba(0,0,0,0.12)   (elevated cards)
Large:  0 8px 16px rgba(0,0,0,0.16)  (modals)
```

### Icons

**Style:** SF Symbols (iOS native)  
**Sizes:**
- Small: 16x16px
- Medium: 24x24px
- Large: 32x32px

**Common Icons:**
- Home: house.fill
- Search: magnifyingglass
- Cart: cart.fill
- Profile: person.fill
- Star: star.fill
- Location: location.fill
- Phone: phone.fill
- Message: message.fill

---

## 🧩 Core Components

### 1. Buttons

**Primary Button:**
- Background: Primary color (#FF6B35)
- Text: White, Semibold
- Height: 48px
- Radius: 12px
- Pressed state: Darken 10%

**Secondary Button:**
- Background: Surface (#F5F5F5)
- Text: Primary color
- Height: 48px
- Radius: 12px

**Text Button:**
- No background
- Text: Primary color
- Underline on press

**Icon Button:**
- 44x44px touch target
- Icon: 24x24px
- Circular background (subtle)

### 2. Input Fields

**Text Input:**
- Height: 48px
- Border: 1px, #E0E0E0
- Radius: 8px
- Focus: Border #FF6B35, 2px
- Error: Border #F44336
- Placeholder: #757575

**Search Bar:**
- Height: 40px
- Background: #F5F5F5
- Radius: 20px (pill shape)
- Icon: magnifyingglass (left)
- Clear button (right)

### 3. Cards

**Restaurant Card:**
```
┌─────────────────────────┐
│    [Cover Image 16:9]   │
│  ┌──────┐               │
│  │ Logo │  Restaurant   │
│  └──────┘  Name         │
│  ⭐ 4.7 • 25-35 min     │
│  🚗 15 SAR delivery     │
│  [Open] 🏷️ OFFER       │
└─────────────────────────┘
```
- Height: ~180px
- Radius: 12px
- Shadow: Medium
- Padding: 12px

**Item Card (Menu):**
```
┌──────────────────────┐
│  [Image]  Item Name  │
│  120x120  Desc...    │
│           35 SAR [+] │
└──────────────────────┘
```
- Horizontal layout
- Image: Square, left
- Radius: 8px

### 4. Bottom Sheets / Modals

**Structure:**
- Slide up animation
- Handle bar (top center)
- Drag to dismiss
- Semi-transparent backdrop
- Radius: 16px (top corners)
- Max height: 80vh

### 5. Navigation

**Bottom Tab Bar:**
- Height: 83px (includes safe area)
- 5 tabs max
- Active: Primary color + filled icon
- Inactive: Gray + outline icon
- Labels: 11pt

**Top Navigation Bar:**
- Height: 44px + status bar
- Large title (scrollable)
- Back button (left)
- Actions (right, max 2)

### 6. Lists

**Standard List Item:**
- Height: 60px
- Divider: 1px, #E0E0E0
- Left: Icon/Avatar
- Center: Title + Subtitle
- Right: Accessory (chevron, switch)

### 7. Badges & Tags

**Status Badge:**
- Height: 24px
- Padding: 8px horizontal
- Radius: 12px (pill)
- Text: 12pt, Semibold
- Colors: Semantic (green, red, etc.)

**Cuisine Tag:**
- Height: 28px
- Background: Light gray
- Text: 13pt
- Radius: 6px

### 8. Progress Indicators

**Loading Spinner:**
- iOS native ActivityIndicator
- Size: Medium
- Color: Primary

**Progress Bar:**
- Height: 4px
- Background: #E0E0E0
- Fill: Primary color
- Animated

**Skeleton Loading:**
- Background: #F5F5F5
- Shimmer animation
- Match content layout

---

## 📱 Key Screens Breakdown

### 🔐 Authentication Flow (8 screens)

**1. Splash Screen**
- Logo (centered, large)
- Tagline below
- Auto-advance after 2s

**2. Welcome Screen**
- Hero illustration (food delivery theme)
- "Get Started" button (primary)
- "Already have account? Login" (text)

**3. Role Selection**
- 3 large cards (equal height):
  - 🛍️ Customer
  - 🍽️ Restaurant
  - 🚗 Driver
- Icon + Title + Brief description
- Tap to select → glow effect

**4. Phone Entry**
- Country code selector (left): +966
- Phone input field
- "Continue" button (disabled until valid)

**5. OTP Verification**
- 6 individual boxes for digits
- Auto-focus next box
- "Resend OTP" (timer: 60s)
- "Verify" button

**6. Customer Profile Setup**
- Avatar placeholder (tap to upload)
- Name field
- Email field
- "Save" button

**7. Restaurant Document Upload**
- List of required docs with upload buttons
- Upload progress indicators
- "Submit for Review" button

**8. Success / Pending Approval**
- Checkmark animation (success)
- OR: Clock icon (pending)
- Message + "Go to App" button

---

### 🏠 Customer App (80 screens)

#### Home & Browse (15 screens)

**Home Screen:**
```
┌─────────────────────────────────┐
│ 📍 Riyadh, Al Olaya     🔔 👤  │ ← Nav bar
├─────────────────────────────────┤
│ [Search bar........................] │
├─────────────────────────────────┤
│ ❤️ 🆕 🔥 🚚              → │ ← Quick filters
├─────────────────────────────────┤
│ 🍕 🍔 🍜 🥗 🍰...        → │ ← Categories
├─────────────────────────────────┤
│ ┌───────────────────────────┐   │
│ │ [Restaurant Card 1]       │   │
│ └───────────────────────────┘   │
│ ┌───────────────────────────┐   │
│ │ [Restaurant Card 2]       │   │
│ └───────────────────────────┘   │
│ ┌───────────────────────────┐   │
│ │ [Restaurant Card 3]       │   │
│ └───────────────────────────┘   │
│         ...more...              │
└─────────────────────────────────┘
│ 🏠  🔍  🛒(3)  📦  👤         │ ← Bottom tabs
└─────────────────────────────────┘
```

**Filters Bottom Sheet:**
- Cuisine (checkboxes)
- Price range (slider)
- Distance (slider)
- Rating (checkboxes)
- "Apply" button (sticky bottom)

**Restaurant Detail:**
```
┌─────────────────────────────────┐
│ ← Restaurant Name         ❤️ ⋯  │
├─────────────────────────────────┤
│ [Cover Image - Full width]      │
│   ┌──────┐                      │
│   │ Logo │                      │
│   └──────┘                      │
├─────────────────────────────────┤
│ Restaurant Name                  │
│ ⭐ 4.8 (450+) • 25-35 min       │
│ 🚗 15 SAR • Saudi, Italian      │
│ 🟢 Open until 11 PM             │
├─────────────────────────────────┤
│ [Appetizers] [Mains] [Desserts] │ ← Sticky tabs
├─────────────────────────────────┤
│ Appetizers                       │
│ ┌─────────────────────────────┐ │
│ │ [img] Hummus       12 SAR [+]│ │
│ └─────────────────────────────┘ │
│ ┌─────────────────────────────┐ │
│ │ [img] Salad        15 SAR [+]│ │
│ └─────────────────────────────┘ │
│                                  │
│ Mains                           │
│ ┌─────────────────────────────┐ │
│ │ [img] Kabsa        45 SAR [+]│ │
│ └─────────────────────────────┘ │
└─────────────────────────────────┘
│ [View Cart (3) - 85 SAR]        │ ← Sticky bottom
└─────────────────────────────────┘
```

**Item Detail Modal:**
- Full-screen bottom sheet (scrollable)
- Image carousel (top)
- Item name + price
- Description
- Customization sections:
  - Size (radio buttons)
  - Add-ons (checkboxes + prices)
  - Remove items (checkboxes)
  - Special instructions (text area)
- Quantity selector (- [1] +)
- "Add to Cart - 45 SAR" (sticky bottom)

#### Cart & Checkout (12 screens)

**Cart Screen:**
```
┌─────────────────────────────────┐
│ ← Cart                   🗑️ Clear│
├─────────────────────────────────┤
│ From: Mama's Kitchen             │
├─────────────────────────────────┤
│ ┌─────────────────────────────┐ │
│ │ Chicken Kabsa               │ │
│ │ Large, Extra rice           │ │
│ │ 45 SAR      [-] 2 [+]   ✏️ │ │
│ └─────────────────────────────┘ │
│ ┌─────────────────────────────┐ │
│ │ Arabic Salad                │ │
│ │ No onions                   │ │
│ │ 15 SAR      [-] 1 [+]   ✏️ │ │
│ └─────────────────────────────┘ │
├─────────────────────────────────┤
│ [Enter coupon code........] Apply│
├─────────────────────────────────┤
│ Subtotal             60.00 SAR  │
│ Delivery Fee         15.00 SAR  │
│ Discount (CODE20)   -12.00 SAR  │
│ ──────────────────────────────  │
│ Subtotal             63.00 SAR  │
│ VAT (15%)             9.45 SAR  │
│ ──────────────────────────────  │
│ Total                72.45 SAR  │
├─────────────────────────────────┤
│ [Proceed to Checkout]           │
└─────────────────────────────────┘
```

**Checkout Screen:**
- Sections (collapsible):
  1. Delivery Address (+ Change)
  2. Delivery Time (Radio: Now / Schedule)
  3. Payment Method (Radio: options)
  4. Order Summary (collapsible list)
  5. Special Instructions (text area)
- "Place Order - 72.45 SAR" (sticky bottom)

**Address Selection:**
- List of saved addresses (radio selection)
- "Add New Address" button
- Map preview per address

**Add Address (with Map):**
- Map view (top 50%)
- Draggable pin
- "Use Current Location" button
- Form (bottom 50%):
  - Label dropdown
  - District, Street, Building inputs
  - "Save Address" button

#### Family Wallet ⭐ (10 screens)

**Family Wallet Dashboard:**
```
┌─────────────────────────────────┐
│ ← Family Wallet            [Top Up]│
├─────────────────────────────────┤
│ Al-Otaibi Family 👨‍👩‍👧            │
│ SAR 850.00                      │
│ Total Balance                    │
├─────────────────────────────────┤
│ [Members] [Transactions] [Settings]│ ← Tabs
├─────────────────────────────────┤
│ Members                          │
│ ┌─────────────────────────────┐ │
│ │ 👤 Sarah (Owner)            │ │
│ │ Limit: 200 | Spent: 45      │ │
│ │ [━━━━━━░░░░] 155 remaining  │ │
│ └─────────────────────────────┘ │
│ ┌─────────────────────────────┐ │
│ │ 👤 Ahmed                    │ │
│ │ Limit: 150 | Spent: 30      │ │
│ │ [━━━━━░░░░░] 120 remaining  │ │
│ └─────────────────────────────┘ │
├─────────────────────────────────┤
│ [+ Add Member]                  │
└─────────────────────────────────┘
```

**Create Family Wallet:**
- Step indicator (1/3, 2/3, 3/3)
- Step 1: Name + Initial balance
- Step 2: Add members (list)
- Step 3: Review + Confirm

**Invitation Screen (Recipient):**
```
┌─────────────────────────────────┐
│ 👨‍👩‍👧 Family Wallet Invitation     │
├─────────────────────────────────┤
│                                  │
│     [Large Family Icon]          │
│                                  │
│ Sarah invited you to join        │
│ "Al-Otaibi Family"               │
│                                  │
│ Your monthly limit: 200 SAR      │
│                                  │
├─────────────────────────────────┤
│ [Accept] (green button)          │
│ [Decline] (text button)          │
└─────────────────────────────────┘
```

#### Group Order ⭐ (8 screens)

**Start Group Order:**
```
┌─────────────────────────────────┐
│ ← Start Group Order              │
├─────────────────────────────────┤
│ Group Name                       │
│ [Office Lunch.................] │
│                                  │
│ Order Deadline                   │
│ ○ 10 minutes                    │
│ ○ 20 minutes                    │
│ ○ 30 minutes                    │
│ ● 1 hour                        │
│                                  │
│ Delivery Address                 │
│ [🏠 Home - Al Olaya, King...] [>]│
│                                  │
├─────────────────────────────────┤
│ [Create Group Order]             │
└─────────────────────────────────┘
```

**Share Group Order:**
```
┌─────────────────────────────────┐
│ 🍕 Share Group Order             │
├─────────────────────────────────┤
│                                  │
│      [QR Code - Large]           │
│                                  │
│ Join Code: ABC123  [Copy]        │
│                                  │
│ Or share link:                   │
│ https://app.com/join/ABC123      │
│ [Copy Link]                      │
│                                  │
├─────────────────────────────────┤
│ Share via:                       │
│ [WhatsApp] [SMS] [Email] [More]  │
└─────────────────────────────────┘
```

**Group Cart (Shared):**
```
┌─────────────────────────────────┐
│ ← Office Lunch 🍕                │
│ ⏱️ Orders close in 45:30         │
│ 3 people ordering                │
├─────────────────────────────────┤
│ [By Person ●] [All Items ○]     │ ← Toggle
├─────────────────────────────────┤
│ 👤 Sarah (Host) ✓                │
│  • Margherita Pizza  35 SAR     │
│  • Caesar Salad      20 SAR     │
│  Subtotal: 55 SAR               │
│                                  │
│ 👤 Ahmed                         │
│  • Pepperoni Pizza   40 SAR     │
│  Subtotal: 40 SAR               │
│                                  │
│ 👤 Khalid                        │
│  Ordering...                     │
├─────────────────────────────────┤
│ Total: 95 SAR                   │
│ [+ Add Items] [Proceed to Pay]   │
└─────────────────────────────────┘
```

**Split Bill Options:**
```
┌─────────────────────────────────┐
│ ← Split Bill                     │
├─────────────────────────────────┤
│ Total: SAR 110 (incl. delivery)  │
│                                  │
│ ● Pay for Own Items Only         │
│   Sarah:  SAR 60                │
│   Ahmed:  SAR 50                │
│                                  │
│ ○ Split Equally                  │
│   Each pays: SAR 55              │
│                                  │
│ ○ Custom Split                   │
│   (Tap to set amounts)           │
│                                  │
├─────────────────────────────────┤
│ [Continue to Payment]            │
└─────────────────────────────────┘
```

**Payment Status Tracker:**
```
┌─────────────────────────────────┐
│ Payment Status                   │
├─────────────────────────────────┤
│ ✅ Sarah (Paid)       SAR 60    │
│ ⏳ Ahmed (Pending)    SAR 50    │
│                                  │
│ Waiting for 1 payment...         │
│ [Send Reminder to Ahmed]         │
└─────────────────────────────────┘
```

#### Order Tracking (6 screens)

**Order Tracking Screen:**
```
┌─────────────────────────────────┐
│ ← Track Order                    │
├─────────────────────────────────┤
│ Order #12345                     │
│ Arriving in ~25 min              │
├─────────────────────────────────┤
│ ● Order Placed         12:00 PM │
│ ● Restaurant Accepted  12:02 PM │
│ ● Preparing           12:05 PM │
│ ◉ Ready for Pickup    12:25 PM │ ← Current
│ ○ Driver Picked Up              │
│ ○ On the Way                    │
│ ○ Delivered                     │
├─────────────────────────────────┤
│ [Map View - Shows driver pin]    │
├─────────────────────────────────┤
│ Driver: Khalid ⭐ 4.9           │
│ 🚗 Toyota Camry • ABC 1234      │
│ [💬 Chat] [📞 Call]              │
├─────────────────────────────────┤
│ [Cancel Order]                  │
└─────────────────────────────────┘
```

#### Other Customer Screens (29 screens)

**Search, Favorites, Order History, Profile, Settings, Notifications, Chat, Ratings, Help, etc.**

---

### 🍽️ Restaurant App (40 screens)

#### Dashboard (5 screens)

**Restaurant Dashboard:**
```
┌─────────────────────────────────┐
│ ☰ Mama's Kitchen        [Open ●]│ ← Toggle
├─────────────────────────────────┤
│ Today's Stats                    │
│ ┌──────┐ ┌──────┐ ┌──────┐     │
│ │ 15   │ │ 850  │ │ 4.8  │     │
│ │Orders│ │ SAR  │ │ ⭐   │     │
│ └──────┘ └──────┘ └──────┘     │
├─────────────────────────────────┤
│ Quick Actions                    │
│ [📋 New Orders (3)]              │
│ [🍕 Manage Menu]                 │
│ [🏷️ Promotions]                  │
│ [⏰ Operating Hours]             │
├─────────────────────────────────┤
│ Recent Orders                    │
│ ┌─────────────────────────────┐ │
│ │ Order #123  •  12:30 PM     │ │
│ │ 3 items  •  SAR 85          │ │
│ │ [Preparing ●]               │ │
│ └─────────────────────────────┘ │
└─────────────────────────────────┘
```

#### Order Management (8 screens)

**Incoming Order (Full-screen Alert):**
```
┌─────────────────────────────────┐
│         🔔 NEW ORDER!            │
├─────────────────────────────────┤
│ Order #12345                     │
│ Customer: Sarah Ahmed            │
│                                  │
│ Items:                           │
│ • Chicken Kabsa x2               │
│ • Arabic Salad x1                │
│                                  │
│ Total: SAR 95                   │
│ Payment: Credit Card ✓          │
│                                  │
│ ⏱️ Auto-decline in 1:45          │
├─────────────────────────────────┤
│ [Reject]        [Accept]         │
└─────────────────────────────────┘
```

**Order Details:**
```
┌─────────────────────────────────┐
│ ← Order #12345                   │
├─────────────────────────────────┤
│ Status: Preparing                │
│ Time: 12:30 PM                   │
│                                  │
│ Customer: Sarah Ahmed            │
│ Phone: +966 50 123 4567         │
│ Address: Al Olaya, King Fahd Rd  │
│                                  │
│ Items:                           │
│ ┌─────────────────────────────┐ │
│ │ • Chicken Kabsa x2          │ │
│ │   Large, Extra rice         │ │
│ │   SAR 90                    │ │
│ └─────────────────────────────┘ │
│                                  │
│ Special Instructions:            │
│ "No spicy please"                │
│                                  │
│ Total: SAR 95                   │
├─────────────────────────────────┤
│ [Mark as Ready]                  │
└─────────────────────────────────┘
```

**Orders List (Tabs):**
- New (3) | In Progress (5) | Completed (120)
- Each order card: #, time, items count, total, status

#### Menu Management (12 screens)

**Menu Management:**
```
┌─────────────────────────────────┐
│ ← Menu                    [+ Add]│
├─────────────────────────────────┤
│ [Appetizers] [Mains] [Desserts]  │ ← Tabs
├─────────────────────────────────┤
│ Mains (8 items)                  │
│                                  │
│ ┌─────────────────────────────┐ │
│ │ [img] Chicken Kabsa         │ │
│ │ 45 SAR  [Available ●]       │ │
│ │ [✏️ Edit] [🗑️ Delete]        │ │
│ └─────────────────────────────┘ │
│ ┌─────────────────────────────┐ │
│ │ [img] Lamb Mandi            │ │
│ │ 60 SAR  [Unavailable ○]    │ │
│ │ [✏️ Edit] [🗑️ Delete]        │ │
│ └─────────────────────────────┘ │
└─────────────────────────────────┘
```

**Add/Edit Item:**
- Item name input
- Description textarea
- Price input
- Category dropdown
- Image upload (camera/gallery)
- Customizations:
  - Add size options (+ button)
  - Add add-ons (+ button)
  - Add removable ingredients
- "Save" button

#### Promotions (6 screens)

**Promotions List:**
- Active promotions (green badge)
- Scheduled (orange badge)
- Expired (gray)
- "Create Promotion" button

**Create Promotion:**
```
┌─────────────────────────────────┐
│ ← Create Promotion               │
├─────────────────────────────────┤
│ Title                            │
│ [20% Off on All Orders.......] │
│                                  │
│ Discount Type                    │
│ ● Percentage                     │
│ ○ Fixed Amount                   │
│                                  │
│ Value                            │
│ [20] %                          │
│                                  │
│ Start Date & Time                │
│ [Dec 25, 2024 - 6:00 PM]  [Pick]│
│                                  │
│ End Date & Time                  │
│ [Dec 25, 2024 - 10:00 PM] [Pick]│
│                                  │
│ Minimum Order Value              │
│ [100] SAR                       │
│                                  │
├─────────────────────────────────┤
│ [Create Promotion]               │
└─────────────────────────────────┘
```

#### Settings (9 screens)

**Operating Hours, Restaurant Profile, Reviews, Settings, etc.**

---

### 🚗 Driver App (40 screens)

#### Dashboard (3 screens)

**Driver Dashboard:**
```
┌─────────────────────────────────┐
│ ☰ Khalid                [Online ●]│ ← Toggle
├─────────────────────────────────┤
│ Today's Stats                    │
│ ┌──────┐ ┌──────┐ ┌──────┐     │
│ │  8   │ │ 120  │ │ 4.9  │     │
│ │Delivs│ │ SAR  │ │ ⭐   │     │
│ └──────┘ └──────┘ └──────┘     │
├─────────────────────────────────┤
│ Active Delivery                  │
│ ┌─────────────────────────────┐ │
│ │ Order #123 • Mama's Kitchen │ │
│ │ Customer: Sarah Ahmed       │ │
│ │ [View Details >]            │ │
│ └─────────────────────────────┘ │
├─────────────────────────────────┤
│ No pending requests              │
└─────────────────────────────────┘
```

#### Delivery Request (5 screens)

**Incoming Request (Full-screen Alert):**
```
┌─────────────────────────────────┐
│     🚗 NEW DELIVERY REQUEST!     │
├─────────────────────────────────┤
│ Pickup: Mama's Kitchen           │
│ 📍 Al Olaya (2.3 km away)       │
│                                  │
│ Dropoff: Sarah Ahmed             │
│ 📍 King Fahd Road (3.8 km)      │
│                                  │
│ Distance: 6.1 km total           │
│ Payment: SAR 15                 │
│                                  │
│ ⏱️ Auto-decline in 0:30          │
├─────────────────────────────────┤
│ [Decline]       [Accept]         │
└─────────────────────────────────┘
```

#### Active Delivery (8 screens)

**Active Delivery Screen:**
```
┌─────────────────────────────────┐
│ ← Active Delivery                │
├─────────────────────────────────┤
│ Order #12345                     │
│ Status: Picked Up ●              │
├─────────────────────────────────┤
│ 📍 Restaurant                    │
│ Mama's Kitchen                   │
│ Al Olaya, King Abdullah St       │
│ [✓ Picked Up]                   │
│                                  │
│ 📍 Customer                      │
│ Sarah Ahmed                      │
│ King Fahd Road, Building 15      │
│ [🗺️ Navigate]                    │
│                                  │
│ [💬 Chat] [📞 Call]              │
├─────────────────────────────────┤
│ Order Items:                     │
│ • Chicken Kabsa x2               │
│ • Arabic Salad x1                │
│                                  │
│ Total: SAR 95                   │
│ Payment: Credit Card ✓          │
├─────────────────────────────────┤
│ [Mark as Delivered]              │
└─────────────────────────────────┘
```

**Status Update Buttons:**
- Heading to Restaurant
- Arrived at Restaurant
- Picked Up Order
- On the Way to Customer
- Delivered

#### Other Driver Screens (24 screens)

**Delivery History, Earnings, Profile, Documents, Settings, etc.**

---

## 🎭 Animations & Transitions

### Screen Transitions
```
Push (Forward):     Slide from right (iOS native)
Pop (Back):         Slide from left
Modal Present:      Slide up from bottom
Modal Dismiss:      Slide down
Tab Switch:         Fade + slight scale
```

### Micro-interactions
```
Button Press:       Scale 0.95x + opacity 0.8 (100ms)
Add to Cart:        Item flies to cart icon (300ms)
Success Checkmark:  Scale up from 0 + rotation (400ms)
Heart (Favorite):   Scale 1.3x + color change (200ms)
Pull to Refresh:    Spinner rotates (iOS native)
Loading:            Skeleton shimmer animation
Toast Notification: Slide up from bottom (300ms)
```

### Gestures
```
Tap:        Standard interaction
Long Press: Show context menu / preview
Swipe Left: Delete / Remove action
Swipe Right: Archive / Mark as done
Pull Down:  Refresh content
Drag:       Reorder items, Dismiss modals
```

---

## 📐 Responsive Layouts

### Device Sizes

**iPhone SE (Small - 375x667):**
- 2 columns for restaurant grid
- Smaller card images
- Compact spacing

**iPhone 14 Pro (Medium - 393x852):**
- 2 columns for restaurant grid
- Standard sizing (base design)
- Notch/Dynamic Island safe area

**iPhone 14 Pro Max (Large - 430x932):**
- 2 columns (wider cards)
- More vertical space
- Utilize extra width for content

### Orientation

**Portrait (Primary):**
- All screens optimized
- Standard layouts

**Landscape (Optional):**
- Restaurant list → 3 columns
- Menu items → 2 columns
- Forms adapt to horizontal space

---

## 🌍 Localization (Arabic RTL)

### RTL Considerations
```
Layout:           Mirror horizontally
Text Alignment:   Right-aligned
Icons:            Flip directional icons (arrows)
Navigation:       Back button on right
Tabs:             Right to left order
Lists:            Icons on right, text on left
```

### Text Length

- Arabic text ~30% longer than English
- Allow text wrapping (max 2-3 lines)
- Truncate with "..." if needed
- Dynamic button widths

### Number Format
```
English: 1,234.50 SAR
Arabic:  ١٬٢٣٤٫٥٠ ر.س
```

---

## 🎯 Unique Feature Highlights

### 1. Family Wallet ⭐

**Visual Identity:**
- 👨‍👩‍👧 Family icon (consistent)
- Purple accent color
- Unique card style with gradient background

**Key Screens:**
1. Dashboard with member list
2. Create wallet flow (3 steps)
3. Invitation card (purple theme)
4. Transaction history with avatars
5. Member management (owner view)

### 2. Group Order ⭐

**Visual Identity:**
- 🍕 Group icon (consistent)
- Orange accent color
- Real-time participant avatars

**Key Screens:**
1. Start group order form
2. Share invitation (QR + link)
3. Group cart with participant sections
4. Split bill options (visual breakdown)
5. Payment status tracker

---

## 🚦 Status & Feedback

### Order Status Colors
```
Placed:         Blue (#2196F3)
Accepted:       Green (#4CAF50)
Preparing:      Orange (#FF9800)
Ready:          Purple (#9C27B0)
On the Way:     Blue (#2196F3)
Delivered:      Green (#4CAF50)
Cancelled:      Red (#F44336)
```

### Empty States

**Pattern:**
- Illustration (grayscale)
- Short message (1-2 lines)
- CTA button (if applicable)

**Examples:**
- Empty cart: Shopping bag icon + "Your cart is empty"
- No orders: Package icon + "No orders yet"
- No results: Magnifying glass + "No restaurants found"

### Error States

**Pattern:**
- Error icon (red)
- Clear error message
- Action button ("Retry", "Go Back")

**Examples:**
- Network error: WiFi icon + "No internet connection"
- Payment failed: Card icon + "Payment unsuccessful"

### Loading States

**Skeleton Screens:**
- Restaurant cards: Gray rectangles (shimmer)
- Menu items: Gray blocks (shimmer)
- Profile: Gray circles + lines

**Spinners:**
- iOS native ActivityIndicator
- Color: Primary (#FF6B35)
- Size: Medium (default)

---

## 📱 Bottom Navigation (Customer App)
```
Tab 1: 🏠 Home       (house.fill)
Tab 2: 🔍 Search     (magnifyingglass)
Tab 3: 🛒 Cart       (cart.fill + badge)
Tab 4: 📦 Orders     (shippingbox.fill)
Tab 5: 👤 Profile    (person.fill)
```

**Active State:**
- Icon: Filled, Primary color
- Label: Primary color

**Inactive State:**
- Icon: Outline, Gray
- Label: Gray

---

## 🎨 Sample Screen Specifications

### Restaurant Card (Detailed Spec)
```
Component: Restaurant Card
Size: 343w x 180h (iPhone 14 Pro width - 40px margin)

Structure:
┌───────────────────────────────────┐
│ Cover Image                       │ 343x120, Radius 12px (top)
│                                   │ Object-fit: Cover
├───────────────────────────────────┤
│ ┌───┐ Restaurant Name            │ Logo: 60x60, -30px top
│ │   │ ⭐4.8 (450+)•25-35min•15SAR│ Name: 17pt Bold
│ └───┘ 🍕Saudi, Italian            │ Subtitle: 13pt Regular
│ [Open] [OFFER]                    │ Badges: 24h, Radius 12px
└───────────────────────────────────┘

Spacing:
- Padding: 12px
- Logo overlap: -30px (half inside/outside)
- Text spacing: 4px between lines
- Badge gap: 8px

Colors:
- Background: #FFFFFF
- Border: None (Shadow instead)
- Shadow: 0 2px 8px rgba(0,0,0,0.08)
- Open badge: #4CAF50
- Offer badge: #FF6B35
```

### Button Specifications
```
Primary Button:
- Height: 48px
- Padding: 16px horizontal
- Radius: 12px
- Background: #FF6B35
- Text: White, 17pt Semibold
- Shadow: 0 2px 4px rgba(255,107,53,0.3)
- Pressed: Background #E55A2A (darker 10%)
- Disabled: Background #FFB899, Text #FFFFFF80

Secondary Button:
- Height: 48px
- Background: #F5F5F5
- Text: #FF6B35, 17pt Semibold
- Border: None
- Pressed: Background #E0E0E0

Text Button:
- Height: 44px (minimum touch target)
- Background: Transparent
- Text: #FF6B35, 15pt Regular
- Underline: On press
```

---

## 🎬 Prototype Flow Specifications

### Flow 1: First Order (Customer)
```
1. Splash → 2. Welcome → 3. Role Selection (Customer)
→ 4. Phone Entry → 5. OTP → 6. Profile Setup
→ 7. Home (Restaurant List) → 8. Restaurant Detail
→ 9. Item Detail Modal → 10. Cart → 11. Checkout
→ 12. Address Selection → 13. Add Address (Map)
→ 14. Payment Method → 15. Place Order (Loading)
→ 16. Success → 17. Order Tracking

Total: 17 screens
```

### Flow 2: Family Wallet Creation
```
1. Home → 2. Profile → 3. Wallet
→ 4. Create Family (Step 1) → 5. Add Members (Step 2)
→ 6. Review (Step 3) → 7. Success
→ 8. [Invitee] Notification → 9. Accept Invitation
→ 10. [Owner] Member Joined → 11. Dashboard Updated

Total: 11 screens
```

### Flow 3: Group Order
```
1. Restaurant Page → 2. Start Group Order
→ 3. Share Link → 4. [Participant] Join Group
→ 5. Group Cart (Adding Items) → 6. Split Bill
→ 7. Payment Status → 8. All Paid → 9. Confirmation
→ 10. Order Tracking (Shared)

Total: 10 screens
```

### Flow 4: Restaurant Receives Order
```
1. Dashboard → 2. Incoming Order Alert
→ 3. Accept Order → 4. Order Details
→ 5. Update Status (Preparing) → 6. Mark Ready
→ 7. Driver Assigned Notification

Total: 7 screens
```

### Flow 5: Driver Delivery
```
1. Dashboard (Available) → 2. Delivery Request
→ 3. Accept → 4. Active Delivery
→ 5. Navigate to Restaurant → 6. Arrived
→ 7. Picked Up → 8. Navigate to Customer
→ 9. Mark Delivered → 10. Success

Total: 10 screens
```

---

## 🔍 Screen Checklist (160 Total)

### Authentication (13 screens)
- [ ] Splash
- [ ] Onboarding (3 slides)
- [ ] Welcome
- [ ] Role Selection
- [ ] Phone Entry
- [ ] OTP Verification
- [ ] Social Sign-In
- [ ] Customer Profile Setup
- [ ] Restaurant Document Upload
- [ ] Driver Document Upload
- [ ] Success/Pending

### Customer (80 screens)
#### Browse & Order (25)
- [ ] Home (Restaurant List)
- [ ] Filters Bottom Sheet
- [ ] Search
- [ ] Search Results
- [ ] Categories
- [ ] Restaurant Detail
- [ ] Menu (Scrollable)
- [ ] Item Detail Modal
- [ ] Customization Options
- [ ] Cart Preview
- [ ] Cart Full Screen
- [ ] Edit Item
- [ ] Remove Confirmation
- [ ] Coupon Entry
- [ ] Empty Cart
- [ ] Checkout
- [ ] Address Selection
- [ ] Add Address (Map)
- [ ] Edit Address
- [ ] Schedule Order Picker
- [ ] Payment Method Selection
- [ ] Card Payment Form
- [ ] Apple Pay Sheet
- [ ] Processing Order
- [ ] Order Confirmation

#### Family Wallet (10)
- [ ] Dashboard
- [ ] Create (Step 1-3)
- [ ] Add Member
- [ ] Member List
- [ ] Edit Member
- [ ] Transaction History
- [ ] Top Up
- [ ] Invitation (Recipient)
- [ ] Accept/Reject

#### Group Order (10)
- [ ] Start Group Order
- [ ] Share Link
- [ ] Join Group
- [ ] Group Cart (By Person)
- [ ] Group Cart (All Items)
- [ ] Participants List
- [ ] Split Bill Options
- [ ] Payment Status
- [ ] Group Confirmation

#### Orders & Tracking (15)
- [ ] Order Tracking
- [ ] Live Map
- [ ] Driver Profile Card
- [ ] Cancel Order
- [ ] Order History List
- [ ] Order Details
- [ ] Reorder Confirmation
- [ ] Rating Modal
- [ ] Report Issue
- [ ] Empty History

#### Communication (5)
- [ ] Chat Interface
- [ ] Call Confirmation

#### Profile & Settings (15)
- [ ] Profile Screen
- [ ] Edit Profile
- [ ] Saved Addresses
- [ ] Payment Methods
- [ ] Wallet
- [ ] Settings
- [ ] Language Switcher
- [ ] Notifications Settings
- [ ] Help & Support
- [ ] FAQ
- [ ] Contact Support
- [ ] About

### Restaurant (40 screens)
- [ ] Dashboard
- [ ] Incoming Order Alert
- [ ] Order Details
- [ ] Accept Modal
- [ ] Reject Modal
- [ ] Orders List (Tabs)
- [ ] Update Status
- [ ] Menu Management
- [ ] Add Item
- [ ] Edit Item
- [ ] Delete Confirmation
- [ ] Image Upload
- [ ] Category Management
- [ ] Promotions List
- [ ] Create Promotion
- [ ] Edit Promotion
- [ ] Promotion Preview
- [ ] Operating Hours
- [ ] Time Picker
- [ ] Restaurant Profile Edit
- [ ] Reviews & Ratings
- [ ] Settings
- [ ] Stats & Analytics
- [ ] Notifications
- [ ] (+ 16 more supporting screens)

### Driver (40 screens)
- [ ] Dashboard
- [ ] Delivery Request Alert
- [ ] Request Details
- [ ] Accept Confirmation
- [ ] Active Delivery
- [ ] Navigate Button
- [ ] Status Update Buttons
- [ ] Delivery Confirmation
- [ ] Delivery History
- [ ] Earnings Summary
- [ ] Driver Profile
- [ ] Edit Profile
- [ ] Vehicle Info
- [ ] Documents
- [ ] Settings
- [ ] Chat
- [ ] Call
- [ ] (+ 23 more supporting screens)

### Shared (17 screens)
- [ ] Notification Center
- [ ] Notification Detail
- [ ] Global Search
- [ ] Search Results
- [ ] Loading States
- [ ] Error States
- [ ] Empty States
- [ ] (+ 10 more supporting screens)

---

## 🎯 Priority for Prototype

### Phase 1: Core Flows (Must Have)
1. ✅ Authentication (all roles)
2. ✅ Customer: Browse → Order → Track
3. ✅ Family Wallet: Create → Invite → Use
4. ✅ Group Order: Start → Join → Split → Pay
5. ✅ Restaurant: Receive → Accept → Update
6. ✅ Driver: Accept → Navigate → Deliver

### Phase 2: Supporting Features (Should Have)
7. ✅ Search & Filters
8. ✅ Order History
9. ✅ Menu Management
10. ✅ Promotions
11. ✅ Chat/Call

### Phase 3: Polish (Nice to Have)
12. ✅ Settings & Profile
13. ✅ Help & Support
14. ✅ Notifications Center
15. ✅ Error States

---

## ✅ Design Checklist

Before finalizing prototype:

**Visual Design:**
- [ ] All screens follow iOS HIG
- [ ] Consistent color palette used
- [ ] Typography hierarchy clear
- [ ] Spacing follows 8px grid
- [ ] Icons are SF Symbols style
- [ ] Shadows are subtle and consistent

**Components:**
- [ ] Button states defined (default, pressed, disabled)
- [ ] Input fields show focus/error states
- [ ] Cards have consistent structure
- [ ] Modals slide up smoothly
- [ ] Navigation is native iOS style

**Content:**
- [ ] All text is placeholder (realistic)
- [ ] Images are high quality (food photography)
- [ ] Empty states have illustrations
- [ ] Error messages are helpful
- [ ] Loading states are clear

**Interactions:**
- [ ] All buttons are clickable
- [ ] Forms validate on submit
- [ ] Modals can be dismissed
- [ ] Back navigation works
- [ ] Tab switching works

**Accessibility:**
- [ ] Touch targets ≥ 44x44px
- [ ] Color contrast ≥ 4.5:1
- [ ] Text is readable (≥ 15pt)
- [ ] Icons have labels

**Localization:**
- [ ] RTL layout tested
- [ ] Arabic text fits in UI
- [ ] Numbers format correctly
- [ ] Date/time format correct

**Flows:**
- [ ] All 6 key flows work end-to-end
- [ ] No dead ends
- [ ] Success states shown
- [ ] Error handling included

---

## 📤 Deliverables

1. **Figma File** with:
   - All 160 screens designed
   - Component library
   - Design system page
   - Interactive prototype
   - Flow annotations

2. **Prototype Link:**
   - Shareable Figma link
   - Starting point: Splash Screen
   - All flows linked

3. **Design System:**
   - Colors
   - Typography
   - Components
   - Icons
   - Spacing

4. **Documentation:**
   - This UI Brief (markdown)
   - Screen descriptions
   - Flow diagrams

---

## 🎬 Final Notes

**Design Philosophy:**
- Less is more (minimalist)
- Let content shine
- Prioritize clarity over decoration
- Follow platform conventions (iOS)
- Make actions obvious
- Provide instant feedback

**Performance:**
- Keep animations smooth (60fps)
- Use skeleton screens for loading
- Progressive image loading
- Cache content where possible

**Testing:**
- Test with real content (long text, missing images)
- Test RTL layout thoroughly
- Test on smallest device (iPhone SE)
- Test all interactive elements

**Iterate:**
- Get feedback early
- Test with users
- Refine based on findings
- Document changes

---

**END OF UI BRIEF**

