#include<iostream>
#include<cstdlib>
#include<ctime>
using namespace std;
int main()
{
    srand((unsigned int)time(NULL));
    int number=(rand()%100)+1;
    int guess;
    int attempts=0;

    cout << "\nwelcome to the number guessing game\n" << endl;
    cout <<"\nlet guess number between 1 to 100\n" <<endl;
    do
    {
        cout <<"enter the guess: \n";
        cin >>guess;

        attempts++;

        if(guess>number)
        {
            cout <<"Number Is Too High\n" <<endl;
        }
        else if(guess<number)
        {
            cout << "Number Is Too Low\n" <<endl;
        }
        else
        {
            cout <<"\nCongrats You Guess The Number...!!! in: " <<attempts<<"attempts\n" <<endl;
            break;
        }
    } while (true);
    return 0;   
}
