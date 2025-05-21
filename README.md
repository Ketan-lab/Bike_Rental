# 🚲 Bike Rental System

## 📖 Overview

This Python project simulates a simple bike rental system. It allows customers to rent bikes on a **daily** or **weekly** basis, with special discounts for **family rentals** (3–5 bikes). The system manages the available stock, calculates rental charges, and applies promotions where applicable.

---

## 📁 Features

- Check available bike stock.
- Rent bikes on a daily or weekly basis.
- Automatically updates inventory after each rental.
- Calculates rental charges based on rental duration.
- Applies a 30% discount for family rentals (3 to 5 bikes).

---

## 🛠️ Classes

### 1. `BikeRental`

- Handles the stock of bikes.
- Methods:
  - `displaystock()`: Displays the current number of available bikes.

### 2. `Customer (BikeRental)`

- Inherits from `BikeRental`.
- Handles individual customer transactions.
- Attributes:
  - `number_of_bikes`: Number of bikes the customer wants to rent.
  - `rentalBasis`: `'day'` or `'week'`.
  - `number_of_days_or_weeks`: Rental period in days or weeks.
- Methods:
  - `rentBike()`: Validates and updates stock.
  - `returnBike(rentalBasis)`: Calculates and returns the rental bill.

---

## 💰 Billing Logic

| Rental Basis | Rate (per bike) | Family Discount |
|--------------|------------------|-----------------|
| Day          | ₹100/day         | 30% off (if 3–5 bikes) |
| Week         | ₹500/week        | 30% off (if 3–5 bikes) |

---

## 🧾 Sample Usage

# Create a customer who rents 2 bikes for 5 days
Customer_1 = Customer(2, 'day', 5)
print(Customer_1.rentBike())
print(Customer_1.returnBike('day'))

📦 Edge Case Handling
Renting 0 or negative bikes shows an error.

If requested bikes exceed available stock, the system displays the current availability.

Welcome to rental bike shop.
Total No. Of Stock Is Available : 100
The Updated Stock is : 98
Bill By daily : 1000
...
You are eligible for Family rental promotion of 30% discount : 840.0

📌 Notes
This is a console-based simulation.

No persistent storage — stock resets when the program restarts.

Code can be extended to support hourly rentals, user login, etc.

📂 File Structure

bike_rental_system.py   # Main Python script containing the BikeRental and Customer classes
README.md               # Project documentation

🔧 To Run the Project
Make sure you have Python 3 installed. Then execute:

👤 Contributors
Ketan Talware

📄 License
This project is open-source and free to use.
