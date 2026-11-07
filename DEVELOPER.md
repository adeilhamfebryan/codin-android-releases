# Kanal developer CODin Native

Kanal ini menyediakan APK pratinjau native untuk pengembang/penguji, terpisah dari aplikasi produksi.

- Branch distribusi: `developer`.
- Tag: `android-native-dev-v<versi>-build<versionCode>`; setiap kandidat menggunakan tag/aset baru.
- GitHub Release selalu **prerelease** dan tidak dijadikan Latest.
- Package developer saat ini: `id.urice.codin.native.debug`, dengan Android Debug signer.
- Metadata kanal: [android-developer-channel.json](android-developer-channel.json). Ini deskripsi unduhan manual, bukan updater yang sudah terpasang dalam APK.
- Source tetap di repositori privat. Branch ini hanya berisi instruksi dan metadata distribusi; APK berada di Release Assets.

## Kandidat pertama

Versi APK `0.1.0-native-preview`, versionCode `3`, Android 8/API26 ke atas. UI Kotlin/Jetpack Compose memakai data contoh lokal; login/auth menunggu `auth.urice.id`, tanpa akun atau transaksi nyata. Empat skenario UI baru dikompilasi, belum diuji di HP.

Unduh APK dari rilis berlabel Developer Preview, lalu cocokkan checksum. APK developer dapat dipasang berdampingan dengan CODin produksi. Signer debug berbeda dari produksi; jangan menggunakannya untuk menggantikan aplikasi produksi atau menjanjikan pembaruan otomatis. Untuk pemasangan di atas preview developer sebelumnya, package dan signer harus cocok. Kontinuitas debug key lintas mesin belum dijamin.

## Prosedur kandidat berikutnya

1. Bangun/test/lint native di repositori privat, verifikasi package developer, versi, signer, ukuran dan SHA-256 dari APK sebenarnya. Catat pemeriksaan perangkat yang belum dilakukan.
2. Buat tag unik pada branch distribusi developer dan draft prerelease. Jangan mengganti tag/aset lama.
3. Unggah hanya APK, checksums.txt dan developer-release.json. Jangan unggah source privat, log build, database, foto pengguna, keystore atau kredensial.
4. Cocokkan data aset yang diunggah dengan kandidat lokal, lalu publikasikan sebagai prerelease dengan make_latest=false.
5. Verifikasi unduhan anonim dan hash APK. Perbarui android-developer-channel.json pada branch developer terakhir, hanya setelah unduhan lulus.
6. Rilis produksi tetap memakai android-update.json pada branch main dan sertifikat produksi. Promosi ke produksi memerlukan implementasi serta persetujuan rilis terpisah; metadata developer tidak disalin ke updater produksi.

Rilis developer ini tidak membangun atau mengirim APK otomatis melalui GitHub Actions. Tidak ada private signing key atau token yang disimpan di branch publik.
