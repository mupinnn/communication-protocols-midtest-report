# Encoding Analysis

Protobuf adalah sebuah bahasa untuk mendefinisikan kontrak secara ketat, dalam binari,
dan teroptimasi untuk _microservices_. Berkas `inference.proto` berfungsi sebagai kontrak
agnostik yang bisa digunakan oleh berbagai _tools_ dan bahasa.

Bisa dilihat pada berkas tersebut, di bagian paling atas ada definisi daftar _service_ apa
yang berjalan. Lalu di bawahnya kita bisa mendefinisikan bagaimana bentuk dari _request_ dan
_response_ pada _service_ tersebut.
