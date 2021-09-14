# Easy Payment Gateway - Java Challenge

## Objective
Evaluate your OO analysis and modelling skills, developing skills, how you structure your code and design an API.
You should not need to spend more than 4 hours in the task, if the solution provided is incomplete, explain which parts you decided
to focus on and why they are relevant.

Keep the objective in mind, feel free to use any tool, libraries, or frameworks, Modify the README.md file, adding about the decisions you
made, what you focused on and what you did not focus and why, as well as how to run and use the program.

## The problem - Car rental system

For a car rental system, we want to create a piece of software for managing the rental administration with three primaries
functions:
  *	Have an inventory of cars
  *	Calculate the price for rental
  *	Keep the track of the customer loyalty points

## Price
The price of rentals is based in the type of the car and how many days it has been rented for.
The users will say when renting the car for how many days they want to rent it and they will pay up front.
If the car is returned late, then rent for extra days will be charged when returning.

The system has three types of cars:

  *	Premium cars- Price is __premium price__ times number of days rented.
    *	Extra day: __premium price__ + 20% of <premium price>

  *	SUV cars - Price is:
    *	For the first 7 days: __SUV price__ per day.
    *	Between 7 and 30 days: 80% of __SUV price__ per day.
    *	More than 30 days: 50% of __SUV price__ per day
    *	Extra day: __SUV price__ + 60% of __small price__ per day

  *	Small cars - Price is:
    *	For the first 7 days: __small price__ per day.
    *	More than 7 days: 60% of <__small price__ per day
    *	Extra day: __small price__ + 30% of __small price__

Prices:
  * __premium price__: 300€
  * __SUV price__: 150€
  * __small price__: 50€

The program should expose a rest-api HTTP API (you could use any framework, if you don’t have a personal preference, you could
use Spring Boot)

The API should (at least) expose the following operations:
  *	Rent one or several cars and calculate the price.
  *	Return a car and calculate surcharges (if exist)
  
Example of price calculations
  *	BMW 7 (Premium) 10 day -> 3000€
  *	Kia Sorento (SUV) 9 days -> 1290€ 
  *	Nissan Juke (SUV) 2 days -> 300€
  *	Seat Ibiza (small) 10 days -> 440€

When returning cars late:
  *	BMW 7 (Premium) 2 extra days -> 720€
  *	Nissan Juke (SUV) 1 day extra -> 180€

## Loyalty points.
 
Customers get loyalty points when renting a car, regardless of the time.
  *	Premium car: 5 points.
  *	SUV car: 3 points.
  *	Small car: 1 point.

