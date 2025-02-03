# Bookshelf API

Bookshelf API adalah RESTful API sederhana untuk mengelola koleksi buku. API ini dikembangkan sebagai bagian dari proyek akhir Back-End Developer di ID Camp Dicoding 2024.

## Fitur Utama
- Menambahkan buku baru.
- Menampilkan daftar buku.
- Menampilkan detail buku berdasarkan ID.
- Memperbarui informasi buku.
- Menghapus buku dari daftar.

## Teknologi yang Digunakan
- **Node.js** (JavaScript runtime)
- **Hapi.js** (Framework backend)
- **nanoid** (Membuat ID unik)
- **Postman** (Pengujian API)

## Instalasi dan Menjalankan Server
### 1. Clone Repository
```bash
 git clone <repository-url>
 cd bookshelf-api
```

### 2. Instal Dependensi
```bash
 npm install
```

### 3. Menjalankan Server
```bash
 npm run start
```

Server akan berjalan pada `http://localhost:9000`.

## API Endpoint
### 1. Menambahkan Buku
- **Method:** `POST`
- **Endpoint:** `/books`
- **Body Request:**
```json
{
    "name": "Buku A",
    "year": 2010,
    "author": "John Doe",
    "summary": "Lorem ipsum dolor sit amet",
    "publisher": "Dicoding Indonesia",
    "pageCount": 100,
    "readPage": 25,
    "reading": false
}
```
- **Response Sukses (201):**
```json
{
    "status": "success",
    "message": "Buku berhasil ditambahkan",
    "data": {
        "bookId": "1L7ZtDUFeGs7VlEt"
    }
}
```

### 2. Mendapatkan Semua Buku
- **Method:** `GET`
- **Endpoint:** `/books`
- **Response Sukses (200):**
```json
{
    "status": "success",
    "data": {
        "books": [
            {
                "id": "Qbax5Oy7L8WKf74l",
                "name": "Buku A",
                "publisher": "Dicoding Indonesia"
            }
        ]
    }
}
```

### 3. Mendapatkan Detail Buku
- **Method:** `GET`
- **Endpoint:** `/books/{bookId}`

### 4. Memperbarui Buku
- **Method:** `PUT`
- **Endpoint:** `/books/{bookId}`

### 5. Menghapus Buku
- **Method:** `DELETE`
- **Endpoint:** `/books/{bookId}`

## Pengujian API dengan Postman
1. **Import File Collection & Environment**:
   - `Bookshelf API Test.postman_collection.json`
   - `Bookshelf API Test.postman_environment.json`
2. **Jalankan Server API** dengan `npm run start`.
3. **Gunakan Postman** untuk menguji setiap endpoint.

## Lisensi
Proyek ini dibuat untuk keperluan edukasi dan mengikuti standar dari ID Camp Dicoding 2024.
