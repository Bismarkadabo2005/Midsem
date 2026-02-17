# Digital Attendance midsem
Bismark Adabo 
#include <iostream>
#include <string>
using namespace std;

int main() {
    string name;
    string id;
    int level;
    int choice;

    cout << "--- WEEK ONE ATTENDANCE SYSTEM ---\n";

    do {
        cout << "\nMenu:\n";
        cout << "1. Add Student Details\n";
        cout << "2. View Student Details\n";
        cout << "3. Exit\n";
        cout << "Enter choice: ";
        cin >> choice;

        if (choice == 1) {
            cin.ignore(); // Clear the buffer

            cout << "Enter Student Name: ";
            getline(cin, name);

            cout << "Enter Student ID: ";
            cin >> id;

            cout << "Enter Level: ";
            cin >> level;

            cout << "Student details saved!\n";
        }
        else if (choice == 2) {
            if (name != "") { // Check if details were entered
                cout << "\n--- STUDENT DETAILS ---\n";
                cout << "Name: " << name << endl;
                cout << "ID: " << id << endl;
                cout << "Level: " << level << endl;
            } else {
                cout << "No student details found. Please add first.\n";
            }
        }
        else if (choice == 3) {
            cout << "Program ended.\n";
        }
        else {
            cout << "Invalid choice! Try again.\n";
        }

    } while (choice != 3);

    return 0;
}
