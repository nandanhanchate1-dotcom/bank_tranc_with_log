# 🏦 Bank Account System with Logging and SMS Notifications

This Python-based banking system simulates deposit and withdrawal operations on a user's bank account, with full transaction **logging** and **SMS notifications** using Twilio.

---

## ✨ Key Features

### ✅ Custom Exception Handling
- Defines a custom exception `InvalidAccountError` for invalid operations such as:
  - Insufficient funds during withdrawal
  - Negative or zero amount deposit attempts

### ✅ Twilio SMS Notifications
- Sends SMS to the user's registered mobile number for:
  - Successful deposits
  - Successful withdrawals
  - Failed operations (like insufficient balance)
- SMS failures are logged with error-level logs

### ✅ Integrated Logging System (Main Feature)
The application uses Python’s built-in `logging` module to track and persist all important events.

| Event                                         | Log Level | Message Format Example                                         |
| --------------------------------------------- | --------- | -------------------------------------------------------------- |
| Account creation                              | INFO      | `Account created: 123456, Initial balance: ₹1000`              |
| Successful withdrawal                         | INFO      | `Withdrawal of ₹500.00 successful. Available balance: ₹500.00` |
| Successful deposit                            | INFO      | `Deposit of ₹200.00 successful. Available balance: ₹700.00`    |
| Failed SMS send                               | ERROR     | `Failed to send SMS to +91xxxxxxxxxx: <error>`                 |
| Withdrawal failure (e.g., insufficient funds) | WARNING   | `Withdrawal failed: Insufficient funds for withdrawal`         |
| Deposit failure (e.g., negative amount)       | WARNING   | `Deposit failed: Deposit amount must be positive`              |
| Unexpected errors                             | CRITICAL  | `Unexpected error: <exception>`                                |

