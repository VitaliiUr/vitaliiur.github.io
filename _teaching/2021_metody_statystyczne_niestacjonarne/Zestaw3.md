#### Symulacja procesu Kolejkowego

<div class="row mt-3" style="margin-bottom: 18px">
    <div class="col-sm mt-3 mt-md-0" align='center'>
        <img class="img-fluid rounded z-depth-1" src="{{ site.baseurl }}/teaching/2021_metody_statystyczne/server.png" width="400">
    </div>
</div>

Zaimplementowanie symulacji procesu kolejkowego.

- **Problem A**  
    Symulacja procesu kolejkowego dla 10 zadań dla $$\lambda_A = 1/30$$, $$\lambda_S = 1/20$$.
    Zrobić wykresy:
    1. Liczba zadań w kolejce w zależności od czasu.
    2. Czas oczekiwania na wykonanie w zależności od czasu.
    3. Liczba wykonanych w zależności od czasu.
    4. Powtórzyć dla $$\lambda_A = 1/30$$, $$\lambda_S = 1/50$$

- **Problem B**  
    1. Sprawdzić prawo Little'a: 
    $$E(R) \lambda_A = E(n)$$  
    E(R) - średni czas spędzony przez zadanie w systemie ($$R_i = D_i - A_i$$)  
    E(n) - średnia ilość zadań w kolejcę  
    2. $$\lambda_A = 1/30$$, $$\lambda_S = 1/20$$\\
    3. Symulacja dla 1000 zadań
