# Mobile App – Customer Experience - UI/UX Design Specification

## Mobile App Architecture

### Bottom Navigation (Primary)
- Home
- Search
- Bookings
- Profile

### Secondary Navigation
- Service categories (horizontal scroll)
- Quick actions (floating buttons)
- Notifications (top bar)

## End-to-End User Flows

### Home Screen
**Components:**
- Search bar (prominent, top)
- Service category cards (horizontal scroll)
  - Flights
  - Hotels
  - Rides
  - Events
  - Spa & Wellness
- Featured deals carousel
- Recently viewed
- Recommended for you
- Quick booking shortcuts
- Notifications icon

**Interactions:**
- Swipe to browse categories
- Tap category to open service search
- Pull to refresh
- Scroll to load more

### Search & Service Listing Screens

**Search Screen:**
- Large search input
- Recent searches
- Popular searches
- Category shortcuts
- Location-based suggestions

**Service Listing Screen:**
- Search bar (sticky top)
- Filter button (top right)
- Sort options (dropdown)
- Service cards (vertical list):
  - Image (hero)
  - Service name
  - Location/destination
  - Rating and reviews
  - Price (prominent)
  - Quick view button
  - Favorite icon
- Map view toggle
- Load more (infinite scroll)

**Filter Sheet:**
- Slide-up bottom sheet
- Price range
- Rating
- Service-specific filters
- Apply/Clear buttons

## Booking Journeys

### 1. Flights Booking Journey

**Screens:**
1. **Flight Search**
   - Origin/Destination (with swap button)
   - Departure/Return dates
   - Passengers selector
   - Class selector
   - Search button

2. **Flight Results**
   - Filter and sort bar
   - Flight cards:
     - Airline logo
     - Departure/Arrival times
     - Duration
     - Stops
     - Price
     - Select button

3. **Flight Details**
   - Full itinerary
   - Baggage info
   - Cancellation policy
   - Price breakdown
   - Continue button

4. **Passenger Information**
   - Form for each passenger
   - Auto-fill from profile
   - Contact information
   - Continue button

5. **Seat Selection** (optional)
   - Seat map
   - Available/Occupied/Selected states
   - Price per seat
   - Skip option

6. **Add-ons**
   - Baggage options
   - Meals
   - Insurance
   - Continue button

7. **Review**
   - Complete booking summary
   - Total price
   - Terms checkbox
   - Proceed to payment

8. **Payment**
   - Payment method selection
   - Card input (if applicable)
   - Apply promo code
   - Pay button

9. **Confirmation**
   - Success animation
   - Booking reference
   - Ticket download
   - Add to calendar
   - View booking

### 2. Hotels Booking Journey

**Screens:**
1. **Hotel Search**
   - Location search
   - Check-in/out dates
   - Guests selector
   - Search button

2. **Hotel Results**
   - Map/List toggle
   - Hotel cards with images
   - Name, location, rating
   - Price per night
   - View details

3. **Hotel Details**
   - Image gallery (swipeable)
   - Name and rating
   - Location map
   - Amenities icons
   - Room types
   - Reviews section
   - Book now button

4. **Room Selection**
   - Available rooms
   - Room details and images
   - Price per night
   - Select room

5. **Guest Information**
   - Primary guest form
   - Additional guests
   - Special requests
   - Continue

6. **Review & Payment**
   - Booking summary
   - Total cost
   - Payment method
   - Confirm booking

7. **Confirmation**
   - Booking voucher
   - Hotel contact
   - Directions
   - Modify/Cancel options

### 3. Rides Booking Journey

**Screens:**
1. **Ride Request**
   - Map view (full screen)
   - Pickup location (current or search)
   - Dropoff location (search)
   - Vehicle type selector
   - Schedule option
   - Request ride button

2. **Vehicle Selection**
   - Economy, Premium, Luxury
   - Estimated fare
   - Estimated time
   - Select vehicle

3. **Review Ride**
   - Route on map
   - Distance and duration
   - Fare estimate
   - Payment method
   - Confirm ride

4. **Driver Matching**
   - Finding driver animation
   - Estimated arrival time

5. **Driver Assigned**
   - Driver details
   - Vehicle information
   - Live tracking map
   - Contact driver
   - Cancel ride option

6. **Ride in Progress**
   - Live tracking
   - Driver location
   - ETA updates
   - Contact options

7. **Ride Complete**
   - Fare breakdown
   - Payment processing
   - Rating driver
   - Receipt

### 4. Events Booking Journey

**Screens:**
1. **Event Search**
   - Category filters
   - Date selector
   - Location
   - Search

2. **Event Listing**
   - Event cards with images
   - Event name, date, venue
   - Price range
   - View details

3. **Event Details**
   - Hero image
   - Event information
   - Date and time
   - Venue details
   - Ticket types and pricing
   - Book tickets

4. **Ticket Selection**
   - Ticket type selector
   - Quantity stepper
   - Total price
   - Continue

5. **Attendee Information**
   - Name for each ticket
   - Contact information
   - Continue

6. **Review & Payment**
   - Order summary
   - Total cost
   - Payment
   - Confirm

7. **Confirmation**
   - E-tickets
   - QR codes
   - Event details
   - Add to calendar

### 5. Spa & Wellness Booking Journey

**Screens:**
1. **Service Search**
   - Service type
   - Location
   - Date
   - Search

2. **Service Listing**
   - Service cards
   - Service name, duration, price
   - Provider info
   - View details

3. **Service Details**
   - Service description
   - Duration and price
   - Provider information
   - Available time slots
   - Book appointment

4. **Time Slot Selection**
   - Calendar view
   - Available times
   - Select time slot

5. **Provider Selection** (if applicable)
   - Provider profiles
   - Ratings
   - Select provider

6. **Guest Information**
   - Personal details
   - Health information (if needed)
   - Special requests
   - Continue

7. **Review & Payment**
   - Appointment summary
   - Total cost
   - Payment
   - Confirm

8. **Confirmation**
   - Appointment details
   - Provider contact
   - Location map
   - Reminder settings

## Unified Cart & Checkout Experience

### Cart Screen
- **Header**: "Your Cart" with item count
- **Cart Items**:
  - Service type badge
  - Service thumbnail
  - Service name and key details
  - Quantity controls
  - Price
  - Remove option
  - Swipe to delete
- **Cart Summary**:
  - Subtotal
  - Fees
  - Promo code input
  - Total (prominent)
- **Checkout Button**: Full-width, sticky bottom

### Checkout Flow
1. **Review Cart**: Verify items
2. **Guest Information**: Contact details form
3. **Payment Method**: 
   - Saved cards
   - Add new card
   - Digital wallet options
4. **Review Order**: Final summary
5. **Payment Processing**: Loading state
6. **Confirmation**: Success screen

### Checkout Screen Layout
- Scrollable content area
- Sticky bottom bar with:
  - Order total
  - Place order button
- Progress indicator (steps)
- Auto-save form data

## Booking Status, Confirmations & History

### Booking Status Screen
- **Status Badge**: Upcoming, Completed, Cancelled
- **Timeline View**: Booking journey progress
- **Service Details**: Complete information
- **Actions**:
  - View full details
  - Modify booking
  - Cancel booking
  - Contact support
  - Download receipt
- **Notifications**: Status updates

### Booking Confirmation Screen
- Success animation/icon
- Booking reference number
- Service details summary
- Next steps information
- Action buttons:
  - View booking
  - Add to calendar
  - Share booking
  - Book similar

### Booking History Screen
- **Tabs**: Upcoming, Past, Cancelled
- **Booking Cards**:
  - Service type icon
  - Service name
  - Booking date
  - Status
  - Key details
  - Quick actions
- **Empty States**: 
  - No bookings message
  - Browse services CTA
- **Filters**: Date range, service type
- **Search**: Find specific bookings
- **Pull to Refresh**

### Booking Details Screen
- **Header**: Status badge, reference number
- **Service Information**: Complete details
- **Timeline**: Booking status updates
- **Payment Information**: Amount, method, receipt
- **Location/Map**: If applicable
- **Contact Information**: Support, provider
- **Actions Section**:
  - Modify booking
  - Cancel booking
  - Contact support
  - Download invoice
  - Leave review
  - Share booking

## High-Fidelity Mobile UI Components

### Navigation Components
- **Bottom Tab Bar**: 4-5 main sections
- **Top App Bar**: Title, actions, search
- **Floating Action Button**: Primary action
- **Drawer Navigation**: Secondary navigation

### Input Components
- **Text Input**: With labels and validation
- **Date Picker**: Native calendar picker
- **Time Picker**: Scrollable time selector
- **Location Picker**: Map-based selection
- **Stepper**: Quantity controls
- **Toggle Switch**: On/off options

### Display Components
- **Service Cards**: Image, title, details, price
- **Booking Cards**: Status, details, actions
- **Status Badges**: Color-coded states
- **Price Display**: Large, prominent
- **Rating Display**: Stars with count
- **Timeline Component**: Booking progress

### Interactive Components
- **Bottom Sheet**: Filters, options
- **Modal**: Confirmations, details
- **Toast Notifications**: Success, error messages
- **Loading States**: Skeleton screens, spinners
- **Pull to Refresh**: Refresh content
- **Swipe Actions**: Delete, favorite

### Map Components
- **Full Screen Map**: For rides, hotels
- **Inline Map**: For service locations
- **Route Display**: For navigation
- **Marker Clusters**: For multiple locations

## Mobile-Specific Considerations

### Gestures
- Swipe to navigate (back, forward)
- Swipe to delete (cart items)
- Pull to refresh
- Long press for context menu
- Pinch to zoom (maps, images)

### Touch Targets
- Minimum 44x44px for all interactive elements
- Adequate spacing between buttons
- Thumb-friendly zones (bottom area)

### Performance
- Optimized images (WebP, compression)
- Lazy loading
- Infinite scroll
- Cached data
- Offline support (view bookings)

### Platform-Specific
- **iOS**: Native iOS design patterns
- **Android**: Material Design guidelines
- **Cross-platform**: Consistent experience

### Notifications
- Push notifications for:
  - Booking confirmations
  - Status updates
  - Reminders
  - Promotions
- In-app notifications center

## Interactive Prototype Requirements

### Figma Prototype Features
- **Navigation**: Between all screens
- **Form Interactions**: Input fields, selections
- **Button States**: Default, pressed, loading
- **Transitions**: Smooth page transitions
- **Micro-interactions**: 
  - Button presses
  - Card taps
  - Swipe gestures
  - Loading animations
- **User Flows**: Complete booking journeys
- **Error States**: Validation, network errors
- **Empty States**: No results, no bookings

### Prototype Scenarios
1. Complete flight booking flow
2. Hotel search and booking
3. Ride request and tracking
4. Event ticket purchase
5. Spa appointment booking
6. Cart with multiple services
7. Booking management
8. Profile and settings

## Empty States (Mobile)

### No Search Results
**Visual Design:**
- Large illustration (centered, 200px height)
- Heading: "No results found" (H3, centered, Text-Secondary)
- Description: "Try adjusting your search or filters" (Body, centered, Text-Secondary)
- Actions:
  - "Clear Filters" button (Secondary, full-width)
  - "Browse All" link (Text button)
- Popular searches: Horizontal scroll chips
- Layout: Centered, vertical stack, padding 32px

### Empty Cart
**Visual Design:**
- Shopping cart icon (120px, Gray-400)
- Heading: "Your cart is empty" (H3, centered)
- Description: "Add services to get started" (Body, centered, Text-Secondary)
- CTA: "Browse Services" button (Primary, full-width, 48px height)
- Quick access: Service category chips (horizontal scroll)
- Layout: Centered, vertical stack

### No Bookings
**Visual Design:**
- Calendar icon (120px, Gray-400)
- Heading: "No bookings yet" (H3, centered)
- Description: "Your booking history will appear here" (Body, centered, Text-Secondary)
- CTA: "Explore Services" button (Primary, full-width)
- Featured services: Horizontal carousel below
- Layout: Centered with suggestions

### No Favorites
**Visual Design:**
- Heart icon (120px, Gray-400, outline style)
- Heading: "No favorites saved" (H3, centered)
- Description: "Tap the heart icon to save services you love" (Body, centered, Text-Secondary)
- CTA: "Discover Services" button (Primary, full-width)
- Layout: Centered

### No Notifications
**Visual Design:**
- Bell icon (120px, Gray-400, outline style)
- Heading: "All caught up!" (H3, centered)
- Description: "You have no new notifications" (Body, centered, Text-Secondary)
- Layout: Centered

## Error States (Mobile)

### Form Validation Errors
**Visual Design:**
- Error message below input (Body-Small, Error-500)
- Error icon (16px) before message
- Input border: Error-500 (2px)
- Input background: Error-50 (subtle)
- Message: Clear, actionable text
- Shake animation on error (200ms)

**Common Errors:**
- "Please enter a valid email"
- "Password must be 8+ characters"
- "This field is required"
- "Phone number is invalid"

### Network Errors
**Visual Design:**
- Error illustration (200px, centered)
- Heading: "Connection Error" (H3, Error-500, centered)
- Description: "Check your internet connection and try again" (Body, centered)
- Error code: Small text (Caption, Gray-500)
- Actions:
  - "Retry" button (Primary, full-width, 48px)
  - "Go Back" link (Text button, centered)
- Layout: Centered, vertical stack, padding 24px

### Payment Errors
**Visual Design:**
- Error icon (120px, Error-500, centered)
- Heading: "Payment Failed" (H3, centered)
- Description: Specific error message (Body, centered)
- Booking status: Badge (Error, "Not Confirmed")
- Actions:
  - "Try Again" button (Primary, full-width)
  - "Change Payment Method" button (Secondary, full-width)
  - "Contact Support" link (Text, centered)
- Layout: Centered, vertical stack

### Booking Errors
**Visual Design:**
- Warning icon (120px, Warning-500, centered)
- Heading: "Booking Unavailable" (H3, centered)
- Description: Specific reason (Body, centered)
- Alternative suggestions: Cards below
- Actions:
  - "View Alternatives" button (Primary, full-width)
  - "Modify Search" button (Secondary, full-width)
- Layout: Centered with suggestions

### Offline State
**Visual Design:**
- Offline icon (120px, Gray-500, centered)
- Heading: "You're Offline" (H3, centered)
- Description: "Connect to the internet to continue" (Body, centered)
- Retry indicator: Spinner when reconnecting
- Cached content: Show if available with offline badge
- Layout: Centered

## Loading States (Mobile)

### Page Loading
**Skeleton Screens:**
- Animated placeholders matching content
- Gray-200 background, pulse animation
- Border radius: 8px
- Maintains layout structure
- Animation: 1.5s ease-in-out infinite

**Skeleton Types:**
- List skeleton: Multiple card placeholders
- Detail skeleton: Image, text lines, button
- Form skeleton: Input field placeholders
- Grid skeleton: Card grid placeholders

### Button Loading
**Visual Design:**
- Spinner (20px) replaces text
- Spinner color: Primary-500
- Button disabled, maintains size
- Optional: "Loading..." text below spinner
- Full-width buttons: Spinner centered

### Pull to Refresh
**Visual Design:**
- Spinner at top of list (40px)
- Message: "Refreshing..." (Body-Small)
- Animation: Pull down to trigger
- Release to refresh
- Success: Brief checkmark animation

### Infinite Scroll Loading
**Visual Design:**
- Spinner at bottom of list (32px)
- Message: "Loading more..." (Body-Small, centered)
- Appears when scrolling near bottom
- Replaces with content when loaded

### Payment Processing
**Visual Design:**
- Full-screen overlay (Background-Overlay)
- Large spinner (64px, Primary-500, centered)
- Heading: "Processing Payment" (H3, white, centered)
- Description: "Please wait..." (Body, white, centered)
- Progress steps: Optional step indicator
- No close option during processing
- Layout: Centered, vertical stack

### Image Loading
**Visual Design:**
- Placeholder: Gray-200 background
- Blur-up effect: Low-res to high-res
- Skeleton: Aspect ratio maintained
- Error fallback: Broken image icon

## Success States & Feedback (Mobile)

### Success Toast
**Visual Design:**
- Bottom sheet style (mobile)
- Background: Success-500
- Icon: Checkmark (white, 24px)
- Message: White text (Body)
- Auto-dismiss: 3 seconds
- Swipe down to dismiss
- Animation: Slide up from bottom

### Booking Confirmation
**Visual Design:**
- Success animation: Animated checkmark (200px)
- Confetti effect (optional, subtle)
- Heading: "Booking Confirmed!" (H2, Success-700, centered)
- Booking reference: Large, prominent (H1, centered)
- Next steps: List with icons
- Actions:
  - "View Booking" button (Primary, full-width)
  - "Download Receipt" button (Secondary, full-width)
  - "Share" button (Text, centered)
- Layout: Centered, vertical stack

### Form Success
**Visual Design:**
- Success icon (80px, Success-500, centered)
- Heading: "Success!" (H3, centered)
- Description: Confirmation message (Body, centered)
- Auto-close: After 2 seconds
- Manual close: X button (top-right)

## Haptic Feedback

### Touch Interactions
- **Button Press**: Light haptic feedback
- **Success Action**: Success haptic (double tap)
- **Error Action**: Error haptic (strong tap)
- **Swipe Actions**: Medium haptic
- **Pull to Refresh**: Light haptic on release

### Haptic Patterns
- Light: Subtle vibration (10ms)
- Medium: Standard vibration (20ms)
- Strong: Strong vibration (30ms)
- Success: Double light tap
- Error: Single strong tap

## Gesture Interactions

### Swipe Gestures
- **Swipe Right**: Go back (navigation)
- **Swipe Left**: Delete/Remove (with confirmation)
- **Swipe Up**: Dismiss bottom sheet
- **Swipe Down**: Pull to refresh
- **Long Press**: Context menu or selection

### Pinch & Zoom
- **Images**: Pinch to zoom (gallery view)
- **Maps**: Pinch to zoom, pan to move
- **Double Tap**: Zoom in/out

### Drag Interactions
- **Bottom Sheet**: Drag down to dismiss
- **Cards**: Drag to reveal actions
- **Sliders**: Drag to adjust values

