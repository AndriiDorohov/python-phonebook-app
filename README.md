🐍 ☎ python-phonebook-app

# Extend Phonebook Application

This is an extended version of the Phonebook application, which provides the following
functionality:

- Add new entries
- Search by first name
- Search by last name
- Search by full name
- Search by telephone number
- Search by city or state
- Delete a record for a given telephone number
- Update a record for a given telephone number
- An option to exit the program

Usage: python phonebook.py <phonebook_name>

The first argument to the application should be the name of the phonebook. The application will load
JSON data from the folder with the application if it is present, otherwise, it will raise an error.
After the user exits the program, all data will be saved to the loaded JSON.

Feel free to explore and use this phonebook application to manage your contacts efficiently! 📞

    phonebook_app/
        ├── database/         # Folder for storing the database file
        │   └── database.json
        ├── src/              # Folder for Python modules
        │   ├── __init__.py
        │   ├── file.py        # Module for file handling
        │   ├── helper.py      # Helper functions and utilities
        │   ├── manager.py     # Module for managing records
        │   └── search.py      # Module for searching records
        ├── main.py           # Main file of the program
        └── README.md         # Documentation and explanations about the project
