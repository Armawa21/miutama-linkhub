# Link Bio — Cara Setup

Isinya 3 file:
- `index.html` — halaman publik (yang dibagikan link-nya, misal di bio Instagram)
- `admin.html` — halaman untuk kamu edit isi (foto, deskripsi, social media, link)
- `data.json` — isi kontennya, otomatis diupdate oleh admin.html

## 1. Buat repo GitHub baru
1. Buka github.com → **New repository**
2. Nama bebas, misal `link-bio`
3. Pilih **Public** (wajib public supaya GitHub Pages gratis bisa jalan)
4. Upload ketiga file di atas ke repo ini (drag & drop lewat "Add file → Upload files" di GitHub, lalu Commit)

## 2. Aktifkan GitHub Pages
1. Di repo → **Settings → Pages**
2. Source: **Deploy from a branch**
3. Branch: **main**, folder: **/ (root)**
4. Save. Tunggu ~1 menit, nanti muncul link publik seperti:
   `https://username.github.io/link-bio/`

## 3. Buat Personal Access Token (supaya admin.html bisa nyimpen perubahan)
1. GitHub → foto profil kanan atas → **Settings → Developer settings → Personal access tokens → Fine-grained tokens**
2. **Generate new token**
3. **Repository access**: pilih **Only select repositories** → pilih repo `link-bio` ini saja
4. **Permissions → Repository permissions → Contents**: pilih **Read and write**
5. Generate, lalu **copy token-nya** (cuma muncul sekali, simpan baik-baik, jangan dibagikan ke siapa pun)

## 4. Cara edit konten sehari-hari
1. Buka `https://username.github.io/link-bio/admin.html`
2. Isi Username GitHub, Nama Repo, Branch (`main`), dan Token
3. Klik **"Muat data saat ini dari GitHub"** untuk narik isi yang sudah ada
4. Ubah nama, deskripsi, upload foto, tambah/hapus/urutkan social media & link
5. Klik **"Simpan ke GitHub"**
6. Tunggu ±30–60 detik, refresh halaman publiknya (`index.html`) untuk lihat hasilnya

Centang "Ingat data ini di browser ini" kalau admin.html cuma dibuka dari HP/laptop pribadimu — biar nggak perlu isi ulang token tiap kali. Jangan centang kalau bukan perangkat pribadi.

## Catatan keamanan
- `admin.html` memang bisa dibuka siapa saja yang tahu link-nya, tapi tanpa token mereka nggak bisa nyimpen perubahan apa pun — jadi jangan sebar token-nya.
- Kalau token bocor/hilang, tinggal revoke di GitHub (Settings → Developer settings → token → Delete) dan buat yang baru.

## Kalau mau ganti tampilan nanti
Semua warna, font, dan style ada di bagian `<style>` di `index.html` — tinggal minta saya ubah kalau mau ganti nuansa warna atau layout-nya.
