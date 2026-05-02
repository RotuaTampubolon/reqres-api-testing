# Test Summary Report — JSONPlaceholder API

---

## Project Info

| Field      | Detail                           |
|------------|----------------------------------|
| Project    | JSONPlaceholder REST API Testing |
| Tester     | Rotua Immanuela Tampubolon       |
| Date       | May 2026                         |
| Tool       | Postman + Newman + GitHub Actions|
| Base URL   | jsonplaceholder.typicode.com     |

---

## Execution Summary

| Metric           | Result |
|------------------|--------|
| Total Test Cases | 10     |
| Pass             | 10     |
| Fail             | 0      |
| Skipped          | 0      |
| Pass Rate        | 100%   |

---

## Bug Summary

| ID      | Title                                              | Severity | Status |
|---------|----------------------------------------------------|----------|--------|
| BUG-001 | DELETE tidak return pesan konfirmasi               | Low      | Open   |
| BUG-002 | POST tidak validasi empty body                     | Medium   | Open   |
| BUG-003 | GET user tidak ada tidak return error message      | Medium   | Open   |

---

## Conclusion

Semua 10 test case berhasil dieksekusi dengan pass rate 100%.
Ditemukan 3 bug terkait response body dan validasi input.
API berfungsi sesuai ekspektasi untuk happy path scenarios.

**Recommendation:** Bug BUG-002 perlu diprioritaskan karena
menyangkut validasi input yang penting untuk keamanan data.