#include <iostream>
#include <string>
#include <time.h>
using namespace std;
int Guess(int random);
int main() 
{
  srand(time(NULL));
  int random = rand() % 9 +1, round = 0;
  
  cout << "###Welcome to guessing number game###" << endl;
  cout << "Secret number has been chosen" << endl;

  round = Guess(random);
  
  
  cout << "Congratulations!" << endl;
  cout << "The secret number is " << random << endl;
  cout << "You made " << round << " guesses" << endl;
  system("pause");
  
  return(0);
  
}

int Guess(int random)
{
  int round = 0,number = 0;
  do
  {
    cout << "Guess the number (1 to 10) : ";
    cin >> number;
    
    if (random > number)
    {
      cout << "the scret number is lower" << endl;
    }
      
    else if (random < number)
    {
      cout << "the secret number is higher" << endl;
    }
      
    round++;
  
  } while (random != number);
  return(round);
}
