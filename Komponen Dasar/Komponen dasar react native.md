Komponen dasar dalam React Native adalah elemen-elemen bawaan yang disediakan oleh framework untuk membangun antarmuka pengguna (UI) aplikasi mobile. Berikut adalah beberapa komponen dasar React Native yang umum digunakan:

1. View
Komponen ini adalah sebuah wadah, div, atau bagian. Komponen tampilan menampilkan tayangan slide, teks, gambar, masukan pengguna, dan lainnya. Dalam artian lain View merupakan sebuah kontainer yang mendukung tata letak dengan flexbox, gaya, beberapa penanganan sentuhan, dan kontrol aksesibilitas.

Code:

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

Code:

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

Code:

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

Code:
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

Code:

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
