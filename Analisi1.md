# Analisi 1
UNIPD | Giacomo Giorgi - Ingenieria Informatica | Prof. Elio Marconi
## Introduzione
L'analisi 1 è una branca della matematica che si occupa di studiare le funzioni di una variabile reale. In particolare, si occupa di studiare le proprietà delle funzioni, come la continuità, la derivabilità e l'integrazione. L'analisi 1 è un corso fondamentale per lo studio della matematica e di molte altre discipline scientifiche.

### Sommatorie
Una sommatoria è una notazione matematica che permette di rappresentare la somma di una sequenza di numeri. 
$$\sum_{i=1}^{n}x_i = x_1+x_2+...+x_n$$
La sommatoria è rappresentata da un simbolo di sommatoria, seguito da una espressione che specifica i termini della sequenza e da un indice che varia da un valore iniziale a un valore finale. La sommatoria può essere utilizzata per calcolare la somma di una sequenza di numeri, come ad esempio la somma dei primi n numeri naturali o la somma dei quadrati dei primi n numeri naturali.

In codice, una sommatoria può essere rappresentata con un ciclo `for`. Per esempio, in C#:
```csharp
for (int i = 1; i <= n; i++)
{
    sum += i;
}
```

Per le sommatorie, esistono due proprietà fondamentali:
1. **Distributiva:** $c\sum_{i=n_0}^{n_1} x_i= \sum_{i=n_0}^{n_1}cx_i$
2. **Associativa:** $\sum_{i=n_0}^{n_1} (x_i+y_i)= \sum_{i=n_0}^{n_1}x_i + \sum_{i=n_0}^{n_1}y_i$

### Principio d'induzione
Il pricipio d'induzione è un metodo di dimostrazione matematica che permette di dimostrare una proprietà per tutti i numeri naturali. Il principio d'induzione si basa su due passi:
1. **Base dell'induzione:** Dimostrare che la proprietà è vera per il primo numero naturale.
2. **Passo induttivo:** Dimostrare che se la proprietà è vera per un numero naturale n, allora è vera anche per n+1.

Il principio d'induzione è un metodo potente per dimostrare proprietà matematiche che dipendono da un parametro naturale. Esso è ampiamente utilizzato in matematica per dimostrare teoremi e proprietà di numeri naturali.

#### Esempio di principio d'induzione $\rarr$ Fattoriali
$$
\begin{align*}
n! &= \text{"n fattoriale"} = 
    \begin{cases} 
        1 & \text{se } n = 0 \\
        n \cdot (n-1)! & \text{se } n > 0
    \end{cases}
    \\
(n+1)! &= (n+1) \cdot n! \\
\end{align*}
$$
#### Dimostrazione

1. **Base dell'induzione:** Dimostriamo che la proprietà è vera per $n=0$:
2. **Passo induttivo:** Supponiamo che la proprietà sia vera per un numero naturale n. Dimostriamo che è vera anche per n+1.
3. **Conclusione:** Per il principio d'induzione, la proprietà è vera per tutti i numeri naturali.

### Maggioranti, minoranti, massimi, minimi estremi superiori e inferiori
- **Maggiorante:** Un numero $M$ è un maggiorante di un insieme $A$ se $x \leq M \space \forall x \in A$.
- **Minorante:** Un numero $m$ è un minorante di un insieme $A$ se $x \geq m \space \forall x \in A$.
- **Massimo:** Un numero $M$ è il massimo di un insieme $A$ se $M \in A$ e $M$ è un maggiorante di $A$.
- **Minimo:** Un numero $m$ è il minimo di un insieme $A$ se $m \in A$ e $m$ è un minorante di $A$.
- **Estremo superiore:** Sia $X \subseteq \R$ un sottoinsieme di numeri reali, se $X$ è limitato superiormente, allora chiameremo $y \subseteq \R$ l'estremo superiore di $X$ e scriveremo $sup(X)=y$ se:
    - $y$ è un maggiorante di $X$.
    - Se scegliamo un numero $z<y$ si ha che $z$ non è un maggiorante di $x$.
  
    Se X è un insieme illimitato superiormente, ossia non ammette alcun maggiorante, diremo per definizione che l'estremo di $X$ è $+\infty$.

- **Estremo inferiore:** Sia $X \subseteq \R$ un sottoinsieme di numeri reali, se $x$ è limitato inferiormente, allora chiameremo $y \in \R$ l'estremo inferiore di $X$ e scriveremo $sup(x)=y$ se:
    - $y$ è un maggiorante di $x$.
    - Se scegliamo un numero $z>y$ si ha che $z$ non è un maggiorante di $x$.
  
    Se X è un insieme illimitato superiormente, ossia non ammette alcun maggiorante, diremo per definizione che l'estremo di $X$ è $-\infty$.

Dato un insieme $X \subseteq \R$, esistono e sono _unici_ l'estremo inferiore e superiore di $X$.

#### Esempio di maggioranti e minoranti
Sia $X = \{x \in \R \mid x \leq 1\}$, allora:
- $M=1$ è un maggiorante di $X$.
- $m=-\infty$ è un minorante di $X$.
- $sup(X)=1$ è l'estremo superiore di $X$.
- $inf(X)=-\infty$ è l'estremo inferiore di $X$.
- $max(X)=1$ è il massimo di $X$.
- $min(X)=-\infty$ è il minimo di $X$.
  
#### Esempio di estremo superiore e inferiore
Sia $X = \{x \in \R \mid x < 1\}$, allora:
- $M=1$ è un maggiorante di $X$.
- $m=-\infty$ è un minorante di $X$.
- $sup(X)=1$ è l'estremo superiore di $X$.
- $inf(X)=-\infty$ è l'estremo inferiore di $X$.
- $max(X)$ non esiste.
- $min(X)=-\infty$ è il minimo di $X$.

### Potenze, radici, logaritmi
Le _potenze_ sono moltiplicazioni ripetute, definide mediante due numeri detti _base_ ed _esponente_.
Sia $\alpha \in \R$ e $p \in \Z$, allora:
$$
\begin{align*}
\alpha^p &= 
    \begin{cases} 
        1 & \text{se } \alpha = 0,\space p \neq 0 \\
        \alpha \cdot \alpha^{p-1} & \text{se } \alpha \neq 0,\space p > 0 \\
        \frac{1}{\alpha^{-p}} & \text{se } \alpha \neq 0,\space p < 0
    \end{cases}
\end{align*}
$$



## Limiti
### Definizione di limite
Il limite di una funzione è un concetto fondamentale dell'analisi matematica che descrive il comportamento di una funzione quando la variabile indipendente si avvicina a un certo valore. Il limite di una funzione f(x) per x che tende a un valore a è indicato con il simbolo $\lim_{x \to a} f(x)$ e si legge "il limite di f(x) per x che tende a a".

La definizione formale di limite è la seguente:
$$\lim_{x \to a} f(x) = L$$

### Teorema di unicità del limite
Se una funzione in un punto ha un limite finito, allora esso è unico.
Basta ricordare che ad ogni valore della X deve corrispondere uno e soltanto un valore della Y. Per assurdo, se $f(x)$ avesse nello stesso punto $x_0$ più di un limite, essa non sarebbe più una funzione e questo contraddice l'ipotesi del teorema.
### Permanenza del segno
Se una funzione in un punto $x_0 è dotatadi limite $l\neq0$, allora esiste almeno un intorno $I$ di $x_0$ taleche per tutti i punti di $I$ (escluso $x_0$) i valori della funzione hanno lo stesso segno del limite.
### Teorema del confronto (carabinieri)
Anche noto come teorema del confronto, il teorema dei Carabinieri serve a determinare il limite di una funzione basandosi sui limiti di altre due funzioni che "incastrano" la nostra funzione.

Siano $f,g,h$ funzioni definite in un intorno di $x_0$ e tali che $f(x)\leq g(x)\leq h(x)$ per ogni $x$ nell'intorno, se $\lim_{x\to x_0}f(x)=\lim_{x\to x_0}h(x)=L$, allora $\lim_{x\to x_0}g(x)=L$.