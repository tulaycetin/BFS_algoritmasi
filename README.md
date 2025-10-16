**BFS (Breadth-First Search) – Genişlik Öncelikli Arama Algoritması**

---

### 🔹 **Tanım**

**BFS (Breadth-First Search)**, bir graf üzerinde arama veya gezme işlemi yapan temel bir algoritmadır.
Bir başlangıç noktasından başlayarak önce o noktaya komşu olan **tüm düğümleri (noktaları)** ziyaret eder, ardından bu komşuların komşularına geçer.
Yani, **grafı katman katman (seviye seviye)** dolaşır.

---

### 🔹 **Çalışma Mantığı**

BFS algoritması **kuyruk (queue)** veri yapısını kullanır.
Her adımda:

1. Başlangıç düğümünden başlanır ve ziyaret edilir.
2. Bu düğümün **komşuları kuyruğa eklenir**.
3. Kuyruğun başındaki düğüm alınır, işlenir ve onun komşuları kuyruğa eklenir.
4. Kuyruk boşalana kadar bu işlem devam eder.

---

### 🔹 **Algoritmanın Adımları**

Bir graf ( G = (V, E) ) ve başlangıç düğümü ( s ) olsun:

1. Tüm düğümler **ziyaret edilmemiş** olarak işaretlenir.
2. Başlangıç düğümü ( s ) **ziyaret edilmiş** olarak işaretlenir ve **kuyruğa eklenir**.
3. Kuyruk boşalana kadar:

   * Kuyruğun başındaki düğüm ( u ) alınır.
   * ( u )’nun **ziyaret edilmemiş tüm komşuları** ziyaret edilir ve kuyruğa eklenir.
4. Tüm düğümler ziyaret edilince algoritma sona erer.

---

### 🔹 **Zaman Karmaşıklığı**

* **O(V + E)**
  Burada

  * ( V ): Düğüm sayısı
  * ( E ): Kenar sayısı

Her düğüm ve kenar **en fazla bir kez işlenir**.

---

### 🔹 **Uygulama Alanları**

* En kısa yol bulma (özellikle ağırlıksız graflarda)
* Ağ veya sosyal bağlantı analizi
* Web tarayıcı indeksleme
* En kısa bağlantı veya minimum seviye arama problemleri
---

 ## Örnek 

<img width="298" height="181" alt="Ekran görüntüsü 2025-10-17 015014" src="https://github.com/user-attachments/assets/78cf4226-8bd8-4cee-b831-8f29c4aede78" />


---

| Adım | Kuyruk (Queue) | Ziyaret Edilenler               | Açıklama                       |
| ---- | -------------- | ------------------------------- | ------------------------------ |
| 1    | A              | A                               | Başlangıç düğümü               |
| 2    | B, C, D        | A, B, C, D                      | A’nın komşuları eklendi        |
| 3    | C, D, E, F     | A, B, C, D, E, F                | B’nin komşuları (E, F) eklendi |
| 4    | D, E, F        | A, B, C, D, E, F                | C’nin komşusu (F) zaten var    |
| 5    | E, F, G, H     | A, B, C, D, E, F, G, H          | D’nin komşuları (G, H) eklendi |
| 6    | F, G, H, H     | A, B, C, D, E, F, G, H          | E’nin komşusu (H) zaten var    |
| 7    | G, H, H        | ...                             | F’nin komşusu (H) zaten var    |
| 8    | H, H, I, J     | A, B, C, D, E, F, G, H, I, J    | H’nin komşuları (I, J) eklendi |
| 9    | H, I, J        | ...                             | G’nin komşusu (H) zaten var    |
| 10   | I, J, J        | ...                             | H’nin komşuları zaten var      |
| 11   | J, J, K        | A, B, C, D, E, F, G, H, I, J, K | I’nin komşusu (J) zaten var    |
| 12   | J, K           | ...                             | J’nin komşusu (K) eklendi      |
| 13   | K              | ...                             | K’nin komşusu yok              |
| ✅    | -              | A, B, C, D, E, F, G, H, I, J, K | Tüm düğümler ziyaret edildi    |
