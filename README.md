# Parking Lot System

The Parking Lot System is designed to efficiently manage vehicle parking spaces and their associated costs. The system supports various vehicle types and handles the management of parking spaces, including cost calculations based on hourly rates and ensuring that vehicles are parked and removed correctly.

## Features

### 1. **Vehicle Types**
   - The system supports different types of vehicles, including:
     - **Car**
     - **Sports Car**
     - **Truck** (requires 2 spaces)
     - **Bus**
     - **Bike**
   - Each vehicle type has specific space requirements, such as a truck requiring 2 parking spaces.

### 2. **Vehicle Class**
   - The `Vehicle` class holds details about a vehicle:
     - Registration number
     - Type (Car, Truck, etc.)
     - Color
     - Entry time
     - Unique token for identification

### 3. **Parking Spaces**
   - The `VehicleSpace` class represents individual parking spots.
   - Each parking space can be either:
     - Available
     - Occupied by a vehicle
   - The system tracks which spaces are occupied and which are free.

### 4. **Floors**
   - The parking lot is divided into multiple floors.
   - Each floor contains several parking spaces and may accommodate different vehicle types based on available spaces.

### 5. **Cost Calculation**
   - The `HourlyCostStrategy` class calculates the parking fee based on the type of vehicle and the time spent in the parking lot.
   - Costs vary based on the vehicle type (e.g., Bikes are cheaper than Trucks).

### 6. **Parking Operations**
   - Vehicles can be parked if there are available spaces.
   - The system checks for availability on each floor and assigns a parking space accordingly.
   - Vehicles can be removed, and the system calculates the total parking fee based on the duration of stay.

### 7. **Error Handling**
   - If no spaces are available, or if a vehicle is already parked, a `ParkingException` is thrown.

### 8. **Status Display**
   - The system provides a function to display the current parking lot status, including the availability of spaces on each floor.

## How It Works

1. **Arrival of a Vehicle:**
   - When a vehicle arrives, the system checks for the first available space that can accommodate its type.
   - The vehicle’s entry details are logged, and a unique token is generated for identification.

2. **Tracking Vehicle Stay:**
   - The system tracks the vehicle's stay and calculates the parking fee based on the time spent in the parking lot.

3. **Leaving the Parking Lot:**
   - When the vehicle leaves, the system vacates the parking space.
   - The total parking fee is calculated and displayed based on the duration of stay.

## Core Classes

- **Vehicle**: Represents the details of the vehicle (e.g., registration number, type, color, entry time, token).
- **VehicleSpace**: Represents a single parking space and its availability status.
- **Floor**: Represents a floor in the parking lot, containing multiple parking spaces.
- **ParkingLot**: Manages the overall parking system, including vehicle parking, space availability, and cost calculations.

## Installation

To use the Parking Lot System, follow these steps:

1. Clone the repository:
   ```bash
   git clone <repository-url>
