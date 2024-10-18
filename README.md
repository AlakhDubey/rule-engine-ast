Rule Engine with Abstract Syntax Tree (AST)

This project is a simple rule engine designed to evaluate user eligibility based on a set of dynamic rules. The rules are represented using an Abstract Syntax Tree (AST) that allows for conditional checks on attributes like age, department, salary, and experience. The engine supports creating, combining, and evaluating rules against user data.

Features of Project:
- Dynamic rule creation using Abstract Syntax Trees (AST)
- Combine multiple rules efficiently
- Evaluate rules based on user data
- Supports logical operators (AND, OR) and conditions (>, <, =)

  ## Table of Contents
1. [Installation](#installation)
2. [Usage](#usage)
3. [API Endpoints](#api-endpoints)
4. [Project Structure](#project-structure)
5. [Contributing](#contributing)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/username/rule-engine-ast.git
   ```

2. Navigate into the project directory:
   ```bash
   cd rule-engine-ast
   ```

3. Set up a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

4. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

5. Start the application:
   ```bash
   python app.py
   ```

6. If using Docker, run:
   ```bash
   docker-compose up --build
   ```
## Usage

You can interact with the rule engine using the following API endpoints:

- **Create a Rule**: POST `/api/create_rule`
  - **Example**:
    ```bash
    curl -X POST -H "Content-Type: application/json" -d '{"rule": "age > 30"}' http://localhost:5000/api/create_rule
    ```

- **Evaluate a Rule**: POST `/api/evaluate_rule`
  - **Example**:
    ```bash
    curl -X POST -H "Content-Type: application/json" -d '{"rule": "age > 30", "data": {"age": 35}}' http://localhost:5000/api/evaluate_rule
    ```

Sample usage for the `create_rule` function:
```python
from rule_engine import create_rule

rule = create_rule("age > 30 AND salary > 50000")
print(rule)  # Outputs the AST representation of the rule

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

For support or any questions, reach out to `alakhdubey72@gmail.com`.

# Rule Engine with AST

## Description
This project is a rule engine that determines user eligibility based on a set of dynamic conditions. The rules are built using Abstract Syntax Trees (AST), allowing for flexibility in defining and evaluating rules based on user attributes like age, department, salary, and experience.

## Features
- Dynamic rule creation using AST
- Combine and evaluate rules
- Supports logical operators like AND, OR
- Simple API for rule creation and evaluation

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/alakhdubey72/rule-engine-ast.git

rule-engine-ast
├── src
├── tests
├── venv
│   ├── Include
│   ├── Lib
│   └── Scripts
├── README.md
└── .gitignore


