#### Process Poissona
  $$t_i$$ - czas pomiędzy zdarzeniami $$(i-1)$$ i $$(i)$$,  
  $$i = 1,2,...$$, $$\qquad t_0=0$$  
  $$t_i$$ jest losowane z rozkładu wykładniczego, $$f(t) = \lambda e^{-\lambda t}$$  
  - losujemy $$t_i$$ metodą odwróconej dystrybuanty
  - $$t_i = \frac{- \ln (n_i)}{\lambda}$$;
  - $$n_i$$ losowane z rozkładu jednorodnego na przedziale (0,1)  
  
  $$N(t)$$ - ilość zdarzeń, które wystąpiły do chwili $$t$$, $$N(0)=0$$  
  Taki proces nazywa się [procesem Poissona][poisson_wiki] o intensywności $$\lambda$$  
  $$N(t)$$ ma rozkład Poissona $$P (N(t)=k) = \frac{(\lambda t)^k}{k!}e^{-\lambda t}$$, z parametrem $$\lambda \cdot t$$ 

- **Problem A**  
  Symulacja procesu Poissona
  $$\lambda = 1$$  
  $$t = 1,10,20,90$$
  1. Zaimplementować symulację pojawienia zdarzeń
  2. Dla każdej wartości t:
    - otrzymać rozkład prawdopodobieństwa ilości zdarzeń
    - porównać z rozkłądem Poissona z parametrem $$\lambda \cdot t$$ 
    - sprawdzić że wartość średnia jest $$\lambda \cdot t$$

- **Problem B**  
  Mamy symulację zdarzeń jak w E  
  $$\lambda = 1$$; $$t = 1,10,20,90$$  
  Każde zdarzenie może należeć do jednej z trzech grup: 1,2,3  
  Należność do jednej z grup jest losowane i prawdopodobieństwa 
  należności do grup: $$p_1 = 0.2$$, $$p_2 = 0.5$$, $$p_3 = 0.3$$ ($$p_1+p_2+p_3=1$$)
  1. Sprawdzić że rozkład prawdopodobieństwa zdarzeń grupy $$i$$ 
  jest rozkładem Poissona z parametrem $$\lambda \cdot t \cdot p_i$$
  2. Sprawdzić że wartość średnia dla takiego rozkładu jest $$\lambda \cdot t \cdot p_i$$


[poisson_wiki]: https://pl.wikipedia.org/wiki/Proces_Poissona "Process Poissona"