# Optymalizacja dyskretna - Maksymalny przepływ i minimalny koszt w sieciach przepływowych

## Opis projektu
Projekt inżynierski dedykowany implementacji, analizie porównawczej oraz badaniu złożoności obliczeniowej zaawansowanych algorytmów grafowych stosowanych do rozwiązywania problemów transportowych i przepływowych. Głównym celem projektu było zbadanie metod wyznaczania maksymalnego przepływu w sieci za pomocą **algorytmu Forda-Fulkersona** (w dwóch wariantach przeszukiwania grafu) oraz wyznaczanie przepływu o minimalnym koszcie przy użyciu **algorytmu Busackera-Gowena**.

Projekt zrealizowany w ramach przedmiotu *Optymalizacja dyskretna* na Politechnice Rzeszowskiej (Kierunek: Inżynieria i Analiza Danych).

## Technologie i narzędzia
* **Język programowania:** Python
* **Struktury danych:** Grafy skierowane, sieci rezydualne, macierze/listy sąsiedztwa
* **Algorytmy pomocnicze:** DFS (Depth-First Search), BFS (Breadth-First Search), algorytm Dijkstry

---

##  Zaimplementowane algorytmy

### 1. Algorytm Forda-Fulkersona (Maksymalny przepływ)
Algorytm wyznacza maksymalną pulę danych/towarów, jaką można przesłać od źródła ($s$) do ujścia ($t$) przez sieć o ograniczonych przepustowościach krawędzi. W projekcie zaimplementowano i porównano dwa podejścia do szukania ścieżek powiększających:
* **Wariant DFS (Depth-First Search):** Przeszukiwanie w głąb. Często znajduje dłuższe ścieżki, a jego wydajność jest silnie zależna od wartości przepustowości krawędzi.
* **Wariant BFS (Breadth-First Search / algorytm Edmondsa-Karpa):** Przeszukiwanie w szerokość. Gwarantuje znalezienie najkrótszej ścieżki pod względem liczby krawędzi, dzięki czemu złożoność obliczeniowa jest niezależna od wartości przepustowości sieci.

### 2. Algorytm Busackera-Gowena (Minimalny koszt)
Rozszerzenie problemu przepływowego o kryterium ekonomiczne. Każda krawędź w sieci prócz przepustowości posiada określony koszt przesłania jednostki przepływu. Algorytm iteracyjnie wykorzystuje zmodyfikowany **algorytm Dijkstry** do wyszukiwania najtańszych ścieżek rezydualnych, dopóki nie zostanie osiągnięta pożądana wartość przepływu docelowego, optymalizując całkowity koszt operacji.

---

##  Zakres analizy i eksperymentów
* **Obliczenia ręczne:** Przeprowadzenie pełnego, krokowego śledzenia matematycznego działania obu algorytmów na przykładowych grafach testowych w celu weryfikacji poprawności logicznej implementacji.
* **Analiza złożoności:** Matematyczne porównanie efektywności struktur DFS i BFS w procesie wyznaczania sieci rezydualnych i korygowania przepływów wstecznych.

---

## 📁 Zawartość repozytorium

* `fordfulkerson.pdf` — Pełna dokumentacja projektowa zawierająca opisy matematyczne, rysunki grafów, przykłady obliczeniowe krok po kroku oraz szczegółową analizę złożoności obliczeniowej.

---
