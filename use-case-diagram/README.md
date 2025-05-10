# Airbnb Clone - Use Case Diagram

## System Overview
![Airbnb Use Case Diagram](use-cases.png)

### Primary Actors
1. **Guest** (Unauthenticated User)
2. **Host** (Property Owner)
3. **Admin** (System Administrator)

### Secondary Actor
- **Payment System** (External Service)

### Core Use Cases

#### Guest Interactions
- Search Properties
- Register Account
- Book Property
- Leave Review
- Book Property
- Make Payment
- Write Review

#### Host Interactions
- Create Listing
- Leave Review
- Update Listing Details
- View Bookings
- Respond to Reviews
- Receive Payouts

#### Admin Interactions
- Manage User
- Manage Listings
- Manage Payment

#### Payment System Interactions
- Process Payments
- Handle Refunds
- Verify Transactions

## Relationships
- Host can perform all Guest actions
- Payment System extends manage payment use case
- Admin includes all management functions