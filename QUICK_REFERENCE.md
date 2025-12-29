# KolaExplore UI/UX - Quick Reference Guide

## 🎨 Design Tokens Quick Reference

### Colors
```
Primary:   #2196F3 (Blue)
Secondary: #4CAF50 (Green)
Accent:    #FF9500 (Orange)
Success:   #4CAF50
Error:     #F44336
Warning:   #FF9800
Info:      #2196F3
```

### Typography
```
Font: Inter
H1: 48px/56px Bold (Desktop), 32px/40px (Mobile)
H2: 36px/44px Bold (Desktop), 28px/36px (Mobile)
Body: 16px/24px Regular
Button: 16px Medium
```

### Spacing
```
Base: 4px
Scale: 4, 8, 12, 16, 24, 32, 48, 64, 96, 128px
```

### Border Radius
```
Small: 4px
Medium: 8px
Large: 12px
Round: 50%
```

## 📱 Platform Overview

### Web Platform
- **Pages**: Home, Search, Service Details, Booking Flows, Cart, Checkout, My Bookings
- **Services**: Flights, Hotels, Rides, Events, Spa & Wellness
- **Key Features**: Multi-service cart, Unified checkout, Booking management

### Mobile App
- **Navigation**: Bottom tabs (Home, Search, Bookings, Profile)
- **Services**: Same as web
- **Key Features**: Touch-optimized, Swipe gestures, Native feel

### Merchant Dashboard
- **Sections**: Dashboard, Services, Bookings, Customers, Analytics, Settings
- **Key Features**: Service management, Availability calendar, Booking management

### Admin Dashboard
- **Sections**: Overview, Users, Merchants, Bookings, Services, Content, Financial, Settings
- **Key Features**: User management, Merchant approval, Booking oversight, Platform controls

## 🔄 Key User Flows

### Customer: Flight Booking
```
Search → Results → Details → Passenger Info → Seat Selection → 
Add-ons → Review → Payment → Confirmation
```

### Customer: Multi-Service Cart
```
Add Services → View Cart → Checkout → Guest Info → Payment → 
Order Confirmation
```

### Merchant: Service Creation
```
Select Type → Basic Info → Pricing → Availability → Details → 
Review → Publish
```

### Admin: Merchant Approval
```
View Application → Review Documents → Verify → Approve/Reject → 
Notify Merchant
```

## 🧩 Component Library

### Buttons
- Primary: Blue background, white text
- Secondary: Transparent, blue border
- Text: Transparent, blue text
- States: Default, Hover, Active, Disabled, Loading

### Inputs
- Height: 44px (mobile), 40px (desktop)
- Border: 1px solid gray-300
- Focus: Blue border + outline
- Error: Red border

### Cards
- Padding: 24px
- Border Radius: 12px
- Shadow: Elevation-2
- Hover: Elevation-3 + translateY(-2px)

### Badges
- Status: Success (green), Error (red), Warning (orange), Info (blue)
- Count: Red circle with white number

## 📐 Layout Guidelines

### Grid System
- Desktop: 12 columns, 24px gutter, 1200px max-width
- Tablet: 8 columns, 24px gutter
- Mobile: Single column, 16px padding

### Breakpoints
- Mobile: 0-575px
- Tablet: 768-991px
- Desktop: 992px+

### Container Padding
- Mobile: 16px
- Tablet: 24px
- Desktop: 32px

## 🎯 Figma Setup Checklist

### Phase 1: Design System
- [ ] Create color styles
- [ ] Create text styles
- [ ] Create effect styles (shadows)
- [ ] Create base components

### Phase 2: Components
- [ ] Buttons (all variants)
- [ ] Inputs (all types)
- [ ] Cards
- [ ] Navigation components
- [ ] Form components

### Phase 3: Screens
- [ ] Web platform pages
- [ ] Mobile app screens
- [ ] Merchant dashboard
- [ ] Admin dashboard

### Phase 4: Prototypes
- [ ] Link customer flows
- [ ] Link merchant flows
- [ ] Link admin flows
- [ ] Add interactions

## 📋 Component Naming Convention

```
[Platform]/[Category]/[Component]/[Variant]/[State]

Examples:
- Web/Button/Primary/Medium/Default
- Mobile/Card/Service/Hover
- Merchant/Table/Bookings/Empty
```

## ⚡ Quick Tips

### Accessibility
- Minimum touch target: 44x44px
- Color contrast: 4.5:1 (text), 3:1 (UI)
- Keyboard navigation: All interactive elements
- Focus indicators: 2px blue outline

### Performance
- Use Auto Layout for flexible components
- Use constraints for responsive design
- Optimize images (WebP format)
- Lazy load heavy content

### Best Practices
- Consistent spacing (4px base unit)
- Clear visual hierarchy
- Error states for all forms
- Loading states for async actions
- Empty states for no data
- Success feedback for actions

## 🔗 File Reference

- **Project Plan**: `PROJECT_PLAN.md`
- **Design System**: `SHARED_DESIGN_SYSTEM.md`
- **Web Platform**: `WEB_PLATFORM_DESIGN.md`
- **Mobile App**: `MOBILE_APP_DESIGN.md`
- **Merchant Dashboard**: `MERCHANT_DASHBOARD_DESIGN.md`
- **Admin Dashboard**: `ADMIN_DASHBOARD_DESIGN.md`
- **User Flows**: `USER_FLOWS.md`
- **States & Feedback**: `STATES_AND_FEEDBACK.md`
- **Figma Guide**: `FIGMA_IMPLEMENTATION_GUIDE.md`
- **Visual Reference**: `design-reference.html`

## 📞 Common Questions

**Q: What's the primary color?**
A: #2196F3 (Blue) - Primary-500

**Q: What's the minimum touch target size?**
A: 44x44px for mobile, 40x40px for desktop

**Q: What spacing should I use?**
A: Use 4px base unit: 4, 8, 12, 16, 24, 32, 48, 64px

**Q: How do I name components in Figma?**
A: `[Platform]/[Category]/[Component]/[Variant]/[State]`

**Q: What breakpoints should I design for?**
A: Mobile (375px), Tablet (768px), Desktop (1440px)

**Q: What font should I use?**
A: Inter (with system font fallbacks)

---

*For detailed information, refer to the full documentation files.*

