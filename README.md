# Python Phonebook — CLI Learning Project

A small command-line contact book written in Python. It reads contact records from a JSON file, lets users search them interactively, and includes basic create, update, and delete commands.

> **Status:** Legacy learning project under review. Searching existing sample contacts is the recommended demo. Editing commands have known bugs and should **not** be used with important personal data until they are fixed and tested.

## Tech stack

- Python 3.8+ (standard library)
- JSON file storage
- Interactive command-line interface

No third-party runtime dependencies are required.

## Quick start

1. Clone the repository:

   ```bash
   git clone https://github.com/AndriiDorohov/python-phonebook-app.git
   cd python-phonebook-app
   ```

2. Copy the fictional example contacts to a local file:

   ```bash
   cp database/database.json database/local-phonebook.json
   ```

3. Run the app using the filename **relative to the `database/` folder**:

   ```bash
   python3 main.py local-phonebook.json
   ```

4. Enter `print` to list sample contacts or `help` to see all commands. Enter `exit` to quit.

**Important:** The app writes edits directly to the selected JSON file. Always use a disposable copy while experimenting. The sample contacts use fictional identifiers, not actual phone numbers.

## Commands

| Command | Purpose |
| --- | --- |
| `print` | List stored contacts |
| `sf` | Search by first name |
| `sl` | Search by last name |
| `sfl` | Search by first and last name |
| `sp` | Search by phone number / record key |
| `sct` | Search by city |
| `sc` | Search by country |
| `new` | Create a contact (**currently unreliable**) |
| `up` | Update a contact (**currently unreliable**) |
| `del` | Delete a contact |
| `help` | Show the command list |
| `exit` | Save and close the application |

## Data format

Each contact is stored under a unique string key (intended to represent its phone number):

```json
{
  "demo-001": {
    "first_name": "Alex",
    "last_name": "Example",
    "city": "Sampletown",
    "country": "Exampleland"
  }
}
```

The committed `database/database.json` contains only fictional demonstration records. Do **not** commit real contact details or use this project to store sensitive data.

## Project structure

```text
.
├── database/
│   └── database.json   # Fictional sample records
├── src/
│   ├── file.py         # JSON persistence
│   ├── helper.py       # CLI prompts and output
│   ├── manager.py      # Create, update, delete
│   └── search.py       # Contact lookups
├── main.py             # Interactive CLI
└── pyproject.toml
```

## Known limitations / next improvements

- Contact creation currently maps some input fields incorrectly.
- Updating a missing record can return `None`, which risks overwriting the JSON data.
- Full-name search assumes the user enters two names.
- Input validation, error handling, automated tests, and CI need improvement.
- File paths are currently interpreted relative to `database/`, not an arbitrary directory.

Planned sequence: fix data handling and validation → add unit tests → set up GitHub Actions → decide whether to present the project as a finished portfolio piece.

## Purpose

This repository documents an early Python exercise. It is being improved incrementally, with an emphasis on correct behavior, understandable documentation, and verifiable tests.
