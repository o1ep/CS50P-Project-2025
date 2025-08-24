# Random Quote Manager"

import csv
import datetime
import random
import os

 
def get_month_filename(month: int) -> str:
    """
    Return CSV filename for the given month number.
    Example: 1 -> 'quotes_01.csv', 12 -> 'quotes_12.csv'
    """
    return f"quotes_{month:02}.csv"


def read_quotes(month_filename: str) -> list:
    """
    Read all quotes from the CSV file for the month.
    Returns a list of quotes. If file doesn't exist, return empty list.
    """
    if not os.path.exists(month_filename):
        return []

    quotes = []
    with open(month_filename, "r", newline="", encoding="utf-8") as file:
        reader = csv.reader(file)
        for row in reader:
            if row:
                quotes.append(row[0])
    return quotes


def append_quote(month_filename: str, quote: str) -> None:
    """
    Add a new quote to the CSV for the given month.
    Creates the file if it doesn't exist.
    """
    with open(month_filename, "a", newline="", encoding="utf-8") as file:
        writer = csv.writer(file)
        writer.writerow([quote])


def choose_random_quote(quotes: list) -> str:
    """
    Randomly select and return a quote from the list.
    If the list is empty, return a fallback message.
    """
    if not quotes:
        return "No quotes available for this month. Add some first!"
    return random.choice(quotes)


def main():
    today = datetime.date.today()
    month_fn = get_month_filename(today.month)

    print("\n--- Daily Quotes ---")
    action = input("Type 'a' to add a quote, 'r' to receive today's quote: ").strip().lower()

    if action == 'a':
        quote = input("Enter your favorite quote: ").strip()
        if quote:
            append_quote(month_fn, quote)
            print("Quote added")
        else:
            print("Empty quote not added")

    elif action == 'r':
        quotes = read_quotes(month_fn)
        print("\n✨ Today's Quote ✨")
        print(choose_random_quote(quotes))

    else:
        print("Invalid choice. Please enter 'a' or 'r'.")


if __name__ == "__main__":
    main()
