# 💳 Simple ATM Banking System (C++)

##  Project Overview
This is a **console-based ATM banking system** built using **C++**.  
It allows users to perform basic banking operations such as checking balance, depositing, and withdrawing money through a simple menu-driven interface.

---

##  Features
✅ Display interactive menu  
✅ Check account balance  
✅ Deposit money  
✅ Withdraw money (with balance check)  
✅ Exit option to safely end the program  

---

##  How It Works
1. The program starts with a **default balance** of `$500`.  
2. The user selects one of the options from the menu:  
   - 1:Check balance  
   - 2: Deposit  
   - 3: Withdraw  
   - 4: Exit  
3. The balance updates automatically after each transaction.  

---

## 💻 Code Example
```cpp
#include <iostream>
using namespace std;

void showmain() {
    cout << "*********** Menu ***********" << endl;
    cout << "1. Check Balance" << endl;
    cout << "2. Deposit" << endl;
    cout << "3. Withdraw" << endl;
    cout << "4. Exit" << endl;
}

int main() {
    int option;
    double balance = 500;

    do {
        showmain();
        cout << "Option: ";
        cin >> option;

        switch(option) {
            case 1:
                cout << "Balance is: $" << balance << endl;
                break;
            case 2:
                double depositAmount;
                cout << "Deposit amount: ";
                cin >> depositAmount;
                balance += depositAmount;
                break;
            case 3:
                double withdrawAmount;
                cout << "Withdraw amount: ";
                cin >> withdrawAmount;
                if (withdrawAmount <= balance)
                    balance -= withdrawAmount;
                else
                    cout << "Insufficient balance!" << endl;
                break;
        }
    } while (option != 4);
}


##  How to Run
1. Copy the code into any C++ IDE (like **Code::Blocks**, **Dev-C++**, or **VS Code**).  
2. Compile and run the program.  
3. Choose options from the menu to interact with the ATM system.


## 🎯 Future Improvements
🔹 Add PIN authentication  
🔹 Save transaction history  
🔹 Use file handling to store data  
🔹 Add multiple user accounts  

## 🧑‍💻 Author
**Mane Tariku**  
📍 Ethiopia  
🚀 Aspiring | Data Analyst |

---

## 🌟 Show Your Support
If you like this project, please **star 🌟** the repository and **follow** for more C++ and data projects!

---

### 🏷️ Short Description
> A simple C++ console-based ATM system to check balance, deposit, and withdraw money. Future upgrades include PIN authentication, file storage, and transaction history.

### 🔖 Suggested Tags
`C++` `ATM System` `Console App` `Banking` `Beginner Project` `Menu Driven Program` `Programming Basics`
