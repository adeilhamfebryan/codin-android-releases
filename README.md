# CODin by URice — Android

Repositori resmi distribusi APK dan metadata pembaruan CODin by URice. Source aplikasi tidak disimpan di sini.

## Unduh aplikasi

[Unduh APK v1.0.0](https://github.com/adeilhamfebryan/codin-android-releases/releases/download/android-v1.0.0/codin-android-v1.0.0.apk) · [Halaman rilis](https://github.com/adeilhamfebryan/codin-android-releases/releases/latest) · [Checksum SHA-256](https://github.com/adeilhamfebryan/codin-android-releases/releases/download/android-v1.0.0/checksums.txt)

Memerlukan Android 8 atau lebih baru dan koneksi internet. Pilih file `.apk`, bukan arsip “Source code” otomatis dari GitHub. Buka APK yang diunduh dan ikuti konfirmasi pemasangan Android; izinkan pemasangan dari sumber tersebut hanya jika Anda mempercayai unduhan resmi ini.

Untuk pembaruan, pasang di atas versi lama tanpa uninstall. Aplikasi memeriksa metadata pembaruan secara berkala; pemeriksaan manual ada di **Tentang → Periksa pembaruan**. Unduhan dan pemasangan tetap memerlukan persetujuan Anda.

## Versi dan verifikasi

Versi pertama: **1.0.0**, versionCode **2**. APK SHA-256:

```
5394fec95ae771c700c2d65bb92e1145ae7bc6b0ff9958ca3fcfd604de9854ad
```

Sertifikat signing SHA-256:

```
48045f88b1bad42121aaf49ba63b610203890833f5eb411f16e037d7aaca47e4
```

Metadata pembaruan tersedia di `android-update.json`. Repositori ini tidak memuat source privat, kredensial, keystore, atau password signing.

## Kanal developer — native preview

[Unduh APK developer 0.1.0 build 3](https://github.com/adeilhamfebryan/codin-android-releases/releases/download/android-native-dev-v0.1.0-build3/codin-native-dev-v0.1.0-build3.apk) · [Halaman prerelease](https://github.com/adeilhamfebryan/codin-android-releases/releases/tag/android-native-dev-v0.1.0-build3) · [Panduan kanal developer](https://github.com/adeilhamfebryan/codin-android-releases/blob/developer/DEVELOPER.md)

Ini **pratinjau UI native dengan data contoh**, ditandatangani Android Debug dan belum diuji di HP. Login/auth menunggu auth.urice.id; belum ada akun atau transaksi nyata. Package `id.urice.codin.native.debug` dapat dipasang berdampingan dengan aplikasi produksi; preview tidak menggantikan APK produksi dan tidak diumumkan melalui updater produksi.

Branch distribusi `developer` menyimpan [metadata developer](https://raw.githubusercontent.com/adeilhamfebryan/codin-android-releases/developer/android-developer-channel.json). Rilis developer selalu prerelease dan belum memiliki pembaruan otomatis dalam aplikasi. Unduhan stabil dan `android-update.json` di atas tetap untuk produksi.
