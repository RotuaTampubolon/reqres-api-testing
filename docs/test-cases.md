# Test Cases — JSONPlaceholder API

---

## Users Endpoint

| TC ID  | Title                  | Method | Endpoint        | Expected Status | Expected Result                        | Type     | Priority |
|--------|------------------------|--------|-----------------|-----------------|----------------------------------------|----------|----------|
| TC-001 | Get all users          | GET    | /users          | 200             | Array of users                         | Positive | High     |
| TC-002 | Get single user        | GET    | /users/2        | 200             | User object dengan id=2                | Positive | High     |
| TC-003 | Create new user        | POST   | /users          | 201             | User baru dengan id & createdAt        | Positive | High     |
| TC-004 | Update existing user   | PUT    | /users/2        | 200             | User dengan data terupdate             | Positive | High     |
| TC-005 | Delete user            | DELETE | /users/2        | 200             | Empty response / success               | Positive | Medium   |

---

## Posts Endpoint

| TC ID  | Title                  | Method | Endpoint        | Expected Status | Expected Result                        | Type     | Priority |
|--------|------------------------|--------|-----------------|-----------------|----------------------------------------|----------|----------|
| TC-006 | Get all posts          | GET    | /posts          | 200             | Array of posts                         | Positive | High     |
| TC-007 | Get posts by user      | GET    | /users/1/posts  | 200             | Array of posts milik user 1            | Positive | Medium   |
| TC-008 | Create new post        | POST   | /posts          | 201             | Post baru dengan id & data             | Positive | High     |

---

## Negative Cases

| TC ID  | Title                  | Method | Endpoint        | Expected Status | Expected Result                        | Type     | Priority |
|--------|------------------------|--------|-----------------|-----------------|----------------------------------------|----------|----------|
| TC-009 | Get user tidak ada     | GET    | /users/9999     | 404             | Empty object / not found               | Negative | High     |
| TC-010 | Get post tidak ada     | GET    | /posts/9999     | 404             | Empty object / not found               | Negative | High     |