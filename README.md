
## Setup

### Prerequisites
- Python 3.x
- Virtual environment tool (optional but recommended)

### Installation

1. **Clone the repository**:
    ```sh
    git clone <repository-url>
    cd flask_sqlalchemy_project
    ```

2. **Create a virtual environment** (optional but recommended):
    ```sh
    python -m venv venv
    ```

3. **Activate the virtual environment**:
    - On Windows:
      ```sh
      venv\Scripts\activate
      ```
    - On macOS/Linux:
      ```sh
      source venv/bin/activate
      ```

4. **Install dependencies**:
    ```sh
    pip install -r requirements.txt
    ```

5. **Initialize the database**:
    ```sh
    python
    >>> from run import app
    >>> from app.extensions import db
    >>> with app.app_context():
    ...     db.create_all()
    ...     exit()
    ```

### Running the Application

1. **Run the application**:
    ```sh
    python run.py
    ```

2. **Access the application**:
    Open your web browser and go to `http://127.0.0.1:5000`.

## API Endpoints

- **GET /api/users/**: Retrieve all users.
- **GET /api/users/<user_id>**: Retrieve a specific user by ID.
- **POST /api/users/**: Create a new user.
- **PUT /api/users/<user_id>**: Update an existing user by ID.

## Running Tests

1. **Install `pytest`** (if not already installed):
    ```sh
    pip install pytest
    ```

2. **Run the tests**:
    ```sh
    pytest
    ```

## Project Structure Details

- **app/**: Contains the main application code.
  - **__init__.py**: Initializes the Flask app and extensions.
  - **config.py**: Contains configuration settings.
  - **extensions.py**: Initializes and configures extensions like SQLAlchemy.
  - **models/**: Contains SQLAlchemy models.
  - **routes/**: Contains route definitions.
  - **services/**: Contains business logic and service classes.
  - **utils/**: Contains utility functions and helpers.

- **tests/**: Contains test cases.
  - **__init__.py**: Makes the directory a package.
  - **test_users.py**: Contains unit tests for user routes.

- **migrations/**: Contains database migration files (if using Flask-Migrate).

- **run.py**: Entry point to run the application.
- **requirements.txt**: Lists project dependencies.
- **README.md**: Project documentation.

## Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes ([`git commit -am 'Add new feature'`](command:_github.copilot.openSymbolFromReferences?%5B%22%22%2C%5B%7B%22uri%22%3A%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2Fc%3A%2FUsers%2Fdanil%2FDocuments%2FDesarrollo%2FZubale%2FGit%20Repo%2FAsys%2Fflask_template%2Fapp%2Froutes%2Fusers.py%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%2C%22pos%22%3A%7B%22line%22%3A22%2C%22character%22%3A15%7D%7D%5D%2C%22e2f3dece-d808-4407-b7bc-af331c37b22a%22%5D "Go to definition")).
5. Push to the branch (`git push origin feature-branch`).
6. Create a new Pull Request.

## License

This project is licensed under the MIT License.