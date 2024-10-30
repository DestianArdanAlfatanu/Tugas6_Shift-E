# ScreenShot Hasil
![image](https://github.com/user-attachments/assets/aa8ef10a-cf4e-4aa4-864d-5eb5f549826c)

# Langkah Menambahkan Komponen di Halaman Ionic

## 1. Membuat Komponen Baru
Ionic menyediakan beragam **komponen siap pakai** seperti tombol, kartu, daftar, search bar, dan lainnya.
## 2. Menambahkan Komponen di Halaman
### a. Buka Halaman yang Ingin Diedit
Navigasikan ke direktori proyek Ionic dan buka halaman yang ingin kamu tambahkan komponen. Halaman ini biasanya ada di `src/app` dan memiliki ekstensi `.page.html` dan `.page.scss`. Contoh:
   ```dart
   src/app/folder/folder.page.html
   src/app/folder/folder.page.scss
   ```
   ### b. Tambahkan Kode HTML
#### Komponen Header dan Toolbar
   ```dart
   <ion-header [translucent]="true">
     <ion-toolbar>
       <ion-buttons slot="start">
        <ion-menu-button></ion-menu-button>
       </ion-buttons>
      <ion-title>{{ folder }}</ion-title>
     </ion-toolbar>
   </ion-header>
   ```
ion-header: Menampilkan header di bagian atas halaman.
ion-toolbar: Wadah untuk tombol dan judul.
ion-buttons & ion-menu-button: Membuat tombol menu di kiri header.
ion-title: Menampilkan judul dengan variabel {{ folder }}.


#### Komponen Search Bar
```dart <ion-searchbar placeholder="Search students..." showCancelButton="focus"></ion-searchbar> ```
Menambahkan kolom pencarian dengan teks placeholder dan tombol cancel.

#### Daftar dengan Ikon
```dart
<ion-list>
  <ion-item>
    <ion-label>Profile</ion-label>
    <ion-icon name="person" slot="end"></ion-icon>
  </ion-item>
  <ion-item>
    <ion-label>Settings</ion-label>
    <ion-icon name="settings" slot="end"></ion-icon>
  </ion-item>
  <ion-item>
    <ion-label>Log Out</ion-label>
    <ion-icon name="log-out" slot="end"></ion-icon>
  </ion-item>
</ion-list>
```
ion-list menciptakan daftar item, dengan setiap item berisi label (ion-label) dan ikon (ion-icon).

#### Kartu dengan Informasi Pengguna
```dart
<ion-card class="custom-card">
  <ion-card-header>
    <ion-card-title>Welcome, Nadhifa Zahra!</ion-card-title>
    <ion-card-subtitle>Student Portal</ion-card-subtitle>
  </ion-card-header>
  <ion-card-content>
    <ion-item lines="none" id="personal-info">
      <ion-avatar slot="start" class="avatar">
        <img src="https://www.gravatar.com/avatar?d=mp&s=100" alt="Avatar">
      </ion-avatar>
      <div class="info">
        <ion-chip color="tertiary" outline="true">
          <ion-label>Nadhifa Zahra</ion-label>
        </ion-chip>
        <ion-chip color="tertiary" outline="true">
          <ion-label>H1D022020</ion-label>
        </ion-chip>
      </div>
    </ion-item>
  </ion-card-content>
</ion-card>
```
ion-card digunakan untuk menampilkan informasi dalam bentuk kartu, dengan bagian header (ion-card-header) dan konten (ion-card-content).

#### Penataan Komponen di CSS
```dart
#container {
  padding: 16px;
}

ion-searchbar {
  margin-bottom: 16px;
}

ion-list {
  margin-bottom: 16px;
}

.custom-card {
  margin-top: 16px;
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

.avatar {
  border-radius: 50%;
}

.info {
  display: flex;
  flex-direction: column;
}
```
Setiap komponen memiliki gaya tersendiri, seperti ion-searchbar dan ion-list yang diberi margin bawah, dan .avatar yang dibuat bulat.

### c. Jalankan Aplikasi
Setelah selesai menambahkan dan menata komponen, jalankan aplikasi menggunakan perintah:
```dart
Ionic Serve
```
