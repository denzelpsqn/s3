# s3

#include <iostream>
#include <string>
using namespace std;

int main() {
	pair<string, double> choc[6] = {
		{"Ice Coffee", 3}, {"Milk Coffee", 2}, {"Black Coffee", 1}, {"Ice Tea", 1}, {"Milk Tea", 1}, {"Black Tea", 1}
	};
	cout << "         Welcome to Coffee Tea Machine" << endl;
	cout << "==============================================" << endl;
	cout << "\n                    MENU             " << endl;
	cout << "\n\nCoffee\t      \t\tPrice\t\tTea      \tPrice" << endl;
	cout << "1. Ice Coffee\t\tAED 3         \t4. Ice Tea  \tAED 3 " << endl;
	cout << "2. Milk Coffee\t\tAED 2         \t5. Milk Tea  \tAED 2 " << endl;
	cout << "3. Black Coffee\t\tAED 1         \t6. Black Tea  \tAED 1 " << endl;
	cout << "\n\n>> What would you like to buy? (Please enter the number): ";


	for (int i = 0; i == 6; i++) {
		cout << i + 1 << ": " << choc[i].first << " AED" << choc[i].second << endl;
	}

	int input;
	cin >> input;
	input--;
	cout << "\n   That will be AED " << choc[input].second << "." << endl;


	string ans;

	cout << "\n\n>> Would you like to add sugar or not? (Yes/No) : ";
	cin >> ans;
	if (ans == "Yes" || ans == "yes") {
		cout << "\n   Okay, Sugar will be added!" << endl;
	}
	else if (ans == "No" || ans == "no") {
		cout << "\n   Okay, No sugar will be added!" << endl;
	}
	else {
		cout << "\n   Invalid answer." << endl;
	}


	cout << "\n\n>> Please enter the amount of your money : ";

	double money;
	cin >> money;



	if (money > choc[input].second) {
		cout << "\n   Here is your change AED " << (money - choc[input].second) << ". Thank you for your order!" << endl;
	}
	else if (money < choc[input].second) {
		cout << "\n   Sorry but you do not have sufficient money." << endl;
	}
	else {
		cout << "\n   Here is your " << ". Thank you for your order!" << choc[input].first << endl;
	}
	return 0;
}
