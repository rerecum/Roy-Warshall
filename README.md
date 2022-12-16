# Roy-Warshall
Opis algorytmu Roya-Warshalla, przykład, dzialanie

Algorytm Roya-Warshalla jest algorytmem do obliczania odległości między wszystkimi parami wierzchołków w grafie skierowanym z wagami. Algorytm ten został zaproponowany przez S. Roya i N. Warshalla w 1962 roku i jest implementacją algorytmu Floyda-Warshalla.

Algorytm działa poprzez iteracyjne ulepszanie odległości między wierzchołkami poprzez dodawanie do grafu pośredników (tzw. "przejść pośrednich"). W każdym kroku algorytmu sprawdzane są wszystkie możliwe trasy między każdą parą wierzchołków przez pośredników i wybierana jest najkrótsza z nich. Dzięki temu możliwe jest znalezienie najkrótszych odległości między wszystkimi parami wierzchołków w grafie.


Przykład:

Rozważmy graf skierowany z wagami, w którym mamy cztery wierzchołki oznaczone literami A, B, C i D. Wierzchołki A i B są połączone krawędzią o wadze 2, wierzchołki B i C są połączone krawędzią o wadze 3, a wierzchołki C i D są połączone krawędzią o wadze 1.

Aby obliczyć odległości między wszystkimi parami wierzchołków za pomocą algorytmu Roya-Warshalla, należy przejść następujące kroki:

Na początek ustawiamy odległości między każdą parą wierzchołków na nieskończoność, z wyjątkiem odległości między wierzchołkami, które są bezpośrednio połączone krawędzią. W naszym przypadku tabela odległości wygląda następująco:
| A | B | C | D
---|---|---|---|---
A | 0 | 2 | ∞ | ∞
B | ∞ | 0 | 3 |


Upatologicznienie opisu działania:
Jest stworzona macierz, która ma jakieś punkty np. tablica dwuwymiarowa 5x5. Chcemy się dowiedzieć jaką trasę musimy odbyć żeby np. z punktu x:1, y:1 dojść do punktu x:3, y:5. Musimy więc przejść dwa razy w prawo oraz 4 razy w górę. Na odbycie tej trasy istnieje masa różnych tras, a alogrytm roya-warshalla powoduje znalezienie jak najlepszej (czyt. najszybszej) trasy do punktu, do którego dążymy.
