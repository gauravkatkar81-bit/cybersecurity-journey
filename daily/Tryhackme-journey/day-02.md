# Module 3: Operating System && Module 4: Software Basic
- **Path:** TryHackMe - Pre-Security
- **Date Completed:** 27 October 2026
- **Focus:** OS Introduction, Windows Basic, Linux Commands, Windows Commands, OS Security, Data Representation, Data Encoding, Python Simple Demo, JS Simple Demo, SQL 

---

## 📌 1. Key Concepts Learned
- **OS Introduction:** System Privilege Layer, OS Duties like User Management, Device Manager, File System Management, Process Management, Memory Management.
- **Windows Basics:** MS-DOS (first computer run on this), Windows 1.0 (1985), Windows ME (2000), Windows 11 (2021).
- **Linux Commands:** `pwd`, `ls`, `cd`, `ls -la`, `find`, `cat`, `whoami`, `uname`, `uname -a`.
- **Windows Commands:** `cd`, `dir`, `dir /s`, `dir /a`, `type`, `whoami`, `ipconfig`, `systeminfo`, `hostname`.
- **OS Security:** Passwords Info, Attack System (Kali Linux), `whoami`, `ssh`, `history`, `su`, `cat`.
---
- **Data Representation:** Binary, Hexadecimal, Octal, Decimal, Conversion using color.
- **Data Encoding:** Decoding Techniques, UTF-16, UTF-32, ASCII.
- **Python Simple Demo:** `print()`, while loop, if-else, elif, guessing game demo.
- **JS Simple Demo:** `console.log()`, `parseInt()`, while loop, guessing game demo.
- **SQL:** `SELECT`, `FROM`, `WHERE`, `ORDER BY`.

---

## 🧪 2. Hands-On Lab Walkthroughs & Exercises

### Lab 1: Linux Command Lab
- **Tasks:** Execute and get information about Linux commands and the system.
- **Action:**
  1. Open Linux Lab in TryHackMe and open the Terminal.
  2. Use various commands like `ls`, `cd`, `pwd`, `find` to get info about the system and search for any file using those commands.
  3. Then use `whoami`, `uname`, `uname -a` to get information about the system.
  4. Then exit from the system.
- **Key Takeaway:** Terminal, `ls`, `cd`, `pwd`, `find`, `whoami`, `cat`, `uname`.

### Lab 2: Windows Command Lab
- **Tasks:** Execute and learn about Windows commands to get info about the system.
- **Action:**
  1. Open Windows lab then search `cmd` or press `Ctrl + R` then type `cmd` to open terminal.
  2. Use `cd`, `dir`, `dir /a`, `dir /s` to search and find specific files and learn about them.
  3. Use `whoami`, `ipconfig`, `systeminfo`, `hostname` to get information about the Windows system.
  4. Then shut down the system.
- **Key Takeaway:** `cmd`, `cd`, `dir`, `type`, `whoami`, `ipconfig`, `systeminfo`, `hostname`.

### Lab 3: OS Security
- **Tasks:** Use Attacker system (Kali Linux) to attack, get info about another user, and run commands in that system.
- **Action:**
  1. Open Attacker System (Kali Linux) and check the list of commonly used passwords.
  2. Run `whoami`, `ssh` to get access to a specific IP or victim system.
  3. Crack password and execute some commands on the victim system (`history`, `whoami`, `su`).
  4. Get info about the victim system and execute some commands.
  5. Exit from the victim and attacker systems.
- **Key Takeaway:** Kali Linux, `whoami`, `ssh`, `cat`, `history`, `su`.

---

### Lab 4: Python Simple Demo
- **Tasks:** Execute and check Python code in the system and run the code.
- **Action:**
  1. Open Python in the system.
  2. Execute Python script and do some changes as needed.
  3. Run and get the output of the Python script.
  4. Paste output and exit.
- **Key Takeaway:** Python, while loops, `print()`, if-else, elif.

### Lab 5: JS Simple Demo
- **Tasks:** Execute and check JS code in the system and run the code.
- **Action:**
  1. Open JS in the system.
  2. Execute JS script and do some changes as needed.
  3. Run and get the output of the JS script.
  4. Paste output and exit.
- **Key Takeaway:** JS, while loops, `console.log()`, `parseInt()`.

### Lab 6: SQL
- **Tasks:** Execute and run commands to get info about tables.
- **Action:**
  1. Open SQL in the system.
  2. Execute SQL command to get info about the table.
  3. Run and get the output of the SQL command.
  4. Paste output and exit.
- **Key Takeaway:** SQL, `SELECT`, `FROM`, `WHERE`, `ORDER BY`.

---

## 🛠️ Commands & Tools Summary
| Tool / Concept | Function |
| :--- | :--- |
| **Linux Terminal** | Command line interface for Linux systems (`pwd`, `ls`, `cd`, `find`) |
| **Windows CMD** | Command line interface for Windows systems (`dir`, `ipconfig`, `systeminfo`) |
| **Kali Linux** | Penetration testing OS used for security lab attacks and enumeration |
| **SSH** | Secure Shell protocol used for remote system access |
| **Python / JS** | Scripting languages used for building basic logic, loops, and scripts |
| **SQL** | Database query language used to retrieve data (`SELECT`, `FROM`, `WHERE`) |
