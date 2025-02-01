
API statis itu gini: endpoint-nya cuma file-file statis. Gak ada proses di server yang ngolah permintaan, datanya langsung disajiin dari file. Kayak ambil data dari lemari arsip, bukan database yang dinamis.

Untungnya Apa Aja?

Hostingnya murah banget: Bisa di-hosting di mana aja yang support static hosting, kayak Github Pages, Netlify, pokoknya yang gratisan dan gampang. Gak perlu repot ngurus server.
Cepet banget: Karena gak pakai server-side processing, responnya kilat. Ambil data langsung dari file, jadi gak pakai lama.

Cara Kerjanya Gimana?

Data wilayah Indonesia (provinsi, kabupaten/kota, kecamatan, kelurahan/desa) disimpan dalam format CSV di folder `data`. Pakai CSV biar gampang diedit dan di-update.

Terus ada skrip (generate.php) yang ngolah file-file CSV itu. Skrip ini otomatis bikin ribuan endpoint (file) di folder `static/api`. Setiap file itu mewakili data wilayah tertentu. Jadi, setelah skrip jalan, API-nya langsung siap pakai. Akses datanya bertahap: provinsi -> kabupaten/kota -> kecamatan -> kelurahan/desa.

Informasi Tambahan:

Dokumen tambahan hanya menunjukkan contoh respons API untuk setiap tingkatan wilayah (Provinsi, Kab/Kota, Kecamatan, Kelurahan).  Dokumen tersebut tidak memberikan informasi kuantitatif seperti jumlah data atau detail teknis lainnya (misalnya, jumlah total provinsi, kabupaten/kota, dll.).  Untuk informasi lebih detail, saya perlu akses ke data CSV atau informasi lain yang relevan.
