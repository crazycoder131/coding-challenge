# Coding Guidelines

 1. Any object-oriented language is acceptable, but it would score points to do it in C# or Java.
 2. We want people who like writing unit tests.  So design your code to be testable, and write the best unit tests you can.  If you do TDD - perfect!
 3. Submit clean code and try to adhere to S.O.L.I.D. principles. Remember this is a test, we will judge your design.
 4. The more efficient your code is, the better.

# Submission Guidelines

 1. Clone this  repo to your git and work on it. 
 2. Include all source code including unit test projects.
 3. Creat a PR(Pull Request) to my master branch from  your branch.
 4. Include a "Readme" file with instructions on how to run your application.

# Build an Elevator Coding Challenge!
Create an application that simulates the operation of a simple elevator.
 In this challenge you will code an elevator that asynchronously accepts inputs in the form of button presses that call the elevator to a floor in a given direction (or to exit the elevator at a floor).  Make your elevator function like it would in the real world.

## Requirements
 - The elevator must travel in one direction at a time until it needs to go no further (**e.g.** keep going until the elevator has reached the top/bottom of the building, or no stop is requested on any floor ahead).
 - Elevator floor request buttons can be pressed **asynchronously** from inside or outside the elevator while it is running.
 - Elevator will stop at the closest floor first, in the direction of motion, then the next closest and so on. Any floors requested while the elevator is moving should be taken into account.
 - Elevator will stop at all asynchronously requested floors, only if the request is made while the elevator is at least one floor away (**e.g.** if elevator is **between** 4th and 5th floor, going up, and the 5th floor is requested at that moment, elevator will not stop at the 5th floor while going up; it will stop there while going down).
 - When elevator arrives at a requested floor, it waits for 1 second. It takes 3 seconds to travel between consecutive floors.
 - A sensor tells the elevator its direction, next/current floor, state (stopped, moving) and if the elevator has reached its max weight limit.
 - Use the sensor data plus the asynchronous floor request button data to work the elevator.
 - Write meaningful **unit tests** that show the elevator works correctly, even if the application is not run.
 - Log the following to a file, to verify elevator works well:
	 - Timestamp and asynchronous floor request, every time one occurs.
	 - Timestamp and floor, every time elevator **passes** a floor.
	 - Timestamp and floor, every time elevator **stops** at a floor.

**Bonus Enhancement:**
 - Enhance the application as follows: If the elevator has reached its weight limit, it should stop only at floors that were selected from inside the elevator (to let passengers out), until it is no longer at the max weight limit.

**Note:** For simplicity, the asynchronous request buttons can be entered by the application user via the console, by entering **"5U"** (request from 5th floor wanting to go Up) or **"8D"** (request from 8th floor wanting to go Down) or **"2"** (request from inside elevator wanting to stop at 2nd floor).  When the user enters **"Q"** on the console, the application must end after visiting all floors entered before **"Q"**.
