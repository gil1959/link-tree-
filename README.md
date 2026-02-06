# Website Linktree 

## Deskripsi Umum

Website pada file zip yang diberikan merupakan **website linktree** . Halaman ini berfungsi sebagai pusat identitas digital, menampilkan foto profil, nama, deskripsi singkat, serta kumpulan tautan eksternal menuju platform lain seperti GitHub, LinkedIn, Instagram, dan kontak email.

Website dibangun sepenuhnya menggunakan **HTML dan CSS**, tanpa JavaScript, framework, maupun backend. Seluruh interaksi hanya memanfaatkan kemampuan standar browser. Pendekatan ini menunjukkan fokus pada penguasaan dasar pengembangan web dan disiplin pemisahan struktur serta tampilan.

---
---

## Struktur File

File zip berisi beberapa file utama yang saling bergantung.  
`index.html` berperan sebagai kerangka halaman dan pengatur konten.  
`style.css` mengatur seluruh tampilan visual dan layout.  
File gambar `bahlil.jpg` digunakan sebagai foto profil, sedangkan `wp.jpg` digunakan sebagai background halaman.  

---

## Penjelasan HTML (index.html)

HTML pada proyek ini berfungsi sebagai **struktur logis dan semantik** dari website. Tidak ada styling atau logika visual yang ditanamkan langsung di HTML selain penggunaan class dan atribut standar.

Dokumen diawali dengan deklarasi HTML5 dan penentuan bahasa dokumen sebagai Bahasa Indonesia. Hal ini penting untuk konsistensi rendering browser, aksesibilitas, dan SEO. Pada bagian `<head>`, HTML memuat metadata dasar seperti encoding UTF-8 dan pengaturan viewport agar tampilan responsif di perangkat mobile. Judul halaman ditetapkan untuk kebutuhan tab browser dan bookmark.

HTML juga memuat file CSS lokal (`style.css`) sebagai sumber utama styling, serta dua resource eksternal, yaitu Google Fonts untuk tipografi dan Font Awesome untuk ikon. Penggunaan `preconnect` bertujuan meningkatkan performa pemuatan font.

Pada bagian `<body>`, seluruh konten dibungkus dalam satu container utama. Container ini berfungsi sebagai pusat layout dan memudahkan pengaturan posisi melalui CSS. Di dalamnya terdapat bagian profil yang memuat gambar avatar, nama, dan deskripsi singkat. Elemen gambar digunakan untuk menampilkan foto profil dengan atribut `alt` guna mendukung aksesibilitas.

Nama ditampilkan sebagai heading utama untuk menandakan informasi terpenting di halaman, sedangkan deskripsi menggunakan paragraf biasa. Keduanya diberi class agar dapat dikontrol tampilannya melalui CSS.

Bagian berikutnya adalah daftar tautan. Setiap tautan menggunakan elemen `<a>` yang diarahkan ke URL eksternal atau alamat email. Untuk tautan eksternal, atribut `target="_blank"` digunakan agar halaman tujuan terbuka di tab baru. Ikon di dalam tautan ditampilkan menggunakan elemen `<i>` dari Font Awesome, sehingga memperjelas fungsi masing-masing link secara visual.

Di bagian paling bawah terdapat elemen `<footer>` yang menampilkan informasi hak cipta. Elemen ini digunakan secara semantik untuk menandai bagian akhir halaman.

Secara keseluruhan, HTML pada proyek ini hanya bertanggung jawab atas **apa yang ditampilkan**, bukan **bagaimana tampilannya**.

---

## Penjelasan CSS (style.css)

File `style.css` bertanggung jawab penuh terhadap **tampilan visual dan pengalaman pengguna**. CSS digunakan untuk mengatur layout, warna, background, tipografi, dan interaksi visual sederhana seperti hover.

CSS diawali dengan reset dasar menggunakan selector universal. Tujuannya adalah menghilangkan margin dan padding bawaan browser serta menyamakan perilaku perhitungan ukuran elemen melalui `box-sizing`. Pada tahap ini juga ditetapkan font default global berbasis font sistem agar tampilan konsisten sebelum font kustom diterapkan.

Pada selector `body`, CSS mengatur background menggunakan gambar `wp.jpg` yang diposisikan di tengah, tidak diulang, dan diperbesar hingga menutupi seluruh layar. Body juga diatur sebagai flex container agar konten utama dapat dipusatkan secara horizontal dan vertikal. Tinggi minimum body diset setara dengan tinggi viewport sehingga halaman selalu memenuhi satu layar penuh. Warna teks global ditentukan agar kontras dengan background.

Pseudo-element `body::before` digunakan untuk membuat lapisan overlay gelap di atas background. Teknik ini bertujuan meningkatkan keterbacaan teks tanpa harus mengedit gambar latar. Overlay diposisikan tetap dan menutup seluruh layar dengan transparansi tertentu.

Class `.container` mengatur batas lebar konten utama agar tampilan tetap rapi di layar besar. Padding diberikan untuk menjaga jarak konten dari tepi layar, dan teks disejajarkan ke tengah.

Class `.containerimg` mengatur bagian profil menggunakan Flexbox dengan arah kolom. Properti ini memastikan foto, nama, dan deskripsi tersusun vertikal dengan jarak yang konsisten.

Class `.avatar` mengatur ukuran gambar profil, memaksanya berbentuk lingkaran melalui `border-radius`, menjaga proporsi gambar dengan `object-fit`, serta menambahkan border agar foto lebih menonjol dari background.

Class `.font` diterapkan pada teks tertentu untuk menggunakan font `Playpen Sans` dari Google Fonts. Properti tambahan digunakan untuk memastikan font dirender dengan ukuran dan gaya yang sesuai.

Class `.fontbg` memberikan latar belakang khusus pada nama, berfungsi sebagai aksen visual agar teks judul lebih menonjol dibanding elemen lain.

Bagian `.links` diatur sebagai flex container vertikal untuk menumpuk tautan satu per satu. Jarak antar tautan diatur agar setiap link terlihat jelas dan mudah diklik.

Elemen `<a>` di dalam `.links` distyling menyerupai tombol. Warna background, padding, radius sudut, dan ketebalan font digunakan untuk menciptakan tampilan tombol modern. Transisi ditambahkan untuk menghasilkan efek halus saat hover, termasuk perubahan warna dan sedikit pergeseran posisi ke atas.

Selector tambahan pada `.links a` memastikan ikon dan teks di dalam tombol sejajar secara horizontal dan memiliki jarak yang proporsional. Ukuran ikon diatur melalui selector `.links i` agar seimbang dengan teks.

Terakhir, elemen `footer` diberi ukuran teks kecil dan transparansi rendah agar tetap terlihat namun tidak mengalihkan fokus dari konten utama.

---

## Kesimpulan

Website dalam file zip ini merupakan implementasi **Linktree sederhana berbasis HTML dan CSS murni**. Struktur HTML disusun secara rapi dan semantik, sementara CSS digunakan secara efektif untuk menciptakan tampilan yang bersih, terpusat, dan mudah digunakan.

Proyek ini menunjukkan pemahaman yang baik terhadap dasar pengembangan web, terutama dalam hal pemisahan struktur dan tampilan, penggunaan Flexbox, serta integrasi resource eksternal. Website ini layak dijadikan dasar pengembangan portofolio atau dikembangkan lebih lanjut dengan JavaScript dan backend di tahap berikutnya.
