# Notes CRUD API

This is a simple REST API to create, read, update, and delete notes (CRUD). 

## 1. Creating the virtual environment
To create a virtual environment, enter the following into the terminal in Visual Studio

```python3 -m venv .venv```

Then activate the environment:

```.venv\Scripts\Activate.ps1```

## 2. Installing the packages

To install the packages:

```python -m pip install -r requirements.txt```

To check the packages installed:

```python -m pip list```

## 3. Running the API

To run the API from the terminal:

```uvicorn main:app --reload```

## 4. Endpoints to test and expected output

| Action | Method | Endpoint | Description | Expected Status |
|---|---|---|---|---|
| Read home | `GET` | `/` | Returns a welcome message | `200 OK` |
| Read all notes | `GET` | `/notes` | Retrieves all notes | `200 OK` |
| Read a note | `GET` | `/notes/{note_id}` | Retrieves note of the given ID | `200 OK` |
| Create a note | `POST` | `/notes` | Creates a new note using the supplied title and text | `201 Created` |
| Update a note | `PATCH` | `/notes/{note_id}` | Updates an existing note with given data, field left blank are left as is | `200 OK` |
| Delete a note | `DELETE` | `/notes/{note_id}` | Deletes an existing note | `204 No Content` |
| Delete a non-existent note | `DELETE` | `/notes/{note_id}` | Error | `404` |

The tests are designed to ensure the notes can be created, read, updated, and deleted correctly. 
