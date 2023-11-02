# Greeting-Card
Membuat aplikasi Android pertama Anda

Tentang codelab ini
subjectTerakhir diperbarui Okt 14, 2022
account_circleDitulis oleh Tim Pelatihan Google Developers
1. Sebelum memulai
Instal Android Studio di komputer jika Anda belum melakukannya. Pastikan komputer Anda memenuhi persyaratan sistem yang diperlukan untuk menjalankan Android Studio (ada di bagian bawah halaman download). Jika Anda memerlukan petunjuk yang lebih mendetail terkait proses penyiapan, lihat codelab Mendownload dan menginstal Android Studio.

Dalam codelab ini, Anda akan membuat aplikasi Android pertama dengan template project yang disediakan oleh Android Studio. Anda menggunakan Kotlin dan Jetpack Compose untuk menyesuaikan aplikasi Anda. Perhatikan bahwa Android Studio selalu diupdate dan terkadang ada perubahan UI, jadi tidak masalah jika Android Studio Anda terlihat sedikit berbeda dari screenshot di codelab ini.

Prasyarat
Pengetahuan Kotlin dasar
Yang akan Anda butuhkan
Versi terbaru Android Studio
Yang akan Anda pelajari
Cara membuat Aplikasi Android dengan Android Studio
Cara menjalankan aplikasi dengan alat Pratinjau di Android Studio
Cara mengubah teks dengan Kotlin
Cara mengupdate Antarmuka Pengguna (UI) dengan Jetpack Compose
Cara melihat pratinjau aplikasi dengan Pratinjau di Jetpack Compose
Yang akan Anda build
Aplikasi yang memungkinkan Anda menyesuaikan pengantar.
Berikut adalah tampilan aplikasi saat Anda menyelesaikan codelab ini (kecuali jika akan disesuaikan dengan nama Anda):

Gambar ini menampilkan pratinjau default dengan teks yang bertuliskan, "Perkenalkan Nama Saya, Hendro Gunawan!" dengan latar belakang magenta dan padding di sekelilingnya.

Yang akan Anda butuhkan
Komputer yang dilengkapi Android Studio.

2. Menonton video tutorial coding langsung (Opsional)
Jika Anda ingin menonton salah satu instruktur kursus saat tengah menyelesaikan codelab, putar video di bawah.

Sebaiknya luaskan video ke layar penuh (dengan ikon ini Simbol ini menampilkan 4 sudut pada kotak yang disorot untuk menunjukkan mode layar penuh. di pojok kanan bawah video) agar Anda dapat melihat Android Studio dan kodenya dengan lebih jelas.

Langkah ini opsional. Anda juga dapat melewati video dan langsung memulai petunjuk codelab.

Video ini dapat dilihat di:https://www.youtube.com/watch?v=eHa84AXEPQY&t=1s

3. Membuat project menggunakan template
Dalam codelab ini, Anda akan membuat aplikasi Android dengan template project Empty Compose Activity yang disediakan oleh Android Studio.

Untuk membuat project di Android Studio:

Klik dua kali ikon Android Studio untuk meluncurkan Android Studio.
Gambar ini menampilkan logo untuk Android Studio.

Dalam dialog Welcome to Android Studio, klik New Project.
Gambar ini adalah halaman pembuka Android Studio

Jendela New Project akan terbuka dengan daftar template yang disediakan oleh Android Studio.

Gambar ini menampilkan jendela New project, yang menyertakan template untuk membuat aplikasi bagi ponsel dan tablet, Wear OS, Android TV, dan Automotive. 

Di Android Studio, template project adalah project Android yang menyediakan cetak biru untuk jenis aplikasi tertentu. Template membuat struktur project dan file yang diperlukan oleh Android Studio untuk membuat project Anda. Berdasarkan template yang dipilih, template ini menyediakan kode awal untuk membantu Anda mengerjakan project lebih cepat.

Pastikan tab Phone and Tablet telah dipilih.
Klik template Empty Compose Activity untuk memilihnya sebagai template untuk project Anda. Template Empty Compose Activity adalah template untuk membuat project sederhana yang dapat Anda gunakan untuk membuat aplikasi Compose. Template ini memiliki satu layar dan menampilkan teks "Perkenalkan Nama Saya, Hendro Gunawan!".
Klik Next. Dialog New Project akan terbuka. Kolom ini memiliki beberapa kolom untuk mengonfigurasi project Anda.
Konfigurasikan project Anda sebagai berikut:
Kolom Name digunakan untuk memasukkan nama project Anda, untuk jenis codelab ini "Kartu Ucapan".

Biarkan kolom Package name apa adanya. Ini adalah cara file Anda akan disusun dalam struktur file. Dalam hal ini, nama paket akan menjadi com.example.greetingcard.

Biarkan kolom Save location sebagaimana adanya. Project ini berisi lokasi tempat semua file yang terkait dengan project Anda disimpan. Catat lokasi tersebut di komputer agar Anda dapat menemukan file Anda.

Kotlin sudah dipilih di kolom Language. Bahasa menentukan bahasa pemrograman yang ingin Anda gunakan untuk project. Karena Compose hanya kompatibel dengan Kotlin, Anda tidak dapat mengubah kolom ini.

Pilih API 21: Android 5.0 (Lollipop) dari menu di kolom Minimum SDK. Minimum SDK menunjukkan versi minimum Android yang dapat dijalankan oleh aplikasi Anda.

Kotak centang Use legacy android.support libraries sudah tidak dicentang.

d22bfe6ae8de4147.png

Tekan Finish. Proses ini mungkin memerlukan waktu lama - sembari menunggu Anda dapat melakukan aktivitas lain. Ketika Android Studio sedang menyiapkan, status progres dan pesan menunjukkan apakah Android Studio masih menyiapkan project Anda. Tampilannya mungkin terlihat seperti ini:
Gambar ini menampilkan status progres yang berputar dan teksnya bertulis, "2 processes running...".

Pesan yang terlihat serupa dengan ini akan menginformasikan Anda saat penyiapan project dibuat.

Gambar ini menampilkan pesan sinkronisasi Gradle yang bertuliskan, "Gradle sync finished in 44s 546 ms".

Anda mungkin melihat panel What's New yang berisi informasi terkini tentang fitur-fitur baru di Android Studio. Tutup sekarang.
Gambar ini menampilkan panel What's New, yang menyediakan informasi tentang update di Android Studio.

Klik Split di kanan atas Android Studio, ini memungkinkan Anda untuk melihat kode dan desain. Anda juga dapat mengklik Code untuk melihat kode saja atau klik Design untuk melihat desain saja.
b19824b6bdd2eb0e.png

Setelah menekan Split, Anda akan melihat tiga area:

1dd07c51c7fff62c.png

Tampilan Project (1) menampilkan file dan folder project Anda
Tampilan Code (2) adalah tempat Anda mengedit kode
Tampilan Design (3) adalah tempat Anda melihat pratinjau tampilan aplikasi
Di tampilan Design, Anda akan melihat panel kosong dengan teks ini:

Teks di bagian ini bertuliskan "A successful build is needed before the preview can be displayed" di satu baris dan "Build and Refresh" di baris di bawah.

Klik Build & Refresh. Proses build mungkin memerlukan waktu beberapa saat, tetapi setelah selesai, pratinjau akan menampilkan kotak teks yang bertuliskan "Hello Android!". Aktivitas Compose kosong berisi semua kode yang diperlukan untuk membuat aplikasi ini.
Gambar ini menampilkan Pratinjau Default dengan teks yang bertuliskan, "Perkenalkan Nama Saya, Hendro Gunawan!".

4. Menemukan file project
Di bagian ini, Anda akan terus menjelajahi Android Studio dengan lebih memahami struktur file.

Di Android Studio, lihat tab Project. Tab Project menampilkan file dan folder project Anda. Saat Anda menyiapkan project, nama paketnya adalah com.example.greetingcard. Anda dapat melihat paket tersebut di sini, di tab Project. Paket pada dasarnya adalah folder tempat kode berada. Android Studio menyusun project dalam struktur direktori yang terdiri dari paket.
Jika perlu, pilih Android dari menu drop-down di tab Project.
Gambar ini menampilkan tab Project dengan menu Android yang dipilih.

Ini adalah tampilan standar dan susunan file yang Anda gunakan. Ini akan berguna saat Anda menulis kode untuk project karena Anda bisa dengan mudah mengakses file yang akan Anda kerjakan di aplikasi. Namun, jika Anda melihat file di file browser, seperti Finder atau Windows Explorer, hierarki file disusun dengan sangat berbeda.

Pilih Project Source Files dari menu drop-down. Sekarang Anda dapat menjelajahi file dengan cara yang sama seperti di file browser apa pun.
Gambar ini menampilkan tab Project dengan menu Project Source Files yang dipilih.

Pilih Android lagi untuk beralih kembali ke tampilan sebelumnya. Anda dapat menggunakan tampilan Android untuk latihan ini. Jika struktur file Anda terlihat aneh, periksa untuk memastikan Anda masih dalam tampilan Android.

5. Memperbarui teks
Setelah mengenal Android Studio, saatnya mulai membuat kartu ucapan!

Lihat tampilan Code file MainActivity.kt. Perhatikan bahwa ada beberapa fungsi yang dihasilkan secara otomatis dalam kode ini, khususnya fungsi onCreate() dan setContent().

Catatan: Ingat bahwa fungsi adalah bagian dari program yang melakukan tugas tertentu.


class MainActivity : ComponentActivity() {
   override fun onCreate(savedInstanceState: Bundle?) {
       super.onCreate(savedInstanceState)
       setContent {
           GreetingCardTheme {
               // A surface container using the 'background' color from the theme
               Surface(
                   modifier = Modifier.fillMaxSize(),
                   color = MaterialTheme.colors.background
               ) {
                   Greeting("Hendro Gunawan")
               }
           }
       }
   }
}
Fungsi onCreate() adalah titik entri ke aplikasi ini dan memanggil fungsi lain untuk membuat antarmuka pengguna. Dalam program Kotlin, fungsi main() adalah tempat spesifik dalam kode Anda tempat compiler Kotlin dimulai. Di aplikasi Android, fungsi onCreate() mengisi peran tersebut.

Fungsi setContent() dalam fungsi onCreate() digunakan untuk menentukan tata letak Anda melalui fungsi composable. Semua fungsi yang ditandai dengan anotasi @Composable dapat dipanggil dari fungsi setContent() atau dari fungsi Composable lainnya. Anotasi ini memberi tahu compiler Kotlin bahwa fungsi ini digunakan oleh Jetpack Compose untuk membuat UI.

Catatan: Compiler mengambil kode Kotlin yang Anda tulis, melihatnya baris demi baris, dan menerjemahkannya menjadi sesuatu yang dapat dipahami komputer. Proses ini disebut mengompilasi kode.

Selanjutnya, lihat fungsi Greeting(). Fungsi Greeting() adalah fungsi composable. Perhatikan anotasi @Composable di atasnya. Fungsi composable mengambil beberapa input dan menghasilkan apa yang ditampilkan di layar.


@Composable
fun Greeting(name: String) {
   Text(text = "Perkenalkan Nama Saya, $name!")
}
Anda telah mempelajari fungsi sebelumnya (jika Anda ingin mengingat kembali, kunjungi fungsi Buat dan gunakan di codelab Kotlin), tetapi ada beberapa perbedaan dengan fungsi composable.

67e3f969c53e7149.png

Nama fungsi @Composable menggunakan huruf besar.
Anda menambahkan anotasi @Composable sebelum fungsi.
Fungsi @Composable tidak dapat menampilkan apa pun.

@Composable
fun Greeting(name: String) {
   Text(text = "Perkenalkan Nama Saya, $name!")
}
Saat ini, fungsi Greeting() menggunakan nama dan menampilkan Hello untuk orang tersebut.

Ubah fungsi Greeting() untuk memperkenalkan diri Anda, bukan mengucapkan "Hello":

@Composable
fun Greeting(name: String) {
   Text(text = "Perkenalkan Nama Saya, $name!")
}
Build ulang DefaultPreview dengan menekan tombol 2c3d9b02e673771c.png di kiri atas panel desain:
Gambar ini menampilkan Pratinjau Default dengan teks yang bertuliskan "Perkenalkan Nama Saya, Hendro Gunawan!".

Bagus. Anda mengubah teks, tetapi teks memperkenalkan Anda sebagai Android, yang mungkin bukan nama Anda. Selanjutnya, Anda akan mempersonalisasinya agar memperkenalkan nama Anda.

Fungsi DefaultPreview() adalah fitur keren yang memungkinkan Anda melihat tampilan aplikasi tanpa harus mem-build seluruh aplikasi. Agar menjadi fungsi Pratinjau, Anda perlu menambahkan anotasi @Preview.

Seperti yang dapat Anda lihat, anotasi @Preview menggunakan parameter yang disebut showBackground. Jika showBackground disetel ke true, latar belakang akan ditambahkan ke pratinjau aplikasi Anda.

Android Studio secara default menggunakan tema terang untuk editor sehingga perbedaan antara showBackground = true dan showBackground = false mungkin akan sulit dilihat. Namun, seperti inilah perbedaan tampilan dengan tema gelap. Perhatikan latar belakang putih pada gambar yang disetel ke true.

Gambar ini menampilkan teks "Perkenalkan Nama Saya, Hendro Gunawan!" dalam font hitam dengan latar belakang putih di bagian atas, dan "Perkenalkan Nama Saya, Hendro Gunawan!" dalam font hitam dengan latar belakang gelap di bagian bawah.

Ubah fungsi DefaultPreview() dengan nama Anda. Kemudian, build ulang dan lihat kartu ucapan yang dipersonalisasi.

@Preview(showBackground = true)
@Composable
fun DefaultPreview() {
   GreetingCardTheme {
       Greeting("Hendro Gunawan")
   }
}
Gambar ini menampilkan Pratinjau Default dengan teks yang bertuliskan "Perkenalkan Nama Saya, Hendro Gunawan!".

6. Mengubah warna latar belakang
Sekarang Anda memiliki teks pengantar, tetapi hal ini cukup membosankan. Di bagian ini, Anda akan mempelajari cara mengubah warna latar belakang.

Untuk menetapkan warna latar belakang yang berbeda pada pendahuluan, Anda harus mengapit teks dengan Surface. Surface adalah penampung yang menampilkan bagian UI tempat Anda dapat mengubah tampilan, seperti warna latar belakang atau batas.

Untuk mengapit teks dengan Surface, tandai baris teks, tekan (Alt+Enter untuk Windows atau Option+Enter di Mac), lalu pilih Surround with widget.
Gambar ini menampilkan komponen Text yang ditandai dan menu di bawahnya dengan "Surround with widget" yang dipilih.

Pilih Surround with Container.
78e713bc774d05b1.png

Penampung default yang akan diberikan kepada Anda adalah Box, tetapi Anda dapat mengubahnya ke jenis penampung lainnya.

9fbdb58d26bd577a.png

Hapus Box dan ketik Surface() sebagai gantinya.

@Composable
fun Greeting(name: String) {
   Surface() {
       Text(text = "Perkenalkan Nama Saya, $name!")
   }
}
Penampung Surface memiliki parameter color, tetapkan ke Color.

@Composable
fun Greeting(name: String) {
   Surface(color = Color) {
       Text(text = "Perkenalkan Nama Saya, $name!")
   }
}
Saat mengetik Color, Anda mungkin melihat warnanya merah dan digarisbawahi. Untuk mengatasi hal ini, scroll ke bagian atas file yang bertuliskan import, lalu tekan ketiga tombol.
Gambar ini menampilkan pernyataan impor di bagian atas MainActivity.kt. 

Tambahkan pernyataan ini ke bagian bawah daftar impor.

import androidx.compose.ui.graphics.Color
Daftar lengkap impor akan terlihat seperti ini:


import android.os.Bundle
import androidx.activity.ComponentActivity
import androidx.activity.compose.setContent
import androidx.compose.foundation.layout.fillMaxSize
import androidx.compose.material.MaterialTheme
import androidx.compose.material.Surface
import androidx.compose.material.Text
import androidx.compose.runtime.Composable
import androidx.compose.ui.Modifier
import androidx.compose.ui.tooling.preview.Preview
import com.example.myapplication.ui.theme.GreetingCard
import androidx.compose.ui.graphics.Color
Dalam kode Anda, praktik terbaiknya adalah dengan tetap mencantumkan impor menurut abjad. Untuk melakukannya, tekan Help di toolbar bagian atas, ketik Optimize Imports, lalu klik Optimize Imports.
Gambar ini menunjukkan cara mencari Optimize Imports 

Sekarang daftar lengkap impor akan terlihat seperti ini:


import android.os.Bundle
import androidx.activity.ComponentActivity
import androidx.activity.compose.setContent
import androidx.compose.foundation.layout.fillMaxSize
import androidx.compose.material.MaterialTheme
import androidx.compose.material.Surface
import androidx.compose.material.Text
import androidx.compose.runtime.Composable
import androidx.compose.ui.Modifier
import androidx.compose.ui.graphics.Color
import androidx.compose.ui.tooling.preview.Preview
import com.example.myapplication.ui.theme.GreetingCard
Perhatikan Color yang Anda ketik di tanda kurung Surface telah berubah dari warna merah dan digarisbawahi menjadi digarisbawahi warna merah. Untuk memperbaikinya, tambahkan titik setelahnya. Anda akan melihat pop-up yang menampilkan berbagai opsi warna.
Ini adalah salah satu fitur keren di Android Studio, yang cerdas dan akan membantu Anda jika bisa. Dalam hal ini, Anda tahu bahwa Anda ingin menentukan warna sehingga fitur ini akan menyarankan warna yang berbeda.

Gambar kode ini menunjukkan Surface yang menerima argumen Color. Color memiliki titik di sampingnya dan terdapat menu di sampingnya dengan nama warna yang berbeda.

Pilih warna untuk permukaan Anda. Codelab ini menggunakan magenta, tetapi Anda dapat memilih favorit Anda.

@Composable
fun Greeting(name: String) {
   Surface(color = Color.Cian) {
       Text(text = "Perkenalkan Nama Saya, $name!")
   }
}
Klik Build & Refresh. Teks dikelilingi oleh warna yang Anda pilih.
Gambar ini menampilkan Pratinjau Default dengan teks yang bertuliskan "Perkenalkan Nama Saya, Hendro Gunawan!" dengan latar belakang cian.

7. Menambahkan padding
Sekarang teks Anda memiliki warna latar belakang, selanjutnya Anda akan menambahkan beberapa ruang (padding) di sekitar teks.

Modifier digunakan untuk menambah atau mendekorasi composable. Satu Pengubah yang dapat Anda gunakan adalah pengubah padding, yang menerapkan ruang di sekitar elemen (dalam hal ini, menambahkan ruang di sekitar teks). Hal ini diperoleh dengan menggunakan fungsi Modifier.padding().

Tambahkan impor ini ke bagian pernyataan impor.
Pastikan Anda menggunakan Optimize Imports untuk mengurutkan impor baru sesuai abjad.


import androidx.compose.ui.unit.dp
import androidx.compose.foundation.layout.padding
Tambahkan pengubah padding ke teks dengan ukuran 24.dp, klik Build & Refresh.
Catatan: Anda mempelajari lebih lanjut piksel kepadatan mandiri (DP) di jalur berikutnya, tetapi lihat artikel ini jika Anda ingin membaca lebih lanjut sekarang.


@Composable
fun Greeting(name: String) {
   Surface(color = Color.Cian) {
       Text(text = "Hi, my name is $name!", modifier = Modifier.padding(24.dp))
   }
}
Gambar ini menampilkan Pratinjau Default dengan teks yang bertuliskan "Perkenalkan Nama Saya, Hendro Gunawan!" dengan latar belakang magenta dan padding di sekelilingnya.

Selamat - Anda telah mem-build aplikasi Android pertama Anda di Compose! Ini adalah pencapaian yang cukup besar. Luangkan waktu untuk bermain-main dengan berbagai warna dan teks lalu buat versi Anda sendiri.

8. Meninjau kode solusi

import android.os.Bundle
import androidx.activity.ComponentActivity
import androidx.activity.compose.setContent
import androidx.compose.foundation.layout.padding
import androidx.compose.material.MaterialTheme
import androidx.compose.material.Surface
import androidx.compose.material.Text
import androidx.compose.runtime.Composable
import androidx.compose.ui.Modifier
import androidx.compose.ui.graphics.Color
import androidx.compose.ui.tooling.preview.Preview
import androidx.compose.ui.unit.dp
import com.example.myapplication.ui.theme.GreetingCardTheme

class MainActivity : ComponentActivity() {
   override fun onCreate(savedInstanceState: Bundle?) {
       super.onCreate(savedInstanceState)
       setContent {
           GreetingCardTheme {
               // A surface container that uses the 'background' color from the theme
               Surface(color = MaterialTheme.colors.background) {
                   Greeting("Hendro Gunawan")
               }
           }
       }
   }
}

@Composable
fun Greeting(name: String) {
   Surface(color = Color.Cian) {
       Text(text = "Perkenalkan Nama Saya, $name!", modifier = Modifier.padding(24.dp))
   }
}

@Preview(showBackground = true)
@Composable
fun DefaultPreview() {
   GreetingCardTheme {
       Greeting("Hendro Gunawan)
   }
}

9. Kesimpulan
Anda telah mempelajari Android Studio dan mem-build aplikasi Android pertama Anda dengan Compose, bagus sekali!

Codelab ini adalah bagian dari kursus Dasar-Dasar Android dengan Compose. Untuk mempelajari cara menjalankan aplikasi Anda di emulator atau perangkat fisik, lihat codelab berikutnya di jalur ini.

Ringkasan
Untuk membuat project baru: Buka Android Studio, klik New Project > Empty Compose Activity > Next, masukkan nama untuk project Anda lalu konfigurasikan setelannya.
Untuk melihat tampilan aplikasi Anda, gunakan panel Preview.
Fungsi composable mirip dengan fungsi reguler dengan beberapa perbedaan: nama fungsi memiliki huruf besar, menambahkan anotasi @Composable sebelum fungsi, fungsi @Composable tidak dapat menampilkan apa pun.
Modifier digunakan untuk menambah atau mendekorasi composable Anda.
Pelajari lebih lanjut
Kosakata Dasar-Dasar Android di Kotlin
Mengenal Android Studio
Ringkasan project
Membuat project
Menambahkan kode dari template
Jetpack Compose

10. Mendapatkan Kode Solusi
Guna mendownload kode untuk codelab yang sudah selesai, Anda dapat mendownloadnya di https://drive.google.com/file/d/1-1G15G-7VEYlcrvp7W3al4E_G-nSRFMe/view?usp=sharing dengna ekstensi RAR kemudian mengekstraknya dan membukanya di Android Studio.
Membuka project di Android Studio
Mulai Android Studio.
Di jendela Welcome to Android Studio, klik Open.
4711318ba1db18a2.png

Catatan: Jika Android Studio sudah terbuka, pilih opsi menu File > Open.

e400aad673cc7e28.png

Di file browser, buka lokasi folder project yang telah diekstrak (kemungkinan ada di folder Downloads).
Klik dua kali pada folder project tersebut.
Tunggu Android Studio membuka project.
Klik tombol Run 1b472ca0dcd0297b.png untuk membangun dan menjalankan aplikasi. Pastikan aplikasi dibangun seperti yang diharapkan.
 
