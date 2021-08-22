# `/cmd`

Aplikasi utama untuk proyek ini.

Nama direktori untuk setiap aplikasi harus sesuai dengan nama executable yang ingin Anda miliki (mis., `/cmd/myapp`).

Jangan menaruh banyak kode di direktori aplikasi. Jika menurut Anda kode tersebut dapat diimpor dan digunakan di proyek lain, kode tersebut harus berada di direktori `/pkg`. Jika kode tidak dapat digunakan kembali atau jika Anda tidak ingin orang lain menggunakannya kembali, letakkan kode tersebut di direktori `/internal`. Anda akan terkejut dengan apa yang akan dilakukan orang lain, jadi ungkapkan niat Anda secara eksplisit!

Biasanya memiliki fungsi `main` kecil yang mengimpor dan memanggil kode dari direktori `/internal` dan `/pkg` dan tidak ada yang lain.
Examples:

* https://github.com/heptio/ark/tree/master/cmd (just a really small `main` function with everything else in packages)
* https://github.com/moby/moby/tree/master/cmd
* https://github.com/prometheus/prometheus/tree/master/cmd
* https://github.com/influxdata/influxdb/tree/master/cmd
* https://github.com/kubernetes/kubernetes/tree/master/cmd
* https://github.com/satellity/satellity/tree/master/cmd/satellity
* https://github.com/dapr/dapr/tree/master/cmd

