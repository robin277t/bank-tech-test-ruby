# Bank Tech Test in Ruby
Coding mini-project designed to demonstrate strong processes at work; Test-Drive-Development, Object-Oriented-Programming, good commits and documentation.

## Overview

### Requirements

- You should be able to interact with your code via a REPL (in this case IRB). You don't need to implement a command line interface that takes input from STDIN.
- Deposits, withdrawal.
- Account statement (date, amount, balance) printing.
- Data can be kept in memory (it doesn't need to be stored to a database or anything).

### Acceptance criteria
**Given** a client makes a deposit of 1000 on 10-01-2023
**And** a deposit of 2000 on 13-01-2023
**And** a withdrawal of 500 on 14-01-2023
**When** she prints her bank statement
**Then** she would see

```
date || credit || debit || balance
14/01/2023 || || 500.00 || 2500.00
13/01/2023 || 2000.00 || || 3000.00
10/01/2023 || 1000.00 || || 1000.00
```

## Installation

## Running the app

## Running the tests

## Notes

## Blueprint of the App

Class: Account:

method: constructor 
    this.accountBalance = 0
    this.transactions = []
    this.transactionsLogs
    this.instructions = "Your new account options and the inputs needed are as follows:"
    "deposit('YYYY/MM/DD', number)
    "withdraw('YYYY/MM/DD', number)"
    "printStatement()"
    console.log(this.instructions)
    
private method: createLogRecord(type, date, amount) 
    private because only an imported transaction should be able to create a log
    triggers with each new transaction that happens, creates a string with date, amount deposited or withdrawn, and accountBalance and pushes into log array of transaction instances

Class: Transactions: 

method: deposit(amount, date)
    checks amount is valid number
    adds amount to accountBalance
    calls logDeposit ("deposit" amount, date)
    return (`deposit of ${amount }successful, new balace is ${this.accountBalance}`)

method: withdraw(amount, date)
    checks amount is valid number
    removes amount from accountBalance 
    calls logWithdraw ("withdraw", amount, date)
    return (`withdrawal of ${amount }successful, new balace is ${this.accountBalance}`)

method: dateCheck (date)
    takes date and returns today's date if date incorrect, or absent


Class: Statement Printer

method: printStatement(account)
    print header, and then each item of log array that's passed to it from the account instance in reverse date order on a newline



### Class 'account' 
- Program run from this file, initializes with usage/welcome instructions
- Tracks balance
- Contains a set of transaction instances and their logs
- Functions; initializer, deposit, withdraw  

2nd class will be 'transaction' - this will either be a deposit or withdraw instance, also tracking the balance and associated data with it including date checking and data type validation
3rd class will be 'printer' - this will be fed the list of transaction instances from the account and return a formatted list

## Test table