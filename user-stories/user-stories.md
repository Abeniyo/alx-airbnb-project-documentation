# Airbnb Clone - Core User Stories

## Guest Stories
1. **As a** Guest  
   **I want to** register an account using email  
   **So that** I can book properties  
   *Acceptance Criteria*:  
   - Email verification required  
   - Password strength enforcement (min 8 chars)  
   - JWT returned on success  

2. **As a** Guest  
   **I want to** search properties with filters  
   **So that** I can find suitable accommodations  
   *AC*:  
   - Filter by: location, price, dates, amenities  
   - Results paginated (10 per page)  
   - <1s response time for common queries  

## Host Stories
3. **As a** Host  
   **I want to** create a property listing  
   **So that** I can rent out my space  
   *AC*:  
   - Required fields: title, description, price, location  
   - Multiple image uploads (max 10)  
   - Instant draft saving  

4. **As a** Host  
   **I want to** receive booking payments automatically  
   **So that** I don't need manual invoicing  
   *AC*:  
   - Payout 24h after guest check-in  
   - Email notification on payment  
   - Dashboard showing earnings  

## Admin Stories
5. **As an** Admin  
   **I want to** remove inappropriate listings  
   **So that** the platform stays safe  
   *AC*:  
   - Audit log of moderation actions  
   - Email notification to host  
   - Appeal process for hosts  

## Payment System Story
6. **Through the** Payment System  
   **I want to** process refunds automatically  
   **So that** guests get timely reimbursements  
   *AC*:  
   - Policy-based refund calculations  
   - Multi-currency support  
   - Receipt generation  