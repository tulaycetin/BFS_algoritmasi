# BFS_algoritmasi



<img width="298" height="181" alt="Ekran görüntüsü 2025-10-17 015014" src="https://github.com/user-attachments/assets/78cf4226-8bd8-4cee-b831-8f29c4aede78" />

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
