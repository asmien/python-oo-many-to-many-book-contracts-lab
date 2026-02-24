# Many-to-Many Relationships – Book Contracts Lab
## Overview
This project implements a many-to-many relationship between Author and Book using a Contract intermediary class.
An author can have multiple books through contracts.
A book can have multiple authors through contracts.

This lab demonstrates relational modeling in Python using object-oriented principles.

## Concepts Demonstrated
Many-to-many relationships
Class attributes
Object validation
Intermediary relationship classes
Data filtering using list comprehensions
Aggregation methods
Test-driven development with pytest

## Project Structure
```
book-contracts/
│
├── many_to_many.py
├── test_many_to_many.py
├── conftest.py
└── README.md
```


## Class Design
### Author
Attributes
name
all (class attribute storing all authors)
Methods
contracts() → returns list of contracts
books() → returns related books
sign_contract(book, date, royalties) → creates new contract
total_royalties() → returns sum of royalties

### Book
Attributes
title
all (class attribute storing all books)
Methods
contracts() → returns list of contracts
authors() → returns related authors

### Contract
Attributes
author (must be Author instance)
book (must be Book instance)
date (string)
royalties (integer)
all (class attribute storing all contracts)
Validation
All properties validate type and raise exceptions if invalid.
Class Method
contracts_by_date(date) → returns all contracts matching date

## Running Tests
Install pytest:
```
python -m pip install pytest
```

Run tests:
```
pytest
```

All tests should pass successfully.

## Features Implemented
✔ Many-to-many relationship modeling
✔ Author ↔ Book linking through Contract
✔ Royalty tracking
✔ Contract filtering by date
✔ Input validation
✔ Fully tested with pytest

## Requirements
Python 3.12+
pytest
Check version:
python --version


