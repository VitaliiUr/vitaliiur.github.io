#### Symulacja procesu kolejkowego (kontynuacja)

Zaimplementowanie symulacji procesu kolejkowego z dwoma serwerami.
Zadania wpływają w tempie $$\lambda_A$$ i wykonane są na pierwszym serwerze
w tempie $$\lambda_D^1$$ i na drugim w tempie $$\lambda_D^2$$


- **Problem A**  
    Symulacja **n=100** zadań dla dwoch konsekwentnych serwerów.  
    $$\lambda_A = 10$$, $$\lambda_D^1 = 10$$, $$\lambda_D^2 = 6$$  
    Zrobić wykresy:
    1. Liczba zadań w kolejce w zależności od czasu.
    2. Czas oczekiwania na wykonanie w zależności od czasu.
    3. Liczba wykonanych w zależności od czasu.
    4. Powtórzyć dla przypadku kiedy zadania na drugim serwerze są wykonane za stały czas równy $$\frac{1}{\lambda_D^2}$$

<div class="row mt-3" style="margin-bottom: 18px">
    <div class="col-sm mt-3 mt-md-0" align='center'>
        <img class="img-fluid rounded z-depth-1" src="{{ site.baseurl }}/teaching/2021_metody_statystyczne/server2.png" width="600">
    </div>
</div>



- **Problem B**  
    Tak samo jak w **A** tylko serwery są paralelne (jeżeli serwer jest zajęty, zadanie idzie do innego)

<div class="row mt-3" style="margin-bottom: 18px">
    <div class="col-sm mt-3 mt-md-0" align='center'>
        <img class="img-fluid rounded z-depth-1" src="{{ site.baseurl }}/teaching/2021_metody_statystyczne/server3.png" width="600">
    </div>
</div>