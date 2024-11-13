 # Jelaskan apa yang dimaksud dengan stateless widget dan stateful widget, dan jelaskan perbedaan dari keduanya.
 
 stateless widget seperti namanya tidak memiliki state(keadaan), artinya widget tersebut bersifat statis atau tidak akan berubah apapun yang dilakukan oleh pengguna.
 Stateful widget seperti namanya memiliki state/keadaan, stateful widget artinya widget tersebut dapat berubah tergantung dengan apa yang dilakukan oleh pengguna terhadap widget tersebut.
 perbedaan kedua widget tersebut ada di interaksinya terhadap faktor luar, stateful akan berubah mengikuti faktor luar sedangkan stateless akan tetap sama apapun keadaannya.
 contoh stateless widget adalah text dll, sedangkan statefull adalah seperti checkbox

 # Sebutkan widget apa saja yang kamu gunakan pada proyek ini dan jelaskan fungsinya.
 
 scaffold : basis struktur 
 appbard : mendisplaykan title "Toko Barang Gak Guna"
 padding : menjaga agar content tidak menyentuh edge screen
 Column : menjaga widget agar tertata vertikal
 Row : mendisplay widget infocard secara horizontal
 SizedBox : memberikan vertikal spacing
 Center : mengatur text grid agar berada di tengah kolom
 GridView.count : mengatur text grid layout menjadi sesuatu jumlah kolom (untuk kasus ini tiga) 
 Card : menjadi wadah container berbeda sehingga widget terlihat lebih mencolok
 Container : membungkus layout agar tetap berada dalam card
 Text : mendisplay title dan content dri setiap card
 name : label untuk setiap item
 icon : memberikan icon yang terasosiasi dengan item
 color : memmberikan background color
 Material : memberikan style card agar pojok dari card menjadi bulat
 InkWell : menambahkan fungsionalitas tap, sehingga ketika dipencet akan mengembalikan feedback snackbar
 
 
 
# Apa fungsi dari setState()? Jelaskan variabel apa saja yang dapat terdampak dengan fungsi tersebut.

setState() seperti namanya berfungsi untuk kembali mengset state sesuai dengan apa yang dilakukan pengguna, artinya method tersebut akan memanggil kembali function build dalam code,
hal ini dilakukan untuk melakukan rebuild tampilan terhadap apa yang dilakukan pengguna, dalam penggunaan setState() variable yang terdampak adalah variable dalam function build.
Contohnya jika user melakukan sesuatu, maka variable color berubah dan warna tampilan berubah, saat variable tersebut berubah.
Ketika setState() dipanggil maka variable yang sudah berubah akan mengakibatkan hasil yang berbeda saat method build kembali dipanggil.
Set state sebaiknya dipanggil ketika variable dalam method build ada yang diubah, apabila tidak ada perubahan maka rebuild tidak akan menghasilkan sesuatu yang beda

# Jelaskan perbedaan antara const dengan final.

keduanya sama sama tidak dapat dilakukan reassign karena bersifat cons dan final, namun pembeda utama dari keduanya adalah field dari final object dapat dilakukan reassign,
sedangkan field pada const object tidak dapat dilakukan reassign juga sama seperti const sendiri, namun dalam kasus final, field tersebut tetap bisa direassign bila tidak mengandung const/final

# Jelaskan bagaimana cara kamu mengimplementasikan checklist-checklist di atas.
Saya membuat sifat widget dalam flutter menjadi stateless, karena state belum dibutuhkan untuk tugas kali ini, kemudian saya membuat card - card yang akan ditampilkan pada tugas kali ini,
mengimplementasikan button - button mereka, kemudian diintegrasikan agar dapat ditampilkan di home page, setelah itu saya mengubah warna tombol tombol tersebut menjadi merah,putih dan biru.

# Tugas 8

# Apa kegunaan const di Flutter? Jelaskan apa keuntungan ketika menggunakan const pada kode Flutter. Kapan sebaiknya kita menggunakan const, dan kapan sebaiknya tidak digunakan?

const berguna untuk membuat suatu object menjadi immutable yang artinya atribut apapun dari objek itu tidak dapat diubah setelah dibuat. penggunaan const bermanfaat untuk menghemat memori karena pemanggilannya tidak memerlukan pembuatan object lagi dikarenakan object tersebut bersifat konstan dan tidak berubah, maka object tersebut bisa digunakan terus menerus dalam program tanpa dilakukan rekonstruksi lain. Const sebaiknya digunakan ketika menggunakan widget dengan state stateless karena widget tersebut juga berrsifat immutable dan const sebaiknya tidak digunakan ketika widget yang digunakan bersifat statefull karena penggunaan statefull widget membutuhkan perubahan dinamis dan perlu merubah isi object.

#  Jelaskan dan bandingkan penggunaan Column dan Row pada Flutter. Berikan contoh implementasi dari masing-masing layout widget ini!

Column dan Row adalah widget layout di Flutter yang digunakan untuk menyusun widget lain dalam bentuk vertical dan horizontal.
contoh coulumn
Column(
  mainAxisAlignment: MainAxisAlignment.center,
  children: <Widget>[
    Text("Text 1"),
    Text("Text 2"),
    Text("Text 3"),
  ],
);
contoh row
Row(
  mainAxisAlignment: MainAxisAlignment.spaceAround,
  children: <Widget>[
    Icon(Icons.star),
    Icon(Icons.favorite),
    Icon(Icons.home),
  ],
);

#  Sebutkan apa saja elemen input yang kamu gunakan pada halaman form yang kamu buat pada tugas kali ini. Apakah terdapat elemen input Flutter lain yang tidak kamu gunakan pada tugas ini? Jelaskan!

elemen input yang saya gunakan adalah TextFormField yang berfungsi Untuk menerima input teks dari pengguna.
Selain itu, ada elemen input lain yang tidak digunakan untuk tugas ini seperti :
Radio: Mirip dengan DropdownButton namun biasanya digunakan saat pilihan lebih sedikit.
Slider: Cocok untuk memilih nilai dalam rentang tertentu, misalnya memilih level volume.
Checkbox: Untuk pilihan ya/tidak.
DropdownButtonFormField: Untuk memilih satu dari beberapa pilihan.
Switch: Alternatif untuk Checkbox, biasanya untuk on/off toggle.

#  Bagaimana cara kamu mengatur tema (theme) dalam aplikasi Flutter agar aplikasi yang dibuat konsisten? Apakah kamu mengimplementasikan tema pada aplikasi yang kamu buat?

penyimpanan aturan tema dalam flutter dapat dilakukan dalam materialApp dengan mendefinisikan ThemeData pada flutter yang membuat tema konsisten. dalam tugas ini, saya tidak mengimplimentasikan tema selain yang diberikan oleh tutorial.

#  Bagaimana cara kamu menangani navigasi dalam aplikasi dengan banyak halaman pada Flutter?

Untuk navigasi dalam aplikasi dengan banyak halaman di Flutter, ada beberapa method yang dapat digunakan dalam tugas ini yaitu :
Navigator.push() dan Navigator.pop(): Untuk berpindah dan kembali ke halaman sebelumnya.
Navigator.pushReplacement(): Untuk mengganti halaman saat ini dengan halaman baru.

