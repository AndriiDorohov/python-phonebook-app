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

phonebook_app/ \n ├── database/ # Folder for storing the database file \n │ └── database.json \n ├──
src/ # Folder for Python modules \n │ ├── **init**.py \n │ ├── file.py # Module for file handling \n
│ ├── helper.py # Helper functions and utilities \n │ ├── manager.py # Module for managing records
\n │ └── search.py # Module for searching records \n ├── main.py # Main file of the program \n └──
README.md # Documentation and explanations about the project \n
