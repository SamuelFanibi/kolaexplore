# Web Platform (Public & Booking) - UI/UX Design Specification

## Information Architecture

### Main Navigation Structure
```
Home
├── Search & Discovery
│   ├── Flights
│   ├── Hotels
│   ├── Rides
│   ├── Events
│   └── Spa & Wellness
├── My Bookings
├── Profile
└── Help & Support
```

## Service Discovery & Search Experience

### Search Interface Components
1. **Universal Search Bar**
   - Location: Top navigation bar (sticky)
   - Features:
     - Service type selector (Flights, Hotels, Rides, Events, Spa)
     - Search input with autocomplete
     - Date range picker
     - Location selector
     - Search button (CTA)

2. **Search Results Page**
   - Filters sidebar (left):
     - Price range slider
     - Rating filter
     - Service-specific filters
     - Availability filter
   - Results area (center):
     - Sort options (Price, Rating, Popularity, Distance)
     - Grid/List view toggle
     - Service cards with key information
     - Pagination
   - Map view toggle (for location-based services)

3. **Service Detail Page**
   - Hero image/gallery
   - Service title and key info
   - Booking widget (sticky sidebar)
   - Description and features
   - Reviews and ratings
   - Similar services recommendations
   - Location map (if applicable)

## Booking Flows

### 1. Flights Booking Flow

**Flow Steps:**
1. Search Page → Flight Search Form
2. Results Page → Flight selection
3. Flight Details → Passenger information
4. Seat Selection (optional)
5. Add-ons (baggage, meals, insurance)
6. Review & Cart
7. Checkout
8. Payment
9. Confirmation

**Key Screens:**
- **Flight Search**: Origin/Destination, Dates, Passengers, Class
- **Flight Results**: List of available flights with filters
- **Flight Details**: Full itinerary, pricing breakdown
- **Passenger Info**: Form for each passenger
- **Seat Map**: Interactive seat selection
- **Add-ons**: Optional services selection
- **Review**: Summary before checkout
- **Payment**: Payment method selection and processing
- **Confirmation**: Booking details and ticket download

### 2. Hotels & Accommodation Booking Flow

**Flow Steps:**
1. Search Page → Hotel Search Form
2. Results Page → Hotel selection
3. Hotel Details → Room selection
4. Guest Information
5. Special Requests
6. Review & Cart
7. Checkout
8. Payment
9. Confirmation

**Key Screens:**
- **Hotel Search**: Location, Check-in/out dates, Guests
- **Hotel Results**: Map and list view with filters
- **Hotel Details**: Gallery, amenities, room types, reviews
- **Room Selection**: Available rooms with pricing
- **Guest Info**: Primary guest and additional guests
- **Special Requests**: Dietary, accessibility, preferences
- **Review**: Booking summary
- **Payment**: Payment processing
- **Confirmation**: Booking voucher

### 3. Rides Booking Flow

**Flow Steps:**
1. Search Page → Pickup/Dropoff locations
2. Vehicle Selection → Choose vehicle type
3. Schedule → Immediate or scheduled ride
4. Review & Cart
5. Checkout
6. Payment
7. Confirmation & Driver Tracking

**Key Screens:**
- **Ride Request**: Pickup/dropoff with map
- **Vehicle Options**: Economy, Premium, Luxury with pricing
- **Schedule**: Time selection for future rides
- **Review**: Fare estimate and route
- **Payment**: Payment method
- **Confirmation**: Driver details and live tracking

### 4. Events Booking Flow

**Flow Steps:**
1. Search Page → Event search
2. Event Listing → Event selection
3. Event Details → Ticket selection
4. Attendee Information
5. Review & Cart
6. Checkout
7. Payment
8. Confirmation

**Key Screens:**
- **Event Search**: Category, date, location filters
- **Event Listing**: Grid/list of events
- **Event Details**: Description, venue, date/time, pricing
- **Ticket Selection**: Quantity and ticket types
- **Attendee Info**: Name and contact for each ticket
- **Review**: Order summary
- **Payment**: Payment processing
- **Confirmation**: E-tickets

### 5. Spa & Wellness Services Booking Flow

**Flow Steps:**
1. Search Page → Service search
2. Service Listing → Service selection
3. Service Details → Time slot selection
4. Therapist/Provider selection (if applicable)
5. Guest Information
6. Review & Cart
7. Checkout
8. Payment
9. Confirmation

**Key Screens:**
- **Service Search**: Service type, location, date
- **Service Listing**: Available services with pricing
- **Service Details**: Description, duration, pricing
- **Time Slot Selection**: Available appointment times
- **Provider Selection**: Choose therapist/provider
- **Guest Info**: Personal information
- **Review**: Booking summary
- **Payment**: Payment processing
- **Confirmation**: Appointment details

## Shopping Cart & Checkout Flow

### Cart Page Components
- **Cart Header**: Item count, total amount
- **Cart Items**: 
  - Service type badge
  - Service details
  - Quantity controls
  - Price breakdown
  - Remove option
- **Cart Summary**:
  - Subtotal
  - Taxes and fees
  - Discount codes
  - Total amount
- **Checkout CTA**: Proceed to checkout button

### Checkout Flow
1. **Cart Review**: Verify all items
2. **Guest Information**: Contact details
3. **Payment Method**: Card, Wallet, Bank transfer
4. **Billing Address**: If different from guest
5. **Review Order**: Final summary
6. **Payment Processing**: Secure payment gateway
7. **Confirmation**: Success page with booking details

### Checkout Page Layout
- **Left Side (70%)**: 
  - Guest information form
  - Payment method selection
  - Billing address
- **Right Side (30%)**: 
  - Sticky order summary
  - Price breakdown
  - Promo code input
  - Terms and conditions
  - Place order button

## Booking Confirmation & Order Management

### Confirmation Page
- **Success Message**: Clear confirmation
- **Booking Reference**: Unique booking ID
- **Booking Details**: All service information
- **Action Buttons**:
  - View Booking Details
  - Download Receipt
  - Add to Calendar
  - Share Booking
  - Book Similar Service

### Order Management Screens

**My Bookings Page:**
- **Tabs**: Upcoming, Past, Cancelled
- **Booking Cards**:
  - Service type and name
  - Booking date and reference
  - Status badge
  - Key details (dates, location, etc.)
  - Actions (View, Modify, Cancel)
- **Filters**: Date range, service type, status
- **Search**: Find specific bookings

**Booking Details Page:**
- **Booking Header**: Status, reference number
- **Service Information**: Complete details
- **Timeline**: Booking journey status
- **Payment Information**: Amount, method, receipt
- **Actions**: 
  - Modify booking
  - Cancel booking
  - Contact support
  - Download invoice
  - Leave review

## High-Fidelity Web UI Components

### Header/Navigation
- Logo (left)
- Main navigation (center)
- Search bar (expandable)
- User account menu (right)
- Cart icon with badge count

### Footer
- Service links (columns)
- Company information
- Legal links
- Social media icons
- Newsletter signup
- Contact information

### Service Cards
- Image/thumbnail
- Service name and location
- Rating and review count
- Key features/icons
- Price (prominent)
- Quick action button
- Favorite/bookmark icon

### Forms
- Input fields with labels
- Error states and validation
- Help text
- Required field indicators
- Auto-save for multi-step forms

### Modals
- Booking confirmation modals
- Payment processing modals
- Error/success notifications
- Cancel booking confirmation

## Responsive Design Considerations

### Breakpoints
- **Mobile**: 320px - 767px
- **Tablet**: 768px - 1023px
- **Desktop**: 1024px - 1439px
- **Large Desktop**: 1440px+

### Mobile Adaptations
- Hamburger menu for navigation
- Full-width search bar
- Stacked filters (collapsible)
- Single column layout
- Bottom navigation bar (sticky)
- Simplified checkout flow
- Touch-optimized buttons (min 44px)

### Tablet Adaptations
- Two-column layouts where appropriate
- Sidebar navigation
- Optimized card grids
- Touch-friendly interactions

### Desktop Enhancements
- Multi-column layouts
- Hover states and interactions
- Keyboard navigation
- Advanced filtering options
- Comparison features

## Performance Considerations
- Lazy loading for images
- Infinite scroll or pagination
- Optimized image formats (WebP)
- Progressive loading
- Skeleton screens for loading states

## Empty States

### No Search Results
**Visual Design:**
- Large illustration or icon (centered)
- Heading: "No results found" (H3, Text-Secondary)
- Description: "We couldn't find any services matching your search. Try adjusting your filters or search terms."
- Suggested Actions:
  - "Clear all filters" button
  - "Browse all [service type]" link
  - Popular searches suggestions
- Layout: Centered, vertical stack, max-width 500px

### Empty Cart
**Visual Design:**
- Shopping cart icon (large, gray)
- Heading: "Your cart is empty" (H3)
- Description: "Start adding services to your cart to continue booking."
- CTA Button: "Browse Services" (Primary)
- Quick links to service categories
- Layout: Centered, vertical stack

### No Bookings
**Visual Design:**
- Calendar or booking icon (large, gray)
- Heading: "No bookings yet" (H3)
- Description: "You haven't made any bookings. Start exploring our services!"
- CTA Button: "Explore Services" (Primary)
- Featured services carousel
- Layout: Centered with suggestions below

### No Favorites
**Visual Design:**
- Heart icon (large, gray)
- Heading: "No favorites yet" (H3)
- Description: "Save your favorite services for quick access later."
- CTA Button: "Browse Services" (Primary)
- Layout: Centered

## Error States

### Form Validation Errors
**Visual Design:**
- Error message below input field
- Text color: Error-500 (#F44336)
- Icon: Error icon (16px) before message
- Message: Clear, actionable error text
- Input border: Error-500 color
- Background: Error-50 (#FFEBEE) for input background (optional)

**Error Message Examples:**
- "Please enter a valid email address"
- "Password must be at least 8 characters"
- "This field is required"
- "Date must be in the future"

### Network/API Errors
**Visual Design:**
- Error illustration or icon (centered)
- Heading: "Something went wrong" (H3, Error-500)
- Description: "We're having trouble loading this page. Please check your connection and try again."
- Error code: Displayed in small text (for debugging)
- Actions:
  - "Retry" button (Primary)
  - "Go back" link (Text button)
  - "Contact support" link

**Error Types:**
- 404 Not Found: "The page you're looking for doesn't exist"
- 500 Server Error: "Our servers are experiencing issues. Please try again later."
- Network Error: "Unable to connect. Please check your internet connection."
- Timeout: "Request took too long. Please try again."

### Payment Errors
**Visual Design:**
- Error icon (large, Error-500)
- Heading: "Payment Failed" (H3)
- Description: Specific error message (e.g., "Insufficient funds", "Card declined", "Expired card")
- Booking status: "Booking not confirmed"
- Actions:
  - "Try Different Payment Method" (Primary)
  - "Contact Support" (Secondary)
  - "View Booking Details" (Text)

### Booking Errors
**Visual Design:**
- Warning icon (large, Warning-500)
- Heading: "Booking Unavailable" (H3)
- Description: Specific reason (e.g., "This service is no longer available", "Selected dates are fully booked")
- Alternative suggestions: Similar services or alternative dates
- Actions:
  - "View Alternatives" (Primary)
  - "Modify Search" (Secondary)

## Loading States

### Page Loading
**Skeleton Screens:**
- Animated placeholder cards matching content layout
- Gray-200 background with pulse animation
- Border radius matching actual content
- Maintains layout structure during load
- Duration: Pulse animation 1.5s ease-in-out infinite

**Skeleton Components:**
- Service card skeleton: Image placeholder, text lines, button placeholder
- List skeleton: Multiple row placeholders
- Form skeleton: Input field placeholders
- Table skeleton: Header and row placeholders

### Button Loading State
**Visual Design:**
- Spinner icon replaces button text (centered)
- Spinner: 16px, Primary-500 color, rotating animation
- Button disabled during loading
- Text: "Processing..." (optional, below spinner)
- Maintains button dimensions

### Form Submission Loading
**Visual Design:**
- Overlay with spinner (if modal)
- Spinner: 40px, centered
- Message: "Processing your request..." (Body, Text-Secondary)
- Background: Semi-transparent overlay (Background-Overlay)
- Prevents multiple submissions

### Search Loading
**Visual Design:**
- Skeleton cards in results area
- Loading indicator in search bar (spinner, 20px)
- Maintains filter sidebar visibility
- Shows "Searching..." text (optional)

### Payment Processing
**Visual Design:**
- Full-screen overlay
- Large spinner (48px, Primary-500)
- Heading: "Processing Payment" (H3)
- Description: "Please wait while we process your payment. Do not close this window."
- Progress indicator (optional): Progress bar showing steps
- No cancel option during processing

### Data Fetching
**Visual Design:**
- Inline spinner where content will appear
- Small spinner (24px) for small data loads
- Skeleton screens for large data loads
- Maintains layout structure

## Success States & Feedback

### Success Messages
**Toast Notification:**
- Background: Success-500 (#4CAF50)
- Icon: Checkmark (white, 20px)
- Text: White, Body
- Position: Top-right (desktop), Bottom-center (mobile)
- Auto-dismiss: 5 seconds
- Animation: Slide in from top/bottom, fade out

**Success Modal:**
- Checkmark icon (large, Success-500, animated)
- Heading: "Success!" (H2)
- Description: Specific success message
- Actions: Primary CTA button
- Animation: Scale in (0.9 to 1.0) with fade

### Booking Confirmation Success
**Visual Design:**
- Success animation: Checkmark circle (animated)
- Confetti animation (optional, subtle)
- Heading: "Booking Confirmed!" (H2, Success-700)
- Booking reference: Large, prominent display
- Next steps: Clear list of actions
- Actions: Multiple CTAs (View Booking, Download Receipt, etc.)

### Form Submission Success
**Visual Design:**
- Success icon (large, Success-500)
- Heading: "Submitted Successfully" (H3)
- Description: Confirmation message
- Redirect or close button
- Auto-redirect after 3 seconds (optional)

## Notification System

### In-App Notifications
**Notification Center:**
- Bell icon in header with badge count
- Dropdown panel: 400px width, max-height 600px
- Notification items:
  - Icon (service type or action type)
  - Title (Bold, Body)
  - Message (Regular, Body-Small, Text-Secondary)
  - Timestamp (Caption, Text-Secondary)
  - Action button (if applicable)
- Unread indicator: Blue dot
- "Mark all as read" option
- Empty state: "No notifications"

### Push Notifications (Mobile)
**Notification Types:**
- Booking confirmations
- Booking reminders
- Status updates
- Promotional offers
- System alerts

**Notification Content:**
- Title: Clear, concise (max 50 chars)
- Body: Descriptive message (max 150 chars)
- Icon: Service type or app icon
- Action buttons: Up to 2 (e.g., "View", "Dismiss")

## Visual Feedback & Micro-interactions

### Hover States
- **Buttons**: Background color darkens, elevation increases
- **Cards**: Elevation increases, slight scale (1.02x)
- **Links**: Underline appears, color darkens
- **Icons**: Scale slightly (1.1x), color changes

### Click/Tap Feedback
- **Buttons**: Scale down (0.98x) on press, scale up on release
- **Cards**: Subtle scale down (0.99x)
- **Icons**: Scale animation (0.9x to 1.0x)
- Duration: 100-150ms

### Focus States
- **Input Fields**: Blue border (Primary-500), 2px outline
- **Buttons**: 2px outline (Primary-500), offset 2px
- **Links**: Underline, blue color
- **Keyboard Navigation**: Visible focus indicators on all interactive elements

### Progress Indicators
- **Multi-step Forms**: Progress bar at top, step indicators
- **File Upload**: Progress bar with percentage
- **Booking Process**: Step indicator showing current step
- **Loading Progress**: Determinate progress bar when possible

