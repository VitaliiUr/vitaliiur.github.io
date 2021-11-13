#### Symulacja procesu Markova

<!-- ![dsfsf](/teaching/2021_metody_statystyczne/diagram.png) -->

<div class="row mt-3" style="margin-bottom: 18px">
    <div class="col-sm mt-3 mt-md-0" align='center'>
        <img class="img-fluid rounded z-depth-1" src="{{ site.baseurl }}/teaching/2021_metody_statystyczne/diagram.png" width="400">
    </div>
</div>


<!-- Mamy process Markova z diagramem powyżej.  -->
Mamy 2 użytkownika i każdy z nich może być zalogowanym lub niezalogowany do komputera, 
niezależnie od drugiego.
Prawdopodobieństwo zalogowania dla użytkownika jest $$P_{zalogowania} = 0.2$$, wylogowania - 
$$P_{wylogowania} = 0.5$$. W takim przypadku mamy trzy możliwych stany:
zalogowanę są 0, 1 lub 2 użytkowniki. Na diagramie powyżej x - ilość zalogowanych
użytkowników i strzałki określają przejście z jednego stanu do innego 
z odpowiednim prawdopodobieństwem. 
W danym przypadku macierz przejść:

$$
\begin{equation*}
P = 
\begin{pmatrix}
    0.64 & 0.32 &  0.04\\
    0.4  & 0.5  & 0.1 \\
0.25 & 0.5  & 0.25
\end{pmatrix}
\end{equation*}
$$

- **Problem A**
  1. Policzyć $$P^N$$ dla dużych N
  2. Kryterium zbieżności: $$ \mid P^n - P^{n-1}\mid < \epsilon$$
  3. $$\epsilon = 10^{-5}$$ lub inne wartości
  4. Narysować wykres $$[P^n]_{ij}$$ w zależności od n
  5. Porównanie z wartościami $$\pi_j$$  na wykresie

- **Problem B**  
  1. Symulacja procesu Markova
     - Zaczynamy z wybranego węzła $$x = \{0,1, 2\}$$
     - Losowanie kolejnego węzła zgonie z $$P$$
     - Przejście do losowanego węzła
     - Powtarzamy  
  2. Losujemy $$N=10^4$$ przejść
  3. Obliczenie $$\pi_i^{exp} = \frac{N_i}{N}$$,  
      $$N_i$$ - ile razy odwiędzone $$x=i\quad(0,1,2)$$
  4. Porównanie z $$P^N$$
  5. Start z różnych węzłów

- **Problem C**  
  100 użytkowników &#8594; trudno jest obliczyć macierz prawdopodobieństw  
  $$x=0,1,2,...,100$$;  
  $$P_{logowania} = 0.2$$, $$P_{wylogowania} = 0.5$$  
  1. Wykonujemy symulację trajektorii (zaczynamy z dowolnego węzła $$x$$)
  2. Ile wynosi $$\pi^{exp}_i$$ dla $$i=0,1,\cdots,100$$?
  3. Wykresy zbieżności $$\pi^{exp}_i = \frac{N_i}{N}$$ jako zależność od $$N$$ 
        dla kilku $$i$$ (np dla pięciu największych wartości $$\pi$$)
  4. Wykres końcowych wartości dla wszystkich $$\pi^{exp}_i$$
   
- **Problem D**  
   Podobna symulacja jak w C, tylko 
     1. $$P_{logowania} = 0.2$$;
     2. $$P_{wylogowania} = 1 - (0.008 \cdot x+0.1)$$ - dla węzła $$x $$;
