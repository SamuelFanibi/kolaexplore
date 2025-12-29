# Merchant Dashboard (Web App) - UI/UX Design Specification

## Merchant Information Architecture

### Main Navigation Structure
```
Dashboard
├── Services
│   ├── All Services
│   ├── Create New Service
│   └── Service Categories
├── Bookings
│   ├── All Bookings
│   ├── Calendar View
│   └── Availability Management
├── Customers
│   ├── Customer List
│   └── Customer Reviews
├── Analytics
│   ├── Overview
│   ├── Revenue
│   └── Performance
├── Settings
│   ├── Profile
│   ├── Business Information
│   ├── Payment Settings
│   └── Notifications
└── Help & Support
```

## Service Creation & Management Flows

### Service Creation Flow

**Step 1: Service Type Selection**
- Choose service category:
  - Flights
  - Hotels
  - Rides
  - Events
  - Spa & Wellness
- Service template selection

**Step 2: Basic Information**
- Service name
- Description (rich text editor)
- Category and subcategory
- Tags/keywords
- Service images (multiple upload)
- Location/address
- Contact information

**Step 3: Pricing & Availability**
- Base price
- Pricing tiers (if applicable)
- Discount options
- Availability calendar
- Time slots (for appointments)
- Capacity/quantity limits

**Step 4: Service Details**
- Features and amenities
- Policies (cancellation, refund)
- Terms and conditions
- Required information from customers
- Add-ons and extras

**Step 5: Review & Publish**
- Preview service listing
- Review all information
- Publish or save as draft
- Submit for approval (if required)

### Service Management Screen

**Service List View:**
- **Filters**:
  - Service type
  - Status (Active, Draft, Pending, Inactive)
  - Date created
  - Search by name
- **Service Cards/Table**:
  - Thumbnail image
  - Service name
  - Category
  - Status badge
  - Views/Bookings count
  - Revenue
  - Actions (Edit, Duplicate, Delete, View)
- **Bulk Actions**: Select multiple, bulk edit, bulk delete
- **Create New Service** button (prominent)

**Service Edit Screen:**
- Tabbed interface:
  - Overview
  - Pricing
  - Availability
  - Details
  - Images
  - Settings
- Auto-save indicator
- Preview button
- Save and publish buttons

## Booking & Availability Management Screens

### Bookings Overview Screen

**Dashboard Widgets:**
- Total bookings (today, week, month)
- Revenue metrics
- Pending confirmations
- Upcoming bookings
- Cancellation rate

**Bookings List:**
- **Filters**:
  - Date range
  - Booking status
  - Service type
  - Customer name
  - Booking reference
- **Table/List View**:
  - Booking reference
  - Customer name
  - Service name
  - Booking date/time
  - Status badge
  - Amount
  - Actions (View, Confirm, Cancel, Contact)
- **Status Badges**:
  - Pending
  - Confirmed
  - Completed
  - Cancelled
  - Refunded

### Booking Details Screen

**Booking Information:**
- Booking reference and status
- Customer details
- Service information
- Booking date and time
- Payment information
- Special requests/notes

**Actions:**
- Confirm booking
- Cancel booking
- Refund (if applicable)
- Contact customer
- Download invoice
- Print receipt
- Add internal notes

**Timeline:**
- Booking creation
- Confirmation
- Modifications
- Completion/cancellation

### Calendar View

**Calendar Interface:**
- Month/Week/Day view toggle
- Service filter
- Color coding by service type
- Booking slots display
- Availability indicators
- Quick booking creation
- Drag and drop to reschedule

**Booking Slot Details:**
- Click to view booking details
- Quick actions menu
- Status indicators
- Capacity information

### Availability Management Screen

**Availability Settings:**
- Default availability hours
- Service-specific schedules
- Holiday/exception dates
- Time slot configuration
- Capacity limits
- Buffer times

**Bulk Availability Actions:**
- Set availability for date range
- Block dates
- Copy schedule
- Import calendar

**Visual Calendar:**
- Available (green)
- Booked (blue)
- Blocked (red)
- Partially available (yellow)

## Order & Customer Overview Screens

### Orders Overview

**Order Statistics:**
- Total orders
- Revenue (daily, weekly, monthly)
- Average order value
- Conversion rate
- Refund rate

**Order List:**
- **Filters**: Date, status, service type, amount range
- **Order Table**:
  - Order ID
  - Customer name
  - Service(s)
  - Order date
  - Status
  - Total amount
  - Actions
- **Export Options**: CSV, PDF

### Customer Overview Screen

**Customer List:**
- **Search and Filters**:
  - Name, email, phone
  - Booking count
  - Total spent
  - Last booking date
- **Customer Cards/Table**:
  - Customer name and avatar
  - Contact information
  - Total bookings
  - Total spent
  - Last booking date
  - Customer rating (if applicable)
  - Actions (View profile, Contact, View bookings)

**Customer Profile:**
- Customer information
- Booking history
- Preferences
- Communication history
- Notes (internal)
- Customer lifetime value

### Customer Reviews Screen

**Reviews Overview:**
- Average rating
- Total reviews
- Rating distribution
- Recent reviews

**Reviews List:**
- **Filters**: Rating, date, service
- **Review Cards**:
  - Customer name and avatar
  - Rating (stars)
  - Review text
  - Service name
  - Date
  - Response option
- **Actions**: Reply, Flag, Delete

## High-Fidelity Merchant Dashboard UI Components

### Dashboard Header
- Merchant name/logo
- Notification bell
- User menu
- Help button

### Sidebar Navigation
- Collapsible sidebar
- Active state indicators
- Icon + label
- Badge for notifications
- Expandable submenus

### Data Tables
- Sortable columns
- Pagination
- Row selection
- Bulk actions
- Export options
- Responsive (mobile-friendly)

### Cards/Widgets
- Metric cards (numbers, charts)
- Quick action cards
- Status cards
- Information cards

### Forms
- Multi-step forms
- Field validation
- Auto-save
- Rich text editor
- File upload
- Date/time pickers
- Select dropdowns

### Modals
- Confirmation dialogs
- Form modals
- Detail view modals
- Alert modals

### Charts & Analytics
- Line charts (revenue trends)
- Bar charts (comparisons)
- Pie charts (distribution)
- Date range selectors
- Export options

## Role-Based Access Considerations

### Service Provider
- Full access to own services
- Booking management
- Customer communication
- Basic analytics

### Service Manager
- All service provider permissions
- Team member management
- Advanced analytics
- Business settings

### Admin (Merchant Level)
- All permissions
- Account settings
- Billing and subscription
- API access

### Permission Indicators
- Lock icons for restricted features
- Tooltips explaining restrictions
- Upgrade prompts for premium features

## Responsive Design

### Desktop (Primary)
- Full sidebar navigation
- Multi-column layouts
- Data tables
- Advanced filtering

### Tablet
- Collapsible sidebar
- Stacked layouts
- Simplified tables
- Touch-optimized controls

### Mobile
- Bottom navigation
- Hamburger menu
- Single column layouts
- Simplified forms
- Card-based lists

## Key Features & Interactions

### Quick Actions
- Floating action button (create service)
- Quick filters
- Bulk operations
- Keyboard shortcuts

### Notifications
- In-app notification center
- Email notifications settings
- Push notification preferences
- Notification badges

### Search
- Global search bar
- Search across services, bookings, customers
- Recent searches
- Search suggestions

### Data Export
- Export bookings (CSV, PDF)
- Export reports
- Scheduled reports
- Custom date ranges

### Integration
- Calendar sync
- Payment gateway settings
- API access
- Webhook configuration

