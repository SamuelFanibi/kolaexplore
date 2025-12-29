# Detailed Booking Flows - Complete Specifications

This document provides comprehensive, step-by-step booking flow specifications for all service types in the KolaExplore platform.

## Table of Contents

1. [Flights Booking Flow](#flights-booking-flow)
2. [Accommodation Booking Flow](#accommodation-booking-flow)
3. [Airport Shuttle Pick Up](#airport-shuttle-pick-up)
4. [Chauffeur Car Services](#chauffeur-car-services)
5. [Fine Dining / Restaurants](#fine-dining--restaurants)
6. [Nightlife / Lounge](#nightlife--lounge)
7. [Events / Attractions](#events--attractions)
8. [Customize Personal / Getaway Experience](#customize-personal--getaway-experience)

---

## Flights Booking Flow

### Step 1: Flight Search

**Screen Components:**
- **Service Type Selector**: "Flights" (pre-selected or selected)
- **Trip Type Selector**:
  - Radio buttons or toggle: "One Way" | "Return"
  - Default: "Return"
- **Location Inputs**:
  - **Departure Location**: 
    - Input field with autocomplete
    - Airport code or city name
    - Icon: Departure/plane icon
    - Placeholder: "From (city or airport)"
  - **Destination Location**:
    - Input field with autocomplete
    - Airport code or city name
    - Icon: Destination/plane icon
    - Placeholder: "To (city or airport)"
  - **Swap Button**: Icon button between fields to swap origin/destination
- **Date Selection**:
  - **Departure Date**:
    - Date picker (always visible)
    - Calendar widget
    - Placeholder: "Departure date"
  - **Return Date**:
    - Date picker (visible only if "Return" selected)
    - Calendar widget
    - Placeholder: "Return date"
    - Disabled if "One Way" selected
- **Date Range Selector**:
  - Toggle: "+/- Date Range"
  - When enabled: Shows flexible date range (±3 days)
  - Visual indicator: "Flexible dates" badge
- **Passenger Selection**:
  - **Adults**: 
    - Stepper control (default: 1)
    - Min: 1, Max: 9
    - Label: "Adults (12+ years)"
  - **Children**:
    - Stepper control (default: 0)
    - Min: 0, Max: 9
    - Label: "Children (2-11 years)"
    - Expandable section: Child age selection (if children > 0)
  - **Infants** (optional):
    - Stepper control (default: 0)
    - Label: "Infants (under 2)"
- **Class Selection** (optional):
  - Dropdown: Economy, Premium Economy, Business, First Class
  - Default: Economy
- **Search Button**: 
  - Primary CTA button
  - Text: "Search Flights"
  - Full width on mobile, fixed width on desktop

**Validation:**
- Departure and destination must be different
- Departure date must be today or future
- Return date must be after departure date (if return selected)
- At least 1 adult required
- Total passengers cannot exceed 9

**User Actions:**
1. Select trip type (One Way or Return)
2. Enter departure location (autocomplete suggestions)
3. Enter destination location (autocomplete suggestions)
4. Select departure date from calendar
5. Select return date (if Return selected)
6. Optionally enable flexible date range
7. Select number of adults and children
8. Optionally select class
9. Click "Search Flights"

### Step 2: Flight Results

**Screen Components:**
- **Search Summary Bar** (sticky top):
  - Route: "Lagos → London"
  - Dates: "Dec 15 - Dec 22, 2024"
  - Passengers: "2 Adults, 1 Child"
  - "Modify Search" button (link)
- **Filters Sidebar** (left, desktop):
  - **Price Range**: Slider (min to max)
  - **Airlines**: Checkboxes (multiple selection)
  - **Stops**: Radio buttons (Non-stop, 1 Stop, 2+ Stops)
  - **Departure Time**: Time range sliders (Morning, Afternoon, Evening, Night)
  - **Arrival Time**: Time range sliders
  - **Duration**: Slider (shortest to longest)
  - **Aircraft Type**: Checkboxes
  - **Clear Filters** button
- **Sort Options** (top of results):
  - Dropdown: "Sort by"
  - Options: Price (Low to High), Price (High to Low), Duration (Shortest), Departure Time, Arrival Time, Best Match
- **View Toggle**:
  - Grid view icon
  - List view icon
- **Flight Cards**:
  - **Airline Logo**: Left side
  - **Flight Details**:
    - Departure time and airport code
    - Duration (with layover info if applicable)
    - Arrival time and airport code
    - Stops indicator (Non-stop badge or "1 stop in [city]")
  - **Price**: Large, prominent (currency symbol)
  - **Select Button**: Primary button
  - **Fare Details Link**: "View fare details"
  - **Baggage Info**: Icon with tooltip
- **Pagination** (if applicable):
  - Page numbers
  - "Load More" button (infinite scroll alternative)
- **Map View Toggle** (optional):
  - Toggle to show route on map

**Empty State:**
- If no results: "No flights found for your search criteria"
- "Modify Search" button
- Popular routes suggestions

**User Actions:**
1. Review flight options
2. Apply filters (price, stops, time, etc.)
3. Sort results
4. View flight details
5. Select preferred flight
6. Click "Select" button

### Step 3: Flight Details & Selection

**Screen Components:**
- **Selected Flight Summary**:
  - Outbound flight card (if return trip)
  - Return flight selection (if return trip)
  - Total price display
- **Return Flight Selection** (if return trip):
  - Same flight results interface
  - "Select Return Flight" section
- **Fare Breakdown**:
  - Base fare
  - Taxes and fees
  - Total per passenger
  - Grand total
- **Baggage Information**:
  - Included baggage (hand luggage, checked)
  - Additional baggage options (with pricing)
- **Cancellation Policy**:
  - Refundable/Non-refundable indicator
  - Cancellation fees
  - Change policy
- **Continue Button**: Primary CTA

**User Actions:**
1. Review selected flight details
2. Select return flight (if applicable)
3. Review fare breakdown
4. Review policies
5. Click "Continue" or "Add to Cart"

### Step 4: Passenger Information

**Screen Components:**
- **Progress Indicator**: Step 3 of 6 (or appropriate step number)
- **Passenger Forms** (one per passenger):
  - **Title**: Dropdown (Mr, Mrs, Miss, Ms, Dr)
  - **First Name**: Text input (required)
  - **Last Name**: Text input (required)
  - **Date of Birth**: Date picker (required)
  - **Gender**: Radio buttons (Male, Female, Other)
  - **Nationality**: Dropdown (country selection)
  - **Passport Number** (for international flights):
    - Text input
    - "I don't have a passport number" checkbox
  - **Passport Expiry Date** (if passport provided)
  - **Passport Issuing Country** (if passport provided)
- **Contact Information**:
  - **Email Address**: Email input (required)
  - **Phone Number**: Phone input with country code (required)
  - **Alternative Phone** (optional)
- **Special Requests** (optional):
  - Textarea: Dietary requirements, special assistance, etc.
- **Continue Button**: Primary CTA

**Validation:**
- All required fields must be filled
- Email format validation
- Phone number format validation
- Passport number format (if provided)
- Date of birth must be valid

**User Actions:**
1. Fill in passenger details for each traveler
2. Enter contact information
3. Add special requests (optional)
4. Click "Continue"

### Step 5: Account Creation or Guest Checkout

**Screen Components:**
- **Account Options**:
  - **Option 1: Continue as Guest**
    - Checkbox: "Continue as guest"
    - Description: "Complete your booking without creating an account"
  - **Option 2: Create Account**
    - Checkbox: "Create an account to manage bookings"
    - **Password Field**: 
      - Text input (type: password)
      - Password strength indicator
      - Requirements shown (min 8 chars, etc.)
    - **Confirm Password Field**:
      - Text input (type: password)
      - Match validation
- **Email Verification** (if account creation selected):
  - Info message: "A verification email will be sent to [email]"
  - "Resend verification email" link (after initial send)
- **Benefits of Account** (if account creation):
  - Bullet list:
    - Manage all bookings in one place
    - Faster checkout for future bookings
    - Exclusive deals and offers
    - Booking history and receipts
- **Continue Button**: Primary CTA

**Email Verification Flow:**
- Email sent immediately upon account creation
- Verification modal/popup: "Please check your email to verify your account"
- "Resend Email" button
- "I've verified my email" button (after user verifies)
- Link expires after 24 hours

**User Actions:**
1. Choose guest checkout or create account
2. If creating account: Enter password
3. If creating account: Confirm password
4. Review email verification message
5. Click "Continue"
6. (If account created) Check email and verify
7. Click "I've verified my email" or continue

### Step 6: Seat Selection (Optional)

**Screen Components:**
- **Skip Option**: "Skip seat selection" link (top right)
- **Seat Map**:
  - Visual aircraft layout
  - **Seat States**:
    - Available: Gray/white (clickable)
    - Selected: Primary-500 (highlighted)
    - Occupied: Gray-300 (disabled)
    - Premium: Gold/border (with pricing)
    - Exit row: Special indicator
  - **Legend**: Seat type explanations
- **Seat Information**:
  - Seat number display
  - Seat type (Standard, Premium, Exit Row)
  - Price (if premium seat)
- **Selected Seats Summary**:
  - List of selected seats
  - Total seat selection cost
- **Continue Button**: Primary CTA

**User Actions:**
1. View seat map
2. Select seats for each passenger
3. Review selected seats and pricing
4. Click "Continue" or "Skip"

### Step 7: Add-ons Selection

**Screen Components:**
- **Baggage Options**:
  - Included baggage display
  - Additional baggage options:
    - Checkbox: "Add 15kg checked baggage" (+$XX)
    - Checkbox: "Add 23kg checked baggage" (+$XX)
    - Checkbox: "Add 32kg checked baggage" (+$XX)
- **Meal Options**:
  - Checkbox list:
    - "Vegetarian meal" (free)
    - "Halal meal" (free)
    - "Kosher meal" (free)
    - "Special dietary meal" (free, with details input)
- **Travel Insurance**:
  - Toggle: "Add travel insurance"
  - Coverage details (expandable)
  - Price display
- **Airport Lounge Access**:
  - Checkbox: "Add lounge access" (+$XX)
  - Details and benefits
- **Priority Boarding**:
  - Checkbox: "Add priority boarding" (+$XX)
- **Add-ons Summary**:
  - List of selected add-ons
  - Total add-ons cost
- **Continue Button**: Primary CTA

**User Actions:**
1. Review included services
2. Select additional baggage (if needed)
3. Select meal preferences
4. Add travel insurance (optional)
5. Add other add-ons (optional)
6. Review add-ons summary
7. Click "Continue"

### Step 8: Review & Add to Cart

**Screen Components:**
- **Booking Summary**:
  - Flight details (outbound and return)
  - Passenger names
  - Selected seats (if selected)
  - Add-ons list
- **Price Breakdown**:
  - Flight fare: $XXX
  - Seat selection: $XXX (if applicable)
  - Add-ons: $XXX
  - Taxes and fees: $XXX
  - **Total**: Large, prominent
- **Terms and Conditions**:
  - Checkbox: "I agree to terms and conditions"
  - Link to full terms
- **Action Buttons**:
  - "Add to Cart" button (Primary)
  - "Book Now" button (Secondary, direct booking)
- **Save for Later** (optional):
  - "Save booking" link

**User Actions:**
1. Review complete booking summary
2. Review price breakdown
3. Accept terms and conditions
4. Click "Add to Cart" or "Book Now"

---

## Accommodation Booking Flow

### Accommodation Types
- Hotels
- Short Stay
- Airbnb / Others

### Step 1: Accommodation Search

**Screen Components:**
- **Service Type Selector**: "Accommodation" (pre-selected)
- **Accommodation Type Filter**:
  - Tabs or buttons: "All" | "Hotels" | "Short Stay" | "Airbnb"
  - Default: "All"
- **Location Search**:
  - Input field with autocomplete
  - Placeholder: "Where are you going?"
  - Location suggestions (cities, landmarks, areas)
  - Map pin icon
- **Date Selection**:
  - **Check-in Date**:
    - Date picker
    - Calendar widget
    - Placeholder: "Check-in"
  - **Check-out Date**:
    - Date picker
    - Calendar widget
    - Placeholder: "Check-out"
  - **Duration Display**: "X nights" (calculated automatically)
- **Guests Selection**:
  - **Adults**: Stepper (default: 2, min: 1, max: 20)
  - **Children**: Stepper (default: 0, min: 0, max: 10)
  - **Rooms**: Stepper (default: 1, min: 1, max: 10)
  - Expandable panel with guest details
- **Search Button**: Primary CTA

**Validation:**
- Location required
- Check-in date must be today or future
- Check-out date must be after check-in
- Minimum 1 night stay
- At least 1 adult required

**User Actions:**
1. Select accommodation type (if filtering)
2. Enter location
3. Select check-in date
4. Select check-out date
5. Select number of guests and rooms
6. Click "Search"

### Step 2: Accommodation Results

**Screen Components:**
- **Search Summary Bar**:
  - Location: "Lagos, Nigeria"
  - Dates: "Dec 15 - Dec 18, 2024 (3 nights)"
  - Guests: "2 Adults, 1 Room"
  - "Modify Search" button
- **Filters Sidebar** (left, desktop):
  - **Price Range**: Slider
  - **Star Rating**: Checkboxes (1-5 stars)
  - **Accommodation Type**: Checkboxes (Hotel, Apartment, Villa, etc.)
  - **Amenities**: Checkboxes (WiFi, Pool, Gym, Parking, etc.)
  - **Property Type**: Checkboxes
  - **Guest Rating**: Slider (minimum rating)
  - **Instant Booking**: Toggle
  - **Free Cancellation**: Toggle
- **View Toggle**:
  - List view
  - Grid view
  - Map view
- **Accommodation Cards**:
  - **Image Gallery**: Hero image with thumbnail strip
  - **Name**: Property name (H3)
  - **Location**: Address with distance from city center
  - **Rating**: Star rating with review count
  - **Amenities Icons**: WiFi, Pool, Gym, etc.
  - **Price**: Per night (large, prominent)
  - **Total Price**: For stay duration
  - **Discount Badge** (if applicable)
  - **Free Cancellation Badge** (if applicable)
  - **"View Details" Button**: Primary button
- **Sort Options**:
  - Dropdown: "Sort by"
  - Options: Recommended, Price (Low to High), Price (High to Low), Rating, Distance

**User Actions:**
1. Browse accommodation options
2. Apply filters
3. View on map (if map view)
4. Click "View Details" on preferred property

### Step 3: Accommodation Details

**Screen Components:**
- **Image Gallery**:
  - Large hero image
  - Thumbnail strip below
  - Full-screen gallery view
- **Property Information**:
  - **Name**: Large heading
  - **Location**: Address with map
  - **Rating**: Stars with review count
  - **Property Type**: Badge (Hotel, Apartment, etc.)
- **Booking Widget** (sticky sidebar, right):
  - Check-in/out dates (editable)
  - Guests selector
  - Room selector
  - Price per night
  - Total price for stay
  - Taxes and fees breakdown
  - "Select Room" or "Book Now" button
- **Description**:
  - Full property description
  - Key features list
- **Amenities**:
  - Icons grid: WiFi, Pool, Gym, Parking, etc.
  - Expandable "View all amenities"
- **Room Types** (if hotel):
  - Room cards with:
    - Room name
    - Images
    - Bed configuration
    - Amenities
    - Price per night
    - "Select Room" button
- **Location Map**:
  - Interactive map
  - Nearby attractions
  - Distance markers
- **Reviews Section**:
  - Overall rating breakdown
  - Review cards with:
    - User name and avatar
    - Rating (stars)
    - Review text
    - Date
  - "View all reviews" link
- **Policies**:
  - Check-in/out times
  - Cancellation policy
  - House rules
  - Payment policy

**User Actions:**
1. Browse property images
2. Read description and amenities
3. Review room types (if applicable)
4. Check location on map
5. Read reviews
6. Review policies
7. Select dates and guests in booking widget
8. Click "Select Room" or "Book Now"

### Step 4: Room Selection (Hotels)

**Screen Components:**
- **Selected Property Summary**: Name and location
- **Available Rooms**:
  - **Room Cards**:
    - Room images (gallery)
    - Room name/type
    - Bed configuration
    - Room size
    - Max occupancy
    - Amenities list
    - Cancellation policy
    - **Price**: Per night and total
    - **"Select Room" Button**: Primary button
- **Room Comparison** (optional):
  - Side-by-side comparison
  - Feature comparison table
- **Continue Button**: After room selection

**User Actions:**
1. Browse available rooms
2. Compare room options
3. Select preferred room
4. Click "Continue" or "Add to Cart"

### Step 5: Guest Information & Special Requests

**Screen Components:**
- **Guest Information Form**:
  - **Primary Guest**:
    - Title: Dropdown
    - First Name: Text input
    - Last Name: Text input
    - Email: Email input
    - Phone: Phone input with country code
  - **Additional Guests** (if applicable):
    - Repeat form for each guest
  - **Special Requests** (optional):
    - Textarea: "Any special requests?"
    - Examples: Early check-in, late check-out, room preferences
  - **Loyalty Program** (if applicable):
    - Input: Loyalty number
- **Continue Button**: Primary CTA

**User Actions:**
1. Fill in primary guest information
2. Add additional guests (if needed)
3. Add special requests (optional)
4. Enter loyalty number (if applicable)
5. Click "Continue"

### Step 6: Review & Add to Cart

**Screen Components:**
- **Booking Summary**:
  - Property name and location
  - Check-in/out dates
  - Duration (nights)
  - Room type (if hotel)
  - Guests information
  - Special requests
- **Price Breakdown**:
  - Room rate: $XXX per night × X nights
  - Taxes and fees: $XXX
  - Service charge: $XXX
  - **Total**: Large, prominent
- **Cancellation Policy**:
  - Policy summary
  - Full policy link
- **Terms and Conditions**:
  - Checkbox: "I agree to terms and conditions"
- **Action Buttons**:
  - "Add to Cart" button (Primary)
  - "Book Now" button (Secondary)

**User Actions:**
1. Review booking summary
2. Review price breakdown
3. Review cancellation policy
4. Accept terms
5. Click "Add to Cart" or "Book Now"

---

## Airport Shuttle Pick Up

### Step 1: Shuttle Search

**Screen Components:**
- **Service Type**: "Airport Shuttle" (pre-selected)
- **Arrival Date Selection**:
  - Date picker
  - Calendar widget
  - Placeholder: "Arrival date"
- **Arrival Time Selection**:
  - Time picker
  - Format: HH:MM (24-hour or 12-hour)
  - Placeholder: "Arrival time"
  - Flight number input (optional):
    - Text input: "Flight number (optional)"
    - Auto-adjust time based on flight (if flight number provided)
- **Drop-off Location**:
  - Input field with autocomplete
  - Placeholder: "Where would you like to be dropped off?"
  - Location suggestions
  - Map icon
- **Pick-up Location** (auto-filled):
  - Display: Airport name
  - Non-editable (or editable with airport selector)
- **Passengers Selection**:
  - Stepper: Number of passengers
  - Default: 1, Min: 1, Max: 8
- **Luggage Selection** (optional):
  - Stepper: Number of large bags
  - Stepper: Number of small bags
- **Search Button**: Primary CTA

**Validation:**
- Arrival date required (today or future)
- Arrival time required
- Drop-off location required
- At least 1 passenger required

**User Actions:**
1. Select arrival date
2. Select arrival time
3. Enter flight number (optional)
4. Enter drop-off location
5. Select number of passengers
6. Select luggage (optional)
7. Click "Search"

### Step 2: Shuttle Options

**Screen Components:**
- **Search Summary**:
  - Route: "Airport → [Drop-off location]"
  - Date and time
  - Passengers
- **Shuttle Type Cards**:
  - **Economy Shuttle**:
    - Image/icon
    - Capacity: "Up to 4 passengers"
    - Features: Shared ride, WiFi, Air conditioning
    - Price: Per person or fixed
    - "Select" button
  - **Private Shuttle**:
    - Image/icon
    - Capacity: "Up to 4 passengers"
    - Features: Private vehicle, Direct route, WiFi
    - Price: Fixed price
    - "Select" button
  - **Luxury Shuttle**:
    - Image/icon
    - Capacity: "Up to 6 passengers"
    - Features: Premium vehicle, Complimentary water, WiFi
    - Price: Fixed price
    - "Select" button
  - **VIP Shuttle**:
    - Image/icon
    - Capacity: "Up to 8 passengers"
    - Features: Luxury vehicle, Meet & greet, Premium service
    - Price: Fixed price
    - "Select" button
- **Route Information**:
  - Estimated distance
  - Estimated duration
  - Route map preview
- **Price Display**: Large, prominent per option

**User Actions:**
1. Review shuttle options
2. Compare features and prices
3. Select preferred shuttle type
4. Click "Select"

### Step 3: Guest Information

**Screen Components:**
- **Contact Information**:
  - Name: Text input
  - Email: Email input
  - Phone: Phone input with country code
- **Flight Information** (if not provided earlier):
  - Flight number: Text input
  - Airline: Dropdown
- **Special Requests** (optional):
  - Textarea: "Any special requests?"
  - Examples: Child seat, wheelchair access, etc.
- **Continue Button**: Primary CTA

**User Actions:**
1. Enter contact information
2. Enter flight information (if not provided)
3. Add special requests (optional)
4. Click "Continue"

### Step 4: Review & Add to Cart

**Screen Components:**
- **Booking Summary**:
  - Shuttle type
  - Route: Airport → Drop-off location
  - Date and time
  - Passengers
  - Flight information
- **Price Breakdown**:
  - Shuttle fare: $XXX
  - Taxes and fees: $XXX
  - **Total**: Large, prominent
- **Terms and Conditions**:
  - Checkbox: "I agree to terms and conditions"
- **Action Buttons**:
  - "Add to Cart" button (Primary)
  - "Book Now" button (Secondary)

**User Actions:**
1. Review booking summary
2. Review price
3. Accept terms
4. Click "Add to Cart" or "Book Now"

---

## Chauffeur Car Services

### Step 1: Chauffeur Service Search

**Screen Components:**
- **Service Type**: "Chauffeur Services" (pre-selected)
- **Service Type Selection**:
  - Radio buttons or tabs:
    - "Airport Pick-up"
    - "Point-to-Point"
    - "Hourly Service"
  - Default: "Point-to-Point"
- **Airport Pick-up Fields** (if Airport Pick-up selected):
  - **Arrival Date**: Date picker
  - **Arrival Time**: Time picker
  - **Flight Number** (optional): Text input
  - **Pick-up Location**: Auto-filled (Airport name)
- **Point-to-Point Fields** (if Point-to-Point selected):
  - **Pick-up Location**: Input with autocomplete
  - **Drop-off Location**: Input with autocomplete
  - **Date**: Date picker
  - **Time**: Time picker
- **Hourly Service Fields** (if Hourly Service selected):
  - **Start Location**: Input with autocomplete
  - **Date**: Date picker
  - **Start Time**: Time picker
  - **Duration**: Hours selector (stepper or dropdown)
- **Passengers**: Stepper (default: 1, min: 1, max: based on vehicle)
- **Search Button**: Primary CTA

**User Actions:**
1. Select service type
2. Fill in location and time details based on service type
3. Select number of passengers
4. Click "Search"

### Step 2: Available Chauffeur Cars

**Screen Components:**
- **Search Summary**: Route, date, time, passengers
- **Vehicle Options**:
  - **Sedan**:
    - Image
    - Capacity: "Up to 3 passengers"
    - Features: Luxury sedan, Professional driver, WiFi
    - Price: Per hour or fixed
    - "Select" button
  - **SUV**:
    - Image
    - Capacity: "Up to 6 passengers"
    - Features: Spacious, Premium, WiFi
    - Price: Per hour or fixed
    - "Select" button
  - **Luxury Sedan**:
    - Image
    - Capacity: "Up to 3 passengers"
    - Features: Premium luxury, Leather seats, WiFi, Refreshments
    - Price: Per hour or fixed
    - "Select" button
  - **Luxury SUV**:
    - Image
    - Capacity: "Up to 6 passengers"
    - Features: Premium luxury, Spacious, All amenities
    - Price: Per hour or fixed
    - "Select" button
- **Date Range Selection** (for hourly service):
  - Calendar widget
  - Select start and end dates
- **Hours Selection** (for hourly service):
  - Stepper or dropdown
  - Minimum: 2 hours
  - Maximum: 24 hours
- **Price Calculator** (for hourly service):
  - Base rate × hours
  - Total display

**User Actions:**
1. Browse available vehicles
2. Select vehicle type
3. Select date range (if hourly)
4. Select number of hours (if hourly)
5. Review pricing
6. Click "Select"

### Step 3: Guest Information

**Screen Components:**
- **Contact Information**:
  - Name: Text input
  - Email: Email input
  - Phone: Phone input
- **Flight Information** (if airport pick-up):
  - Flight number: Text input
  - Airline: Dropdown
- **Special Requests** (optional):
  - Textarea: "Any special requests?"
  - Examples: Child seat, specific route, etc.
- **Continue Button**: Primary CTA

**User Actions:**
1. Enter contact information
2. Enter flight information (if applicable)
3. Add special requests
4. Click "Continue"

### Step 4: Review & Add to Cart

**Screen Components:**
- **Booking Summary**:
  - Vehicle type
  - Route or service type
  - Date and time
  - Duration (if hourly)
  - Passengers
- **Price Breakdown**:
  - Base rate: $XXX
  - Hours (if hourly): X hours × $XXX
  - Taxes and fees: $XXX
  - **Total**: Large, prominent
- **Terms and Conditions**:
  - Checkbox: "I agree to terms and conditions"
- **Action Buttons**:
  - "Add to Cart" button (Primary)
  - "Book Now" button (Secondary)

**User Actions:**
1. Review booking summary
2. Review pricing
3. Accept terms
4. Click "Add to Cart" or "Book Now"

---

## Fine Dining / Restaurants

### Step 1: Browse Restaurants

**Screen Components:**
- **Service Type**: "Fine Dining / Restaurants" (pre-selected
- **Location Search**:
  - Input field with autocomplete
  - Placeholder: "Search by location"
  - Map icon
- **Filters**:
  - **Cuisine Type**: Checkboxes (Italian, French, Asian, etc.)
  - **Price Range**: Radio buttons ($, $$, $$$, $$$$)
  - **Rating**: Slider (minimum rating)
  - **Features**: Checkboxes (Outdoor seating, Live music, etc.)
- **Restaurant Cards**:
  - **Image**: Hero image
  - **Name**: Restaurant name
  - **Cuisine Type**: Badge
  - **Location**: Address
  - **Rating**: Stars with review count
  - **Price Range**: $ symbols
  - **Minimum Spend**: Displayed if applicable
  - **"View Details" Button**: Primary button

**User Actions:**
1. Search by location
2. Apply filters
3. Browse restaurant options
4. Click "View Details" on preferred restaurant

### Step 2: Restaurant Details

**Screen Components:**
- **Image Gallery**: Hero image with thumbnails
- **Restaurant Information**:
  - Name: Large heading
  - Cuisine type: Badge
  - Location: Address with map
  - Rating: Stars with review count
  - Price range: $ symbols
- **Booking Widget** (sticky sidebar):
  - Date selector: Date picker
  - Time selector: Time picker
  - Guests selector: Stepper
  - **Option Types** (based on minimum spend):
    - **Option 1**: "Standard Experience"
      - Minimum spend: $XXX
      - Deposit required: $XXX
      - Description
    - **Option 2**: "Premium Experience"
      - Minimum spend: $XXX
      - Deposit required: $XXX
      - Description
    - **Option 3**: "VIP Experience"
      - Minimum spend: $XXX
      - Deposit required: $XXX
      - Description
  - Price display
  - "Make Reservation" button
- **Description**: Full restaurant description
- **Menu Preview** (optional): Sample menu items
- **Reviews**: Review section
- **Policies**:
  - Cancellation policy
  - Dress code
  - Reservation policy

**User Actions:**
1. Browse restaurant details
2. Select date and time
3. Select number of guests
4. Select option type (based on minimum spend)
5. Review deposit requirement
6. Click "Make Reservation"

### Step 3: Reservation Details

**Screen Components:**
- **Guest Information**:
  - Name: Text input
  - Email: Email input
  - Phone: Phone input
- **Special Requests** (optional):
  - Textarea: "Dietary requirements, special occasions, etc."
- **Deposit Information**:
  - Deposit amount: Displayed prominently
  - Note: "Deposit will be charged now, remaining balance at restaurant"
- **Continue Button**: Primary CTA

**User Actions:**
1. Enter guest information
2. Add special requests (optional)
3. Review deposit information
4. Click "Continue"

### Step 4: Review & Add to Cart

**Screen Components:**
- **Reservation Summary**:
  - Restaurant name
  - Date and time
  - Guests
  - Option type selected
  - Minimum spend
- **Price Breakdown**:
  - Deposit: $XXX (charged now)
  - Remaining balance: $XXX (payable at restaurant)
  - **Total Deposit**: Large, prominent
- **Terms and Conditions**:
  - Checkbox: "I agree to terms and conditions"
  - Cancellation policy summary
- **Action Buttons**:
  - "Add to Cart" button (Primary)
  - "Book Now" button (Secondary)

**User Actions:**
1. Review reservation details
2. Review pricing and deposit
3. Accept terms
4. Click "Add to Cart" or "Book Now"

---

## Nightlife / Lounge

### Step 1: Browse Nightlife Options

**Screen Components:**
- **Service Type**: "Nightlife / Lounge" (pre-selected)
- **Location Search**:
  - Input field with autocomplete
  - Placeholder: "Search by location"
- **Filters**:
  - **Venue Type**: Checkboxes (Club, Lounge, Bar, Rooftop, etc.)
  - **Music Type**: Checkboxes (Hip-hop, EDM, Live music, etc.)
  - **Price Range**: Radio buttons
  - **Rating**: Slider
- **Venue Cards**:
  - **Image**: Hero image
  - **Name**: Venue name
  - **Type**: Badge (Club, Lounge, etc.)
  - **Location**: Address
  - **Rating**: Stars
  - **Price Range**: $ symbols
  - **Minimum Spend**: Displayed
  - **"View Details" Button**: Primary button

**User Actions:**
1. Search by location
2. Apply filters
3. Browse venue options
4. Click "View Details"

### Step 2: Venue Details

**Screen Components:**
- **Image Gallery**: Hero image with thumbnails
- **Venue Information**:
  - Name: Large heading
  - Type: Badge
  - Location: Address with map
  - Rating: Stars
- **Booking Widget** (sticky sidebar):
  - Date selector: Date picker
  - Time selector: Time picker
  - Guests selector: Stepper
  - **Option Types** (based on minimum spend):
    - **Option 1**: "Standard Entry"
      - Minimum spend: $XXX
      - Deposit required: $XXX
    - **Option 2**: "VIP Table"
      - Minimum spend: $XXX
      - Deposit required: $XXX
    - **Option 3**: "Premium VIP"
      - Minimum spend: $XXX
      - Deposit required: $XXX
  - Price display
  - "Make Reservation" button
- **Description**: Full venue description
- **Features**: Music type, ambiance, etc.
- **Reviews**: Review section
- **Policies**: Age restrictions, dress code, etc.

**User Actions:**
1. Browse venue details
2. Select date and time
3. Select number of guests
4. Select option type
5. Review deposit
6. Click "Make Reservation"

### Step 3: Reservation Details

**Screen Components:**
- **Guest Information**:
  - Name: Text input
  - Email: Email input
  - Phone: Phone input
- **Special Requests** (optional):
  - Textarea: "Special requests or preferences"
- **Deposit Information**:
  - Deposit amount displayed
  - Note about remaining balance
- **Continue Button**: Primary CTA

**User Actions:**
1. Enter guest information
2. Add special requests
3. Review deposit
4. Click "Continue"

### Step 4: Review & Add to Cart

**Screen Components:**
- **Reservation Summary**:
  - Venue name
  - Date and time
  - Guests
  - Option type
  - Minimum spend
- **Price Breakdown**:
  - Deposit: $XXX
  - Remaining balance: $XXX
  - **Total Deposit**: Large, prominent
- **Terms and Conditions**:
  - Checkbox: "I agree to terms and conditions"
- **Action Buttons**:
  - "Add to Cart" button (Primary)
  - "Book Now" button (Secondary)

**User Actions:**
1. Review reservation
2. Review pricing
3. Accept terms
4. Click "Add to Cart" or "Book Now"

---

## Events / Attractions

### Step 1: Browse Events & Attractions

**Screen Components:**
- **Service Type**: "Events / Attractions" (pre-selected)
- **Location Search**:
  - Input field with autocomplete
  - Placeholder: "Search by location"
- **Category Filters**:
  - Tabs or buttons: "All" | "Concerts" | "Sports" | "Theater" | "Tours" | "Museums" | etc.
- **Date Filter**:
  - Date range picker
  - "This Week", "This Month" quick filters
- **Event/Attraction Cards**:
  - **Image**: Hero image
  - **Name**: Event/attraction name
  - **Category**: Badge
  - **Location**: Venue name and address
  - **Date & Time**: Display
  - **Price Range**: From $XXX
  - **Deposit Required**: Badge (if applicable)
  - **"View Details" Button**: Primary button

**User Actions:**
1. Search by location
2. Filter by category
3. Filter by date
4. Browse options
5. Click "View Details"

### Step 2: Event/Attraction Details

**Screen Components:**
- **Image Gallery**: Hero image with thumbnails
- **Event Information**:
  - Name: Large heading
  - Category: Badge
  - Date & Time: Prominent display
  - Location: Venue with map
  - Duration: Display
  - Rating: Stars (if applicable)
- **Booking Widget** (sticky sidebar):
  - Date selector (if multiple dates)
  - Time selector (if multiple times)
  - **Ticket Options**:
    - **Option 1**: "General Admission"
      - Price: $XXX
      - Deposit: $XXX (if required)
    - **Option 2**: "VIP"
      - Price: $XXX
      - Deposit: $XXX (if required)
    - **Option 3**: "Premium VIP"
      - Price: $XXX
      - Deposit: $XXX (if required)
  - Quantity selector: Stepper
  - Price display
  - "Make Reservation" button
- **Description**: Full event description
- **Schedule**: Event timeline (if applicable)
- **Reviews**: Review section (if applicable)
- **Policies**: Cancellation, refund policy

**User Actions:**
1. Browse event details
2. Select date/time (if options available)
3. Select ticket option
4. Select quantity
5. Review deposit (if required)
6. Click "Make Reservation"

### Step 3: Attendee Information

**Screen Components:**
- **Ticket Quantity**: Display selected quantity
- **Attendee Forms** (one per ticket):
  - Name: Text input
  - Email: Email input (optional, if different from primary)
  - Age (if age-restricted): Date picker or number input
- **Primary Contact**:
  - Name: Text input
  - Email: Email input
  - Phone: Phone input
- **Special Requests** (optional):
  - Textarea: "Any special requests?"
- **Deposit Information** (if applicable):
  - Deposit amount per ticket
  - Total deposit
  - Note about remaining balance
- **Continue Button**: Primary CTA

**User Actions:**
1. Enter attendee information for each ticket
2. Enter primary contact
3. Add special requests (optional)
4. Review deposit
5. Click "Continue"

### Step 4: Review & Add to Cart

**Screen Components:**
- **Reservation Summary**:
  - Event/attraction name
  - Date and time
  - Ticket type and quantity
  - Attendee names
- **Price Breakdown**:
  - Ticket price: $XXX × quantity
  - Deposit: $XXX (if applicable)
  - Remaining balance: $XXX (if deposit)
  - **Total** or **Total Deposit**: Large, prominent
- **Terms and Conditions**:
  - Checkbox: "I agree to terms and conditions"
- **Action Buttons**:
  - "Add to Cart" button (Primary)
  - "Book Now" button (Secondary)

**User Actions:**
1. Review reservation details
2. Review pricing
3. Accept terms
4. Click "Add to Cart" or "Book Now"

---

## Customize Personal / Getaway Experience

### Step 1: Experience Builder - Basic Information

**Screen Components:**
- **Service Type**: "Customize Experience" (pre-selected)
- **Date Selection**:
  - Date picker
  - Calendar widget
  - Placeholder: "Select experience date"
  - Date range option (for multi-day experiences)
- **Number of Guests**:
  - Stepper: Number of guests
  - Default: 2, Min: 1, Max: 50
- **Package Selection**:
  - **Radio Buttons or Cards**:
    - **Regular Package**:
      - Description: Basic experience
      - Features list
      - Base price: $XXX
    - **Standard Package**:
      - Description: Enhanced experience
      - Features list
      - Base price: $XXX
    - **VIP Package**:
      - Description: Premium experience
      - Features list
      - Base price: $XXX
- **Continue Button**: Primary CTA

**User Actions:**
1. Select experience date
2. Select number of guests
3. Select package type
4. Click "Continue"

### Step 2: Accommodation Selection

**Screen Components:**
- **Accommodation Type Selection**:
  - Tabs or buttons: "Beach House" | "Villa" | "Event Location" | "Provide Custom Location"
- **Browse Options** (if Beach House or Villa selected):
  - **Location Search**: Input with autocomplete
  - **Property Cards**:
    - Image gallery
    - Property name
    - Location
    - Capacity (guests)
    - Features list
    - Price per night
    - "Select Property" button
  - Filters: Price range, capacity, amenities
- **Custom Location** (if selected):
  - **Location Input**: Text input with autocomplete
  - **Address**: Full address input
  - **Location Type**: Dropdown (Beach, Mountain, City, etc.)
  - **Map Picker**: Interactive map to select location
- **Selected Accommodation Summary**:
  - Property name or custom location
  - Dates
  - Guests
  - Price
- **Continue Button**: Primary CTA

**User Actions:**
1. Select accommodation type
2. Browse and select property (if applicable)
3. Or provide custom location
4. Review selection
5. Click "Continue"

### Step 3: Add-ons Selection

**Screen Components:**
- **Add-ons Categories**:
  - **Transportation**:
    - **Book a Boat**: 
      - Toggle: "Add boat rental"
      - Boat type selector: Speedboat, Yacht, Catamaran, etc.
      - Duration selector: Hours or days
      - Price display
    - **Jet Ski**:
      - Toggle: "Add jet ski rental"
      - Quantity: Stepper
      - Duration: Hours selector
      - Price display
    - **Buggies**:
      - Toggle: "Add buggy rental"
      - Quantity: Stepper
      - Duration: Days selector
      - Price display
  - **Services**:
    - **Hire a Chef**:
      - Toggle: "Add private chef"
      - Service level: Dropdown (Basic, Premium, Gourmet)
      - Number of meals: Stepper
      - Price display
    - **Bar Tender**:
      - Toggle: "Add bartender service"
      - Service duration: Hours selector
      - Price display
    - **Waiters**:
      - Toggle: "Add waiter service"
      - Quantity: Stepper
      - Service duration: Hours selector
      - Price display
    - **Disc Jockey (DJ)**:
      - Toggle: "Add DJ service"
      - Service duration: Hours selector
      - Equipment included: Checkbox list
      - Price display
  - **Additional Requests**:
    - **Textarea**: "Any additional requests or special requirements?"
    - Placeholder: "E.g., specific dietary requirements, decoration preferences, etc."
    - Character limit: 500
- **Add-ons Summary** (sticky sidebar or bottom):
  - List of selected add-ons
  - Individual prices
  - Subtotal
- **Continue Button**: Primary CTA

**User Actions:**
1. Browse add-on categories
2. Select transportation add-ons (boat, jet ski, buggies)
3. Select service add-ons (chef, bartender, waiters, DJ)
4. Add additional requests in textarea
5. Review add-ons summary
6. Click "Continue"

### Step 4: Experience Summary & Quote Request

**Screen Components:**
- **Experience Summary**:
  - **Basic Information**:
    - Date(s)
    - Number of guests
    - Package type
  - **Accommodation**:
    - Property name or custom location
    - Address (if custom)
  - **Selected Add-ons**:
    - Transportation: List with details
    - Services: List with details
  - **Additional Requests**: Display text
- **Price Estimate**:
  - Package base price: $XXX
  - Accommodation: $XXX (if selected property)
  - Add-ons breakdown:
    - Boat: $XXX
    - Jet Ski: $XXX
    - Chef: $XXX
    - etc.
  - **Estimated Total**: Large, prominent
  - Note: "Final price will be confirmed after review"
- **Guest Information**:
  - Name: Text input
  - Email: Email input
  - Phone: Phone input with country code
  - Company/Organization (optional): Text input
- **Terms and Conditions**:
  - Checkbox: "I agree to terms and conditions"
  - Note: "By submitting, you agree to receive a customized quote"
- **Submit Request Button**: Primary CTA
- **Save as Draft** (optional): Secondary button

**User Actions:**
1. Review complete experience summary
2. Review price estimate
3. Enter contact information
4. Review additional requests
5. Accept terms
6. Click "Submit Request" or "Save as Draft"

### Step 5: Quote Request Confirmation

**Screen Components:**
- **Success Message**:
  - Large checkmark icon (animated)
  - Heading: "Quote Request Submitted!" (H2)
  - Description: "We've received your request and will send you a customized quote within 24 hours."
- **Request Reference Number**:
  - Display: "Request #XXXXX"
  - Copy button
- **What Happens Next**:
  - Numbered list:
    1. "Our team will review your request"
    2. "We'll prepare a customized quote"
    3. "You'll receive an email with the quote within 24 hours"
    4. "You can then proceed to book your experience"
- **Email Confirmation**:
  - Note: "A confirmation email has been sent to [email]"
  - "Resend email" link
- **Action Buttons**:
  - "View Request Status" button (Primary)
  - "Browse Other Experiences" link (Text button)
  - "Create Another Request" link (Text button)

**User Actions:**
1. View confirmation message
2. Note request reference number
3. Check email for confirmation
4. Click "View Request Status" or continue browsing

---

## Common Elements Across All Flows

### Cart Integration
- All services can be added to a unified shopping cart
- Cart shows all selected services with summaries
- Services can be modified or removed from cart
- Total price calculated across all services

### Guest Checkout vs Account
- Option to book as guest or create account
- Account creation includes email verification
- Guest bookings can be converted to account later

### Payment Flow
- Payment method selection
- Secure payment processing
- Payment confirmation
- Receipt generation

### Booking Confirmation
- Success message
- Booking reference number
- Booking details summary
- Downloadable receipt/invoice
- Email confirmation
- Calendar integration (add to calendar)

### Error Handling
- Form validation errors
- Payment errors
- Availability errors
- Network errors
- All with clear recovery options

### Loading States
- Search loading (skeleton screens)
- Payment processing (full-screen overlay)
- Form submission (button loading state)
- All with appropriate feedback

---

## Notes for Implementation

1. **Date Selection**: All date pickers should prevent past dates (except for historical bookings if applicable)
2. **Time Selection**: Consider timezone handling for international services
3. **Pricing**: All prices should display currency symbol and be clearly labeled
4. **Validation**: Real-time validation with helpful error messages
5. **Accessibility**: All forms and interactions must be keyboard accessible
6. **Mobile Optimization**: All flows must work seamlessly on mobile devices
7. **Progressive Enhancement**: Core functionality works without JavaScript
8. **Error Recovery**: Always provide clear paths to recover from errors
9. **Confirmation**: Always confirm destructive actions (cancellation, deletion)
10. **Feedback**: Provide immediate feedback for all user actions

