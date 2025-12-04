Updated version:
PROJECT TITLE: Transportanize

Problem Statement:
Transportation data not being properly utilized, distributed or analyzed and traffic congestion.
These are problems being faced in the
Philippines in regards to transportation. Why should we even worry about such problems?
These problems
can lead to even more issues in the future, 
let's take traffic congestion for example. If all cars are stuck in one place they would be forced to stay on for a longer period therefore releasing more dangerous funes from the exhaust of diesel-power ed vehicles, this leads to air pollution and even more complicated issues in the future.

In conclusion, these problems on transportation may start out small but with time it can become a much bigger threat.

Project Objectives:
1. Let users filter trips using different criteria such as destination, bus type, trip ID, or status.
2. Keep a record of previously displayed trips for easy reference.
3. Allow users to perform multiple searches continuously without restarting the program.

Planned Features:
The code will ask the user for a criteria to sort the trips with (destination, travel duration, bus operator).
The code will ask for a secondary criteria if any.
The code will display the number of trips that fill the criteria.
The code will display the average occupancy rate of the trips that fill the criteria.
The code will display the average fare of the trips that fill the criteria.

Planned inputs:

1.) The user will search primary criterions such as destination, trip_id, bus_type, etc.
“Choose a primary criteria:”
2.)  The user will then select a specific value from the list of available values under that criterion.
“Enter a value from the list above:”
3.)  The user can also choose whether to view previously displayed trips or exit the program.
“Choose an option:”

Planned outputs: 

1.) Display the list of trips that match the selected criterion and value.
“All values under 'main_criteria':”, list of trips
2.) The program will display all previously viewed trips when the user requests it.
“All previously displayed trips”, list of previous trips 
3.)  Allow the user to perform multiple searches through a loop until they choose to exit.
“Choose an option:”

Planned Logic:
Load JSON file
Display options for criteria
Input first criteria
Input second criteria 
Take and display the average occupancy rate based on the range of the criteria/s
Take and display the average fare based on the range of the criteria/s
Take and display the number of trips that are within the range of the criteria/s

PSEUDOCODE:

Start Main
Load tripData using loadJsonFile
Flatten the trip data and store it in flatTripData = flatten(tripData)
Set history as a string
Set userInput as an integer
While userInput is not equal to 0:
    Display "[1] Search Trips"
    Display "[2] View History"
    Display "[0] Exit"
    Get userInput
    If userInput equals 1:
        Display availableCriteria
        Get chosenCrit
        Display allValInCriteria
        Get chosenVal
        Find matching trips using findMatchingTripsBasedOnCriteria and store as tripsFound
        Display tripsFound
        Append tripsFound to history
    Else if userInput equals 2:
        Display allTripsInHistory
    Else if userInput equals 0:
        Display "You have exited the program."
End While
End Main
