# Connection-with-SQLite
Connect to an SQLite database and perform basic operations.
import sqlite3

# Connect to or create an SQLite database
conn = sqlite3.connect('my_database.db')
cursor = conn.cursor()

# Execute SQL queries
cursor.execute('CREATE TABLE IF NOT EXISTS users (id INTEGER PRIMARY KEY, name TEXT, age INTEGER)')
cursor.execute('INSERT INTO users (name, age) VALUES (?, ?)', ('John Doe', 25))

# Commit changes and close the connection
conn.commit()
conn.close()
