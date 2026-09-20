# software-essentials
PRACTICAL DEVELOPMENT SET UP
Hot Reload injects updated source code into the already running Dart Virtual Machine without losing the app's current state. Widget trees are rebuilt with your changes but variables, navigation stack and scroll position stay intact. It is used it for small, fast iterations like tweaking UI layout, colors, text or fixing a minor logic bug when you don't need the app to restart from scratch.
Hot Restart destroys the current app state entirely and restarts the app from main(), reloading the whole Dart code. It's slower than Hot Reload but necessary when changes can't be picked up incrementally for example changes to main(), global variables/state initialization, enums, generic types or if Hot Reload produces odd/inconsistent behavior after a change.
# Database creation
CREATE DATABASE school;
USE school;
CREATE TABLE students (
id INT PRIMARY KEY AUTO_INCREMENT,
name VARCHAR (100),
email VARCHAR (150) UNIQUE,
enrolled_on DATE
);
INSERT INTO students (name, email, enrolled_on)
VALUES 
    ('David Kiptoo', 'david.kiptoo@example.com', '2026-03-12'),
    ('Faith Nekesa', 'faith.nekesa@example.com', '2026-03-15'),
SELECT * FROM students;
# security reflection
It is because ‘root’ has extensive privileges across the database server. If the application's credentials are leaked or the application is compromised, an attacker could potentially modify or delete databases, create users, change permissions, or access unrelated data. 

