#include<vector>
#include <iostream>
using namespace std;

int main()
{
	char selection=0;
	int number;
	vector<int> vec;
	int total=0;
	double average;



	do {
		cout << endl;
		cout << "P - Print Number: " << endl;
		cout << "A - Add number: " << endl;
		cout << "M - Mean of the numbers: " << endl;
		cout << "S - Smallest number: " << endl;
		cout << "L - Biggest number" << endl;
		cout << "Q - Quit: " << endl;
		
		cin >> selection;

		if (selection == 'P' || selection == 'p') {
			if (vec.size() != 0) {
				cout << "[";
				for (auto array : vec) {
					cout << array<<" ";
				}
				cout << "]";
			}
			else {
				cout << "the list is empty";
			}
		}
		else if (selection == 'A' || selection == 'a') {
			
				cout << "Enter a integer to add list: ";
				cin >> number;
				cout << number << " added to the list.";
				vec.push_back(number);
		}


		else if (selection == 'M' || selection == 'm') {
			if (vec.size() !=0 ) {
				for(auto array:vec)
					total += array;
				cout << "the mean of this list: " <<static_cast<double> (total) / vec.size();
			}
			else {
				cout << "the list is empty";
			}
		}
		else if (selection == 'S' || selection == 's') {
			if (vec.size() != 0) {
				int smallest = vec.at(0);
				for (auto array : vec) {

					if (array < smallest) {
						smallest = array;
					}

				}
				cout << "the smallest number in the list is " << smallest;
			}
			else {
				cout << "Unable to determine to find smallest";
			}
		
		}
		else if (selection == 'L' || selection == 'l') {
			if (vec.size() != 0) {
				int largest = vec.at(0);
				for (auto array : vec) {

					if (array > largest) {
						largest = array;
					}

				}
				cout << "the largest number in the list is " << largest;
			}
			else {
				cout << "Unable to determime largest number";
			}
		}
		else if (selection == 'Q' || selection == 'q') {
			cout << "GOOD BYE...";
		}
		else {
			cout << "Unknowed character...";
		}
				
			
		
		


			
			
		

		
		





		
	} while (selection != 'Q' && selection != 'q');
   









	return 0;
}
