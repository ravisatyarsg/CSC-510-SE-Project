# How to Run Tests

This guide explains how to run the test suites for TiffinTrails Proj2.

## Prerequisites

### Python Environment
- Python 3.11 or higher
- pip package manager

### Node.js Environment
- Node.js 18 or higher
- npm package manager

## Running Python Tests

### 1. Navigate to Proj2 directory
```bash
cd Proj2
```

### 2. Install Python dependencies
```bash
pip install -r requirements.txt
```

### 3. Run all Python tests
```bash
pytest tests/ -v
```

### 4. Run specific test file
```bash
pytest tests/test_api_app.py -v
```

### 5. Run tests with coverage report
```bash
pytest tests/ -v --cov=src --cov-report=term-missing
```

### 6. Run tests and generate HTML coverage report
```bash
pytest tests/ -v --cov=src --cov-report=html
# Then open htmlcov/index.html in your browser
```

## Running Node.js Tests

### Backend Tests

1. Navigate to backend directory
```bash
cd Proj2/src/backend
```

2. Install dependencies
```bash
npm install
```

3. Run all backend tests
```bash
npm test
```

4. Run tests with coverage
```bash
npm test -- --coverage
```

### Frontend Tests

1. Navigate to frontend directory
```bash
cd Proj2/src/frontend
```

2. Install dependencies
```bash
npm install
```

3. Run frontend tests
```bash
npm test
```

## Running All Tests

### Quick Test Run (Python only)
```bash
cd Proj2
pytest tests/ -v
```

### Quick Test Run (Node.js backend only)
```bash
cd Proj2/src/backend
npm test
```

### Full Test Suite (from project root)
```bash
# Python tests
cd Proj2
pytest tests/ -v

# Backend tests
cd src/backend
npm test

# Frontend tests
cd ../frontend
npm test
```

## Test Categories

### Run only unit tests
```bash
pytest tests/ -v -m unit
```

### Run only integration tests
```bash
pytest tests/integration/ -v
```

### Run only API tests
```bash
pytest tests/test_api_app.py tests/test_leaderboard_api.py -v
```

## Common Options

### Verbose output
```bash
pytest tests/ -v
```

### Show print statements
```bash
pytest tests/ -v -s
```

### Run specific test function
```bash
pytest tests/test_api_app.py::TestHealthCheck::test_health_check_returns_200 -v
```

### Stop on first failure
```bash
pytest tests/ -v -x
```

### Run tests in parallel (if pytest-xdist installed)
```bash
pytest tests/ -v -n auto
```

## Troubleshooting

### Python tests not found
- Make sure you're in the `Proj2` directory
- Verify `requirements.txt` is installed: `pip list | grep pytest`
- Check Python version: `python --version` (should be 3.11+)

### Node.js tests not found
- Make sure you're in the correct directory (`Proj2/src/backend` or `Proj2/src/frontend`)
- Verify dependencies: `npm list jest`
- Try reinstalling: `rm -rf node_modules && npm install`

### Import errors
- For Python: Make sure you're running from `Proj2` directory
- For Node.js: Check that all dependencies are installed

## CI/CD

Tests automatically run on GitHub Actions when you:
- Push to `main`, `proj2`, or `develop` branches
- Create a pull request

View test results in the "Actions" tab of your GitHub repository.

