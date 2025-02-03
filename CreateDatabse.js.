const { open } = require('sqlite');
const sqlite3 = require('sqlite3');
const path = require('path');

const dbPath = path.join(__dirname, 'userData.db');

const initializeDB = async () => {
  let db;
  try {
    db = await open({
      filename: dbPath,
      driver: sqlite3.Database,
    });

    // Create the user table if it doesn't exist
    await db.run(`
      CREATE TABLE IF NOT EXISTS user (
        id INTEGER PRIMARY KEY AUTOINCREMENT,
        username TEXT NOT NULL,
        name TEXT NOT NULL,
        password TEXT NOT NULL,
        gender TEXT NOT NULL,
        location TEXT NOT NULL
      );
    `);

    console.log('Database initialized successfully');
  } catch (e) {
    console.log(`Database error: ${e.message}`);
  } finally {
    if (db) {
      await db.close();
    }
  }
};

initializeDB();
