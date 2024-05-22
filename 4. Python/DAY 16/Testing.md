# Testing in Software Development

Testing is an essential part of software development, ensuring that code works as intended and meets quality standards. Different types of testing target various aspects of the application, from performance to functionality. This guide explains various types of testing, the testing pyramid, Test-Driven Development (TDD), and provides examples using Python's `unittest` framework.

## Types of Testing

1. **Performance Testing**: Evaluates the speed, responsiveness, and stability of a system under a workload.
2. **Load Testing**: Assesses how the system handles a high volume of data.
3. **Stress Testing**: Determines the system's robustness by testing its limits with a high number of users.
4. **Resilience Testing**: Checks how well the system recovers from failures.
5. **Regression Testing**: Ensures that recent code changes have not reintroduced old bugs.

## Testing Pyramid

- **E2E Testing (End-to-End)**: Conducted by QA, it tests the entire application flow. Tools like Selenium are commonly used.
- **Integration Testing**: Verifies the interactions between different modules or services.
- **Unit Testing**: Performed by developers to test individual units of code, such as functions or methods.

## Test-Driven Development (TDD)

TDD is a modern approach to development where tests are written before the production code. The cycle involves:
1. Writing a failing test.
2. Developing production code to pass the test.
3. Refactoring the code to improve its quality.

## Using `unittest` in Python

Python's `unittest` module provides a framework for creating and running tests.

### Example: Simple Unit Tests

```python
import unittest

def add(a, b):
    return a + b

class TestMyModule(unittest.TestCase):
    def test_add(self):
        self.assertEqual(add(1, 1), 2)
    def test_negative_1(self):
        self.assertEqual(add(-1, 1), 0)
    def test_negative_2(self):
        self.assertEqual(add(-1, -1), -2)
    def test_add_decimal(self):
        self.assertEqual(add(1, 1.1), 2.1)
```

### Explanation:
- **TestMyModule**: A test case class derived from `unittest.TestCase`.
- **test_add, test_negative_1, test_negative_2, test_add_decimal**: Test methods that check the `add` function for various inputs.

### Setup and Teardown Methods

`setUp` and `tearDown` methods allow you to prepare and clean up the test environment.

```python
def adds_interest(accounts, rate):
    for account in accounts:
        if account['isActive']:
            account['balance'] += account['balance'] * rate
    return accounts

class TestInterestModule(unittest.TestCase):
    def setUp(self):
        print("Setup Ran...")
        self.accounts = [
            {"id": 1, "name": "John Doe", "email": "johndoe@example.com", "isActive": True, "balance": 150.75},
            {"id": 2, "name": "Jane Smith", "email": "janesmith@example.com", "isActive": True, "balance": 500.50},
            {"id": 3, "name": "Emily Jones", "email": "emilyjones@example.com", "isActive": True, "balance": 0.00},
        ]

    def tearDown(self):
        print("TearDown: Clear resources")

    def test_interest_rate_for_active_user(self):
        output = adds_interest(self.accounts, 0.1)
        self.assertEqual(output[0]["balance"], 165.825)
        self.assertEqual(output[1]["balance"], 550.55)
        self.assertEqual(output[2]["balance"], 0.0)

    def test_interest_rate_for_non_active_user(self):
        self.accounts[2]['isActive'] = False
        output = adds_interest(self.accounts, 0.1)
        self.assertEqual(output[2]["balance"], 0.0)

if __name__ == "__main__":
    unittest.main()
```

### Explanation:
- **setUp**: Initializes the test environment before each test method.
- **tearDown**: Cleans up after each test method.
- **test_interest_rate_for_active_user**: Tests that interest is correctly added to active accounts.
- **test_interest_rate_for_non_active_user**: Ensures no interest is added to inactive accounts.

### Summary
- **Performance Testing**: Evaluates system performance under workload.
- **Load Testing**: Assesses handling of large volumes of data.
- **Stress Testing**: Tests system limits with numerous users.
- **Resilience Testing**: Checks recovery from failures.
- **Regression Testing**: Ensures new code changes don't reintroduce bugs.

The testing pyramid emphasizes the importance of different levels of testing, from unit tests to E2E tests. TDD promotes writing tests first, followed by production code, ensuring thorough testing coverage and better code quality. The `unittest` module in Python provides a structured way to create and run tests, making it easier to maintain robust and error-free code.
