# Password Brute Force (Purpose)
This project was created for the educational purpose of visually demonstrating how long it would take to crack passwords of varying lengths containing characters from the ASCII table. 

## Contribution
I do not see myself updating this project, but it is a very good project for someone who is early in their C# journey to play around with, check out the [issues](https://github.com/bonganibg/password-brute-force/issues) page to see some things that can be added to the project.

## Running
* Enter the password you want to test in the `password` variable in [Program.cs](https://github.com/bonganibg/password-brute-force/blob/main/Program.cs)
* Run the project and you should see all of the combinations that being tested
* The script will run until the password has been cracked

## How it Works
Inside the [Program.cs](https://github.com/bonganibg/password-brute-force/blob/main/Program.cs) file, you will find various methods, these methods are used to incremet the password attempts in the same way a number is incremented. 
* `BruteForce`: Stores the password attempt variable and compares it to the correct password. The method contains a while loop which runs until the password has been cracked and controls when the password attempt should be incremented
* `CheckPassword`: Converts the password attempt list into a string and comapres the password attempt to the correct password, if the passwords match true is returned and the program can be stopped otherwise false is returned and the application will continue running
* `GetUpdateIndex`: The function checks which character needs to be updated in the list and send the index in the list, if none of the characters can be updated -1 will be returned to indicate that a new character needs to be added to the list. The function works as follows: 
    *  Checks if the character in the last index is greater than the last character in the ASCII table list
    * If the character is equal to the last charcter in the ASCII table, the index is decremented
    * If the character is less than the last character in the ASCII table, the index of the character is returned as the character that needs to be updated
    * If all of the characters in the list are equal to the last character in the ASCII table, -1 is returned to indicate that the a new character needs to be added to the list
* `UpdatePasswordAttempt`: Gets the index of the character that needs to be updated in the list and changes it to the value of the next character in the ASCII table
* `AddNewCharacter`: Adds a new character to the password attempt list. All of the characters in the list will be set to the first character in the ASCII table.
* `ASCII`: Resturns a list of the characters in the ASCII table


