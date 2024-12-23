Parking Lot System Overview
The Parking Lot System is designed to manage vehicle parking spaces efficiently, handling different vehicle types and their space requirements. The system also calculates parking fees based on hourly rates and ensures that vehicles are parked and removed from spaces correctly.

Key Features:
Vehicle Types:
Different types of vehicles like Car, Sports Car, Truck, Bus, and Bike are supported. Each vehicle type has a defined number of spaces required (e.g., Trucks require 2 spaces, Cars require 1 space).
Vehicle Class:
The Vehicle class holds information about a vehicle’s registration number, type, color, entry time, and a unique token for identification.
Parking Spaces:
VehicleSpace represents an individual parking spot. Each space can either be available or occupied by a vehicle. The system can track which space is occupied and which is free.
Floors:
The parking lot consists of multiple floors, with each floor containing several parking spaces. Each floor can accommodate different vehicle types based on the available spaces.
Cost Calculation:
HourlyCostStrategy calculates the parking fee based on the type of vehicle and the time spent in the parking lot. The cost is calculated per hour and varies based on the vehicle type (e.g., Bikes are cheaper than Trucks).
Parking Operations:
Vehicles can be parked if there is sufficient space. The system checks for availability on each floor and assigns a parking space.
Vehicles can be removed, and the system calculates the total parking fee based on the duration of the stay.


Error Handling:
If there are no available spaces or a vehicle is already parked, a ParkingException is thrown.


Status Display:
The system provides a function to display the current parking lot status, including the availability of spaces on each floor.


How it Works:
When a vehicle arrives, it is assigned to the first available space that can accommodate its type.
The vehicle’s entry is logged, and a unique token is generated.
The system tracks the vehicle's stay and calculates the cost when it leaves based on the time spent in the parking lot.
The parking space is vacated once the vehicle leaves.


Core Classes:
Vehicle: Represents the vehicle's details.
VehicleSpace: Represents a parking space.
Floor: Represents a floor in the parking lot, containing several spaces.
ParkingLot: Manages the overall parking system, including vehicle parking, space availability, and cost calculation.
