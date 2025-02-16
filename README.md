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
