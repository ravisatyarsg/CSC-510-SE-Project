# Test Suite Documentation

This directory contains comprehensive test suites for the TiffinTrails Proj2 application.

## Test Structure

### Python Tests (60 tests)
- `test_api_app.py` - Flask API application tests (15 tests)
- `test_leaderboard_api.py` - Leaderboard API tests (10 tests)
- `test_data_loader.py` - Data loading and integration tests (12 tests)
- `test_delivery_metrics.py` - Delivery metrics computation tests (10 tests)
- `test_efficiency_scoring.py` - Efficiency scoring tests (10 tests)
- `test_correlate_efficiency_waste.py` - Correlation analysis tests (13 tests)
- `test_data_generator.py` - Data generation tests (10 tests)
- `test_rescue_meals_integration.py` - Rescue meals integration tests (10 tests)

### Node.js Tests (40 tests)
- `backend/test_server.js` - Express server tests (10 tests)
- `backend/test_home_routes.js` - Home routes tests (10 tests)
- `backend/test_cart_routes.js` - Cart routes tests (20 tests)
- `backend/test_dashboard_routes.js` - Dashboard routes tests (10 tests)

### Integration Tests (20 tests)
- `integration/test_api_integration.py` - API integration tests (10 tests)

## Running Tests

### Python Tests
```bash
cd Proj2
pip install -r requirements.txt
pytest tests/ -v
```

### Node.js Tests
```bash
cd Proj2/src/backend
npm install
npm test
```

### All Tests
The GitHub Actions CI/CD pipeline runs all tests automatically on push and pull requests.

## Test Coverage

Tests cover:
- API endpoints and error handling
- Data processing and validation
- Business logic and calculations
- Integration between components
- Edge cases and error scenarios

## Total Test Count: 120 tests

