# States, Feedback & Error Handling - Complete Guide

## Overview

This document provides comprehensive descriptions of all UI states, user feedback mechanisms, error handling, and edge cases across all platforms.

## Empty States

### Purpose
Empty states inform users when there's no content to display, guide them on next steps, and maintain engagement.

### Design Principles
- **Clear Communication**: Explain why the state is empty
- **Helpful Guidance**: Provide actionable next steps
- **Visual Interest**: Use illustrations or icons (not just text)
- **Maintain Context**: Keep navigation and structure visible

### Empty State Components

#### No Search Results
**When it appears:**
- User searches with no matching results
- Filters exclude all items
- Search query returns zero results

**Visual Elements:**
- Illustration: Search icon or magnifying glass (120-200px, Gray-400)
- Heading: "No results found" (H3, Text-Secondary, centered)
- Description: "We couldn't find anything matching '[search term]'. Try different keywords or adjust your filters." (Body, Text-Secondary, centered)
- Actions:
  - "Clear Filters" button (Secondary)
  - "Browse All [Service Type]" link (Text button)
  - Popular searches: Chips or links below
- Layout: Centered, vertical stack, max-width 500px, padding 48px

#### Empty Cart
**When it appears:**
- Shopping cart is empty
- User navigates to cart with no items

**Visual Elements:**
- Illustration: Shopping cart icon (120px, Gray-400)
- Heading: "Your cart is empty" (H3, centered)
- Description: "Start adding services to your cart to continue booking." (Body, Text-Secondary, centered)
- CTA: "Browse Services" button (Primary, full-width on mobile)
- Quick Links: Service category chips (horizontal scroll on mobile)
- Layout: Centered, vertical stack, padding 32px

#### No Bookings
**When it appears:**
- User has no booking history
- Filtered view shows no bookings
- New user account

**Visual Elements:**
- Illustration: Calendar or booking icon (120px, Gray-400)
- Heading: "No bookings yet" (H3, centered)
- Description: "Your booking history will appear here once you make your first booking." (Body, Text-Secondary, centered)
- CTA: "Explore Services" button (Primary, full-width on mobile)
- Suggestions: Featured services carousel or grid
- Layout: Centered with suggestions below

#### No Favorites
**When it appears:**
- User has no saved favorites
- Favorites list is empty

**Visual Elements:**
- Illustration: Heart icon (outline style, 120px, Gray-400)
- Heading: "No favorites saved" (H3, centered)
- Description: "Tap the heart icon on any service to save it for later." (Body, Text-Secondary, centered)
- CTA: "Discover Services" button (Primary, full-width on mobile)
- Layout: Centered, vertical stack

#### No Notifications
**When it appears:**
- Notification center is empty
- All notifications have been read

**Visual Elements:**
- Illustration: Bell icon (outline style, 120px, Gray-400)
- Heading: "All caught up!" (H3, centered)
- Description: "You have no new notifications." (Body, Text-Secondary, centered)
- Layout: Centered, vertical stack

#### No Reviews
**When it appears:**
- Service has no reviews yet
- User hasn't left any reviews

**Visual Elements:**
- Illustration: Star icon (outline style, 120px, Gray-400)
- Heading: "No reviews yet" (H3, centered)
- Description: "Be the first to review this service!" (Body, Text-Secondary, centered)
- CTA: "Write a Review" button (Primary, if user can review)
- Layout: Centered

## Error States

### Purpose
Error states inform users when something goes wrong, explain the issue clearly, and provide recovery options.

### Design Principles
- **Clear Communication**: Explain what went wrong in plain language
- **Actionable**: Provide clear next steps
- **Non-Blaming**: Don't make users feel at fault
- **Recovery Options**: Always provide a way forward

### Error State Components

#### Form Validation Errors

**Inline Field Errors:**
- **Visual Design:**
  - Error message: Body-Small, Error-500 (#F44336)
  - Error icon: 16px, Error-500, before message
  - Input border: 2px solid Error-500
  - Input background: Error-50 (#FFEBEE, subtle tint)
  - Message position: Below input field, 4px spacing
  - Animation: Shake animation (200ms) on error appearance

- **Error Messages:**
  - "This field is required"
  - "Please enter a valid email address"
  - "Password must be at least 8 characters"
  - "Passwords do not match"
  - "Phone number is invalid"
  - "Date must be in the future"
  - "Please select an option"

- **Real-time Validation:**
  - Validate on blur (when user leaves field)
  - Show error immediately for critical fields
  - Clear error when user starts typing (if fixable)

**Form-Level Errors:**
- Alert banner at top of form
- Error-500 border, Error-50 background
- List of all errors with links to fields
- Sticky position (stays visible while scrolling)

#### Network/API Errors

**404 Not Found:**
- **Visual Design:**
  - Illustration: 404 or broken link icon (200px, Gray-400)
  - Heading: "Page Not Found" (H2, Error-500)
  - Description: "The page you're looking for doesn't exist or has been moved." (Body, Text-Secondary)
  - Actions:
    - "Go to Homepage" button (Primary)
    - "Go Back" link (Text button)
  - Layout: Centered, vertical stack

**500 Server Error:**
- **Visual Design:**
  - Illustration: Server or warning icon (200px, Error-500)
  - Heading: "Something went wrong" (H2, Error-500)
  - Description: "Our servers are experiencing issues. Please try again in a few moments." (Body, Text-Secondary)
  - Error ID: Small text (Caption, Gray-500) for support reference
  - Actions:
    - "Retry" button (Primary)
    - "Contact Support" link (Text button)
  - Layout: Centered, vertical stack

**Network Error:**
- **Visual Design:**
  - Illustration: WiFi or connection icon (200px, Warning-500)
  - Heading: "Connection Error" (H2, Warning-500)
  - Description: "Unable to connect to the server. Please check your internet connection and try again." (Body, Text-Secondary)
  - Actions:
    - "Retry" button (Primary)
    - "Go Offline" link (Text button, if offline mode available)
  - Layout: Centered, vertical stack

**Timeout Error:**
- **Visual Design:**
  - Illustration: Clock or timeout icon (200px, Warning-500)
  - Heading: "Request Timed Out" (H2, Warning-500)
  - Description: "The request took too long to complete. Please try again." (Body, Text-Secondary)
  - Actions:
    - "Retry" button (Primary)
    - "Go Back" link (Text button)
  - Layout: Centered, vertical stack

#### Payment Errors

**Payment Failed:**
- **Visual Design:**
  - Error icon (120px, Error-500, centered)
  - Heading: "Payment Failed" (H2, Error-500, centered)
  - Description: Specific error message:
    - "Insufficient funds in your account"
    - "Your card was declined"
    - "Card has expired"
    - "Invalid card details"
    - "Payment gateway error"
  - Booking status: Badge (Error, "Not Confirmed")
  - Actions:
    - "Try Different Payment Method" button (Primary, full-width on mobile)
    - "Update Card Details" button (Secondary, if applicable)
    - "Contact Support" link (Text button)
  - Layout: Centered, vertical stack

**Payment Processing Error:**
- **Visual Design:**
  - Warning icon (120px, Warning-500)
  - Heading: "Payment Processing Error" (H2, Warning-500)
  - Description: "Your payment is being processed. Please check your email for confirmation or contact support if you don't receive a confirmation within 24 hours."
  - Booking reference: Displayed prominently
  - Actions:
    - "Check Email" button (Primary)
    - "Contact Support" link (Text button)
  - Layout: Centered

#### Booking Errors

**Service Unavailable:**
- **Visual Design:**
  - Warning icon (120px, Warning-500, centered)
  - Heading: "Service Unavailable" (H2, Warning-500, centered)
  - Description: Specific reason:
    - "This service is no longer available"
    - "Selected dates are fully booked"
    - "Service has been removed"
  - Alternative suggestions: Similar services or alternative dates
  - Actions:
    - "View Alternatives" button (Primary, full-width on mobile)
    - "Modify Search" button (Secondary, full-width on mobile)
    - "Browse Similar Services" link (Text button)
  - Layout: Centered with suggestions below

**Booking Conflict:**
- **Visual Design:**
  - Warning icon (120px, Warning-500)
  - Heading: "Booking Conflict" (H2, Warning-500)
  - Description: "This booking conflicts with an existing booking. Please choose different dates or cancel the existing booking."
  - Existing booking: Link to view existing booking
  - Actions:
    - "Choose Different Dates" button (Primary)
    - "View Existing Booking" link (Text button)
  - Layout: Centered

#### Authentication Errors

**Login Failed:**
- **Visual Design:**
  - Error message below login form
  - Alert banner: Error-500 border, Error-50 background
  - Message: "Invalid email or password. Please try again."
  - Actions:
    - "Forgot Password?" link (Text button)
    - "Create Account" link (Text button)
  - Clear error on new attempt

**Session Expired:**
- **Visual Design:**
  - Modal or alert banner
  - Warning icon (48px, Warning-500)
  - Heading: "Session Expired" (H3)
  - Description: "Your session has expired. Please log in again to continue."
  - Actions:
    - "Log In" button (Primary)
    - "Continue as Guest" link (Text button, if applicable)
  - Layout: Modal centered

## Loading States

### Purpose
Loading states inform users that content is being fetched or processed, reducing perceived wait time and maintaining engagement.

### Design Principles
- **Immediate Feedback**: Show loading state immediately
- **Maintain Layout**: Use skeleton screens to preserve layout
- **Progress Indication**: Show progress when possible
- **Non-Blocking**: Allow cancellation when appropriate

### Loading State Components

#### Page Loading

**Skeleton Screens:**
- **Purpose**: Maintain layout structure while content loads
- **Visual Design:**
  - Animated placeholder matching content layout
  - Background: Gray-200 (#EEEEEE)
  - Border radius: Matches actual content (8px for cards, 4px for text)
  - Animation: Pulse (opacity 0.5 to 1, 1.5s ease-in-out infinite)
  - Maintains aspect ratios for images
  - Preserves spacing and layout

- **Skeleton Types:**
  - **Service Card Skeleton**: Image placeholder (16:9), 3 text lines, button placeholder
  - **List Skeleton**: Multiple row placeholders with icons and text
  - **Detail Skeleton**: Hero image, title line, multiple body text lines
  - **Form Skeleton**: Input field placeholders with labels
  - **Table Skeleton**: Header row, multiple data rows

#### Button Loading State

**Visual Design:**
- Spinner replaces button text (centered)
- Spinner: 16-20px, Primary-500 color, rotating animation
- Button disabled during loading (opacity 70%, cursor not-allowed)
- Optional: "Processing..." text below spinner
- Maintains button dimensions and styling
- Duration: Until operation completes

**Variants:**
- **Inline Spinner**: Spinner replaces text, button stays same size
- **Spinner + Text**: Spinner on left, "Loading..." text on right
- **Full-Width**: Spinner centered, full button width maintained

#### Form Submission Loading

**Visual Design:**
- **Modal Overlay** (for critical forms):
  - Background: Background-Overlay (rgba(0, 0, 0, 0.5))
  - Spinner: 48px, Primary-500, centered
  - Message: "Processing your request..." (Body, white, centered)
  - Prevents multiple submissions
  - No close option during processing

- **Inline Loading** (for non-critical forms):
  - Spinner in submit button
  - Disable form fields
  - Show progress message below form

#### Search Loading

**Visual Design:**
- Skeleton cards in results area
- Loading indicator in search bar (spinner, 20px, right side)
- Optional: "Searching..." text (Body-Small, Text-Secondary)
- Maintains filter sidebar visibility
- Results area shows skeleton placeholders
- Duration: Until results load

#### Payment Processing

**Visual Design:**
- **Full-Screen Overlay:**
  - Background: Background-Overlay (rgba(0, 0, 0, 0.7))
  - Large spinner: 64px, Primary-500, centered
  - Heading: "Processing Payment" (H3, white, centered)
  - Description: "Please wait while we process your payment. Do not close this window." (Body, white, centered)
  - Progress indicator: Optional step indicator showing progress
  - No cancel option during processing
  - Layout: Centered, vertical stack

- **Payment Steps** (if multi-step):
  1. Validating payment method
  2. Processing payment
  3. Confirming booking
  4. Sending confirmation

#### Data Fetching

**Visual Design:**
- **Small Data Loads:**
  - Inline spinner (24px) where content will appear
  - Minimal layout shift
  - Quick transition to content

- **Large Data Loads:**
  - Skeleton screens matching content structure
  - Maintains layout
  - Smooth transition to actual content

- **Infinite Scroll:**
  - Spinner at bottom of list (32px)
  - Message: "Loading more..." (Body-Small, centered, Text-Secondary)
  - Appears when scrolling near bottom
  - Replaces with content when loaded

#### Image Loading

**Visual Design:**
- **Placeholder:**
  - Gray-200 background
  - Maintains aspect ratio
  - Optional: Blur-up effect (low-res to high-res)

- **Progressive Loading:**
  - Low-quality placeholder first
  - High-quality image loads in background
  - Smooth transition

- **Error Fallback:**
  - Broken image icon (48px, Gray-400)
  - Alt text displayed
  - Retry option (if applicable)

## Success States & Feedback

### Purpose
Success states confirm completed actions, provide next steps, and create positive user experiences.

### Design Principles
- **Clear Confirmation**: Immediately confirm successful actions
- **Next Steps**: Guide users on what to do next
- **Celebration**: Subtle positive reinforcement
- **Actionable**: Provide clear next actions

### Success State Components

#### Success Toast Notifications

**Visual Design:**
- Background: Success-500 (#4CAF50)
- Icon: Checkmark (white, 20px, left side)
- Text: White, Body
- Position: 
  - Desktop: Top-right, 24px from edge
  - Mobile: Bottom-center, 24px from bottom
- Auto-dismiss: 3-5 seconds
- Animation: 
  - Entrance: Slide in from edge (300ms ease-out)
  - Exit: Fade out (200ms ease-in)
- Stacking: Multiple toasts stack vertically with 8px spacing

**Common Messages:**
- "Booking confirmed!"
- "Service added to cart"
- "Profile updated successfully"
- "Payment processed"
- "Review submitted"

#### Success Modals

**Visual Design:**
- **Animated Checkmark:**
  - Large checkmark icon (80-120px, Success-500)
  - Scale animation: 0.8 to 1.0 (300ms ease-out)
  - Circle background: Success-50, optional

- **Content:**
  - Heading: "Success!" (H2, Success-700)
  - Description: Specific success message (Body, Text-Secondary)
  - Actions: Primary CTA button

- **Layout:**
  - Centered modal
  - Max-width: 480px
  - Padding: 32px
  - Border radius: Large (12px)

#### Booking Confirmation Success

**Visual Design:**
- **Success Animation:**
  - Animated checkmark circle (200px, Success-500)
  - Optional: Confetti animation (subtle, 2-3 seconds)
  - Scale and fade animation

- **Content:**
  - Heading: "Booking Confirmed!" (H2, Success-700, centered)
  - Booking reference: Large, prominent (H1, Primary-500, centered)
  - Booking details: Summary card
  - Next steps: List with icons

- **Actions:**
  - "View Booking" button (Primary, full-width on mobile)
  - "Download Receipt" button (Secondary, full-width on mobile)
  - "Add to Calendar" button (Secondary)
  - "Share Booking" link (Text button)
  - "Book Similar Service" link (Text button)

- **Layout:**
  - Centered, vertical stack
  - Padding: 48px
  - Max-width: 600px

#### Form Submission Success

**Visual Design:**
- Success icon (80px, Success-500, centered)
- Heading: "Submitted Successfully" (H3, centered)
- Description: Confirmation message (Body, centered, Text-Secondary)
- Actions:
  - Primary CTA button
  - Optional: Auto-redirect after 3 seconds with countdown
- Layout: Centered, vertical stack

## Notification System

### In-App Notifications

**Notification Center:**
- **Trigger**: Bell icon in header with badge count
- **Panel Design:**
  - Width: 400px (desktop), full-width (mobile)
  - Max-height: 600px, scrollable
  - Background: Background-Primary
  - Shadow: Elevation-3
  - Border radius: Large (12px) top corners

- **Notification Item:**
  - Icon: Service type or action icon (24px, left)
  - Title: Bold, Body (truncated if long)
  - Message: Regular, Body-Small, Text-Secondary (2 lines max)
  - Timestamp: Caption, Text-Secondary (e.g., "2 hours ago")
  - Unread indicator: Blue dot (8px, Primary-500)
  - Action button: Optional (e.g., "View", "Dismiss")
  - Hover: Background Gray-50

- **Empty State:**
  - Icon: Bell (outline, 80px, Gray-400)
  - Message: "No notifications" (Body, Text-Secondary, centered)
  - Layout: Centered, padding 32px

- **Actions:**
  - "Mark all as read" button (top of panel)
  - Individual "Mark as read" on hover
  - Click notification: Navigate to related page

### Push Notifications (Mobile)

**Notification Types:**
- Booking confirmations
- Booking reminders (24h, 2h before)
- Status updates (confirmed, cancelled, modified)
- Promotional offers
- System alerts

**Notification Content:**
- Title: Clear, concise (max 50 characters)
- Body: Descriptive message (max 150 characters)
- Icon: Service type icon or app icon
- Image: Optional service image
- Action buttons: Up to 2 (e.g., "View", "Dismiss")

**Design:**
- Native platform styling
- Rich notifications with images
- Actionable buttons
- Grouped notifications (by type)

## Visual Feedback & Micro-interactions

### Hover States

**Buttons:**
- Background: Darkens by 1 shade (e.g., Primary-500 → Primary-700)
- Elevation: Increases by 1 level
- Cursor: Pointer
- Transition: 200ms ease-in-out

**Cards:**
- Elevation: Increases by 1 level (e.g., Elevation-2 → Elevation-3)
- Transform: Scale 1.02x (subtle)
- Cursor: Pointer
- Transition: 200ms ease-in-out

**Links:**
- Underline: Appears (if not always visible)
- Color: Darkens by 1 shade
- Cursor: Pointer
- Transition: 200ms ease-in-out

**Icons:**
- Scale: 1.1x
- Color: Changes to Primary-500 (if not already)
- Cursor: Pointer
- Transition: 200ms ease-in-out

### Click/Tap Feedback

**Buttons:**
- Press: Scale down to 0.98x
- Release: Scale back to 1.0x
- Duration: 100-150ms
- Provides tactile feedback

**Cards:**
- Press: Scale down to 0.99x
- Release: Scale back to 1.0x
- Duration: 100ms
- Subtle feedback

**Icons:**
- Press: Scale down to 0.9x
- Release: Scale back to 1.0x
- Duration: 100ms
- Quick feedback

### Focus States

**Input Fields:**
- Border: 2px solid Primary-500
- Outline: 2px solid Primary-500, offset 2px
- Background: Optional Primary-50 tint
- Transition: 200ms ease-in-out

**Buttons:**
- Outline: 2px solid Primary-500, offset 2px
- Maintains button styling
- Visible for keyboard navigation

**Links:**
- Underline: Appears (if not always)
- Outline: 2px solid Primary-500, offset 2px
- Color: Primary-500

**Keyboard Navigation:**
- All interactive elements must have visible focus indicators
- Tab order: Logical flow
- Skip links: For main content areas

### Progress Indicators

**Multi-Step Forms:**
- Progress bar: Top of form, full width
- Step indicators: Numbered or icon-based
- Current step: Highlighted (Primary-500)
- Completed steps: Success-500
- Remaining steps: Gray-300
- Step labels: Below indicators

**File Upload:**
- Progress bar: Below file input
- Percentage: Displayed (e.g., "45%")
- Cancel button: Optional, right side
- Success: Checkmark when complete

**Booking Process:**
- Step indicator: Horizontal timeline
- Steps: Search → Select → Details → Payment → Confirm
- Current step: Highlighted
- Completed steps: Checkmark icons
- Progress: Visual progress bar

**Loading Progress:**
- Determinate: Shows percentage (when known)
- Indeterminate: Animated fill (when unknown)
- Buffer: Shows buffered vs loaded (for media)

## Haptic Feedback (Mobile)

### Touch Interactions

**Button Press:**
- Type: Light haptic
- Duration: 10ms
- When: On button press

**Success Action:**
- Type: Success haptic (double light tap)
- Duration: 20ms total
- When: On successful completion

**Error Action:**
- Type: Error haptic (strong tap)
- Duration: 30ms
- When: On error occurrence

**Swipe Actions:**
- Type: Medium haptic
- Duration: 20ms
- When: On swipe gesture completion

**Pull to Refresh:**
- Type: Light haptic
- Duration: 10ms
- When: On release after pull

### Haptic Patterns

- **Light**: Subtle vibration (10ms) - For standard interactions
- **Medium**: Standard vibration (20ms) - For important actions
- **Strong**: Strong vibration (30ms) - For errors or critical actions
- **Success**: Double light tap (10ms + 10ms) - For successful completions
- **Error**: Single strong tap (30ms) - For errors

## Gesture Interactions (Mobile)

### Swipe Gestures

**Swipe Right:**
- Action: Go back (navigation)
- Distance: 50px minimum
- Feedback: Medium haptic

**Swipe Left:**
- Action: Delete/Remove (with confirmation)
- Distance: 100px minimum
- Feedback: Medium haptic
- Confirmation: Required for destructive actions

**Swipe Up:**
- Action: Dismiss bottom sheet
- Distance: 100px minimum
- Feedback: Light haptic

**Swipe Down:**
- Action: Pull to refresh
- Distance: 80px to trigger
- Feedback: Light haptic on release

**Long Press:**
- Action: Context menu or selection mode
- Duration: 500ms
- Feedback: Medium haptic
- Visual: Selection indicator appears

### Pinch & Zoom

**Images:**
- Pinch to zoom: Gallery view
- Double tap: Zoom in/out
- Max zoom: 3x
- Min zoom: Fit to screen

**Maps:**
- Pinch to zoom: Standard map interaction
- Pan: Drag to move
- Double tap: Zoom in

### Drag Interactions

**Bottom Sheet:**
- Drag down: Dismiss sheet
- Drag up: Expand sheet (if collapsible)
- Feedback: Visual drag indicator

**Cards:**
- Drag left: Reveal actions (delete, favorite)
- Drag right: Dismiss or archive
- Feedback: Action icons appear

**Sliders:**
- Drag: Adjust value
- Feedback: Value updates in real-time
- Haptic: Light on value change (optional)

## Accessibility Considerations

### Screen Reader Support

**Empty States:**
- Announce: "No results found" or "Cart is empty"
- Describe available actions
- Provide navigation options

**Error States:**
- Announce error immediately
- Describe error clearly
- Provide recovery instructions
- Link to error fields

**Loading States:**
- Announce: "Loading" or "Processing"
- Describe what is loading
- Provide cancel option when possible

**Success States:**
- Announce: "Success" or "Completed"
- Describe what succeeded
- Provide next steps

### Keyboard Navigation

**All States:**
- Tab through all interactive elements
- Enter/Space to activate
- Escape to dismiss modals
- Arrow keys for navigation (where applicable)

### Color Contrast

**Error States:**
- Error text: Error-700 on Error-50 (meets WCAG AA)
- Error borders: Error-500 (meets WCAG AA)

**Success States:**
- Success text: Success-700 on Success-50 (meets WCAG AA)
- Success icons: Success-500 (meets WCAG AA)

## Best Practices

### Do's
- ✅ Show loading states immediately
- ✅ Provide clear error messages
- ✅ Offer recovery options
- ✅ Use appropriate animations
- ✅ Maintain layout during loading
- ✅ Test all states thoroughly
- ✅ Consider offline scenarios
- ✅ Provide haptic feedback (mobile)

### Don'ts
- ❌ Leave users without feedback
- ❌ Use technical error messages
- ❌ Block users without options
- ❌ Overuse animations
- ❌ Break layout during loading
- ❌ Ignore accessibility
- ❌ Forget error recovery
- ❌ Skip empty states

