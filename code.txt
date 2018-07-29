#include<iostream>
#include<string>
using namespace std;
int check_winner(int, string);
int main(){
	int n = 0;
	cin >> n;
	string game;
	cin.ignore();
	getline(cin, game);
	
	for (int i = 0; i < n; i++)
	{
		if (game[i] == 'A' || game[i] =='D')
			break;
		else
		exit(EXIT_FAILURE);
	}
		
		if (check_winner(n, game) == 1)
			cout << "Anton\n";
		else if (check_winner(n, game) == 0)
			cout << "Danik\n";
		else
			cout << "Friendship\n";

	
	
	
return 0;
}
int check_winner(int n, string game)
{
	int count = 0;

	
	if (game.length() == n)
	{


		{
			for (int i = 0; i < n; i++)
			if (game[i] == 'A')
				count++;
		}


	}
	else
		exit(EXIT_FAILURE);
	
		if (count > 0.5*n)
			return 1; //Alian win
		else if (count < 0.5*n)
			return 0; //danial
		else
			return 2; //draw
	}