# `/pkg`

Kode perpustakaan yang boleh digunakan oleh aplikasi eksternal (mis., `/pkg/mypubliclib`). Proyek lain akan mengimpor perpustakaan ini dan mengharapkannya berfungsi, jadi pikirkan dua kali sebelum Anda meletakkan sesuatu di sini :-) Perhatikan bahwa direktori `internal` adalah cara yang lebih baik untuk memastikan paket pribadi Anda tidak dapat diimpor karena dijalankan oleh Go. Direktori `/pkg` masih merupakan cara yang baik untuk mengkomunikasikan secara eksplisit bahwa kode dalam direktori tersebut aman untuk digunakan oleh orang lain. Postingan blog [`I'll take pkg over internal`](https://travisjeffery.com/b/2019/11/i-ll-take-pkg-over-internal/) oleh Travis Jeffery memberikan gambaran yang baik tentang direktori `pkg` dan `internal` dan kapan masuk akal untuk menggunakannya.

Ini juga merupakan cara untuk mengelompokkan kode Go di satu tempat ketika direktori root Anda berisi banyak komponen dan direktori non-Go sehingga memudahkan untuk menjalankan berbagai alat Go (sebagaimana disebutkan dalam pembicaraan ini: [`Praktik Terbaik untuk Pemrograman Industri`](https ://www.youtube.com/watch?v=PTE4VJIdHPg) dari GopherCon EU 2018, [GopherCon 2018: Kat Zien - Bagaimana Anda Menyusun Aplikasi Go Anda](https://www.youtube.com/watch?v= oL6JBUk6tj0) dan [GoLab 2018 - Massimiliano Pippi - Pola tata letak proyek di Go](https://www.youtube.com/watch?v=3gQa1LWwuzk)).

Perhatikan bahwa ini bukan pola yang diterima secara universal dan untuk setiap repo populer yang menggunakannya, Anda dapat menemukan 10 yang tidak. Terserah Anda untuk memutuskan apakah Anda ingin menggunakan pola ini atau tidak. Terlepas dari apakah itu pola yang baik atau tidak, lebih banyak orang akan tahu apa yang Anda maksud daripada tidak. Mungkin sedikit membingungkan untuk beberapa pengembang Go baru, tetapi ini adalah kebingungan yang cukup sederhana untuk diselesaikan dan itulah salah satu tujuan repo tata letak proyek ini.

Oke untuk tidak menggunakannya jika proyek aplikasi Anda sangat kecil dan di mana tingkat tambahan bersarang tidak menambah banyak nilai (kecuali jika Anda benar-benar menginginkannya). Pikirkan tentang hal itu ketika itu menjadi cukup besar dan direktori root Anda menjadi sangat sibuk (terutama jika Anda memiliki banyak komponen aplikasi non-Go).

Asal direktori `pkg`: Kode sumber Go lama digunakan untuk menggunakan `pkg` untuk paketnya dan kemudian berbagai proyek Go di komunitas mulai menyalin polanya (lihat [`this`](https://twitter.com/bradfitz /status/1039512487538970624) Tweet Brad Fitzpatrick untuk konteks lebih lanjut)

Examples:

* https://github.com/prometheus/prometheus/tree/master/pkg
* https://github.com/jaegertracing/jaeger/tree/master/pkg
* https://github.com/istio/istio/tree/master/pkg
* https://github.com/GoogleContainerTools/kaniko/tree/master/pkg
* https://github.com/google/gvisor/tree/master/pkg
* https://github.com/google/syzkaller/tree/master/pkg
* https://github.com/perkeep/perkeep/tree/master/pkg
* https://github.com/minio/minio/tree/master/pkg
* https://github.com/heptio/ark/tree/master/pkg
* https://github.com/argoproj/argo/tree/master/pkg
* https://github.com/heptio/sonobuoy/tree/master/pkg
* https://github.com/helm/helm/tree/master/pkg
* https://github.com/kubernetes/kubernetes/tree/master/pkg
* https://github.com/kubernetes/kops/tree/master/pkg
* https://github.com/moby/moby/tree/master/pkg
* https://github.com/grafana/grafana/tree/master/pkg
* https://github.com/influxdata/influxdb/tree/master/pkg
* https://github.com/cockroachdb/cockroach/tree/master/pkg
* https://github.com/derekparker/delve/tree/master/pkg
* https://github.com/etcd-io/etcd/tree/master/pkg
* https://github.com/oklog/oklog/tree/master/pkg
* https://github.com/flynn/flynn/tree/master/pkg
* https://github.com/jesseduffield/lazygit/tree/master/pkg
* https://github.com/gopasspw/gopass/tree/master/pkg
* https://github.com/sosedoff/pgweb/tree/master/pkg
* https://github.com/GoogleContainerTools/skaffold/tree/master/pkg
* https://github.com/knative/serving/tree/master/pkg
* https://github.com/grafana/loki/tree/master/pkg
* https://github.com/bloomberg/goldpinger/tree/master/pkg
* https://github.com/Ne0nd0g/merlin/tree/master/pkg
* https://github.com/jenkins-x/jx/tree/master/pkg
* https://github.com/DataDog/datadog-agent/tree/master/pkg
* https://github.com/dapr/dapr/tree/master/pkg
* https://github.com/cortexproject/cortex/tree/master/pkg
* https://github.com/dexidp/dex/tree/master/pkg
* https://github.com/pusher/oauth2_proxy/tree/master/pkg
* https://github.com/pdfcpu/pdfcpu/tree/master/pkg
* https://github.com/weaveworks/kured/tree/master/pkg
* https://github.com/weaveworks/footloose/tree/master/pkg
* https://github.com/weaveworks/ignite/tree/master/pkg
* https://github.com/tmrts/boilr/tree/master/pkg
* https://github.com/kata-containers/runtime/tree/master/pkg
* https://github.com/okteto/okteto/tree/master/pkg
* https://github.com/solo-io/squash/tree/master/pkg
