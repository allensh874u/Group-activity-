# Group-activity-
#include <iostream>

using namespace std;

int main() {
  // Constants for the conversion factor
  const double gramsPerPound = 453.592;

  //Declare variables
  double grams, pounds;

  // Get input from the user
  cout << "Enter weight in grams: ";
  cin >> grams;

  //Error handling for negative input
  if (grams < 0) {
    cout << "Weight cannot be negative. Please enter a non-negative value." << endl;
    return 1; // Indicate an error
  }

  // Perform the conversion
  pounds = grams / gramsPerPound;

  // Display the result
  cout << grams << " grams is equal to " << pounds << " pounds." << endl;

  return 0; // Indicate successful execution

}

#include <iostream>
#include <cmath>

using namespace std;

int main() {
  double diameter, radius, area;

  cout << "Enter the diameter of the circle: ";
  cin >> diameter;

  //Error handling for negative diameter
  if (diameter < 0) {
    cout << "Diameter cannot be negative. Please enter a non-negative value." << endl;
    return 1;
  }

  //Calculate radius
  radius = diameter / 2.0;

  //Calculate area using M_PI for better precision.
  area = M_PI * radius * radius;

  cout << "The area of the circle is: " << area << endl;

  return 0;
}

#include <iostream>
#include <limits> // Required for numeric_limits

using namespace std;

int main() {
    double distance, time, speed;

    // Get inputs from the user.  Improved input validation included.
    cout << "Enter the distance traveled (in kilometers): ";
    while (!(cin >> distance) || distance < 0) {
        cout << "Invalid input. Please enter a non-negative number: ";
        cin.clear(); // Clear error flags
        cin.ignore(numeric_limits<streamsize>::max(), '\n'); // Discard invalid input
    }

    cout << "Enter the time taken (in hours): ";
    while (!(cin >> time) || time <= 0) {
        cout << "Invalid input. Please enter a positive number: ";
        cin.clear();
        cin.ignore(numeric_limits<streamsize>::max(), '\n');
    }

    // Calculate the speed.
    speed = distance / time;

    // Display the result.
    cout << "The speed of the car is: " << speed << " km/h" << endl;

    return 0;
}
