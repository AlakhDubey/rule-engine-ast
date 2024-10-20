**Rule Engine with Abstract Syntax Tree (AST)**
This project is a simple rule engine designed to evaluate user eligibility based on a set of dynamic rules. The rules are represented using an Abstract Syntax Tree (AST) that allows for conditional checks on attributes like age, department, salary, and experience. The engine supports creating, combining, and evaluating rules against user data.

**Features of the Project:**
Dynamic rule creation using Abstract Syntax Trees (AST)
Combine multiple rules efficiently
Evaluate rules based on user data
Supports logical operators (AND, OR) and conditions (>, <, =)

**Table of Contents**
Installation
Usage
API Endpoints
Project Structure
Testing
Contributing

**Installation**
Clone the repository:

bash
git clone https://github.com/AlakhDubey/rule-engine-ast.git
Navigate into the project directory:

bash
cd rule-engine-ast
Set up a virtual environment (optional but recommended):

bash
python -m venv venv
Activate the virtual environment:

Windows:

bash
venv\Scripts\activate
Mac/Linux:

bash
source venv/bin/activate
Install dependencies:

bash
pip install -r requirements.txt

**Usage
** 
To start the application, you can use the following commands:

Start the Flask API:

bash
export FLASK_APP=src/api/app.py  # For Mac/Linux
set FLASK_APP=src/api/app.py     # For Windows

flask run
The application will be available at http://localhost:5000.

**API Endpoints
**
1. Create a Rule: POST /api/create_rule
This endpoint allows you to create a rule using an AST.

Request Body:

json
{
  "rule": "age > 30"
}
Example Usage:

bash
curl -X POST -H "Content-Type: application/json" -d '{"rule": "age > 30"}' http://localhost:5000/api/create_rule
Response:

json
{
  "message": "Rule created",
  "ast": {
    "type": "operator",
    "value": "age > 30"
  }
}
2. Evaluate a Rule: POST /api/evaluate_rule
This endpoint evaluates a rule against the provided data.

Request Body:

json
{
  "rule": "age > 30",
  "data": {
    "age": 35
  }
}
Example Usage:

bash
curl -X POST -H "Content-Type: application/json" -d '{"rule": "age > 30", "data": {"age": 35}}' http://localhost:5000/api/evaluate_rule
Response:

json
{
  "result": true
}

**Project Structure
** Here's the layout of the project directory:

bash
rule-engine-ast/
├── src
│   ├── ast/
│   │   └── ast.py         # AST logic for rule creation and evaluation
│   ├── api/
│   │   └── app.py         # Flask API for creating and evaluating rules
│   └── database/
│       └── db.py          # Database logic for storing rules
├── tests/
│   ├── test_ast.py        # Unit tests for AST logic
│   └── test_api.py        # Unit tests for API endpoints
├── venv/                  # Virtual environment (not included in Git)
├── README.md              # Project documentation
└── .gitignore             # Git ignore file

Testing
To run the unit tests for both the AST and API logic:

Run all tests using unittest:

bash
python -m unittest discover -s tests
Example Output:

bash
Ran 5 tests in 0.005s

OK

**Contributing
**
Contributions are welcome! To contribute, follow these steps:

Fork the repository.
Create a new branch (git checkout -b feature-branch).
Make your changes and commit them (git commit -m 'Add new feature').
Push to the branch (git push origin feature-branch).
Open a pull request.

**License
**This project is licensed under the MIT License - see the LICENSE file for details.

Contact
For support or any questions, reach out to alakhdubey72@gmail.com.
