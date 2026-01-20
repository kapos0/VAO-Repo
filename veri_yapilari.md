# Veri Yapıları (Data Structures) Cheat Sheet

Verinin bellekte nasıl tutulacağını ve işleneceğini belirleyen yapılardır.

## 1. Doğrusal Yapılar (Linear)

### a. Array (Dizi)

- **Nedir:** Aynı türden verilerin yan yana dizildiği sabit boyutlu kutulardır.
- **Avantajı:** İndeks numarası ile (örn: `dizi[5]`) verilere çok hızlı erişilir (O(1)).
- **Dezavantajı:** Boyutu baştan bellidir, sonradan değiştirilemez.

### b. Linked List (Bağlı Liste)

- **Nedir:** Tren vagonları gibidir. Her eleman (düğüm), kendinden sonraki elemanın adresini tutar.
- **Avantajı:** Boyutu dinamiktir, hafıza dolana kadar eleman eklenebilir.
- **Dezavantajı:** 5. elemana gitmek için baştan başlayıp tek tek gitmek gerekir (O(n)).

---

## 2. LIFO ve FIFO Prensibi

### a. Stack (Yığın) - LIFO

- **Mantık:** Last In First Out (Son Giren İlk Çıkar).
- **Örnek:** Üst üste dizilmiş tabaklar. En son koyduğunuz tabağı ilk alırsınız.
- **Kullanım:** "Geri Al" (Undo) işlemleri, tarayıcı geçmişi.

### b. Queue (Kuyruk) - FIFO

- **Mantık:** First In First Out (İlk Giren İlk Çıkar).
- **Örnek:** Ekmek kuyruğu. Sıraya ilk giren ekmeği ilk alır.
- **Kullanım:** Yazıcıya gönderilen belgeler, işlemci görev sırası.

---

## 3. Gelişmiş Yapılar

### a. Hash Table (Hash Tablosu)

- **Nedir:** Anahtar-Değer (Key-Value) eşleşmesi.
- **Mantık:** Bir anahtar kelime verirsiniz, o size karşılığındaki veriyi getirir.
- **Hız:** Arama yapmak çok hızlıdır (Ortalama O(1)).
- **Örnek:** Telefon rehberi (İsim -> Numara).

### b. Tree (Ağaç)

- **Nedir:** Kök (Root) ve dallardan oluşan hiyerarşik yapı.
- **Binary Search Tree (BST):** Bir düğümün solundaki değerler ondan küçük, sağındakiler ondan büyüktür. Arama yapmayı çok kolaylaştırır.
- **Örnek:** Bilgisayar klasör sistemi, HTML yapısı (DOM).

### c. Graph (Çizge)

- **Nedir:** Düğümler (Vertex) ve bunları birbirine bağlayan yollardan (Edge) oluşur.
- **Örnek:** Sosyal medya arkadaşlık ağları, navigasyon uygulamalarında şehirler ve yollar.
