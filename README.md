# Exercise-8



#include <iostream>
#include <exception>
#include <string>

using namespace std;
int main()
{


    

    cout << "Enter your full name" << endl;
    string name;
  // cin cannot read spaces, that is why we can use the getline code to read the input untill the next line
    getline(cin, name);
    

    cout << "\nEnter The Marks Between 0 To 100 to check your grade:";

    cout << "\nEnter The Mark: ";
    int marks;

    std::cin >> marks;
    //Using the cin.fail function (when user enters alphabet instead of numbers)
    if (std::cin.fail())
    {
        std::cin.clear();
        std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');
        std::cout << "Incorrect command\n: ";
    }

    else if (marks > 100)

    {

        /* Marks greater than 100 */

        cout << "\nKindly input your Marks Between Limit\n";
    }

    else

    {

        switch (marks / 10)

        {

        case 10:

        case 9:
        case 8:

        {
            /* Marks between 80-100 */


            cout << name <<" Your Grade Is: A Excellent";


            break;
        }
        case 7:
        {    /* Marks between 70-79 */
            cout << name << " Your Grade Is: B Very Good";
            break;
        }
        case 6:
        {
            /* Marks between 60-69 */


            cout << name << " Your Grade Is: C Fair";
            break;
        }
        case 5:
        {
            /* Marks between 50-59 */
            cout << name << " Your Grade Is: D Need more practice";
            break;
        }
        case 4:
        {
            /* Marks between 40-49 */
            cout << name << " Your Grade Is: E Need more practice";
            break;
        }
        default:
        {
            /* Marks less than 40 */
            cout << name << " You Grade Is: F or Fail\n";

        }
        }
    }
}
  
  
  
  
  
  #include <iostream>
using namespace std;
int main()
{
    cout << "What is the capital of France? Select the option from below\n";
    cout << "\n Enter 'P' for Paris";
    cout << "\n Enter 'D' for Dubai";
    cout << "\n Enter 'N' if you don't know\n";
    char capital;
    cin >> capital;
    switch (capital)
    {
    case 'P':
    case 'p':
    {
        cout << "You're right, the capital of France is Paris" << endl;
        break;
    }
    case 'd':
    case 'D':
    {
        cout << "You're wrong, the capital of France is Paris not Dubai " << endl;
        break;
      }
    case 'n':
    case 'N':
    {
        cout << "The capital of France is Paris" << endl;
        break; 
    }
    default:
    {
        cout << "Incorrect command";
    }
    }
    return 0;
}
  
  
  
  
  
  #include<iostream>
using namespace std;
int main()
{
	int side;
	cout << "Enter the sides number to see the shape name (minimum 3 sides, maximum 10) \n";
	cin >> side;
	switch (side)
	{
	case 1:
	case 2:
	{ cout << "The minimum side required is 3, you have entered less than the requirement" << endl; break; }
	case 3:
	{ cout << "Triangle  has " << side << " sides" << endl;
		break;
	}
	case 4:
	{ cout << "Square | Rectangle has " << side << " sides" << endl;
		break;
	}
	case 5:
	{cout << "Pentagon has " << side << " sides" << endl;
		break;
	}
	case 6:
	{ cout << "Hexagon has " << side << " sides" << endl;
		break;
	}
	case 7:
	{ cout << "Heptagon has " << side << " sides" << endl;
		break;
	}
	case 8: 
	{ cout << "Octagon has " << side << " sides" << endl;
		break;
	}
	case 9:
	{ cout << "Nonagon has " << side << " sides" << endl;
		break;
	}
	case 10:
	{ cout << "Decagon has " << side << " sides" << endl;
		break;
	}
	default:
	{
		cout << "Incorrect command" << endl;
		break;
	}
	}
}
  
  
  
  
  
  
  
#include <iostream>
using namespace std;
int main()
{
    
    char temp;
    double tempInput;

    cout << "Would you like to convert Celsius to Farenheit? or Farenheit to Cesius? \n";
    cout << "[C] for C to F or [F] for F to C \n";
    cin >> temp;

    switch (temp)
    {
    case 'C':
    case 'c':
        cout << "insert temperature in Celsius to convert in Farenheit\n";
        cin >> tempInput;
        cout << "You entered " << tempInput << "C's. That would be " << (tempInput * 1.8) + 32 << "Degrees Farenheit";

        break;

    case 'F':
    case 'f':
        cout << "Insert temperature in Farenheit to convert in Celsius\n";
        cin >> tempInput;
        cout << "You entered " << tempInput << ". That would be " << 5 * (tempInput - 32) / 9 << "Degrees Celsius";

        break;
    default:
        cout << "Invalid input!  Please enter a number.";

        break;

    }
    return 0;
}


  
  
  
  #include <iostream>
using namespace std;
int main()
{
    
    char gas;
    int gasAmt;

    cout << "Please enter your type of fuel to continue\n";
    cout << "[P] for Petrol or [D] for Diesel\n";
    cin >> gas;


    switch (gas)
    {
    case 'p':
    case 'P':
        cout << "You chose petrol, how many liters do you need? Rate: 2AED Per liters\n";
        cin >> gasAmt;
        cout << "You entered " << gasAmt << " liters. that would be " << gasAmt * 2 << " AED";

        break;

    case 'd':
    case 'D':
        cout << "You chose diesel, how many liters do you need? Rate: 3AED Per liter\n";
        cin >> gasAmt;
        cout << "You entered " << gasAmt << " liters. that would be " << gasAmt * 3 << " AED";

        break;
    default:
        cout << "Invalid input";

        return 0;

    }
    
}
  
  
  
  
  
  
  
  
  #include <iostream>

using namespace std;
int main()
{

		cout << "Would you like to continue? (Y/N): "; 
		char answer; 
		cin >> answer; 

			switch (answer)
			{ 
			
			case 'Y':
			case 'y':
			{
				cout << "You selected yes";
				break;
			}
					
			case 'N':
			case 'n':
			{
				cout << "You selected no";
				break;
			}
					
			default: 
			{
				cout << "incorrect command";
			}

			}
		cin.get(); //keeps console window open in Visual Studio
		return 0;
	}

  
  
  
  
  
  
  
  #include <iostream>
using namespace std;
int main()
{

	cout << "Kindly select the option number for the month you want to see the days of:\n";

	cout << " 1. January\n 2. February\n 3. March\n 4. April\n 5. May \n 6. June \n 7. July \n 8. August\n 9. September\n 10. October\n 11. November\n 12. December\n";
	int a;
	cin >> a;


	switch (a)
	{
	case 1:
	{
		cout << "The month of January have  days 31";
		break;
	}
	case 2:
	{
		cout << "The month of February have  days 28 if there is a leap year than 29";
		break;
	}
	case 3:
	{
		cout << "The month of March have  days 31";
		break;
	}
	case 4:
	{
		cout << "The month of April have  days 30";
		break;
	}
	case 5:
	{
		cout << "The month of May have  days 31";
		break;
	}
	case 6:
	{
		cout << "The month of June have  days 30";
		break;
	}
	case 7:
	{
		cout << "The month of July have  days 31";
		break;
	}
	case 8:
	{
		cout << "The month of August have  days 31";
		break;
	}
	case 9:
	{
		cout << "The month of September have  days 30 ";
		break;
	}
	case 10:
	{
		cout << "The month of October have  days 31";
		break;
	}
	case 11:
	{
		cout << "The month of November have  days 30";
		break;
	}
	case 12:
	{
		cout << "The month of December have  days 31";
		break;
	}

	default:
	{
		cout << "Invalid Input" << endl;
		break;
	}
	}

}
  
