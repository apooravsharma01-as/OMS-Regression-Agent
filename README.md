# OMS Regression Agent

An API automation framework designed to validate critical Order Management System (OMS) workflows through reusable test modules, structured test data, and maintainable automation practices.

The goal of this project is to build a scalable regression testing framework that helps QA engineers identify functional issues, validate business workflows, and reduce repetitive manual testing.

---

## Project Overview

OMS Regression Agent is being developed to automate API-level regression scenarios for Uniware OMS.

The framework will focus on validating critical business operations, including:

- Sales Order Management
- Inventory Management
- Shipping and Fulfilment
- Invoice Management
- Order Lifecycle Validations
- API Request and Response Validations

The initial implementation focuses on API automation. UI automation may be introduced separately in a future phase.

## Tech Stack

| Technology | Purpose |
|---|---|
| JavaScript | Automation programming language |
| Node.js | JavaScript runtime |
| Playwright | API testing and request handling |
| Axios | HTTP client |
| dotenv | Environment configuration |
| Git | Version control |
| GitHub | Source code management |

## Project Structure

```text
OMS-Regression-Agent/
│
├── src/
│   ├── config/          # Environment and framework configuration
│   ├── clients/         # Reusable API clients
│   ├── modules/         # Reusable business workflow modules
│   └── utils/           # Common helper functions
│
├── tests/
│   ├── order/           # Order-related API test cases
│   ├── inventory/       # Inventory-related API test cases
│   ├── shipping/        # Shipping-related API test cases
│   └── invoice/         # Invoice-related API test cases
│
├── test-data/           # Test data and request payloads
├── reports/             # Generated test reports
├── docs/                # Framework and testing documentation
│
├── .gitignore
├── README.md
├── package.json
└── package-lock.json
```

## Prerequisites

Before setting up the project, ensure the following are installed:

- Node.js (LTS version recommended)
- npm
- Git
- GitHub access to this repository
- VS Code or any preferred code editor

Verify your installation:

```bash
node -v
npm -v
git --version
```

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/apooravsharma01-as/OMS-Regression-Agent.git
```

### 2. Navigate to the Project

```bash
cd OMS-Regression-Agent
```

### 3. Install Dependencies

```bash
npm install
```

### 4. Configure Environment Variables

Create a local environment file:

```bash
cp .env.example .env
```

Add the required environment-specific configuration to `.env` once the framework configuration is defined.

**Important:** Never commit `.env` files, authentication tokens, passwords, or other sensitive credentials to GitHub.

## Running Tests

The framework is currently in its initial setup phase. Test modules and execution scripts will be added as the implementation progresses.

To see the available npm scripts:

```bash
npm run
```

Once the API test execution scripts are configured, the relevant commands will be documented here.

## Adding New Test Cases

Follow these guidelines when contributing new API test scenarios:

1. Identify the relevant OMS business module.
2. Add the test case under the appropriate directory inside `tests/`.
3. Keep reusable API request logic inside `src/clients/`.
4. Keep reusable business operations inside `src/modules/`.
5. Store reusable request payloads and test data inside `test-data/`.
6. Validate HTTP status codes, response bodies, and relevant business rules.
7. Ensure test cases are independent wherever possible.
8. Avoid hardcoding environment-specific URLs or credentials.

## Contribution Guidelines

All contributors should follow the branch-based development workflow.

### 1. Get the Latest Code

```bash
git checkout main
git pull origin main
```

### 2. Create a Feature Branch

Use descriptive branch names:

```bash
git checkout -b feature/order-api-tests
```

Examples:

- `feature/order-api-tests`
- `feature/inventory-validation`
- `feature/shipping-api-tests`
- `bugfix/invoice-validation`

### 3. Make Changes and Commit

```bash
git add .
git commit -m "Add order API regression tests"
```

### 4. Push Your Feature Branch

```bash
git push -u origin feature/order-api-tests
```

### 5. Create a Pull Request

- Open the repository on GitHub.
- Create a Pull Request from your feature branch into `main`.
- Provide a clear description of the changes.
- Request a review from another team member.
- Merge only after the required review and validation.

**Important:** Do not push directly to `main`. All project changes should go through Pull Requests.

## Coding Guidelines

- Use JavaScript consistently across the framework.
- Prefer `async/await` for asynchronous operations.
- Write reusable functions instead of duplicating API logic.
- Keep test cases readable and maintainable.
- Use meaningful variable and function names.
- Keep test data separate from test implementation.
- Validate both API-level responses and OMS business behaviour.
- Never commit credentials or sensitive environment data.

## Reporting

Test reporting will be integrated as the framework develops.

The `reports/` directory is reserved for generated reports and execution artifacts. Generated reports should not be committed unless explicitly required.

## Future Enhancements

Planned improvements include:

- Reusable authentication and API request handling.
- End-to-end OMS API regression coverage.
- Data-driven test execution.
- Centralized environment configuration.
- Improved test reporting and failure analysis.
- CI/CD integration.
- Automated regression execution.

## Support and Collaboration

For questions, suggestions, or issues related to the framework, raise the concern with the QA team or create an issue in the GitHub repository.

---

**OMS Regression Agent**  
*Building reliable and maintainable OMS regression automation.*
