# Random Quote Manager

#### Description

Random Quote Manager is a lightweight Python CLI app for storing, organizing, and displaying quotes monthly. Quotes are saved in CSV files (one per month) for easy retrieval. Users can add new quotes or view a random quote for the current month. The program handles empty inputs and missing files gracefully, requiring only Python’s built-in libraries.

## Files

### RandomQouteManager.py

Main script for reading, writing, and displaying quotes:

* Detects current month using `datetime`.
* Handles CSV files with `os` and `csv`.
* Stores/retrieves quotes and selects a random one with `random`.

### CSV Files

Monthly CSV files (e.g., `quotes_01.csv`) store one quote per row. Minimal format allows easy manual editing or backup.

## Functionality

* **Add a Quote (`a`)**: Appends a new quote to the current month’s CSV. Empty inputs are ignored.
* **Retrieve Today’s Quote (`r`)**: Displays a random quote from the current month or a message if none exist.

## Design Choices

* **Monthly files**: Keeps quotes organized and manageable.
* **CLI**: Simple, lightweight, and widely compatible.
* **Fallback handling**: Provides helpful messages when data is missing.

#### How to Use

1. Run the program:
   `python quote_manager.py`
2. Choose an action:

   * `a` to add a quote
   * `r` to view a random quote

---

If you want, I can also make an **ultra-condensed one-paragraph version** that’s perfect for GitHub’s main README view. Do you want me to do that?
