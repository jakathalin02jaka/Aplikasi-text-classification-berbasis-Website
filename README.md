
## Simple Sentimen Analysis

Untuk membuat aplikasi yang melakukan curl / pengambilan data twit melalui API Twitter Search dan melakukan klasifikasi sentimen positif atau negatif, Anda dapat mengikuti langkah-langkah berikut:
1.	Daftar akun Twitter Developer: Untuk menggunakan API Twitter Search, Anda harus memiliki akun Twitter Developer dan membuat sebuah aplikasi. Setelah aplikasi Anda dibuat, Anda akan diberikan akses token dan consumer key untuk mengakses API Twitter.
2.	Buat antarmuka aplikasi: Buat sebuah antarmuka aplikasi yang memungkinkan pengguna memasukkan kata kunci atau hashtag yang akan digunakan untuk mencari twit. Anda dapat menggunakan bahasa pemrograman seperti Python, Java, atau JavaScript untuk membuat antarmuka aplikasi tersebut.
3.	Lakukan pencarian menggunakan API Twitter: Dalam antarmuka aplikasi, gunakan API Twitter Search untuk melakukan pencarian tweet berdasarkan kata kunci atau hashtag yang dimasukkan oleh pengguna. Anda dapat menggunakan bahasa pemrograman seperti Python atau Java untuk melakukan koneksi ke API Twitter dan melakukan pencarian tweet.
4.	Lakukan klasifikasi sentimen: Setelah Anda mengambil data tweet dari API Twitter, Anda dapat melakukan klasifikasi sentimen positif atau negatif menggunakan teknik klasifikasi teks seperti Naive Bayes atau Support Vector Machine. Anda dapat menggunakan bahasa pemrograman seperti Python untuk melakukan klasifikasi sentimen.
5.	Tampilkan hasil: Terakhir, tampilkan hasil dari klasifikasi sentimen pada antarmuka aplikasi sehingga pengguna dapat melihat apakah tweet yang ditemukan memiliki sentimen positif atau negatif.
Beberapa referensi yang dapat membantu Anda untuk membuat aplikasi seperti ini adalah sebagai berikut:
1.	"Twitter Sentiment Analysis using Python" oleh Shatakshi Singh: Artikel ini menjelaskan bagaimana melakukan klasifikasi sentimen pada tweet menggunakan bahasa pemrograman Python dan teknik klasifikasi teks Naive Bayes.
Link: https://www.datacamp.com/community/tutorials/simplifying-sentiment-analysis-python
2.	"Building a Sentiment Analysis App with Twitter API and Flask" oleh Tadej Magajna: Artikel ini menjelaskan bagaimana membuat aplikasi sentimen analisis menggunakan bahasa pemrograman Python, Flask framework, dan Twitter API.
Link: https://towardsdatascience.com/building-a-sentiment-analysis-app-with-twitter-api-and-flask-7935588ce34d
3.	"Twitter API: Extracting Tweets with Specific Phrase and Sentiment Analysis" oleh Hulya Karakaya: Artikel ini menjelaskan bagaimana menggunakan Twitter API untuk mengambil tweet berdasarkan kata kunci dan melakukan klasifikasi sentimen menggunakan teknik klasifikasi teks.
Link: https://towardsdatascience.com/twitter-api-extracting-tweets-with-specific-phrase-and-sentiment-analysis-10b544375317



pengambilan data :
![SS Aplikasi](https://raw.githubusercontent.com/ajikamaludin/SimpleSentimentAnalistics/2c9f2a81aad2d03eabe9182f98fb072add765965/1.png)
analisis sentimen :
![SS Aplikasi 2](https://raw.githubusercontent.com/ajikamaludin/SimpleSentimentAnalistics/master/2.png)

status: work, last test 11/10/2021

aplikasi ini didukung dengan menggukaan library/pustaka :
1. PHP dg/Twitter-php https://github.com/dg/twitter-php
2. Sastrawi PHP Stemmer https://github.com/sastrawi/sastrawi
3. PHPID sentianalysis https://github.com/yasirutomo/php-sentianalysis-id

cara menjalankan aplikasi :

1. copy file `env.example` menjadi `env`
2. install depedencies dengan composer `composer install`
3. buat database dan import database `sentiment.sql`
4. edit file `env` untuk mengubah koneksi database, untuk `customer dan token api` twitter dapatkan dari https://developer.twitter.com/
5. ekstrak PHPID-sentianalysis `php-sentianalysis-id-master.zip` di directori `lib` ubah nama folder hasil ekstrak menjadi `php-sentianalysis-id`
6. aplikasi siap dijalankan dalam webserver atau juga dengan `php -S localhost:8000 -t .`

notes : 
- if something didn't work maybe something not support or not update anymore, please fix it by yourself.
- mencari nilai akurasi yang saya sarankan, buat dataset / list cuitann yang anda klasifikasikan sendiri secara manusiawi anda tentunya dapat paham sebuah kalimat mengandung nilai positif atau negatif , kemudian bandingkan data yang anda buat dengan cuitan yang diambil melalui aplikasi menggunakan metode cross validition , dengan metode ini anda dapat mencari nilai akurasi dari aplikasi ini sesuai dengan sentiment keyword /hastag yang anda gunakan.
- aplikasi ini hanya sekedar contoh yang saya gunakan untuk memenuhi tugas akhir mata kuliah , jika anda ingin menggunakannya untuk riset/projek atau sejenisnya silahkan boleh digunakan, diubah dan dilarang keras untuk memperjual belikan dengan mengambil sumber asli tanpa melakukan perubahan pada aplikasi.
