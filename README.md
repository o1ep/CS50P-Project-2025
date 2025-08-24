# Random Quote Manager

#### Description
Random Quote Manager is a Python-based command-line application designed to store, organize, and display quotes on a monthly basis.
The project aims to provide users with a simple tool to collect their favorite quotes and receive daily inspiration.
Quotes are organized into CSV files, with each file corresponding to a specific month of the year.
This structure allows users to maintain a chronological record of their quotes and ensures easy retrieval of quotes relevant to the current month.
The application is lightweight and requires only Python’s built-in libraries, making it accessible and easy to run without installing additional packages.
Users can add new quotes, view a random quote for the day, or receive a helpful message if no quotes exist for the current month. The program also gracefully handles empty inputs and missing CSV files, preventing runtime errors.


## Files and Their Purpose
### project.py
This is the main script of the project. It contains all the functionality for reading, writing, and displaying quotes. The script performs the following tasks:

- Determine the current month: Using the `datetime` module, the program identifies the current month to select or create the corresponding CSV file.
- File handling: The `os` module is used to check if a CSV file exists for the current month. If it does not exist, the program creates one when a new quote is added.
- Quote storage and retrieval: The `csv` module is used to save and read quotes from CSV files. Users can append new quotes or read all existing quotes for a month.
- Random selection: The `random` module selects a quote from the list of stored quotes, ensuring that users receive a different experience each day.
### CSV Files
Each CSV file stores the quotes for a specific month. For example, `quotes_01.csv` stores quotes for January, while `quotes_12.csv` stores quotes for December. Each row contains a single quote, allowing for simple storage and retrieval. This design choice was made to keep the file format minimal and human-readable, enabling users to manually edit or backup their quotes if desired.

## Functionality and User Interaction
The program begins by greeting the user and offering two options:
1. Add a Quote (`a`): The user can input their favorite quote, which will be appended to the current month’s CSV file. Empty inputs are ignored to maintain data integrity.
2. Retrieve Today’s Quote (`r`): The program reads all quotes for the current month and selects one at random to display. If no quotes exist, it shows a helpful message encouraging the user to add some.

This simple interface was chosen to maximize usability while keeping the program lightweight and focused on its core functionality.

## Design Choices and Considerations

Several design decisions were made during development:

- Monthly file separation: By storing quotes in monthly CSV files, the program avoids creating an overwhelming single file, keeping data organized and easily maintainable.
- Command-line interface: A CLI was chosen for simplicity and compatibility. While a GUI could enhance user experience, it would add unnecessary complexity for this lightweight project.
- Fallback handling: The program provides clear messages when no quotes exist, preventing errors and guiding the user on the next steps.

These choices strike a balance between functionality, simplicity, and user experience.

#### How to Use
1. Run the program:
    - python quote_manager.py

2. Choose an action:
    - Type a to add a new quote
    - Type r to receive a random quote for today
