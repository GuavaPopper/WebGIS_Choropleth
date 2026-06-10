# WebGIS Choropleth Kecamatan Pontianak

Aplikasi WebGIS sederhana untuk menampilkan peta choropleth jumlah penduduk per kecamatan di Kota Pontianak. Peta dibuat dengan Leaflet, data batas administrasi kecamatan dalam format GeoJSON, serta konversi koordinat dari EPSG:32749 ke EPSG:4326 menggunakan Proj4.

## Fitur

- Peta dasar citra satelit dari Esri.
- Layer batas kecamatan Kota Pontianak.
- Pewarnaan choropleth berdasarkan jumlah penduduk.
- Popup dan panel info saat area kecamatan diarahkan cursor.
- Zoom otomatis ke batas kecamatan saat area diklik.
- Legenda rentang jumlah penduduk.

## Struktur File

```text
.
|-- Admin_Kecamatan.json
|-- index.html
`-- README.md
```

## Teknologi

- HTML, CSS, dan JavaScript
- Leaflet
- Proj4js
- Turf.js
- GeoJSON

## Cara Menjalankan

Jalankan project melalui web server lokal agar pemanggilan file GeoJSON dapat berjalan normal.

Jika menggunakan Laragon, letakkan folder project di direktori `www`, lalu buka:

```text
http://localhost/GIS_Brutal/
```

Atau gunakan server lokal lain dari direktori project:

```bash
python -m http.server 8000
```

Kemudian buka:

```text
http://localhost:8000/
```

## Data

File `Admin_Kecamatan.json` berisi batas administrasi kecamatan Kota Pontianak. Data jumlah penduduk didefinisikan langsung di `index.html` pada objek `populationData`.

## Catatan

Aplikasi membutuhkan koneksi internet untuk memuat library CDN dan tile peta Esri.
