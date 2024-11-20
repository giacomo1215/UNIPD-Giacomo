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