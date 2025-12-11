# Bank Account Encapsulation

A robust Python implementation of a Bank Account class, demonstrating the core principles of Object-Oriented Programming (OOP) with a focus on **Encapsulation**.

## 🚀 About The Project

This project serves as a practical implementation of encapsulation in Python. It models a simple bank account system where sensitive data like account balances are protected from direct access, ensuring date integrity and secure transactions.

### ✨ Key Features

*   **Encapsulation**: Uses private attributes (`__account_number`, `__balance`) to hide internal state.
*   **Secure Transactions**: Validates all deposits and withdrawals to prevent invalid operations (e.g., negative amounts, overdrafts).
*   **Getters**: Provides public methods to safely access private data.
*   **Error Handling**: Raises informative `ValueError` exceptions for invalid inputs.

## 🧠 What I Learned

Through this project, I deepened my understanding of:

*   **Python OOP**: Defining classes, methods, and constructors (`__init__`).
*   **access Modifiers**: Using double underscores (`__`) to make attributes private and inaccessible from outside the class.
*   **Data Protection**: The importance of controlling how data is modified to maintain a valid state.
*   **Test-Driven Development (basic)**: Writing code that satisfies specific test cases.

## 🛠️ Getting Started

### Prerequisites

*   Python 3.x

### Installation

1.  Clone the repository:
    ```sh
    git clone https://github.com/PeterNex14/bank-account-encapsulation.git
    ```
2.  Navigate to the project directory:
    ```sh
    cd bank-account-encapsulation
    ```

## 💻 Usage

You can import the `BankAccount` class into your own scripts:

```python
from main import BankAccount

# Create a new account with account number and initial balance
my_account = BankAccount("123456789", 100.0)

# Deposit funds
my_account.deposit(50.0)
print(f"Balance after deposit: ${my_account.get_balance()}") # Output: 150.0

# Withdraw funds
try:
    my_account.withdraw(20.0)
    print(f"Balance after withdrawal: ${my_account.get_balance()}") # Output: 130.0
except ValueError as e:
    print(f"Error: {e}")

# Attempting to access private attributes directly will fail based on Python's name mangling
# print(my_account.__balance) # AttributeError
```

## 🧪 Running Tests

To verify the implementation, run the provided test suite:

```sh
python main_test.py
```
