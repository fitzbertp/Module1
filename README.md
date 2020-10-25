# Module1
//This Program use A Structure and takes two separate time as input then displays the sum of both time values.

#include <iostream>
using namespace std;

struct TimeIn
{
	int hour1, minute1;
	int hour2, minute2;
	int hour, minute;
};

int main(void)
{
	struct TimeIn t1, tfnl; 
	struct TimeIn t2 = { 1 };

	cout << "**Enter first time as formatted below**" << endl;
	cout << " hh mm" << endl;

	cin >> t1.hour1;
	while (t1.hour1 >= 24)
	{
		cout << "invalid input\n" << endl;
		cout << " hh mm" << endl;
		cin >> t1.hour1;
	}

	cin >> t1.minute1;
	while (t1.minute1 >= 60)
	{
		cout << "invalid input\n" << endl;
		cout << " hh mm" << endl;
		cin >> t1.minute1;
	}

	cout << endl;
	cout << "**Enter second time as formatted below**" << endl;
	cout << " hh mm" << endl;

	cin >> t1.hour1;
	while (t1.hour1 >= 24)
	{
		cout << "invalid input\n" << endl;
		cout << " hh mm" << endl;
		cin >> t1.hour1;
	}

	cin >> t1.minute1;
	while (t1.minute1 >= 60)
	{
		cout << "invalid input\n" << endl;
		cout << " hh mm" << endl;
		cin >> t1.minute1;
	}
		
	tfnl.minute1 = t1.minute1 + 60 * t1.hour1;
	tfnl.minute2 = t2.minute2 + 60 * t2.hour2;

	if (tfnl.minute2 > tfnl.minute1)
	{
		tfnl.minute = tfnl.minute2 - tfnl.minute1;
		tfnl.hour = tfnl.minute / 60;
		tfnl.minute = tfnl.minute % 60;
		cout << tfnl.hour << ":" << tfnl.minute << endl;
	}
	else (tfnl.minute1 > tfnl.minute2)
	{
		tfnl.minute = tfnl.minute1 - tfnl.minute2;
		tfnl.hour = tfnl.minute / 60;
		tfnl.minute = tfnl.minute % 60;
		cout << tfnl.hour << ":" << tfnl.minute << endl;
	}
	
	return 0;

}
