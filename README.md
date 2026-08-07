# Update Server

Repository ini digunakan sebagai server update untuk aplikasi.

## File

```
update.json
```

---

## Struktur JSON

```json
{
  "show": true,
  "id": 1,
  "title": "Update v1.2",
  "message": "• Menambahkan Import JSON\n• Menambahkan Export JSON",
  "button": "Download Sekarang",
  "url": "https://your-download-link.com"
}
```

---

## Penjelasan

| Key | Tipe | Keterangan |
|------|------|------------|
| show | Boolean | Menampilkan atau menyembunyikan popup update |
| id | Integer | ID update. Naikkan setiap ada update baru |
| title | String | Judul update |
| message | String | Isi informasi update |
| button | String | Teks tombol download |
| url | String | Link download aplikasi |

---

## Nilai `show`

### Menampilkan informasi update

```json
{
  "show": true
}
```

Saat bernilai **true**, aplikasi akan menampilkan BottomSheet informasi update.

---

### Menyembunyikan informasi update

```json
{
  "show": false
}
```

Saat bernilai **false**, aplikasi tidak akan menampilkan popup update.

---

## Cara Mengirim Update

1. Edit `update.json`
2. Ubah `show` menjadi `true`
3. Naikkan nilai `id`
4. Isi `title`
5. Isi `message`
6. Isi `url` download
7. Commit perubahan ke GitHub

Contoh:

```json
{
  "show": true,
  "id": 2,
  "title": "Update v1.3",
  "message": "• Perbaikan bug\n• Optimasi performa",
  "button": "Download Sekarang",
  "url": "https://example.com/download"
}
```

---

## Menonaktifkan Update

Setelah pengguna mendapatkan informasi update, ubah kembali menjadi:

```json
{
  "show": false,
  "id": 2,
  "title": "",
  "message": "",
  "button": "",
  "url": ""
}
```

---

## License

MIT License