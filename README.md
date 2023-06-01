# SERU Testing Back-end Developer

## Vehicle REST API

Pada test ini anda diminta untuk membuat API dengan konsep RESTful. Ada beberapa hal yang perlu diperhatikan sebagai berikut:

1. API dibuat mengikuti kaidah RESTful API yang baik dan benar (GET all, GET by ID, POST, PATCH, DELETE)

Sample API Request:
```js
  GET /users => retrieved all users
  GET /users/:id => retrieved user with spesific ID
  POST /users => create or save data to DB
  PATCH /users/:id => update data to DB
  DELETE /users/:id => delete data to DB
```

2. Implementasi authentication

Sample API Request:
```js
  POST /authentication => sending email & password and get access token back
```

3. Implementasi pagination (metadata: total, limit, skip, etc)

Sample API Response:

```json
{
    "total": 313,
    "limit": 10,
    "skip": 0,
    "data": []
}
```

4. Implementasi filter tiap entity (API) dengan column yang tersedia

Contoh: Kita punya data Vehicle Brand (vehicle_brands) dengan ID = 1. Maka kita bisa melakukan filter dengan kolom `brand_id` seperti di bawah ini.

Endpoint: `/vehicle-types?brand_id=1`

Response:
```json
[
    {
        "name": "SUV",
        "brand_id": 1
    },
    {
        "name": "Sedan",
        "brand_id": 1
    },
    ...
]
```

## Cara Pengerjaan:
1. Buat repo public di Github/Gitlab
2. Bisa menggunakan bahasa pemrograman:
    - Java
    - .NET
    - Node.JS
3. Database bisa menggunakan salah 1 pilihan berikut: PostgresQL, SQL Server, MySQL
4. Docker file untuk deployment (nilai plus)
5. Kirim link source code dan docs (jika ada) ke email: noval@bangsacerdas.com

## Catatan Tambahan:
1. Untuk mengakses API yang sudah dibuat diperlukan token dari hasil login (authentication)
2. Setiap entity diberi f
ield audit (`created_at`, `updated_at`)
3. User Admin bisa mengubah dan menghapus data (authorization)
4. User non admin hanya bisa melihat data (read-only)
5. Tambahkan collection Postman dan push ke source code
6. Buat sekreatif mungkin sesuai case yang diberikan
7. Pengerjaan 3 hari (dihitung 1 hari setelah test ini diterima)
8. Deploy hasil ke server menjadi nilai plus (sehingga bisa langsung share link yang bisa dicek)

## ERD:
Berikut adalah garis besar koneksi anter table, sehingga yang ditampilan disini adalah versi minimal. Silahkan melengkapi kolom-kolom yang relevan sesuai dengan konteks tentang vehicle.


![seru_back_end_erd_test](https://github.com/SERU-APP/back-end-testing/assets/19776836/213d2425-1350-4d01-8abe-2400612ee916)
