# JSONPlaceholder API Testing Portfolio

![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![Newman](https://img.shields.io/badge/Newman-CLI-green?style=for-the-badge)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)
![CI](https://github.com/RotuaTampubolon/reqres-api-testing/actions/workflows/newman-tests.yml/badge.svg)

> REST API Testing Portfolio — Postman + Newman + CI/CD  
> **Tester:** Rotua Immanuela Tampubolon | Information Systems Student

---

## Project Overview

Proyek ini merupakan implementasi API testing lengkap pada
[JSONPlaceholder](https://jsonplaceholder.typicode.com) REST API, mencakup:

- Manual API Testing dengan **Postman**
- Test Scripts dengan **JavaScript (pm.test)**
- Automation via **Newman CLI**
- CI/CD pipeline dengan **GitHub Actions**
- Dokumentasi lengkap: Test Plan, Test Cases, Bug Reports

---

## Tools & Tech Stack

| Tool           | Purpose                  |
| -------------- | ------------------------ |
| Postman        | API Testing & Collection |
| Newman         | CLI Test Runner          |
| GitHub Actions | CI/CD Automation         |
| JavaScript     | Test Scripts             |
| GitHub         | Version Control          |

---

## Testing Scope

| Endpoint         | Method           | Tested |
| ---------------- | ---------------- | ------ |
| /users           | GET, POST        | ✅     |
| /users/:id       | GET, PUT, DELETE | ✅     |
| /posts           | GET, POST        | ✅     |
| /users/:id/posts | GET              | ✅     |
| Negative Cases   | Invalid ID       | ✅     |

---

## Project Structure

```
reqres-api-testing/
├── .github/
│   └── workflows/
│       └── newman-tests.yml
├── docs/
│   ├── test-plan.md
│   ├── test-scenarios.md
│   ├── test-cases.md
│   ├── bug-reports.md
│   ├── test-execution-result.md
│   └── test-summary-report.md
├── postman/
│   ├── collection.json
│   └── environment.json
├── reports/
├── package.json
└── README.md
```

---

## Test Result Summary

| Metric           | Result   |
| ---------------- | -------- |
| Total Test Cases | 10       |
| ✅ Pass          | 10       |
| ❌ Fail          | 0        |
| Pass Rate        | **100%** |
| Bugs Found       | 3        |

---

## Bug Summary

| ID      | Title                                         | Severity  |
| ------- | --------------------------------------------- | --------- |
| BUG-001 | DELETE tidak return pesan konfirmasi          | 🟢 Low    |
| BUG-002 | POST tidak validasi empty body                | 🟡 Medium |
| BUG-003 | GET user tidak ada tidak return error message | 🟡 Medium |

---

## How to Run

```bash
# Clone repo
git clone https://github.com/RotuaTampubolon/reqres-api-testing.git
cd reqres-api-testing

# Install dependencies
npm install

# Run tests (terminal output)
npm test

# Run tests with HTML report
npm run test:report
# Report tersimpan di reports/report.html
```

---

## Documentation

| Doc              | Link                                                           |
| ---------------- | -------------------------------------------------------------- |
| Test Plan        | [docs/test-plan.md](docs/test-plan.md)                         |
| Test Scenarios   | [docs/test-scenarios.md](docs/test-scenarios.md)               |
| Test Cases       | [docs/test-cases.md](docs/test-cases.md)                       |
| Bug Reports      | [docs/bug-reports.md](docs/bug-reports.md)                     |
| Execution Result | [docs/test-execution-result.md](docs/test-execution-result.md) |
| Summary Report   | [docs/test-summary-report.md](docs/test-summary-report.md)     |
