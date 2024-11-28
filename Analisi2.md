# Analisi Matematica 2

# Probabilità

## Unità 1 - Sequenze e spartizioni

### Combinatoria

Contare il numero di elementi di un insieme attraverso delle tecniche più veloci dell'enumerazione. Per esempio, il numero di anagrammi di una parola, numero di sequenze che contengono una data parola, numeri di mani di 5 carte tra 52, e via dicendo. 

### Cardinalità

La **cardinalità** di un insieme finito $X$ è il numero dei suoi elementi distinti, e si indica con $|X|$.

**Proposizione** -> Siano A, B due insiemi finiti. Allora:
1. $|A \cap B| = \empty$, allora $|A \cup B| = |A| + |B|$
2. $|A \cup B| = |A| + |B| - |A \cap B|$
3. $|A \times B| = |A| \times |B|$
4. Se $X$ è finito, allora $|A^C| = |X| - |A|$

### Biiezione

Due insiemi finiti hanno la stessa cardinalità se e solo se sono in corrispondenza binunivoca.
Una funzione $f: A \rightarrow B$ è detta **biiezione** se è sia iniettiva che suriettiva. In tal caso, si dice che $A$ e $B$ sono **equipotenti** e si scrive $|A| = |B|$.

### Sequenze

Siano $n, k \in \mathbb{N}$, Diciamo k-sequenza di $I_n$ una k-upla ordinata di elementi di $I_n$, ovvero un elemento del prodotto cartesiano $I_n^k$. La sequenza è detta senza ripetizione se i suoi termini sono distinti.

### Permutazioni

Data una qualunque k-sequenza $(a_1, ..., a_k)$ di un insieme X, diciamo permutazione di $(a_1, ..., a_k)$ una k-sequenza $(b_1, ..., b_k)$ tale che $(b_1, ..., b_k)$ = $(a_1, ..., a_k)$.

Una permutazione di un insieme finito $X$ è una biiezione da $X$ in se stesso. Il numero di permutazioni di un insieme finito $X$ di cardinalità $n$ è $n! = n \times (n-1) \times \ldots \times 2 \times 1$.

### Spartizioni

Diciamo n-spartizione di $I_k$ una n-upla ordinata (C1, ..., Cn) di sottoinsiemi di $I_k$ tali che $C1 \cup \ldots \cup Cn = I_k$ e $Ci \cap Cj = \empty$ per ogni $i \neq j$. Gli insiemi $C1, ..., Cn$ sono detti parti della spartizione. Una n-spartizione di $I_k$ è detta senza ripetizione se le sue parti sono distinte. Un elenco è una n-spartizione di $I_k$ se e solo se è una n-sequenza di $I_k$.

Per esempio: 
Si distribuiscono le 10 carte di picche a 4 persone A, B, C, D. A: 3, 7; B: 1, 2, 4; C: null; D = le altre.
$$ ((3,7), (1,2,4),(\empty), (5,6,8,9,10)) $$
Per rappresentare in modo migliore, si potrebbe fare nel seguente modo: 

### Insiemi e Sottoinsiemi

Diciamo k-sottoinsieme di $I_n$ un sottoinsieme formato da k elementi distinti in $I_n$. Indichiamo con C(n,k) il numero di k-sottoinsiemi di $I_n$. Si ha che $C(n,k) = \frac{n!}{k!(n-k)!}$. L'ordine degli elementi di un sottoinsieme non conta.
Esempio: distribuiamo una mano di 5 carte da un mazzo di 52 carte. L'esito dell'esperimento può essere descritto dal sottoinsieme di 5 carte prescelte tra le 52. Il numero di mani possibili è $C(52,5)$.

### Principio di moltiplicazione

Supponiamo che gli elementi di un insieme $X$ possano essere individuati in una procedura in $n$ fasi, dove:
- la prima fase ha $m_1$ esiti possibili
- la seconda fase ha $m_2$ esiti possibili
- ...
- la n-esima fase ha $m_n$ esiti possibili
- $!\cdot!$ elemento costruito determina univocamente gli esiti delle $n$ fasi

allora il numero totale di esiti possibili è $|X|=m_1 \times m_2 \times \ldots \times m_n$. C'è però una verifica importante da fare. Se due esiti sono tali che l'uno non influenza l'altro, allora il numero di esiti possibili è il prodotto dei due numeri di esiti possibili.

---
## Unità 2 - Definizione di probabilità

Prendiamo un esempio... Dado, forse truccato. Qual'è la probabilità di $E:= \text{ esce il }6$?
Idea: fare n lanci, calcolare la frequenza dei successi
$$P_n(E)= \frac{\text{numero di volte che si realizza E su n lanci}}{n}$$
$$ P(E) = \lim_{n \to \infty} \frac{f_n(E)}{n} $$

Abbiamo la possibilità di usare l'assiomatica di probabilità.

### Assiomatica di probabilità
Sia $\Omega$ un insieme arbitrario, diciamo funzione di probabilità su $\Omega$ una funzione $P: \mathcal{P}(\Omega) \rightarrow [0,1], A \to P(A)$ che soddisfa le seguenti proprietà:
- $0 \leq P(A) \leq 1$
- $P(\emptyset) = 0, P(\Omega) = 1$
- se $A_1, A_2, ...$ sono insiemi a due a due disgiunti, allora $P(A_1 \cup A_2 \cup ...) = P(A_1) + P(A_2) + ...$
  - allora $P(U_{i=1}^{\infty} A_i) = \sum_{i=1}^{\infty} P(A_i):= \lim_{n \to + \infty}(P(A_1)+\cdots+P(A_n))$

Una probabilità su $\Omega$ è quindi per noi una probabilità definita su **tutti** i sottoinsiemi di $\Omega$. In testi più avanzati si richiede solo su una famiglia di sottoinsiemi di $\Omega$.

### Proprietà delle funzioni di probabilità

- Se $A_1, \cdots, A_n \subseteq \Omega$ sono a due a due disgiunti allora
$$ P(A_1 \cup \cdots \cup A_n) = P(A_1) + \cdots + P(A_n) $$
- Se $E \subseteq F \subseteq \Omega$ allora $P(E) \leq P(F)$

### Principio di Inclusione / Esclusione

Notazione Ross: $AB:= A\cap B$. 

Siano $A_1, A_2, A_3 \subseteq \Omega$. Allora
- $P(A_1 \cup A_2) = P(A_1) + P(A_2) - P(A_1 \cap A_2)$
- $P(A_1 \cup A_2 \cup A_3) = \sum^3_{i=1}P(A_i) - \sum_{1 \leq i < j \leq 3} P(A_iA_j) + P(A_1 \cap A_2 \cap A_3)$

### Cardinalità

Due insiemi infiniti hanno la stessa cardinalità se essi possono essere messi in corrispondenza biunivoca. Gli insiemi in corrispondenza biunivoca $\mathbb{N}$ sono detti **numerabili**, gli elementi si possono elencare con una successione.

> Un insieme $X$ è numerabile se $X = \{ x_1, x_2, x_3, \ldots \}$ cioè $n \in \mathbb{N} \rarr x_n\in X$. Si dice che $X,Y$ hanno la stessa cardinalità se esiste una biiezione tra $X$ e $Y$.
> 
> $\mathbb{R}$ non è numerabile. Si dice che la cardinalità di $\mathbb{R}$ è la cardinalità del continuo.

I numeri razionali $\mathbb{Q}$ sono numerabili, mentre i numeri reali $\mathbb{R}$ non lo sono.

$$
\mathbb{Q} \text{ è numerabile}
$$
$$
\begin{align*}
\frac{1}{1} & \frac{2}{1} & \frac{3}{1} & \cdots \\
\frac{1}{2} & \frac{2}{2} & \frac{3}{2} & \cdots \\
\frac{1}{3} & \frac{2}{3} & \frac{3}{3} & \cdots \\
\vdots & \vdots & \vdots & \ddots
\end{align*}
$$

### Probabilità condizionata

Sia $\Omega$ uno spazio campionario, $P$ una funzione di probabilità su $\Omega, E, F \subseteq \Omega \text{ con } P(F)\not ={0}$, diciamo probabilità condizionata di $E$ dato $F$ il numero $P(E|F) = \frac{P(E\cap F)}{P(F)} =\frac{P(EF)}{P(F)}$.

Sia $P$ una funzione di probabilità su $\omega, F \subseteq \Omega$ con $P(F) \not = 0$. La funzione 

$$E\subset F \rarr P(E \backslash F)$$

è funzione di probabilità su F. Analogamente $E \subset \Omega \rarr P(E|F)$ è funzione di probabilità su $\Omega$.

**Lingauggio:** Si è realizzato F o Sapendo che si è realizzato F... Calcolare la probabilità che... $\rarr$ usare $P(\cdot|F)$

### Formula d'inversione

Sia $F \subseteq \Omega$ con $P$ una funzione di probabilità su $\Omega$ con $P(F) > 0$. Allora per ogni $E \subseteq \Omega$ si ha che $P(F|E) = \frac{P(E|F)P(F)}{P(E)}$

Fissati $P(E),P(F)$ se $P(E(F))$ cresce, allora $P(F|E)$ cresce.