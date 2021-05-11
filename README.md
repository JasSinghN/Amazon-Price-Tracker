# Amazon-Price-Tracker

Have you ever purchased something on Amazon only to find that the price has dropped the next day? Business Insider has found that Amazon product prices change on average every 10 minutes. This product tracker is an updated and improved version of my previous product tracker application made with python. The objective is to create an app which can track increases and decreases in the price of an amazon product over the desired period. The app will then use the price data accumulated over weeks or months and determine the lowest price that the product has ever dropped to. Once this is determined, the app will scrape the amazon page every time it runs and notifies the consumer (via email) once the price drops to that all-time low value. This way, you can be sure that you are purchasing the product at the lowest possible price. Alternatively, like the previous version, if the consumer does not have weeks or months to spare, the lowest price can be manually added. If added manually, the program will send a notification by email once it finds a similar, or lower price. 

--------------------------Steps--------------------------------

1.	The user is prompted to pick one of two modes. The “0” mode will scrape the website data (price and ratings) and save the data along with date and time in a csv file of choice (will be saved in same directory as program file). 
2.	The program also asks for the max run time and sleep time. The max time will be how long your program will run for continuously, and the sleep time is how often it will  download the html code from Amazon and record the price
3.	The data is saved in an external file, so once the program is closed, it can be re-run, and it will still append data onto the same file (assuming the correct file name is entered)
4.	You can do this as many times as desired, simply run the program whenever your computer is on. If you wanted to, you could run the program everyday for a year.
5.	Once you have accumulated the data in mode ‘”0”, you can run mode “1”. 
6.	In this mode, it will open the previously made csv file and determine the lowest price recorded 
7.	Now the program will download the Amazon page source code and parse the html (according to the sleep time) to determine if the price meets or beats the lowest recorded price
8.	Once such a price is discovered, the application will send an automated email to the account specified in the python source code. 
9.	If desired, the user could skip mode “0” of price tracking, and manually add in a value for the price at which they would like to receive an email.
10.	All data is saved in a csv file, which is formatted nicely to open in any spreadsheet editor. For example: using Microsoft Excel commands, the user can create a scatter plot of the recorded prices or customer ratings and make observations or deduce trends

**Note**, for email notofications to be sent, you must enter a **gmail** adress and password into the top of the python source code

**Final** project file is called **main.py**
