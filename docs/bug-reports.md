# Bug Reports — JSONPlaceholder API

---

## BUG-001

| Field           | Detail                                                          |
| --------------- | --------------------------------------------------------------- |
| **ID**          | BUG-001                                                         |
| **Title**       | DELETE request mengembalikan body kosong tanpa pesan konfirmasi |
| **Reporter**    | Rotua Immanuela Tampubolon                                      |
| **Date**        | May 2026                                                        |
| **Environment** | Postman, Windows 11                                             |
| **Severity**    | Low                                                             |
| **Priority**    | Medium                                                          |
| **Status**      | Open                                                            |

**Steps to Reproduce:**

1. Send DELETE request ke `/users/2`
2. Perhatikan response body

**Expected Result:**
Response berisi pesan konfirmasi seperti `{"message": "User deleted"}`

**Actual Result:**
Response body kosong `{}`

---

## BUG-002

| Field           | Detail                                       |
| --------------- | -------------------------------------------- |
| **ID**          | BUG-002                                      |
| **Title**       | POST /users tidak validasi field yang kosong |
| **Reporter**    | Rotua Immanuela Tampubolon                   |
| **Date**        | May 2026                                     |
| **Environment** | Postman, Windows 11                          |
| **Severity**    | Medium                                       |
| **Priority**    | High                                         |
| **Status**      | Open                                         |

**Steps to Reproduce:**

1. Send POST request ke `/users`
2. Kirim body kosong `{}`
3. Perhatikan response

**Expected Result:**
Response 400 Bad Request dengan pesan validasi error

**Actual Result:**
Response 201 Created meski body kosong — tidak ada validasi

---

## BUG-003

| Field           | Detail                                                        |
| --------------- | ------------------------------------------------------------- |
| **ID**          | BUG-003                                                       |
| **Title**       | GET /users/9999 mengembalikan body kosong bukan error message |
| **Reporter**    | Rotua Immanuela Tampubolon                                    |
| **Date**        | May 2026                                                      |
| **Environment** | Postman, Windows 11                                           |
| **Severity**    | Medium                                                        |
| **Priority**    | Medium                                                        |
| **Status**      | Open                                                          |

**Steps to Reproduce:**

1. Send GET request ke `/users/9999`
2. Perhatikan response body

**Expected Result:**
Response 404 dengan pesan `{"message": "User not found"}`

**Actual Result:**
Response 404 tapi body kosong `{}`
