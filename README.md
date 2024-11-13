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
