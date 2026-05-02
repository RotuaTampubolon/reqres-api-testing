# Test Plan — JSONPlaceholder API Testing

| Field        | Detail                                    |
|--------------|-------------------------------------------|
| Project      | JSONPlaceholder REST API Testing          |
| Tester       | Rotua Immanuela Tampubolon                |
| Date         | May 2026                                  |
| Version      | 1.0                                       |
| Environment  | Windows 11                                |
| Base URL     | https://jsonplaceholder.typicode.com      |

---

## Objective
Memastikan endpoint REST API JSONPlaceholder mengembalikan
response yang sesuai dengan requirement, status code yang benar,
dan struktur data yang valid.

---

## Scope of Testing

### In Scope
- Users endpoint (GET, POST, PUT, DELETE)
- Posts endpoint (GET, POST)
- Authentication simulation
- Negative testing (invalid ID, missing field)

### Out of Scope
- Performance / load testing
- Security testing
- Database validation

---

## Testing Types

| Type             | Approach           |
|------------------|--------------------|
| Functional       | Postman + Newman   |
| Negative Testing | Postman + Newman   |
| Regression       | Newman + CI/CD     |

---

## Entry Criteria
- Base URL dapat diakses
- Postman collection sudah siap
- Environment variable sudah dikonfigurasi

## Exit Criteria
- Semua test case dieksekusi
- Pass rate minimal 90%
- Newman report sudah digenerate

---

## Tools

| Tool           | Purpose                    |
|----------------|----------------------------|
| Postman        | API Testing & Collection   |
| Newman         | CLI Test Runner            |
| GitHub Actions | CI/CD Automation           |
| GitHub         | Version Control            |