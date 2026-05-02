# Test Scenarios — JSONPlaceholder API

---

## Feature: Users

**Scenario 1 — Get all users**
Given API server berjalan normal
When client mengirim GET request ke /users
Then response status 200
And response berisi array of users

**Scenario 2 — Get single user**
Given user dengan ID 2 ada di sistem
When client mengirim GET request ke /users/2
Then response status 200
And response berisi data user dengan id 2

**Scenario 3 — Create user**
Given client memiliki data user yang valid
When client mengirim POST request ke /users
And body berisi name dan job
Then response status 201
And response berisi data user yang baru dibuat

**Scenario 4 — Update user**
Given user dengan ID 2 ada di sistem
When client mengirim PUT request ke /users/2
And body berisi data yang diupdate
Then response status 200
And response berisi data yang sudah diupdate

**Scenario 5 — Delete user**
Given user dengan ID 2 ada di sistem
When client mengirim DELETE request ke /users/2
Then response status 200

---

## Feature: Negative Cases

**Scenario 6 — Get user yang tidak ada**
Given user dengan ID 9999 tidak ada di sistem
When client mengirim GET request ke /users/9999
Then response status 404

**Scenario 7 — Get posts by user**
Given user dengan ID 1 ada di sistem
When client mengirim GET request ke /users/1/posts
Then response status 200
And response berisi array of posts milik user 1
