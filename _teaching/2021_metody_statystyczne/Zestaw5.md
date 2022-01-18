#### Symulacja współdzielonego serweru

Zaimplementowanie symulacji procesu kolejkowego z jednym współdzielonym serwerem.

Zadania wpływają w tempie $$\lambda_A$$ i wykonane są
w tempie $$\lambda_D$$.

Wszystkie zadania z kolejki są wykonywane jednocześnie. Obliczalna 
moc serwera jest dzielona przez wszystkie wykonywane zadania.

Na przykład mamy 2 zadania do wykonania i łosowane czasy wykonań są $$t_1$$
i $$t_2$$($$t_1 < t_2$$). 
Wtedy one bedą wykonywanę jednocześnie ale czas wykonania będzie zmieniony.
Pierwsze zadania zostanie wykonane za czas $$2 t_1$$
(wtedy cały czas na serwerze było 2 zadania).
Za ten samy czas drugie zadanie było wykonane tylko częściowo, i ta wykonana częsć
jest  $$\frac{t_1}{t_2}$$.

Potem na serwerze się zostanie tylko jedno zadanie i ono
zacznie być wykonywanym szybciej.
To znaczy, że zostało się do obliczenia $$1 - \frac{t_1}{t_2}$$. To już będzie obliczane
z pełną mocą i zostanie obliczone za $$t_2(1 - \frac{t_1}{t_2}) = t_2 - {t_1$$.


Czyli dla pierwszego zadania całkowity czas obliczenia będzie $$2 t_1$$, a
 dla drugiego zadania całkowity czas obliczenia będzie $$t_2 - t_1 + 2 t_1 = t_2 + t_1$$.

Podobnie można rozglądać przypadki dla dowolnej iłości wykonywanych zadań.


- Zrobić symulacje 100 zadań dla $$\lambda_A = 6$$, $$\lambda_D = 5$$
- Zrobić wykresy:
    1. Liczba zadań w systemie w zależności od czasu.
    2. Czas oczekiwania na wykonanie w zależności od czasu.
    3. Liczba wykonanych w zależności od czasu.
- Porównać z wykresami dla zwykłego (nie współdzielonego) serweru
