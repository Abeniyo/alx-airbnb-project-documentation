# Airbnb Clone - Backend Requirements

## 1. User Authentication

### Functional Requirements
- Email/password registration
- Social login (Google/Facebook)
- JWT-based session management

### Technical Specifications
| Endpoint | Method | Input | Output | Status Codes |
|----------|--------|-------|--------|--------------|
| `/auth/register` | POST | `{email, password}` | `{user_id, token}` | 201, 400, 409 |
| `/auth/login` | POST | `{email, password}` | `{token, user_data}` | 200, 401 |

### Validation Rules
- Email: Valid format, unique
- Password: 8+ chars, special char required
- JWT: 24h expiry, refresh token

### Performance
- Auth response time < 500ms
- Support 1000 auth requests/minute

## 2. Property Management

### Functional Requirements
- CRUD operations for listings
- Media upload handling
- Availability management

### Technical Specifications
| Endpoint | Method | Input | Output |
|----------|--------|-------|--------|
| `/properties` | POST | Listing details + images | `{property_id, status}` |
| `/properties/{id}/availability` | PUT | Date ranges | Updated calendar |

### Validation Rules
- Required fields: title, price, location
- Image format: JPG/PNG <5MB
- Date conflicts prevented

### Performance
- Image upload < 3s (avg)
- Availability checks < 300ms

## 3. Booking System

### Functional Requirements
- Date-based reservation
- Conflict prevention
- Payment integration

### Technical Specifications
| Endpoint | Method | Input | Output |
|----------|--------|-------|--------|
| `/bookings` | POST | `{property_id, dates, payment}` | `{booking_id, receipt}` |
| `/bookings/{id}` | GET | - | Full booking details |

### Business Rules
- Minimum stay: 1 night
- Cancellation policy enforcement
- Host payout 24h post-check-in

### Performance
- Booking creation < 1s
- Payment processing < 2s