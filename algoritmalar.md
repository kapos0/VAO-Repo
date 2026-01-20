# Arama ve Sıralama Algoritmaları Cheat Sheet

## 1. Arama Algoritmaları (Searching)

Bir veri setinin içinde belirli bir elemanı bulmak için kullanılır.

### a. Linear Search (Doğrusal Arama)

- **Mantık:** Listenin başından başlar, aranan elemanı bulana kadar tek tek herkese bakar.
- **Gereklilik:** Liste sıralı olmak zorunda değildir.
- **Hız (Big O):** O(n) - (Yavaş, listenin boyutu arttıkça süre doğru orantılı artar).

### b. Binary Search (İkili Arama)

- **Mantık:** Liste tam ortadan ikiye bölünür. Aranan sayı ortadakinden küçükse sol tarafa, büyükse sağ tarafa bakılır. Her adımda seçenekler yarıya iner.
- **Gereklilik:** Liste **kesinlikle sıralı** olmalıdır.
- **Hız (Big O):** O(log n) - (Çok hızlı).

---

## 2. Sıralama Algoritmaları (Sorting)

Verileri belirli bir düzene (küçükten büyüğe vb.) sokmak için kullanılır.

### a. Bubble Sort (Kabarcık Sıralaması)

- **Mantık:** Yan yana duran iki elemanı karşılaştırır. Soldaki sağdakinden büyükse yer değiştirirler. En büyük eleman her turda "köpük gibi" en sona gider.
- **Hız:** O(n²) - (Genellikle yavaştır, öğretim amaçlıdır).

### b. Selection Sort (Seçmeli Sıralama)

- **Mantık:** Listenin tamamını tarar, en küçük elemanı bulur ve en başa koyar. Sonra kalan kısımdan en küçüğü bulup ikinci sıraya koyar.
- **Hız:** O(n²) - (Yavaştır).

### c. Insertion Sort (Eklemeli Sıralama)

- **Mantık:** Elinizdeki oyun kartlarını dizer gibi çalışır. Sıradaki elemanı alır, geriye doğru gidip uygun boşluğa yerleştirir.
- **Hız:** O(n²) - (Küçük listelerde hızlıdır).

### d. Merge Sort (Birleştirmeli Sıralama)

- **Mantık (Böl ve Yönet):** Listeyi sürekli ikiye böler, tek eleman kalana kadar parçalar. Sonra bu parçaları sıralı bir şekilde birleştirerek (merge) yukarı çıkar.
- **Hız:** O(n log n) - (Büyük verilerde çok verimlidir).

### e. Quick Sort (Hızlı Sıralama)

- **Mantık:** Bir "Pivot" (referans) eleman seçer. Pivottan küçükleri sola, büyükleri sağa atar.
- **Hız:** Genelde O(n log n) - (Pratikte en hızlı çalışanlardan biridir).
