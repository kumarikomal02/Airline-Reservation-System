# Airline-Reservation-System

Project Overview:
This project is a simple Flight Reservation System implemented in C++. The program allows users to reserve seats on available flights. It manages flight information (flight number, departure and destination locations, capacity) and facilitates seat reservations for passengers.

Key Features:
Flight Management:

The program maintains a list of available flights, each having a flight number, departure location, destination, and total seat capacity.
Seat Reservation:

The user can choose to reserve a seat on a flight. The system checks if there are available seats, reserves one if possible, and informs the user accordingly.
User Interaction:

The user interacts with the system via a simple menu where they can either reserve a seat or exit the program.
Classes Explanation:
Flight Class:

Private Attributes:

flightNo: The flight number (string).
departure: The departure location (string).
destination: The destination location (string).
capacity: The total number of seats available (integer).
reserved: The number of seats that have been reserved (integer).
Constructor:

Initializes the flight details, with reserved set to 0 initially.
reservation() Method:

Checks if a seat can be reserved by comparing the number of reserved seats with the total capacity. If there is space, it reserves one seat and returns true; otherwise, it returns false.
friend class ReservationSystem:

The ReservationSystem class is granted access to the private members of the Flight class, allowing it to manage the reservations.
ReservationSystem Class:

Private Attributes:
ve: A vector that stores all the flights available for reservation.
Methods:
add(): Adds a new flight to the system by creating a Flight object and pushing it to the vector ve.

reserveSeat(): Displays available flights to the user, prompts them to choose a flight by its number, and attempts to reserve a seat. If seats are available, it reserves one seat; otherwise, it informs the user that no seats are available.

main() Function:

The main function initializes the ReservationSystem, adds a few flights to the system, and enters a loop where the user can choose to reserve a seat or exit.
It uses system("cls") (Windows-specific) to clear the screen after each reservation attempt.
Flow of the Program:
Flight Initialization:

In main(), three flights are added to the system using the add() method, each with a specific flight number, departure location, destination, and seating capacity.
User Interaction:

After the flights are added, the user is prompted with the option to either reserve a seat or exit.
If the user selects to reserve a seat, they are shown a list of available flights.
Seat Reservation:

The user enters a flight number to reserve a seat.
The system checks if seats are available on the chosen flight using the reservation() method of the Flight class.
If a seat is available, it reserves one seat and notifies the user.
If no seats are available, the system notifies the user that the flight is fully booked.
Exit:

If the user selects 0, the program exits the loop and terminates.
Sample Input/Output:
Input: The user selects to reserve a seat and enters a flight number (e.g., F101).

Output: The system shows flight details and either reserves a seat or informs the user that no seats are available.

Example Flow:
Adding Flights: The system initially adds three flights with different destinations and seat capacities.

Flight Reservation: The user chooses to reserve a seat by selecting option 1 from the menu, views available flights, and inputs a flight number (e.g., F101).

Successful Reservation: If seats are available on the chosen flight, a seat is reserved, and the user is notified.

Exit: The user can exit the system by selecting option 0 from the menu.

Improvements and Extensions:
Validation: Add checks for invalid flight numbers or incorrect user input.
Dynamic Capacity: Allow dynamic adjustment of flight capacity.
Flight Deletion: Implement functionality to remove flights from the system.
User Authentication: Add functionality for users to log in before making a reservation.
Conclusion:
This project demonstrates basic object-oriented programming (OOP) concepts such as classes, constructors, methods, and friend functions in C++. It creates a simple flight reservation system where users can view available flights and reserve seats based on the availability.


