# Market slot solution 
Market stall booking and management system
| Full Name | Student Number |
|-----------|----------------|
| Ngelekwa Peter  | 2410101 |
| Elizabeth Mubanga |2410016|
| Ben Kambikiya  |2410086 |
| Manda Mowa  |2410659 |
| Sampa Kennedy  | 2410111 |

problems
1. Problems for Traders (Sellers)
- Queueing and Waking Up Early: Traders currently wake up 4:00 AM to queue for physical booking. System allows booking from home via phone.
2. Problems for Market Officer
- Manual Bookkeeping Errors: Officer writes in book, mistakes happen, double-booking happens. System prevents this via StallAlreadyBookedException.

   http://localhost:8081/dashboard.html


   CLASSES
1. User (abstract) - Abstract parent class for Trader and MarketOfficer with common fields id, name, phone.
2. Trader extends User - Represents a seller at Masala Market with nrc, goodsType, books stalls.
3. Stall (abstract) - Abstract parent for TableStall/FloorSpace with stallId, location, abstract calculateDailyFee().
4. TableStall extends Stall - Table type stall with daily fee K15 (implements polymorphism).
5. FloorSpace extends Stall - Floor type stall with daily fee K5 (implements polymorphism).
6. Booking - Links Trader + Stall + date, throws StallAlreadyBookedException if double-booked.
7. Payment implements Payable - Handles payment processing with receipt generation.
8. MarketOfficer extends User - Officer who manages bookings and payments.
