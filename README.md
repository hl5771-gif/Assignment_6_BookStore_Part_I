# Homework 1: Bookstore Database + Python CLI

-Eric Li
This project creates a SQLite database for a bookstore
The Python CLI allows the user to browse/search, add, update, and delete books, as well as filter
books by price range.

## Files
- `createTables.sql` - creates the tables
- `insertRows.sql` - inserts sample categories and books
- `bookstore_cli.py` - Python CRUD program
- `bookstore.db` - database file you will create by running the commands below

## Create the database

Run these commands in the terminal:

```bash
python3 - <<'PY'
import sqlite3
sqlite3.connect('bookstore.db').close()
PY
```

Then load the SQL files using SQLite in Python or DB Browser for SQLite.

If your environment has the `sqlite3` shell installed, you can run:

```bash
sqlite3 bookstore.db < createTables.sql
sqlite3 bookstore.db < insertRows.sql
```

## Run the Python CLI

```bash
python3 bookstore_cli.py
```

## Notes

- This example uses parameterized queries in Python.
- The `image` field stores the filename only.
- The actual images can be reused later in the Flask web app.
