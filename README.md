## 🎯 Tujuan Praktikum

Praktikum ini bertujuan untuk:

- Memahami berbagai jenis sistem navigasi pada framework Flutter.
- Menerapkan dan membedakan konsep Navigator 1.0, Navigator 2.0, Nested Navigation, dan Deep Link Navigation.
- Membangun aplikasi Flutter dengan arsitektur navigasi yang efisien, modular, dan mudah dikelola.
- Menyiapkan dasar untuk pengembangan aplikasi skala besar dengan navigasi kompleks atau berbasis web.

---

## 🗺️ Gambaran Navigasi Flutter

### 1. Navigation (Navigator 1.0)

- Navigasi dasar menggunakan metode imperatif: Navigator.push() dan Navigator.pushNamed().
- Sangat cocok untuk aplikasi sederhana hingga menengah.
- Rute didefinisikan menggunakan MaterialApp.routes atau secara langsung melalui konstruktor.
- Contoh:
  - Navigasi dari HomeScreen ke DetailScreen, SettingsScreen, dan AboutScreen.
  - Data dapat dikirim melalui constructor atau arguments.

### 2. Navigation 2.0 (Router API)

- Navigasi deklaratif menggunakan Navigator, pages, dan onPopPage.
- Memungkinkan kontrol penuh atas tumpukan halaman (page stack).
- Cocok untuk aplikasi kompleks, seperti aplikasi web, e-commerce, dll.
- Navigasi dikendalikan melalui perubahan state, bukan dengan push/pop langsung.

Contoh:  
Ketika item dipilih pada HomeScreen, halaman DetailScreen ditambahkan ke dalam daftar pages, dan akan dihapus saat pop.

### 3. Nested Navigation

- Menggunakan Navigator di dalam halaman tertentu (child Navigator) untuk mengelola alur internal.
- Sering digunakan dalam alur multi-langkah (wizard), tab bar, atau onboarding screen.
- Tidak mengganggu navigator utama.

Contoh:  
Alur pengaturan perangkat dari:
- FindDevicesScreen → ConnectDeviceScreen → ConfirmDeviceScreen, dikelola oleh nested Navigator di dalam SetupFlowScreen.

### 4. Deep Link Navigation

- Menggunakan URI atau path (misalnya: /home, /detail/3) untuk menavigasi langsung ke halaman tertentu.
- Penting untuk aplikasi berbasis web atau integrasi link eksternal (email, notifikasi, dsb).
- Menggunakan Router, RouteInformationParser, dan RouterDelegate.

Contoh:  
Pengguna membuka URL /detail/1 dan langsung diarahkan ke halaman detail item dengan ID 1, tanpa melalui navigasi manual dari HomeScreen.
