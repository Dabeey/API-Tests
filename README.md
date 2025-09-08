# API Tests Project

A comprehensive API testing suite built with modern JavaScript testing tools to ensure robust and reliable API endpoints.

## 📁 Project Structure

```
API-Tests/
├── .github/
│   └── workflows/          # CI/CD pipeline configurations
├── api-tests/
│   ├── users/             # User-related API test suites
│   ├── products/          # Product-related API test suites  
│   ├── orders/            # Order-related API test suites
│   ├── utils/             # Utilities and helper functions
│   └── config.js          # Test configuration settings
├── docs/                  # Documentation and test reports
├── scripts/               # Utility scripts for test execution
├── .gitignore            # Git ignore rules
├── package.json          # Project dependencies and scripts
└── README.md             # Project documentation
```

## 🚀 Getting Started

Prerequisites

· Node.js (v14 or higher)
· npm or yarn

## Installation

1. Clone the repository:

```bash
git clone https://github.com/Dabeey/API-Tests.git
cd API-Tests
```

## 1. Install dependencies:

```bash
npm install
```

## 🧪 Running Tests

Execute the full test suite:

```bash
npm test
```

Run tests in watch mode (development):

```bash
npm run test:watch
```

Run specific test files:

```bash
npx mocha api-tests/users/*.test.js
```

## 🛠️ Tech Stack

· Mocha: Test framework for running test cases
· Chai: Assertion library for validation
· Supertest: HTTP assertions for API testing
· Axios: HTTP client for API requests

## 📋 Test Categories

· User API Tests: Authentication, registration, profile management
· Product API Tests: CRUD operations, inventory management
· Order API Tests: Order processing, payment validation

## ⚙️ Configuration

Update api-tests/config.js to modify:

· Base API URLs
· Test environment settings
· Authentication tokens
· Timeout configurations

## 🏗️ Writing Tests

Create new test files in the appropriate category directory:

```javascript
const { expect } = require('chai');
const request = require('supertest');
const { baseUrl } = require('../config');

describe('Feature Tests', function() {
  it('should test specific functionality', function(done) {
    request(baseUrl)
      .get('/endpoint')
      .expect(200)
      .end(function(err, res) {
        expect(res.body).to.have.property('data');
        done();
      });
  });
});
```

## 📊 Test Reports

Test results and coverage reports are generated in the docs/ directory after test execution.

🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Add tests for new functionality
4. Ensure all tests pass
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🆘 Support

For support or questions, please open an issue in the GitHub repository or contact the maintainers.
