📱 Pengenalan React Native

React Native adalah framework open-source buatan Meta (Facebook) yang memungkinkan developer membangun aplikasi mobile lintas platform (Android dan iOS) hanya dengan satu basis kode JavaScript. Framework ini pertama kali dirilis pada tahun 2015, lahir dari kebutuhan Facebook untuk meningkatkan performa aplikasi mobile mereka.

Berbeda dari pengembangan native tradisional yang membutuhkan dua kode terpisah (Swift untuk iOS dan Kotlin/Java untuk Android), React Native memungkinkan penggunaan komponen native (bukan webview) melalui komunikasi antara JavaScript dan kode native menggunakan bridge atau JSI (JavaScript Interface) terbaru.

Beberapa keunggulan utama React Native:

🔄 Code Reusability: Satu kode untuk banyak platform.

⚡ Fast Refresh: Perubahan kode langsung terlihat tanpa rebuild.

🌐 Ekosistem JavaScript: Mendukung banyak pustaka dan tools yang sudah populer.

📉 Efisiensi Waktu & Biaya: Cocok untuk startup atau tim kecil dengan deadline cepat.

Banyak perusahaan besar menggunakan React Native seperti Facebook, Instagram, Shopify, dan Microsoft Teams karena stabilitas dan fleksibilitasnya.

Meski masih kalah performa dari native dalam skenario berat, React Native menawarkan kombinasi ideal antara kecepatan pengembangan, tampilan native, dan komunitas aktif, menjadikannya salah satu pilihan terbaik untuk proyek aplikasi mobile modern.
# Contoh Sederhana Implementasi Aplikasi dengan React Native

Bagian ini menjelaskan langkah-langkah lengkap untuk membangun, menjalankan, dan mengorganisir aplikasi pada React Native Anda.

---

## 1. Persiapan Tools

Pastikan Anda telah menginstal dan mengonfigurasi komponen berikut:

- **Node.js** (v16.x atau lebih baru)  
- **npm** atau **Yarn**  
- **Watchman** (khusus macOS)  
- **Java JDK** (untuk Android)  
- **Android Studio** dengan SDK dan emulator yang sesuai  
- **Xcode** (hanya macOS, untuk build iOS)
- **React Native CLI &/atau Expo CLI**  

```bash

# Cek versi Node.js dan npm
node -v && npm -v

# (Opsional) Instalasi Watchman di macOS
brew install watchman
```

## 2. Implementasi

Dalam membuat proyek baru kali ini kami menggunakan Expo Cli namun anda juga bisa menggunakan React Native Cli. Menggunakan Expo Cli bisa di bilang lebih mudah dan tidak membutuhkan konfigurasi.

### a. Inisiasi 

```bash

npx expo init Contoh-App
cd Contoh-App
```
- Hasil: folder Contoh-App dan file App.js, plus konfigurasi Expo.

### b. Struktur Folder Dasar

Setelah inisiasi Berikut Struktur folder dari hasil inisiasi sebelumnya:

![Struktur Folder](https://github.com/corazonjordan/Project-Kelompok-2-React/blob/jordan--Pengenalan%26Impelementasi-React/Pengenalan%20React/Screenshot%202025-05-28%20222114.png)

### c. Contoh Pembuatan Portofolio sederhana berbasis Android 

Ganti isi App.js (Jika tidak ada pada directory app maka pada app/(tabs)/index.tsf) dengan kode berikut:

```javaScript
import React from "react";
import "react-native-gesture-handler";
import { NavigationContainer } from "@react-navigation/native";
import { createNativeStackNavigator } from "@react-navigation/native-stack";

import HomeScreen from "./Screen/HomeScreen";
import PortofolioScreen from "./Screen/PortofolioScreen";
import AboutScreen from "./Screen/AboutScreen";

const Stack = createNativeStackNavigator();

export default function App() {
  return (
    <NavigationContainer>
      <Stack.Navigator initialRouteName="Home">
        <Stack.Screen name="Home" component={HomeScreen} />
        <Stack.Screen name="Portofolio" component={PortofolioScreen} />
        <Stack.Screen name="About" component={AboutScreen} />
      </Stack.Navigator>
    </NavigationContainer>
  );
}

```
Penjelasan Kode Navigasi:

- `NavigationContainer` : Pembungkus utama navigasi React Native.

- `createNativeStackNavigator()` : Membuat sistem navigasi seperti tumpukan halaman.

- `Stack.Navigator` : Menampung daftar halaman yang bisa dinavigasi.

- `Stack.Screen-` : Mendaftarkan tiap halaman (Home, Portofolio, About).

- `initialRouteName="Home"` : Menentukan halaman pertama yang ditampilkan.

- `HomeScreen, PortofolioScreen, AboutScreen` : Komponen halaman utama aplikasi.

### d. Menjalankan Aplikasi 

- Android
  ```bash
  npx react-native run-android
  ```

- iOS
  ```bash
  npx react-native run-ios
  ```

- npx expo start
  ```bash
  npx expo start
  ```

  Lalu scan QR code dengan Expo Go di HP atau pilih “Run on Android/iOS simulator” di browser.
  
  ![Expo](https://github.com/corazonjordan/Project-Kelompok-2-React/blob/jordan--Pengenalan%26Impelementasi-React/Pengenalan%20React/Screenshot%202025-05-26%20225747.png)


### e. Hasil Contoh-App Portofolio berbasis Android Yang Sudah Di Buat

![hasill](https://github.com/corazonjordan/Project-Kelompok-2-React/blob/jordan--Pengenalan%26Impelementasi-React/Pengenalan%20React/hasil1jpg.jpg)
![hasil2](https://github.com/corazonjordan/Project-Kelompok-2-React/blob/jordan--Pengenalan%26Impelementasi-React/Pengenalan%20React/hasil3.jpg)
![hasil3](![hasi2](https://github.com/corazonjordan/Project-Kelompok-2-React/blob/jordan--Pengenalan%26Impelementasi-React/Pengenalan%20React/hasil3.jpg)










