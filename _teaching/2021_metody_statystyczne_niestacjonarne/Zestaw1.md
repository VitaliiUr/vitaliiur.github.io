
#### Generator liczb losowych

- **Problem A1**
  1. Implementacja generatora liczb losowych z
    [rozkładu normalnego][normalny_wiki] 
    $$N(0,1)$$ metodą polarną
  2. Narysowanie histogramu i porównanie ze wzorem analitycznym
  3. Obliczyć eksperymentalne wartości średniej oraz wariancji

- **Problem A2**
  1. Implementacja generatora liczb losowych z [rozkładu Cauchy'ego][cauchy_wiki] $$C(y_0,\gamma)$$, metodą odwróconej dystrybuanty:
$$
\begin{equation}
  f(y) = \frac{1}{\pi\gamma\left[1+\left(\frac{y-y_0}{\gamma}\right)^2\right]}, \qquad y \in (-\infty, \infty)\nonumber
\end{equation}
$$
  1. Narysowanie histogramu i porównanie ze wzorem analitycznym
    dla różnych wartości $$y_0$$ i $$\gamma$$
  2. Obliczyć eksperymentalne wartości średniej oraz wariancji
  


### Ruina gracza
Ruina gracza dla 2 graczy: gracz **A** z kapitałem początkowym **a** i
gracz **B** z kapitałem początkowym **b**.
Po każdej rozgrywce wygrywający gracz otrzymuje jedną jednostkę kapitału od przegranego. Nie ma remisów.
$$p_A$$ - prawdopodobieństwo wygranej gracza **A** w jednej rozgrywce
(dla dwóch graczy $$p_B = 1- p_A$$).  

Dla każdego z problemów wyniki są pobierane z zaimplementowanej
symulacji gry(gier) ruiny gracza.  
**N** - parametr który wyznaćza ilość symulowanych gier, 
dla różnych zadań ten parametr może być różnym
(generalnie im więcej tym lepiej, może być wybrany tak,
żeby symulacją nie trwała za długo).

  - **Problem B**  
  **a** = 50, **b** = 50  
  Symulacja **N** gier z różnymi
  wartościami $$p_A$$. Dla każdej wartości obliczyć prawdopodobieństwo
  ruiny gracza **A**. 
  1. Wykres $$P_{ruiny}(p_A)$$ - zależności prawdopodobieństwa ruiny gracza A od 
    prawdopodobieństwa wygranej w jednej rozgrywce $$p_A$$
  2. Porównanie z wynikiem teoretycznym
  3. Spróbować dla różnych wartości **a** i **b**

- **Problem C**    
**a** + **b** = 100;  
$$p_A = \frac{1}{2}$$  
Symulacja **N** gier z różnymi
  wartościami **a**. Dla każdej wartości obliczyć prawdopodobieństwo
  ruiny gracza **A**. 
  1. Wykres $$P_{ruiny}(a)$$ - zależności prawdopodobieństwa ruiny gracza A od 
    początkowego kapitału a
  2. Porównanie z wynikiem teoretycznym
  3. Spróbować dla różnych wartości $$p_A$$

- **Problem D**    
**L** - liczba rozgrywek do ukończenia gry  
$$p_A = \frac{1}{2}, \frac{1}{5}, \frac{4}{5}$$;  
**a** = **b**=50  
Proponowana całkowita liczba gier **N** = 20000  
Symulacja **N** gier, dla każdej gry obliczyć ilość rozgrywek. 
  1.  Histogram prawdopodobieństwa P(L) - liczby rozgrywek do ukończenia gry
  2.  Wyliczyć średnią długość rozgrywki 

- **Problem E**  
**N** - wybrana wartość symulowanych gier  
Symulacja **N** gier z różnymi wartościami $$p_A$$.
Dla każdej wartości $$p_A$$ obliczyć maksymalną ilość rozgrywek.
  1. Wykres $$L_{max}(p_A)$$ - maksymalna długość rozgrywek $$L_{max}$$ przy **N** rozgrywkach jako zależność od wartości $$p_A$$

- **Problem F** 
**n** = 2,10,20,...,100  
**a** = **b** = 50  
$$p_A = \frac{1}{2}, \frac{1}{5}, \frac{4}{5}$$  
Symulacja **n** rozgrywek **N** razy.
  1. Histogram prawdopodobieństwa **P(M)** - że gracz **A** ma kapitał **M** po **n** rozgrywkach

- **Problem G**  
  Symulacja kilku gier (do 10)  
  spróbować dla różnych wartości $$p_A$$
  1. Wykres trajektorii **liczby wygranych**  jednego z graczy jako zależność od numera rozgrywki
  2. Wykres trajektorii **kapitału** jednego z graczy jako zależność od numera rozgrywki  


- **Problem H**
  Problemy B, C, D, H dla kilku, np. pięciu,  graczy.  
  Różne kombinacje wartości $$p_i$$ - prawdopodobieństw
  wygranej dla gracza numer $$i$$.  
  $$a_i$$ = 20 - kapitały początkowe gracze
  (lub spróbować inne wartości).
  *(jeden punkt za każdy problem)*

[normalny_wiki]: https://pl.wikipedia.org/wiki/Rozk%C5%82ad_normalny "Rozkład normalny"
[cauchy_wiki]: https://pl.wikipedia.org/wiki/Rozk%C5%82ad_Cauchy%E2%80%99ego "Rozkład Cauchy'ego"