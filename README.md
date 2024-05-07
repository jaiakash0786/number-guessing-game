# number-guessing-game
#include<iostream>
#include<cstdlib>
#include<ctime>
using namespace std;
class guess {
    int target;
    int choice;
public:
    guess() {
        srand((unsigned int)time(NULL));
        choice = (rand() % 10) + 1;
        target = 0;

        do {
            cout << "enter your guess (1-10): ";
            cin >> target;
            if (target > choice)
                cout << "just lower your guess" << endl;
            else if (target < choice)
                cout << "just higher your guess" << endl;
            else
                cout << "hurray ! you won the game !" << endl;

        } while (target != choice);
    }
};
int main() {
    guess g1;
    return 0;
}