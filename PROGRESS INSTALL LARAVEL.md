## PROGRESS INSTALL LARAVEL

#### Nabila Nur Amalia_1202190013

- Before installing Laravel, we have to install Xampp and Composer first

then the next step is:

- Enter Command Prompt -> Win+R, type cmd and ok

  ![1.jpeg](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/1.jpeg?raw=true)

- then, go to Command Prompt or terminal to file server directory. 

  The file server location on XAMPP by default is in the xampp/htdocs directory. to go to the htdocs directory, enter this command. :

  ```
  cd \xampp\htdocs
  ```

   ![2.jpeg](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/2.jpeg?raw=true)

- after being in the htdocs directory, you must make a request to install the laravel file provided in the github repository, the command :

  ```
  composer create-project--prefer-dist laravel/laravel tubes_pi
  ```

  when the command is successfully entered, Composer will carry out the process of retrieving data and installing Laravel into the directory you have specified. Make sure the internet connection is stable so that there are no interruptions during the Laravel data retrieval process.

​		![3.jpeg](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/3.jpeg?raw=true)

​		![4.jpeg](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/4.jpeg?raw=true)

- After the Laravel file download process is complete, there is a new folder in the file server directory with a name according to the project name that has been previously specified in the /xampp/htdocs folder.

  ![6.png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/6.png?raw=true)

  

- To make sure Laravel is successfully installed and ready to use, go to Command Prompt to the directory that was created earlier. Then, enter the following command into Command Prompt or Terminal:

```
php artisa serve
```

![5.jpeg](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/5.jpeg?raw=true)

- then open the link using the ip address which is 127.0.0.1:8000, and the results will appear as below :

  ![7.png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/7.png?raw=true)

## FINAL PROJECT [CHAPTER 2]

- Jalankan xampp, Vs Code dan phpmyadmin

- Buatlah database pada phpmyadmin

- Pada Vs Code : Open folder -> (C;) -> tubespi -> Select Folder

  ![(1).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(1).png?raw=true)

  ![(2).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(2).png?raw=true)

- masuk pada folder .env, atur sesuai dengan database yang telah di buat

  ```
  DB_DATABASE=tubespi
  DB_USERNAME=root
  DB_PASSWORD=
  ```

  ![(3).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(3).png?raw=true)

- Buka Terminal yang ada pada Vs Code

   ![(4).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(4).png?raw=true)

  ketikkan perintah berikut pada terminal

  ```
  php artisan serve
  ```

  ![(5).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(5).png?raw=true)

​		Lalu buka browser, dan ketikkan 	

```
http://127.0.0.1:8000
```

​		![(6).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(6).png?raw=true)

​		Maka akan muncul tampilan seperti berikut,

​		![(7).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(7).png?raw=true)

- ketikkan perintah berikut pada terminal

  ```
  php artisan make:migration create_rss_table
  ```

  ![(8).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(8).png?raw=true)

  ![(9).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(9).png?raw=true)

- kemudian buka file "create_rss_table.php", lalu isi sesuai skema database yang di inginkan 

  ![(10).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(10).png?raw=true)

- kemudian buka file "create_news_table.php", lalu isi sesuai skema database yang di inginkan 

  ![(11).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(11).png?raw=true)

- beri Foreign Key pada tabel news_table.php

  ```
   //FOREIGN KEY
              $table->unsignedBigInteger('rss_id');
              $table->foreign('rss_id')->references('id')->on('rss');
              $table->timestamps();
  ```

  ![(12).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(12).png?raw=true)

- kembali ke terminal, untuk merefresh. gunakan perintah :

  ```
  php artisan migrate:fresh
  ```

  ![(13).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(13).png?raw=true)

  kemudian cek pada database phpmyadmin

  ![(14).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(14).png?raw=true)

- kembali ke terminal lagi, dan ketikkan perintah di bawah ini, untuk membuat model rss seed controller

  ```
  php artisan make:model Rss --seed --controller
  ```

  ![(15).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(15).png?raw=true)

- untuk melihatnya, buka folder Models. maka sudah terdapat 2 file 

  Rss.php dan User.php

  ![(16).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(16).png?raw=true)

- buka file Rss.php dan isi sesuai pada gambar di bawah ini :

  ![(17).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(17).png?raw=true)

  ![(18).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(18).png?raw=true)

- lalu buka folder seeders, dan buka file RssSeeder.php dan isi sesuai pada gambar dibawah ini :

  ![(19).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(19).png?raw=true)

- lalu buka folder seeders, dan buka file DatabaseSeeder.php dan isi sesuai pada gambar dibawah ini :

  ![(20).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(20).png?raw=true)

- Cek Phpmyadmin untuk memastikan apakah url sudah masuk pada database

  ![(21).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(21).png?raw=true)

- kembali ke terminal dan ketikkan perintah dibawah ini, untuk membuat model News controller

  ```
  php artisan make:model News --controller
  ```

  ![(22).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(22).png?raw=true)

- masuk pada file News.php, dan ketikkan perintah 

  ```
  protected $table='news';
      //bahwa pada model news ->menggunakan table news
      protected $fillable=['title','img_url','description','source_url','rss_id'];
      //bahwa hanya bisa diisi untuk kolom
  ```

  ![(23).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(23).png?raw=true)

- Masuk pada folder controllers dan buka pada NewsController. isi sesuai gambar berikut

  ![(24).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(24).png?raw=true)

- Kemudian buka file web.php dan isi sesuai pada gambar di bawah

  ![(25).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(25).png?raw=true)

  ![(26).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(26).png?raw=true)

- Buka file NewsController.php dan isi sesuai dengan gambar, jika sudah 

  Maka buka browser untuk mengecek

  ![(29).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(29).png?raw=true)

  ![(27).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(27).png?raw=true)

  ![(28).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(28).png?raw=true)

- kemudian buka RssSeeder.php dan isi sesuai pada gambar di bawah ini :

  dan referesh pada terminal 

  ![(30).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(30).png?raw=true)

  ![(31).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(31).png?raw=true)

- lalu cek pada browser 

  dan Hasilnya

  ![(32).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(32).png?raw=true)

  ![(33).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(33).png?raw=true)

  ![(34).png](https://github.com/nabill13/Integratif--IT0202---1202190013-/blob/main/(34).png?raw=true)
  
  ## FINAL PROJECT [CHAPTER 3]
  
  RSS yang di pake : 
  1. Allnews : http://www.koreatimes.co.kr/www/rss/rss.xml
  2. sport : http://www.koreatimes.co.kr/www/rss/sports.xml
  3. entertainment : http://www.koreatimes.co.kr/www/rss/entertainment.xml

  ![35](https://user-images.githubusercontent.com/92932656/178118463-babca233-b074-4747-ad55-093b8a343288.PNG)
  ![36](https://user-images.githubusercontent.com/92932656/178118469-a3ad7784-6513-4d98-97ee-bcb1d0a64cd0.PNG)


## GOMAWOYOO
