# How to Run Node.js Tests

## Quick Start

### From the backend directory:
```bash
cd Proj2/src/backend
npm install  # If you haven't already
npm test
```

### From the Proj2 directory:
```bash
cd Proj2
npx jest --config jest.config.js tests/backend --coverage
```

## What the tests cover

- **test_server.js** - Express server and authentication (10 tests)
- **test_home_routes.js** - Home routes and impact endpoints (10 tests)  
- **test_cart_routes.js** - Cart and order management (17 tests)
- **test_dashboard_routes.js** - Dashboard and restaurant data (14 tests)

**Total: 51 Node.js tests**

## Troubleshooting

### Port 5000 already in use
If you get `EADDRINUSE: address already in use :::5000`, stop any running server:
```bash
# Find and kill process on port 5000
lsof -ti:5000 | xargs kill -9
```

### Module not found errors
Make sure dependencies are installed:
```bash
cd Proj2/src/backend
npm install
```

### Watch mode
To run tests in watch mode (auto-rerun on file changes):
```bash
cd Proj2/src/backend
npm run test:watch
```

## Test Output

The tests will show:
- ✅ Passing tests
- ❌ Failing tests with error details
- Coverage report showing code coverage percentages

