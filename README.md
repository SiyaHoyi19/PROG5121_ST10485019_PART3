# PROG5121_ST10485019_PART3
# QuickChat - PROG5121 POE

A Java-based messaging application built for the PROG5121 Programming module at The Independent Institute of Education (IIE).

---

## Project Overview

QuickChat is a console-based chat application that allows users to register, log in and send messages. The application was built across three parts: progressively adding features such as login validation, message sending, JSON storage and array-based message management.

---

## Features

### Part 1 - User Registration and Login
- User registration with validation rules
- Username must contain `_` and be 5 characters or less
- Password must be 8+ characters with a capital letter, number and special character
- Cell phone number must include international code (e.g. +27)
- Login with retry loop
- Unit tests for all validation methods using JUnit 5

### Part 2 - Messaging System
- Welcome message after successful login
- Numeric menu with while loop
- Send multiple messages using a for loop
- Message ID generated as a random 10-digit number
- Message hash generated from ID, message number, first and last word
- Recipient cell number validation
- Message text limited to 250 characters
- Options to Send, Disregard, or Store each message
- Stored messages saved to `messages.json` using org.json library
- Unit tests for all message methods

### Part 3 - Arrays and Stored Messages
- Five arrays to track all session activity:
  - Sent Messages
  - Disregarded Messages
  - Stored Messages (loaded from JSON at startup)
  - Message Hashes
  - Message IDs
- Stored messages loaded from `messages.json` at application startup
- Fourth menu option: Stored Messages with six sub-features:
  - a) Display sender and recipient of all stored messages
  - b) Display the longest stored message
  - c) Search for a message by ID
  - d) Search messages by recipient
  - e) Delete a message using the message hash
  - f) Display a full report of all messages
- Six new unit tests for all Part 3 features

---

## Test Data

The following test data is used in unit tests:

| Message | Recipient | Message Text | Status |
|---------|-----------|--------------|--------|
| 1 | +27834557896 | Did you get the cake? | Sent |
| 2 | +27838884567 | Where are you? You are late! I have asked you to be on time. | Stored |
| 3 | +27834484567 | Yohoooo, I am at your gate. | Disregard |
| 4 | 0838884567 | It is dinner time ! | Sent |
| 5 | +27838884567 | Ok, I am leaving without you. | Stored |

---

## Project Structure

```
QuickChat/
├── src/
│   ├── main/
│   │   └── java/com/mycompany/chatapp/
│   │       ├── Login.java        # Registration and login logic
│   │       ├── MainApp.java      # Main application entry point
│   │       └── Message.java      # Message class with all features
│   └── test/
│       └── java/com/mycompany/chatapp/
│           ├── LoginTest.java    # Unit tests for Login class
│           └── MessageTest.java  # Unit tests for Message class
├── messages.json                 # Stored messages (auto-generated)
├── pom.xml                       # Maven configuration
└── README.md
```

---

## How to Run

### Prerequisites
- Java JDK 11 or higher
- Apache Maven
- NetBeans IDE 28 (or any Java IDE)

### Steps
1. Clone the repository:
   ```
   git clone https://github.com/SiyaHoyi19/PROG5121_ST10485019_PART3/edit/main/README.md
   ```
2. Open the project in NetBeans
3. Right-click the project → **Clean and Build**
4. Right-click `MainApp.java` → **Run File**

### Running Unit Tests
- Right-click the project → **Test**
- Or run in PowerShell:
  ```
  mvn test
  ```

---

## Dependencies

| Library | Version | Purpose |
|---------|---------|---------|
| JUnit Jupiter API | 5.10.0 | Unit testing |
| JUnit Jupiter Engine | 5.10.0 | Running JUnit 5 tests |
| org.json | 20231013 | JSON file storage |

> Attribution: org.json library from https://mvnrepository.com/artifact/org.json/json

---

## How to Use the Application

1. **Register** — Enter a valid username, password and phone number
2. **Login** — Enter your credentials (retries if incorrect)
3. **Main Menu:**
   - Option 1: Send messages
   - Option 2: Coming Soon
   - Option 3: Quit
   - Option 4: Stored Messages menu
4. **Stored Messages Menu:**
   - Choose a, b, c, d, e or f for each feature
   - Type x to go back to the main menu

---

## GitHub Release

### v1.0.0 - Final Submission
- All three parts complete and working
- All unit tests passing
- JSON storage working
- Stored messages loaded from file at startup
- 6+ commits on GitHub

---

### GitHub Link
https://github.com/SiyaHoyi19/PROG5121_ST10485019_PART3/edit/main/README.md

---

###Youtube Link


---

## Author

**Siyahluma Hoyi**  
PROG5121 - Programming  
The Independent Institute of Education (IIE)  
2026
