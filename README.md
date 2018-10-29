// Learning Functions Test 1.cpp : This file contains the 'main' function. Program execution begins and ends there.
//Nicholas Buckley 10.28.2018

#include "pch.h"
#include <iostream>
#include <string>

using namespace std;

//function prototype(declaration)
void Instructions(); // function to display instructions
string GetText(string prompt); // function to gather input
int GetNumber(int high = 10, int low = 1); // getting number function
void Tellstory(string name, string weapon, int number, string bodypart, string queen); // telling story function

// main function
int main()
{
	Instructions(); // call instrunction function

	string name = GetText("Please enter a name: "); // return get text to string name
	string weapon = GetText("Please enter a weapon: "); // return get text to string weapon
	int number = GetNumber(); // return get number to int number
	string bodyPart = GetText("Please enter a body part: "); //return get text to string body part
	string queen = GetText("Please enter a second name: "); // return get text to string name

	Tellstory(name, weapon, number, bodyPart, queen); // call tell story function

	system("pause"); // pause system
	return 0;
}

// instruction function
void Instructions()
{
	cout << "\t\tWelcome to Knights Adventure!\n\n";
	cout << "You will be asked to input numbers and words to help complete the adventure.\n";
	cout << "Make sure to look at the options available when asked each question.\n";
	cout << "\n\n";
}

// get text function
string GetText(string prompt)
{
	string text; // create string text
	cout << prompt; // print prompt
	cin >> text; // assign input to text
	return text; // return user input
}

// get number function
int GetNumber(int high, int low) //restrict high and low input
{
	int num; // create in num
	do
	{
		cout << "Please enter a number" << " (" << low << " - " << high << "): "; //tell user high and low
		cin >> num; // assign input
	} while (num > high || num < low); // if not in range of high and low try again

	return num; // return valid number
}

//tell story function
void Tellstory(string name, string weapon, int number, string bodypart, string queen) // using input gathered from user
{
	cout << "\n\n";
	cout << "========================================================================================\n\n";
	cout << "A long time ago on a far away land there was a farmer named ";
	cout << name;
	cout << ".\n";
	cout << name;
	cout << " lived a large kingdom that was ruled by a beloved queen named ";
	cout << queen;
	cout << ".\n";
	cout << "But something horrible had happened and the queen was taken by a dragon!\n";
	cout << name;
	cout << " knew that if they had the right gear they might have a chance at saving the queen.\n";
	cout << "Stopping by the local market ";
	cout << name;
	cout << " started to look for the perfect weapon to defeat the dragon.\n";
	cout << "Thats when they finally saw it .... the perfect ";
	cout << weapon;
	cout << " that would give them the strength to vanquish the dragon.\n";
	cout << name;
	cout << " must have it no matter the cost so they offered the shop keep ";
	cout << number;
	cout << " gold coins and they accepted!\n";
	cout << name;
	cout << " set off on the quest to save the queen at first light.\n";
	cout << "After four days of searching ";
	cout << name;
	cout << " finally found the dragons secret cave.\n";
	cout << "The battle raged on for hours as ";
	cout << name;
	cout << " used the ";
	cout << weapon;
	cout << " the best that they could to save the queen.\n";
	cout << "...\n";
	cout << "...\n";
	cout << "...\n";
	cout << name;
	cout << " finally defeated the dragon but lost their ";
	cout << bodypart;
	cout << " in the process.\n";
	cout << "Returning queen ";
	cout << queen;
	cout << " to the village ";
	cout << name;
	cout << " was a true hero and lived out the rest of their days as queen ";
	cout << queen;
	cout << "'s loyal protector.\n";
	cout << "\n\n";
	cout << "The End\n";
	cout << "========================================================================================\n\n";
}
