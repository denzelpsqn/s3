# s3

#include <iostream>
#include <string>
using namespace std;

int main() {

	string ans;
	char loc;

	cout << "Welcome to Coffee Tea Machine" << endl;
	cout << "============================" << endl;
	cout << "           MENU           " << endl;
	cout << "Coffee\t      Price(AED)\tTea      \tPrice(AED)" << endl;
	cout << "Ice Coffee\t3         \tIce Tea  \t3 " << endl;
	cout << "Milk Coffee\t2         \tMilk Tea  \t2 " << endl;
	cout << "Black Coffee\t1         \tBlack Tea  \t1 " << endl;

	cout << "\n\nWhat would you like to drink?\n" << endl;
	cout << "\n Enter 'A' for Ice Coffee";
	cout << "\n Enter 'B' for Milk Coffee";
	cout << "\n Enter 'C' for Black Coffee";
	cout << "\n Enter 'D' for Ice Tea";
	cout << "\n Enter 'E' for Milk Tea";
	cout << "\n Enter 'F' for Black Tea\n";
	cout << "\n Please enter your order: ";
	cin >> loc;

	switch (loc) {

	case 'A':
		cout << " Ice Coffee : AED 3." << endl;
		break;
	case 'B':
		cout << " Milk Coffee : AED 2." << endl;
		break;
	case 'C':
		cout << " Black Coffee : AED 1." << endl;
		break;
	case 'D':
		cout << " Ice Tea : AED 3." << endl;
		break;
	case 'E':
		cout << " Milk Tea : AED 2." << endl;
		break;
	case 'F':
		cout << " Black Tea : AED 1." << endl;
		break;
	default:
		cout << " No Drinks available." << endl;
	}

	cout << "\n\nWould you like to add sugar or not? (Yes/No)" << endl;
	cin >> ans;

	if (ans == "Yes") {
		cout << "Okay, Sugar will be added!" << endl;
	}
	else if (ans == "No") {
		cout << "Okay, No sugar will be added!" << endl;
	}
	else {
		cout << "Invalid answer." << endl;
	}


	return 0;
}
