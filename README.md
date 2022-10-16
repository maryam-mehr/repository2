# repository2
copy constructor
#include<iostream>
using namespace std;
class Time
{
	//private data members
	int hours;
	int minutes;
	int seconds;
public:
	//mutators
	void getvalues()
	{
		cout << "enter hours" << endl;
		cin >> hours;
		cout << "enter minutes" << endl;
		cin >> minutes;
		cout << "enter seconds" << endl;
		cin >> seconds;
	}
    //accessors
	void display(Time &t)
	{
		cout << t.hours << ":" << t.minutes << ":" << t.seconds << endl;
	}
	//default constructor
	Time()
	{
		cout << "default constructor called" << endl;
		hours = 0;
		minutes = 0;
		seconds = 0;
	}
	//copy constructor
	Time ( const Time &t)
   {
		cout << "copy constructor called" << endl;
		hours = t.hours;
		minutes = t.minutes;
		seconds = t.seconds;
	}
};
int main()
{
	Time t; 
	t.getvalues();
	Time t2 = t;
	Time::Time(t);
	t.display(t);
	t2.display(t2);

}
