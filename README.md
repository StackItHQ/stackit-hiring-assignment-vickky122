
# StackIt Hiring Assignment

### Welcome to StackIt's hiring assignment! 🚀

**If you didn't get here through github classroom, are you sure you're supposed to be here? 🤨**


We are glad to have you here, but before you read what you're going to beat your head over for the next few hours (maybe days?), let's get a few things straight:
- We really appreciate honesty. Don't copy anyone else's assignment, it'll only sabotage your chances :P
- You're free to use any stack, and library of your choice. Use whatever you can get your hands on, on the internet!
- We love out of the box solutions. We prefer to call it *Jugaad* 
- This might be just the first round, but carries the most importance of all. Give your best, and we hope you have a fun time solving this problem.

## ✨ **Problem Statement: Crafting a CSV Importer for Google Sheets** ✨

**Context**:
Data analysts around the world 🌍, handle massive amounts of data to derive meaningful insights for their organization 📊. Among the tools they use, Google Sheets 📈 stands out due to its ease of use, accessibility, and collaborative features. However, many analysts have identified a recurring pain point: the cumbersome process of importing CSV files into Google Sheets repeatedly.

A typical week of an analyst in an e-commerce company 🛒 involves receiving multiple CSV files 📁 containing sales, inventory, customer feedback, and more. The data from these files needs to be meticulously analyzed and presented in the company’s weekly meetings. However, instead of diving directly into analysis, most analysts need to spend an inordinate amount of time just importing and structuring these CSV files into Google Sheets ⏳. This repetitive, time-consuming task reduces the efficiency of these professionals and delays the extraction of crucial insights 😫.

**Today, you are going to make their lives better.**

**Problem Statement**:
Make a CSV Importer for Google Sheets that lets users drag and drop CSV files onto the Google Sheet. The moment they drop the CSV file, allow them to select which columns to import 🗂️.

You get brownie points 🍪 if you can make it even easier by allowing them to filter the data as well before importing it into Google Sheets 🔍.

**Other pointers**:
- Import to Sheet – After validation and mapping, devise a method to populate the data into a chosen Google Sheet, either appending to existing data or creating a new sheet 📥📋.
- Optimize for Large Files – Large datasets are common in analytics. Your solution should effectively handle large CSV files (~15MB CSV file) without causing performance issues or prolonged waiting times 📈📦.

## Submission ⏰
The timeline for this submission is: **9AM, 30th Sept, 2023 - 12PM, 2nd Oct, 2023**

Some things you might want to take care of:
- Make use of git and commit your steps!
- Use good coding practices.
- Write beautiful and readable code. Well-written code is nothing less than a work of art.
- Use semantic variable naming.
- Your code should be organized well in files and folders which is easy to figure out.
- If there is something happening in your code that is not very intuitive, add some comments.
- Add to this README at the bottom explaining your approach (brownie points 😋)

Make sure you finish the assignment a little earlier than this so you have time to make any final changes.

Once you're done, make sure you **record a video** showing your project working. The video should **NOT** be longer than 120 seconds. While you record the video, tell us about your biggest blocker, and how you overcame it! Don't be shy, talk us through, we'd love that.

We have a checklist at the bottom of this README file, which you should update as your progress with your assignment. It will help us evaluate your project.

- [✅] My code's working just fine! 🥳
- [✅] I have recorded a video showing it working and embedded it in the README ▶️
- [✅] I have tested all the normal working cases 😎
- [✅] I have even solved some edge cases (brownie points) 💪
- [✅] I added my very planned-out approach to the problem at the end of this README 📜

## Got Questions❓
Feel free to check the discussions tab, you might get something of help there. Check out that tab before reaching out to us. Also, did you know, the internet is a great place to explore 😛

## Developer's Section
*Add your video here, and your approach to the problem (optional). Leave some comments for us here if you want, we will be reading this :)*

https://github.com/StackItHQ/stackit-hiring-assignment-vickky122/assets/95705066/ddb23054-6a74-4b23-a765-7014a7c4db7c

Video Link-- https://drive.google.com/file/d/1CpkqQSFEo06z1iLS51Z8vtm3gGof6v90/view?usp=sharing


Approach of the problem_
Problem Statement: Crafting a CSV Importer for Google Sheets
Objective:
To create a CSV importer for Google Sheets that allows users to drag and drop CSV files onto the Google Sheet, select columns to import, and optionally filter data before importing.

High-Level Steps:
Google Apps Script Functions:


onOpen():
Create a menu in the Google Sheet for CSV Import.
Add an option to trigger the CSV Import dialog.

showDialog():
Create and display an HTML dialog for CSV import.
Set the width and height of the dialog.

parseCSV(csvData):
Parse CSV data and return the header row.

getSheetNames():
Get the names of all sheets in the active spreadsheet.
importCSV(csvData, selectedColumns, filter, destinationSheet):

Parse CSV data.
Apply filters if specified.
Determine the destination sheet (create a new one if needed).
For each selected column, create a new column in the destination sheet and import the corresponding data.

HTML File:
Create an HTML file for the CSV import dialog.
Include input elements for file selection, column selection, filter input, and destination sheet selection.
Buttons to trigger loading CSV data and importing.

JavaScript Functions:

updateColumnsList(columns):
Update the columns dropdown with the provided list of columns.

updateSheetList(sheets):
Update the destination sheet dropdown with the provided list of sheets.

loadCSV():
Triggered when the user selects a CSV file.
Read the CSV file using FileReader.
Call parseCSV and getSheetNames functions in Google Apps Script.
Update the UI with columns and sheet names.

importCSV():
Triggered when the user clicks the "Import" button.

Get selected columns, filter, destination sheet, and CSV file.

Read the CSV file using FileReader.

Call the importCSV function in Google Apps Script with the selected parameters.

toggleLoader(show):
Toggle a loading indicator based on the show parameter.

Additional Considerations:

Error Handling:
Add error handling to handle potential issues during file reading, parsing, or importing.
Display meaningful error messages to users.

User Feedback:
Consider adding notifications or alerts to inform users of successful imports or any errors.
Optimization:

Optimize the code to handle large CSV files efficiently.
Test the solution with various file sizes to ensure performance.

Usability:
Ensure the UI is user-friendly and intuitive.
Test the solution with different users to gather feedback on usability.

Code Organization:
Keep the code modular and well-organized.
Use meaningful variable and function names for better readability.

Testing:
Perform thorough testing with various scenarios, including different file formats, column selections, and filter conditions.
By following this approach, we can create a robust and user-friendly CSV importer for Google Sheets that addresses the pain points mentioned in the problem statement.
