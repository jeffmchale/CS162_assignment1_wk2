#include <iostream>
#include <cctype>
#include <cmath>

using namespace std;

//////////////////////////////////////////////////////////////////////////////////////////////////////////////////
//CS162
//Time Management Program
//Jeff McHale
// ––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––––
//A program that helps users manage their time with important assignments. A user will determine how many hours
//they need to finish an upcoming assignment. Then, after inputting the total amount of free days they have
//available to work on the assignment, a calculation is performed to determine the average hours of work that
//are required per day to meet the deadline. After determining total free hours that the user has available,
//the program will compare the average hours of work per day to this value, notifying the user if they have enough
//time free in order to finish their assignment or not.
//////////////////////////////////////////////////////////////////////////////////////////////////////////////////



int main()
{

        // Variables
        double hours_Expected = 0;              //Total hours expected to complete assignment

        double available_Days = 0;              //Total amount of days user is able to work before due date

        double average_Hours = 0;               //Holds the amount of hours a user will need to program per day

        double free_Hours = 0;                  //Stores total hours user spends on free time

        double counter = 0;                     //Used alongside free_Hours to keep track of user's total spent time throughout the day

        char user_Choice;                       //Will be used to allow user to reset values if desired


    //Greet User
    cout << "Welcome! This program will help manage your time with programming assignments!" << endl;


    //Entire program is inside this do while loop. 
    //If the user chooses to reset values at the end, they have the option to jump back up to the beginning.
    do
    {
         //Get hours expected to complete assignment
         cout << "How many hours are anticipated to complete this programming assignment?" << endl;
         cin >> hours_Expected;
         cin.ignore(100, '\n');

         //Put in place to protect program against bad data input
         if (hours_Expected == 0)
         {
            cout << "You've already failed." << "\nGoodbye" << endl;
            return 0;
         }

        cout << "You entered: " << abs(hours_Expected) << " hours." << "\nIs this a sufficient amount of time?"
             << "\nTo change value, input N. Otherwise, enter c to continue" << endl;


        cin >> user_Choice;
        cin.ignore(100, '\n');
        user_Choice = toupper(user_Choice);

        do
        {

          if (user_Choice == 'N')
            {
                cout << "Please enter new value" << endl;
                cin >> hours_Expected;
                cin.ignore(100, '\n');
                cout << "You entered: " << abs(hours_Expected) << " hours."
                     << "\nIs this amount correct? Enter N to change value. Otherwise, enter c to continue." << endl;

                cin >> user_Choice;
                cin.ignore(100, '\n');
                user_Choice = toupper(user_Choice);
            }

         } while (user_Choice == 'N');
         
        //Get total available days to work on assignment
        cout << "How many days are you able to work until your assignment is due?" << endl;
        cin >> available_Days;
        cin.ignore(100, '\n');

        cout << "You entered: " << abs(available_Days) << " days." 
             << "\nIs this the correct amount of days? Enter N to change value. Otherwise, enter c to continue." << endl;

        cin >> user_Choice;
        cin.ignore(100, '\n');
        user_Choice = toupper(user_Choice);

        do
        {

          if (user_Choice == 'N')
            {
                cout <<  "Please enter the amount of days you're able to work until your assignment is due." << endl;
                cin >> available_Days;
                cin.ignore(100, '\n');
                cout << "You entered: " << abs(available_Days) << " days." 
                     << "\nIs this correct? Enter N to change value. Otherwise, enter c to continue." << endl;

                cin >> user_Choice;
                cin.ignore(100, '\n');
                user_Choice = toupper(user_Choice);
            }

        } while(user_Choice == 'N');


        // Uses absolute value for calculation so sneaky TA's won't break program with negative integers
        average_Hours = abs(hours_Expected / available_Days);

        cout << "\n--------------------------------------------------------------------------------------------------------\n"
        cout << "Based on the numbers provided, you need to work " << average_Hours << " hours each day to meet your deadline" << endl;

        do
        {
                //Get total hours spent on average each day
                cout << "\n--------------------------------------------------------------------------------------------------------\n"
                     << "Now, please enter how many free hours per day are spent on school and/or work?" << endl;
                cin >> counter;
                cin.ignore(100, '\n');
                free_Hours += abs(counter);

                cout << "How many personal hours are needed per day? (Ex: eating, sleeping, exercise, etc..)" << endl;
                cin >> counter;
                cin.ignore(100, '\n');
                free_Hours += abs(counter);

                cout << "How many hours a day are spent with free time?" << endl;
                cin >> counter;
                cin.ignore(100, '\n');
                free_Hours += abs(counter);

                cout << "How many additional hours per day are spent on classes and homework?" << endl;
                cin >> counter;
                cin.ignore(100, '\n');
                free_Hours += abs(counter);

                cout << "Based on the data provided, total time spent on mentioned tasks is: " << abs(free_Hours) << " hours." 
                     << "\nWould you like to reset these values?" 
                     << "\nEnter N to change values. Otherwise, enter c to continue." << endl;

                cin >> user_Choice;
                cin.ignore(100, '\n');
                user_Choice = toupper(user_Choice);
                counter = free_Hours;                //counter is set equal to free_Hours to perform future calculation if do while is not repeated
                free_Hours = 0;                      //free_Hours is set to zero to prevent adding old values if the do while loop is repeated
                                                        
        } while(user_Choice == 'N');


        //Takes total free time user has and subtracts from 24 to determine available hours to program
        counter = 24 - abs(counter);


        //Compares user free time with average amount of hours required to finish assignment
        if(counter >= average_Hours)
        {
            cout << "\nWith current inputs, you will be able to meet programming deadline!" << endl;
        }
        else
        {
            cout << "\nWith current inputs, you will not be able to meet programming deadline. :(" << endl;
        }

        cout << "\n--------------------------------------------------------------------------------------------------------\n"
             << "Would you like to reset this program to test new values?" 
             << "\nPlease enter Y to reset. Otherwise, press t to terminate program." << endl;
             
        cin >> user_Choice;
        cin.ignore(100, '\n');
        user_Choice = toupper(user_Choice);


    } while(user_Choice == 'Y');


        cout << "Thanks for using this program!" << endl;

        return 0;

}
