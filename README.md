# Java-begin-to-multi-threads
Java'ya tamamen yeni olan bir kişiye Java'yı öğretmek ve ardından multi-threading ve socket programlaması konularını anlatmak, birkaç aşamada ilerleyen bir süreç gerektirir. İlk olarak, Java'nın temel yapı taşlarına odaklanmalıyız. Aşağıda, Java'ya genel bir giriş ve ardından multi-threading ve socket konularına doğru bir adım atmak için takip edebileceğiniz bir genel yol bulunmaktadır:

### Adım 1: Java Temelleri

#### 1.1 Java'nın Genel Tanıtımı:

- Java'nın ne olduğu, neden kullanıldığı ve hangi tür uygulamalarda tercih edildiği hakkında genel bir bilgi verin.

Tabii ki, işte temel Java syntax, sınıflar ve nesnelerle ilgili örnekler:

### 1.2 Temel Java Syntax:

#### 1.2.1 Değişkenler:

```java
// Değişken tanımlama
int sayi = 5;
double pi = 3.14;
String mesaj = "Merhaba, Dünya!";
boolean dogruMu = true;

// Değişken kullanma
System.out.println("Sayı: " + sayi);
System.out.println("Pi: " + pi);
System.out.println("Mesaj: " + mesaj);
System.out.println("Doğru mu? " + dogruMu);
```

#### 1.2.2 Veri Tipleri:

```java
// Temel veri tipleri
int tamSayi = 10;
double kesirliSayi = 3.14;
char karakter = 'A';
boolean mantiksalDeger = true;

// Diziler
int[] sayiDizisi = {1, 2, 3, 4, 5};
String[] isimler = {"Ahmet", "Ayşe", "Mehmet"};

// ArrayList
ArrayList<String> stringListesi = new ArrayList<>();
stringListesi.add("Java");
stringListesi.add("Python");
```

#### 1.2.3 Operatörler:

```java
int x = 5;
int y = 3;

// Aritmetik operatörler
int toplam = x + y;
int fark = x - y;
int carpim = x * y;
int bolum = x / y;
int mod = x % y;

// Karşılaştırma operatörleri
boolean esitMi = (x == y);
boolean kucuktur = (x < y);
boolean buyukturEsit = (x >= y);

// Mantıksal operatörler
boolean andSonucu = (x > 0) && (y > 0);
boolean orSonucu = (x > 0) || (y > 0);
boolean notSonucu = !(x > 0);
```

#### 1.2.4 Koşullu İfadeler:

```java
int puan = 75;

// if-else yapısı
if (puan >= 50) {
    System.out.println("Geçtiniz");
} else {
    System.out.println("Kaldınız");
}

// switch-case yapısı
switch (puan / 10) {
    case 10:
    case 9:
        System.out.println("A");
        break;
    case 8:
        System.out.println("B");
        break;
    case 7:
        System.out.println("C");
        break;
    default:
        System.out.println("Geçer not alınamadı");
}
```

#### 1.2.5 Döngüler:

```java
// for döngüsü
for (int i = 1; i <= 5; i++) {
    System.out.println("Sayı: " + i);
}

// while döngüsü
int j = 1;
while (j <= 5) {
    System.out.println("Sayı: " + j);
    j++;
}

// do-while döngüsü
int k = 1;
do {
    System.out.println("Sayı: " + k);
    k++;
} while (k <= 5);
```

### 1.3 Java Sınıfları ve Nesneleri:

#### 1.3.1 Sınıf ve Nesne Oluşturma:

```java
// Bir sınıf tanımı
class Araba {
    String marka;
    String model;
    int uretimYili;

    // Kurucu metod (constructor)
    public Araba(String marka, String model, int uretimYili) {
        this.marka = marka;
        this.model = model;
        this.uretimYili = uretimYili;
    }

    // Bir metod
    void bilgileriGoster() {
        System.out.println("Marka: " + marka);
        System.out.println("Model: " + model);
        System.out.println("Üretim Yılı: " + uretimYili);
    }
}

// Araba sınıfından bir nesne oluşturma
Araba araba1 = new Araba("Toyota", "Corolla", 2022);

// Nesnenin metodunu çağırma
araba1.bilgileriGoster();
```

#### 1.3.2 Miras Alma ve Arayüzler:

```java
// Üst sınıf (base class)
class Sekiller {
   

 void ciz() {
        System.out.println("Şekil çizildi.");
    }
}

// Alt sınıf (derived class) - Miras alma
class Dikdortgen extends Sekiller {
    void ozelFonksiyon() {
        System.out.println("Bu bir dikdörtgen.");
    }
}

// Arayüz tanımı
interface HareketEdebilir {
    void hareketEt();
}

// Sınıfın bir arayüzü uygulaması
class Araba implements HareketEdebilir {
    public void hareketEt() {
        System.out.println("Araba hareket ediyor.");
    }
}
```


- ### 1.4 Java Temel Kütüphaneleri:

#### 1.4.1 `java.lang` Kütüphanesi:
- `java.lang`, `java.util`, `java.io` gibi temel kütüphaneleri anlatarak Java'nın sağladığı hazır araçları öğretin.
`java.lang` kütüphanesi, Java dilinin temelini oluşturan sınıfları içerir.

```java
// String sınıfı kullanımı
String mesaj = "Merhaba, Java!";
System.out.println(mesaj);

// Math sınıfı kullanımı
double karekok = Math.sqrt(25);
System.out.println("Karekök: " + karekok);
```

#### 1.4.2 `java.util` Kütüphanesi:

`java.util` kütüphanesi, genel amaçlı veri yapıları ve araçları içerir.

```java
import java.util.ArrayList;
import java.util.HashMap;

// ArrayList kullanımı
ArrayList<String> liste = new ArrayList<>();
liste.add("Java");
liste.add("Python");
System.out.println("Liste: " + liste);

// HashMap kullanımı
HashMap<String, Integer> sozluk = new HashMap<>();
sozluk.put("Java", 1995);
sozluk.put("Python", 1991);
System.out.println("Sözlük: " + sozluk);
```

#### 1.4.3 `java.io` Kütüphanesi:

`java.io` kütüphanesi, giriş/çıkış işlemleri için sınıfları içerir.

```java
import java.io.FileReader;
import java.io.BufferedReader;
import java.io.FileWriter;
import java.io.BufferedWriter;
import java.io.IOException;

// Dosya okuma
try (BufferedReader reader = new BufferedReader(new FileReader("dosya.txt"))) {
    String satir;
    while ((satir = reader.readLine()) != null) {
        System.out.println(satir);
    }
} catch (IOException e) {
    e.printStackTrace();
}

// Dosya yazma
try (BufferedWriter writer = new BufferedWriter(new FileWriter("yeniDosya.txt"))) {
    writer.write("Merhaba, dünya!");
} catch (IOException e) {
    e.printStackTrace();
}
```

### 1.5 Hata Yakalama ve İstisna İşleme:
- `try`, `catch`, `finally` blokları ile hata yakalama ve istisna işleme konularını anlatın.
#### 1.5.1 `try`, `catch`, `finally` Blokları:

```java
// Dosya okuma ve yazma işlemlerinde hata yakalama
try {
    // Dosya okuma işlemi
    BufferedReader reader = new BufferedReader(new FileReader("dosya.txt"));

    // Dosya yazma işlemi
    BufferedWriter writer = new BufferedWriter(new FileWriter("yeniDosya.txt"));

    // İşlemler...

} catch (FileNotFoundException e) {
    System.err.println("Dosya bulunamadı: " + e.getMessage());
} catch (IOException e) {
    System.err.println("Giriş/Çıkış hatası: " + e.getMessage());
} finally {
    // Her durumda çalışacak kod bloğu
    System.out.println("İşlem tamamlandı.");
}
```

#### 1.5.2 Özel İstisna Türleri:

```java
public class CustomExceptionExample {

    // Kendi istisna sınıfınızı tanımlama
    static class OzetHatasi extends Exception {
        public OzetHatasi(String message) {
            super(message);
        }
    }

    public static void main(String[] args) {
        try {
            // Özel istisna fırlatma
            throw new OzetHatasi("Bu bir özel istisna örneğidir.");
        } catch (OzetHatasi e) {
            System.err.println("Özel İstisna Yakalandı: " + e.getMessage());
        }
    }
}
```



#### 1.6 Java Çok Biçimliliği:

- Çok biçimliliği (polymorphism) ve arayüzleri anlatarak Java'nın güçlü yanlarını vurgulayın.

### Adım 2: Multi-Threading

#### 2.1 Temel Multi-Threading Kavramları:

- Thread oluşturma, başlatma, duraklatma, öldürme gibi temel multi-threading kavramlarını öğretin.

#### 2.2 Senkronizasyon ve Kritik Bölge:

- Birden fazla thread arasında güvenli bir şekilde veri paylaşımı için senkronizasyonu öğretin.

#### 2.3 Thread Havuzları ve Çoklu İş Parçacıklı Tasarım:

- Thread havuzları ve çoklu iş parçacıklı tasarım prensipleri ile daha karmaşık multi-threading senaryolarını anlatın.

### Adım 3: Socket Programlama

#### 3.1 Temel Socket Kavramları:

- ServerSocket ve Socket sınıfları aracılığıyla temel ağ iletişimi kavramlarını öğretin.

#### 3.2 TCP ve UDP Protokoller:

- TCP ve UDP protokollerini anlatarak temel ağ protokollerini kavramalarını sağlayın.

#### 3.3 Veri Akışları ve Nesne Serileştirme:

- InputStream ve OutputStream kullanarak veri akışlarını yönetmeyi, nesne serileştirmeyi öğretin.

#### 3.4 Asenkron Socket Programlama:

- Asenkron socket programlama konseptlerini anlatın ve temel kullanım senaryolarını gösterin.

### Adım 4: Uygulama ve Proje

- Öğrenilen bilgileri pekiştirmek için küçük bir proje veya örnek uygulama üzerinde çalışma yapın.

Bu adımlar, kişinin Java ve ağ programlaması konularında sağlam bir temel oluşturmasına yardımcı olacaktır. Her konuyu öğrenirken örneklerle pratik yapmak, gerçek dünya senaryolarını anlamak için önemlidir. Bu nedenle her adımı örnek uygulamalar veya projelerle desteklemek öğrenmeyi daha etkili hale getirecektir.
