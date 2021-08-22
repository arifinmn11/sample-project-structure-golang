# `/build`

Pengemasan dan Integrasi Berkelanjutan.

Letakkan konfigurasi paket dan skrip cloud (AMI), container (Docker), OS (deb, rpm, pkg) Anda di direktori `/build/package`.

Letakkan konfigurasi dan skrip CI (travis, circle, drone) Anda di direktori `/build/ci`. Perhatikan bahwa beberapa alat CI (mis., Travis CI) sangat pilih-pilih tentang lokasi file konfigurasi mereka. Coba letakkan file konfigurasi di direktori `/build/ci` yang menghubungkannya ke lokasi di mana alat CI mengharapkannya bila memungkinkan (jangan khawatir jika tidak dan jika menyimpan file-file itu di direktori root lebih mudah.
Examples:

* https://github.com/cockroachdb/cockroach/tree/master/build
