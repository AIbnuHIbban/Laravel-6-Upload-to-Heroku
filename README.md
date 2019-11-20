# Laravel-6-Upload-to-Heroku
Cara Upload Project Laravel ke Heroku

> **Perhatian !! Cara Ini hanya untuk pengguna Linux**

# Langkah - langkah Upload Project Laravel ke Heroku

## Persiapan

 - Create Akun di [Heroku](heroku.com)
 - Install Snap di Linux Anda: `sudo apt install snapd`
 - Buka Terminal lalu copy paste kode dibawah
```
echo  'export PATH=$PATH:/snap/bin' >> ~/.bashrc 
```

## Langkah - langkah

 1. Buat File dengan nama **Procfile**  di Project Laravel (Letaknya Setara dengan .env, dan kawan - kawan)
 2. Copy Paste code di bawah ke **Procfile** tadi, lalu **Save**

     web: vendor/bin/heroku-php-apache2 public/

 3. buka terminal lalu arahkan ke directory folder project, lalu ketik **git init**
 4. ketik lagi **heroku login**
 5. ketik lagi **heroku create** (Ingat masih di directory folder Project)
 6. ketik lagi **php artisan key:generate --show**
 7. akan muncul kode Key dari Laravel, Copy Code tersebut.
 8. lalu ketik lagi **heroku config:set APP_KEY={Key yang tadi di copy}**
 9. Setelah itu ketik **git add .**
 10. lalu commit dengan mengetik **git commit -m "pesan commit"** 
 11. setelah itu Push dengan ketik **git push heroku master**
 12. Selesai, Jika anda ingin membuat Halaman Heroku anda ketik **heroku open**


Ok, Sekian.. Semoga Bermanfaat ~

### Thanks

 
