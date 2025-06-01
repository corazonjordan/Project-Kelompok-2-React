# Project-Kelompok-2-React

Selamat datang di repositori **Project-Kelompok-2-React**! 🎉  
Repositori ini dibuat untuk mendokumentasikan materi pembelajaran dan implementasi **React Native**, framework populer untuk pengembangan aplikasi mobile lintas platform (iOS & Android).

---

## 👥 Tim Pengembang

| Nama Lengkap                   | Tugas Materi                    |
|--------------------------------|---------------------------------|
| Muhammad Jordan                | Pengenalan React Native         |
| Ika Mi'rad Saputri             | Komponen Dasar React Native     |
| M.Raga Al Abtad Purma          | State dan Props                 |
| Muhammad Ismail                | Navigasi React Native           |

---
📱 Pengenalan React Native

🚀 Apa itu React Native?

React Native adalah framework open-source buatan Meta (Facebook) yang memungkinkan developer membangun aplikasi mobile lintas platform (Android dan iOS) hanya dengan satu basis kode JavaScript. Framework ini pertama kali dirilis pada tahun 2015, lahir dari kebutuhan Facebook untuk meningkatkan performa aplikasi mobile mereka.

Berbeda dari pengembangan native tradisional yang membutuhkan dua kode terpisah (Swift untuk iOS dan Kotlin/Java untuk Android), React Native memungkinkan penggunaan komponen native (bukan webview) melalui komunikasi antara JavaScript dan kode native menggunakan bridge atau JSI (JavaScript Interface) terbaru.

Beberapa keunggulan utama React Native:

🔄 Code Reusability: Satu kode untuk banyak platform.

⚡ Fast Refresh: Perubahan kode langsung terlihat tanpa rebuild.

🌐 Ekosistem JavaScript: Mendukung banyak pustaka dan tools yang sudah populer.

📉 Efisiensi Waktu & Biaya: Cocok untuk startup atau tim kecil dengan deadline cepat.

Banyak perusahaan besar menggunakan React Native seperti Facebook, Instagram, Shopify, dan Microsoft Teams karena stabilitas dan fleksibilitasnya.

Meski masih kalah performa dari native dalam skenario berat, React Native menawarkan kombinasi ideal antara kecepatan pengembangan, tampilan native, dan komunitas aktif, menjadikannya salah satu pilihan terbaik untuk proyek aplikasi mobile modern.

---

```bash
npm install -g expo-cli
expo init ProjectKelompok2React
cd ProjectKelompok2React
npm start
```
**Komponen Dasar React Native**

Komponen dasar dalam React Native adalah elemen-elemen bawaan yang disediakan oleh framework untuk membangun antarmuka pengguna (UI) aplikasi mobile. Berikut adalah beberapa komponen dasar React Native yang umum digunakan:

1. View
Komponen ini adalah sebuah wadah, div, atau bagian. Komponen tampilan menampilkan tayangan slide, teks, gambar, masukan pengguna, dan lainnya. Dalam artian lain View merupakan sebuah kontainer yang mendukung tata letak dengan flexbox, gaya, beberapa penanganan sentuhan, dan kontrol aksesibilitas.

```js
import React from "react";
import { View, Text } from "react-native";
const App = () => {
  return (
    <View style={{ margin: 10 }}>
      <Text style={{ marginBottom: 10 }}>
        Hello Readers, I'm inside View Component
      </Text>
      <Text style={{ marginBottom: 10 }}>You can also define image</Text>
    </View>
  );
};
export default App;
```

2. Text
Pada komponen ini untuk menampilkan teks di dalam aplikasi.
Dapat mendukung penumpukan teks, dan acara sentuh beserta opsi gaya standar sepertii font khusus, ukuran font, dll.

```js
import React from "react";
import { View, Text } from "react-native";
const App = () => {
  return (
    <View style={{ margin: 10 }}>
      <Text style={{ marginBottom: 10 }}>Hello, I am Text Component</Text>
      <Text style={{ marginBottom: 10 }}>I am also a Text Component</Text>
    </View>
  );
};
export default App;
```

3. Image
Komponen ini dapat memungkinkan kita dalam menambahkan gambar ke dalam aplikasi.
Selain itu kita juga dapat menambahkan sebuah gambar jaringan sementara, gambar statis dan banyak lagi.

```js
import React from "react";
import { View, Text, Image } from "react-native";
const App = () => {
  return (
    <View>
      <Text>The Image Component is next to me.</Text>
      <Image
        source={{
          uri: "https://reactnative.dev/docs/assets/p_cat2.png",
        }}
        style={{ width: 200, height: 200 }}
      />
      <Image
        style={styles.logo}
        source={{
          uri: 'data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADMAAAAzCAYAAAA6oTAqAAAAEXRFWHRTb2Z0d2FyZQBwbmdjcnVzaEB1SfMAAABQSURBVGje7dSxCQBACARB+2/ab8BEeQNhFi6WSYzYLYudDQYGBgYGBgYGBgYGBgYGBgZmcvDqYGBgmhivGQYGBgYGBgYGBgYGBgYGBgbmQw+P/eMrC5UTVAAAAABJRU5ErkJggg==',
        }}
      />


    </View>
  );
};
export default App;
```

4. Text Input
Komponen ini memungkiankan pengguna untuk menambahkan sebuah masukan.
Kita bisa menambahkan lebih banyak fungsi ke dalamnya dengan meneruskan properti untuk menyimpan respons masukan dari pengguan, memperbarui beberapa bagian, dan teks, atau dapat melihat aplikasi setelah pengguna menggirimkan masukan.
Pada peristiwa lain, seperti onChange, onSubmitEditing, onScroll, dll., yang mana dapat digunakan untuk memodifikasi komponen TextInput.

```js
import React from "react";
import { View, Text, TextInput } from "react-native";
const App = () => {
  return (
    <View style={{ margin: 10 }}>
      <Text>The user can type something.</Text>
      <TextInput
        style={{
          height: 30,
          borderColor: "black",
          borderWidth: 1,
        }}
        defaultValue="I am a Text Input"
      />
    </View>
  );
};
export default App;
```

5. ScrollView
Komponen ini dapat digunakan untuk menggulir area tertentu secara horizontal atau vertikal. Dengan kata lain, kita bisa menggunakan ScrollView ketika kita memiliki banyak komponen anak yang tidak cukup dalam satu layar sekaligus.
Untuk menggunakannya kita hanya perlu membungkus bagian tersebut dalam komponen ScrollView.
ScrollView merender semua komponen anaknya dalam waktu bersamaan yang mungkin mengakibatkan rendering dan kinerja yang buruk.

```js
import React from "react";
import { View, Text, Image, ScrollView, TextInput } from "react-native";
const App = () => {
  return (
    <ScrollView>
      <Text style={{ fontSize: 100 }}>
        I am a text component inside ScrollView component
      </Text>
      <Text style={{ fontSize: 100 }}>Some more text</Text>
    </ScrollView>
  );
};
export default App;
```

**Tiga Jenis Komponen React Native untuk Aplikasi**

Terdapat tiga tipe komponen dari react native yang diklasifikasikan secara luas yang tersedia untuk digunakan, diantaranya sebagai berikut:
**a. Komponen Inti**
**b. Komponen Kustom**
**c. Komponen Komunitas**

Komponen adalah sebuah blok penyusun aplikasi React Native atau React lainnya. Semua komponen, apa pun jenisnya, merangkum potongan kode yang dapat digunakan kembali dan mewakili bagian dari antarmuka pengguna (UI) aplikasi.

**a. Komponen Inti**
Komponen inti adalah sebuah elemen fundamental yang menjadi _inti_ di setiap aplikasi React Native. Komponen-komponen itu ialah elemen JavaScript lintas platform yang telah dirender dengan lancar menggunakan komponen UI asli dari antarmuka seluler masing-masing, seperti iOS atau Android. Dimana komponen-komponen ini akan menjadi jembatan antara basis kode JavaSript dan elemen asli platform.

Dengan tersedianya rendering lintas platform, Komponen inti mempunyai manfaat besar yakni, menyediakan pengalaman pengguna yang konsisten pada semua platform penerapan. Pada waktu yang sama, dengan memanfaatkan elemen asli platform, komponen inti akan memastikan kinerja dan persepsi pengguna lebih baik kepada aplikasi.

Contoh komponen inti dalam React Native:

```js
import  React  dari  'react' ; 
// impor komponen inti dari React Native 
import { View , Text , Image , ScrollView , TextInput , StyleSheet } dari  'react-native' ; 

// komponen tampilan inti (wadah dasar) 
fungsi  ViewComponent ( ){ 
  // prop styles memungkinkan Anda untuk mengontrol/memanipulasi presentasi visual 
  return <View><Text>Komponen Inti!</Text></View>; 
}; 

// komponen gambar inti 
fungsi  ImageComponent ( ){ 
  return <Image source='https://via.placeholder.com/150' />; 
}; 

// komponen tampilan gulir inti (daftar gulir) 
fungsi  ScrollViewComponent ( ){ 
  return ( 
    <ScrollView> 
      <Text}</* Konten teks panjang untuk daftar gulir */}</Text> 
    </ScrollView> 
  ); 
}; 

// komponen masukan teks inti (mirip formulir) fungsi 
TextInputComponent  ( ) { 
  return <TextInput placeholder="Masukkan teks di sini..." />; 
}; 

fungsi  CoreComponentsExample ( ){ 
  kembali ( 
    <> 
      <ViewComponent /> 
      <ImageComponent /> 
      <ScrollViewComponent /> 
      <TextInputComponent /> 
    </> 
  ); 
};
```
Komponen-komponen ini memiliki tujuan yang berbeda-beda dalam memenuhi kebutuhan antarmuka pengguna, selain itu komponen-komponen ini dapat memperluas perangkat yang tersedia bagi pengembang React Native yang dapat memungkinkan terciptanya antarmuka yang beragam dan kaya fitur.

**b. Komponen Kustom**
komponen kustom merupakan sebuah komponen yang dapat disesuaikan dengan fungsi yang ditetapkan oleh pengembang aplikasi. Komponen kustum sendiri didukung oleh platform, yang artinya komponen ini dapat diubah menjadi elemen asli masing-masing untuk platform iOS dan Android pada saat dijalankan lewat React Native.

Komponen kustum mempunyai sifat yang dapat disesuaikan, sehingga pengembang dapat menggunakan komponen khusus untuk mengakses fungsionalitas dan API khusus perangkat yang tidak disertakan dalam basis kode. Contohnya adalah membuat aplikasi berinteraksi dengan kamera atau GPS perangkat tempat aplikasi dijalankan.

Contoh komponen khusus sederhana untuk membuka dan menutup kamera:

```js
Bahasa Indonesia: import  React , { useState} dari  'react' ; 
import { View , Button , StyleSheet , Platform } dari  'react-native' ; 
// impor pustaka untuk berinteraksi dengan kamera perangkat 
import { RNCamera } dari  'react-native-camera' ; 

// atur status untuk 
fungsi status kamera  CameraComponent ( ) { 
  const [cameraOpen, setCameraOpen] = useState ( false ); 

  // ubah status sakelar kamera 
  fungsi  handleOpenCamera ( ){ 
    setCameraOpen ( true ); 
  }; 
  
  // ubah status sakelar kamera 
  fungsi  handleCloseCamera ( ){ 
    setCameraOpen ( false ); 
  }; 

  // menggunakan komponen inti untuk membangun/meningkatkan fungsionalitas komponen kustom 
  fungsi  renderCamera ( ){ 
    return ( 
      <View> 
        <RNCamera 
          type={RNCamera.Constants.Type.back} 
          autoFocus={RNCamera.Constants.AutoFocus.on} 
          flashMode={RNCamera.Constants.FlashMode.off} 
          captureAudio={false} 
        /> 
        <Button title="Tutup Kamera" onPress={handleCloseCamera} /> 
      </View> 
    ); 
  }; 

  return ( 
    // menggunakan modul untuk menentukan pada platform apa aplikasi dijalankan
     <View> 
      {Platform.OS === 'ios' && !isCameraOpen && <Button title="Buka Kamera" onPress={handleOpenCamera} />} 
      {Platform.OS === 'ios' && isCameraOpen && renderCamera()} 
    </View> 
  ); 
}
```

**c. Komponen Komunitas**
komponen komunitas seperti namanya komponen ini dapat dikembangkan, dikelola, dan dibagikan oleh komunitas pengembang React Native yang besar. Komponen ini memiliki beragam fungsi dan pengalaman pengguna. Selain itu komponen ini dianggap sebagai komponen khusus yang dibuat oleh pengembang atau lingkaran pengembangan lain.

Komponen komunitas adalah cara bagi individu untuk membuat dan memperbaiki komponen khusus yang dibagikan demi kebaikan komunitas pembuat kode.

Berikut contoh code membuat navigasi layar dasar menggunakan komponen komunitas, _react-navigation_:

```js
impor  React  dari  'react' ; 
impor { View , Text , Button , StyleSheet } dari  'react-native' ; 

// impor komponen komunitas 
impor { NavigationContainer } dari  '@react-navigation/native' ; 
impor { createStackNavigator} dari  '@react-navigation/stack' ; 

const  Stack = createStackNavigator (); 

fungsi  App ( ){ 
  return ( 
    // mengimplementasikan komponen komunitas tersebut di aplikasi Anda
     <NavigationContainer> 
      <Stack.Navigator initialRouteName="ScreenOne"> 
        <Stack.Screen 
          name="ScreenOne" 
          komponen={() => ( 
            <View style={styles.container}> 
              <Text>Layar Satu</Text> 
              <Button title="Pergi ke Layar Dua" onPress={() => navigation.navigate('ScreenTwo')} /> 
            </View> 
          )} 
        /> 
        <Stack.Screen 
          name="ScreenTwo" 
          komponen={() => ( 
            <View style={styles.container}> 
              <Text>Layar Dua</Text> 
              <Button title="Kembali" onPress={() => navigation.goBack()} /> 
            </View> 
          )} 
        /> 
      </Stack.Navigator> 
    </NavigationContainer> 
  ); 
}; 

export  default  App ;
```

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










