# Practice
//Asking age with range 16-30

              #include <iostream>
              using namespace std;
              void response(string choice) {
                while ((choice != "y" || choice != "Y") || (choice != "n" || choice != "N")) {
                  if (choice == "y" || choice == "Y") {
                    cout << "You pressed yes, Enjoy the trip" << endl;
                    break;
                  }
                  else if (choice == "n" || choice == "N") {
                    cout << "You pressed no, your trip is now Cancelled" << endl;
                    break;
                  }
                  else {
                    cout << "Try again" << endl;
                    cin.clear();
                    cin.ignore();
                    cin >> choice;
                  }
                }
              }
              void display(int age) {
                string choice;
                if (age >= 16 && age <= 21) {
                  cout << "would you like to go to the mall?(Y/N)";
                  cin >> choice;
                  while (cin.fail()) {
                    cout << "Try again" << endl;
                    cin.clear();
                    cin.ignore();
                    cin >> choice;
                  }
                  response(choice);
                }
                else if (age >= 22 && age <= 30) {
                  cout << "would you like to go to a trip to Hawaii?(Y/N)";
                  cin >> choice;
                  while (cin.fail()) {
                    cout << "Try again" << endl;
                    cin.clear();
                    cin.ignore();
                    cin >> choice;
                  }
                  response(choice);
                }
                else {
                  cout << "INVALID INPUT" << endl;
                }
              }
              int main() {
                int age;
                cout << "Enter Age only between (16-30): "; cin >> age;
                while (cin.fail()) {
                  cout << "Try again" << endl;
                  cin.clear();
                  cin.ignore();
                  cin >> age;
                }
                display(age);
                return 0;
              }
