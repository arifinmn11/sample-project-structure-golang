# `/test`

Aplikasi pengujian eksternal tambahan dan data pengujian. Jangan ragu untuk menyusun direktori `/test` sesuka Anda. Untuk proyek yang lebih besar, masuk akal untuk memiliki subdirektori data. Misalnya, Anda dapat memiliki `/test/data` atau `/test/testdata` jika Anda memerlukan Go untuk mengabaikan apa yang ada di direktori tersebut. Perhatikan bahwa Go juga akan mengabaikan direktori atau file yang dimulai dengan "." atau "_", sehingga Anda memiliki lebih banyak fleksibilitas dalam hal bagaimana Anda menamai direktori data pengujian Anda.

Examples:

* https://github.com/openshift/origin/tree/master/test (test data is in the `/testdata` subdirectory)


