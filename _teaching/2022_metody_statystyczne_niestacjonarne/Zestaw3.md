#### Symulacja procesu kolejkowego

<div class="row mt-3" style="margin-bottom: 18px">
    <div class="col-sm mt-3 mt-md-0" align='center'>
        <img class="img-fluid rounded z-depth-1" src="{{ site.baseurl }}/teaching/2022_metody_statystyczne_niestacjonarne/server.png" width="600">
    </div>
</div>

Zaimplementowanie symulacji procesu kolejkowego z jednym serwerem.

- **Problem A**  
    Symulacja procesu kolejkowego dla 10 zadań dla $$\lambda_A = 2$$, $$\lambda_D = 2.5$$.  
    Zrobić wykresy:
    1. Liczba zadań w kolejce w zależności od czasu.
    2. Czas oczekiwania na wykonanie w zależności od czasu.
    3. Liczba wykonanych w zależności od czasu.
    4. Powtórzyć dla $$\lambda_A = 2$$, $$\lambda_D = 1.5$$

- **Problem B**  
    1. Sprawdzić prawo Little'a: 
    $$E(R) \lambda_A = E(n)$$  
    E(R) - średni czas spędzony przez zadanie w systemie ($$R_i = D_i - A_i$$)  
    E(n) - średnia ilość zadań w kolejcę  
    2. $$\lambda_A = 2$$, $$\lambda_D = 3$$
    3. Symulacja dla 1000 zadań
    4. Sprawdzić również dla  $$\lambda_A = 2$$, $$\lambda_D = 5$$

- **Problem C**  
    1. Zaobserwować zatykanie systemu
    2. $$\lambda_A = 15$$, $$\lambda_D = 8$$
    3. **n=1000** zadań
    4. Wykresy jak w **A**
    5. Pomyśleć co mogą znaczyć następne wzory *(narysować wykresy i porównać z tymi które juz mamy)* :  
     $$
     \begin{eqnarray*}
        (\lambda_A - \lambda_D)t\\ 
        \frac{\lambda_A - \lambda_D}{\lambda_D}t
    \end{eqnarray*}
    $$  

- **Problem D** 
    Zrobić następne wykresy:  
    1. E(liczba zadań) w zależności od $$\lambda_A$$
    2. E(liczba zadań) w zależności od $$\lambda_D$$
    3. E(liczba zadań) w zależności od $$r = \frac{\lambda_A}{\lambda_D}$$
    4. ... to samo dla E(czas oczekiwania)
   
   E(x) - znaczy wartość oczekiwana

- **Problem E**  
   Zrobić graf jak w [poprzednim zestawie](#symulacja-procesu-markova)
   ale dla 3 użytkowników (dowolną metodą) 