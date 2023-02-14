#### Symulacja określania liczebności populacji [metodą kolejnych złowień][wiki_polska]

<div class="row mt-3" style="margin-bottom: 18px">
    <div class="col-sm mt-3 mt-md-0" align='center'>
        <img class="img-fluid rounded z-depth-1" src="{{ site.baseurl }}/teaching/2022_metody_statystyczne_niestacjonarne/Iterated_mark_and_recapture_Bayesian_inference.gif" width="600">
    </div>
</div>

<!-- Zaimplementowanie symulacji określania liczebności populacji [metodą kolejnych złowień][wiki_polska]. -->
Mamy populacje rozmiaru **N** z której przez serie pomiarów łowimy 
pewną ilość osobników, oznakujemy ich i uwalniamy. Znając całkowitą ilość oznakowanych osób i porównując ją
z liczbą ponownie złowionych - można oszacować rozmiar populacji.

Używamy dla tego [Twierdzenie Bayesa](https://pl.wikipedia.org/wiki/Twierdzenie_Bayesa), czyli prawdopodobieństwo 
tego że rozmiar populacji jest równy do $N_j$:

$$P(N_j|m, t, M) \propto \frac{P(m|N_j, t, M) P(N_j)}{\sum_i P(m|N_i, t, M) P(N_i)},$$

gdzie **N_j** - rozmiar populacji, **M** - całkowitą ilość oznakowanych osób, **t** - ilość złowionych osób w danym pomiarze, 
**m** - ilość ponownie złowionych w danym pomiarze.


* $P(N_j)$ - *prior* - rokład prawdopodobieństwa przed pomiarem.   Przed pierwszym pomiarem zakładamy że wierzymy w to że rozmiar populacji jest wartość losowa w pewnym przedziale $[a, b]$
i każda wartość z tego przedziału ma to samo prawdopodobieństwo. Czyli  $P(N)$ jest  z rozkładu jednorodnego
i $P(N_j) = \frac{1}{b-a}$, dla wszystkich $N_j \in [a, b]$. W kolejnych pomiarach bierzemy $P(N)$ zako posterior z poprzedniego pomiaru.  

* $P(m\mid N_j, t, M)$ - *likelihood* - prawdopodobieństwo ponownie złowić **m** osób jeżeli rozmiar populacji jest **N**.  

*  $P(N_j \mid m, t, M)$ - *posterior* - szukany rozkład prawdopodobieństwa że rozmiar populacji jest **N**.  

*  $\sum_i P(m \mid N_i, t, M) P(N_i)$ - używany dla normalizacji.




Wartość $P(m \mid N_j, t, M)$ jest z rozkładu [hipergeometrycznego][hipergeometryczny_wiki]:  

$$P(m|N_j, t, M) = \frac{\binom{M}{m}\binom{N_j-M}{t-m}}{\binom{N_j}{t}},$$  

gdzie [Symbol Newtona][newton_wiki]:  
$$\binom{n}{k} \equiv \frac{n!}{k!(n-k)!}$$

*Zakładamy że rozmiar populacji jest stały i każda osoba ma takie same prawdopodobieństwo zostać złowioną.*

- **Problem A**  
    Sprawdzić że jeżeli przy kolejnym pomiarze złowiliśmy **t** osobników, to
    liczba ponownie złowionych osobników **m** jest zmienna z rozkładu hipergeometrycznego.
    Zakładamy że znamy wartości **N** (rozmiar populacji) i **M** (liczba złowionych poprzednio osób).
    1. Zasymulować łosowanie **t** osobników z **N** populacji. Wielokrotnie powtarzając takie losowanie (wartość **M** jest stała, czyli złowione osoby nie dodajemy do listy), dostać rozkład prawdopodobieństwa dla wartości **m**.  
    N = 50, M = 20, t = 12  
    2. Narysować histogram wygenerowanego rozkładu i porównać z teoretycznym.  


- **Problem B**
  1. Zrobić symulację procesu metody kolejnych złowień.
  2. N = 1000.
  3. Zakładamy że rozmiar populacji jest w przedziale [0, 2000].
  4. Liczba złowionych osób **t** dla każdego pomiaru jest losowana z rozkładu jednorodnego na przedziale $[40, 60]$.
  5. Zrobić symulację **10** pomiarów.
  6. Narysować wykres rozkładu prawdopodobieństwa rozmiaru populacji po każdym pomiarze. 

- **Problem C**
  1. Dla wyników z **Problemu B** zrobić jeszce 10 pomiarów.
  2. Po każdym pomiarze oszacować rozmiar populacji dwoma metodami:
     1. Znaleźć rozmiar który ma maksymalną wartość prawdopodobieństwa;
     2. Obliczyć wartość oczekiwaną: $(\bar{X}) = \sum_i P(X_i)*X_i$
  3. Narysować wykres oszacowanych wartości w zależności od numeru pomiaru.
  4. Narysować takie same wykresy ale na osi poziomowej będzie wartość **M** (całkowitą ilość oznakowanych osób w danym pomiarze).


[wiki_polska]: https://pl.wikipedia.org/wiki/Metoda_wielokrotnych_z%C5%82owie%C5%84 "Metoda wielokrotnych złowień"
[hipergeometryczny_wiki]: https://pl.wikipedia.org/wiki/Rozk%C5%82ad_hipergeometryczny "Rozkłąd hipergeometryczny"
[newton_wiki]: https://pl.wikipedia.org/wiki/Symbol_Newtona "Symbol Newtona"