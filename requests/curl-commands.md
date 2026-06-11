# cURL commands

Berikut adalah daftar perintah `cURL` dari Case 1 - User/Profile yang saya gunakan:

1. GET - Daftar Profile

```sh
curl --request GET \
  --url http://localhost:8088/api/profiles
```

2. GET - Detail Profile

```sh
curl --request GET \
  --url http://localhost:8088/api/profiles/1
```

3. POST - Create Profile

```sh
curl --request POST \
  --url http://localhost:8088/api/profiles \
  --header 'Content-Type: application/json' \
  --data '{
  "userId": 3,
  "fullName": "Jim Geovedi",
  "program": "Cyber Security",
  "semester": 6,
  "skills": [
    "insomnia",
    "curl",
    "wireshark"
  ],
  "city": "Bandung"
}'
```

```sh
curl --request POST \
  --url http://localhost:8088/api/profiles \
  --header 'Content-Type: application/json' \
  --data '{
  "userId": 4,
  "fullName": "Linus Torvalds",
  "program": "Operating System",
  "semester": 2,
  "skills": [
    "linux",
    "git",
    "open source"
  ],
  "city": "Helsinki"
}'
```

4. PATCH - Update Profile (partial)

```sh
curl --request PATCH \
  --url http://localhost:8088/api/profiles/3 \
  --header 'Content-Type: application/json' \
  --data '{
  "semester": 4
}'
```

5. PUT - Update Profile (must include all)

```sh
curl --request PUT \
  --url http://localhost:8088/api/profiles/3 \
  --header 'Content-Type: application/json' \
  --data '{
  "userId": 3,
  "fullName": "Jim Geovedi",
  "program": "Cyber Security",
  "semester": 2,
  "skills": [
    "insomnia",
    "curl",
    "wireshark"
  ],
  "city": "Jakarta"
}'
```

6. DELETE - Delete a Profile

```sh
curl --request DELETE \
  --url http://localhost:8088/api/profiles/3
```
