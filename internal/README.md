# `/internal`

Aplikasi pribadi dan kode perpustakaan. Ini adalah kode yang Anda tidak ingin orang lain mengimpor di aplikasi atau pustaka mereka. Perhatikan bahwa pola tata letak ini diterapkan oleh kompiler Go itu sendiri. Lihat [`catatan rilis`] Go 1.4(https://golang.org/doc/go1.4#internalpackages) untuk detail selengkapnya. Perhatikan bahwa Anda tidak terbatas pada direktori `internal` tingkat atas. Anda dapat memiliki lebih dari satu direktori `internal` di level mana pun dari pohon proyek Anda.

Anda dapat secara opsional menambahkan sedikit struktur ekstra ke paket internal Anda untuk memisahkan kode internal bersama dan tidak bersama Anda. Itu tidak diperlukan (terutama untuk proyek yang lebih kecil), tetapi bagus untuk memiliki petunjuk visual yang menunjukkan penggunaan paket yang dimaksudkan. Kode aplikasi Anda yang sebenarnya dapat masuk ke direktori `/internal/app` (mis., `/internal/app/myapp`) dan kode yang dibagikan oleh aplikasi tersebut di direktori `/internal/pkg` (mis., `/internal/ pkg/myprivlib`).

Examples:

* https://github.com/hashicorp/terraform/tree/master/internal
* https://github.com/influxdata/influxdb/tree/master/internal
* https://github.com/perkeep/perkeep/tree/master/internal
* https://github.com/jaegertracing/jaeger/tree/master/internal
* https://github.com/moby/moby/tree/master/internal
* https://github.com/satellity/satellity/tree/master/internal

## `/internal/pkg`

Examples:

* https://github.com/hashicorp/waypoint/tree/main/internal/pkg
