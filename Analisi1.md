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
- **Estremo superiore:** Sia $X \subseteq \mathbb{R}$ un sottoinsieme di numeri reali, se $X$ è limitato superiormente, allora chiameremo $y \subseteq \mathbb{R}$ l'estremo superiore di $X$ e scriveremo $sup(X)=y$ se:
    - $y$ è un maggiorante di $X$.
    - Se scegliamo un numero $z<y$ si ha che $z$ non è un maggiorante di $x$.
  
    Se X è un insieme illimitato superiormente, ossia non ammette alcun maggiorante, diremo per definizione che l'estremo di $X$ è $+\infty$.

- **Estremo inferiore:** Sia $X \subseteq \mathbb{R}$ un sottoinsieme di numeri reali, se $x$ è limitato inferiormente, allora chiameremo $y \in \mathbb{R}$ l'estremo inferiore di $X$ e scriveremo $sup(x)=y$ se:
    - $y$ è un maggiorante di $x$.
    - Se scegliamo un numero $z>y$ si ha che $z$ non è un maggiorante di $x$.
  
    Se X è un insieme illimitato superiormente, ossia non ammette alcun maggiorante, diremo per definizione che l'estremo di $X$ è $-\infty$.

Dato un insieme $X \subseteq \mathbb{R}$, esistono e sono _unici_ l'estremo inferiore e superiore di $X$.

#### Esempio di maggioranti e minoranti

Sia $X = \{x \in \mathbb{R} \mid x \leq 1\}$, allora:
- $M=1$ è un maggiorante di $X$.
- $m=-\infty$ è un minorante di $X$.
- $sup(X)=1$ è l'estremo superiore di $X$.
- $inf(X)=-\infty$ è l'estremo inferiore di $X$.
- $max(X)=1$ è il massimo di $X$.
- $min(X)=-\infty$ è il minimo di $X$.
  
#### Esempio di estremo superiore e inferiore

Sia $X = \{x \in \mathbb{R} \mid x < 1\}$, allora:
- $M=1$ è un maggiorante di $X$.
- $m=-\infty$ è un minorante di $X$.
- $sup(X)=1$ è l'estremo superiore di $X$.
- $inf(X)=-\infty$ è l'estremo inferiore di $X$.
- $max(X)$ non esiste.
- $min(X)=-\infty$ è il minimo di $X$.

### Potenze, radici, logaritmi

Le _potenze_ sono moltiplicazioni ripetute, definide mediante due numeri detti _base_ ed _esponente_.
Sia $\alpha \in \mathbb{R}$ e $p \in \Z$, allora:
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
**Teorema:** Esistenza e unicità della radice n-esima di un numero reale positivo.`
Siano $y \in \mathbb{R},\space y \geq 0,\space n\in N \backslash \{0\}$ allora esiste un unico numero reale positivo $x$ tale che $r^n=y$. $r$ si dice "radice n-esima di y" e si scrive $r=\sqrt[n]{y}$.

#### Potenze razionali

Le potenze con esponente fratto vengono definite come radici dalla base della potenza, dove il numeratore dell'esponente è l'esponente della base e il denominatore è l'indice della radice.
$$
\begin{align*}
\alpha^{{p}/{q}} &:= 
\begin {cases}
\sqrt[q]{\alpha^p} = (a^p)^{(1/q)} & \text{ se } a\neq0,\text{ oppure }p\neq0\\
1 & \text{ se } a\neq0,\space p=0\\
0 & \text{ se } a=0,\space p\neq0\\
\end{cases}
\end{align*}
$$

#### Potenze reali

Sia $a\in\mathbb{R},\space a>0$ e $r\in\mathbb{R}$, allora definiamo $a^r$ come:
$$
\begin{align*}
&\text{Se }a>1 &\text{ allora }a^r = \sup\{a^p \mid p\in\mathbb{Q},\space p\leq r\}\\
&\text{Se }a=1 &\text{ allora }a^r = 1\\
&\text{Se }a\in(0,1) &\text{ allora }a^r = \frac{1}{a^{-r}}
\end{align*}
$$

#### Logaritmi

Il logaritmo è l'inverso della potenza, indicato generalmente con $\log_a(b)$. Sia $a>0,\space a\neq1$ e $x>0$, allora il logaritmo di $x$ in base $a$ è definito come:
$$
\begin{align*}
\log_a(x) &= y \iff a^y = x
\end{align*}
$$
Siano $a$ e $b$ due numeri reali, entrambi positivi e con $a\neq1$, definiamo il logaritmo in base $a$ di $b$ e scriviamo $\log_a(b)$ per indiare quel numero reale $x$ tale che $a^x=b$.
$$
c = 
\begin{cases}
\sup\{r\in\mathbb{R} : a^c\leq b\}\text{ se }a>1\\
\sup\{r\in\mathbb{R} : a^c\geq b\}\text{ se }a\in(0,1)
\end{cases}
$$

### Numeri Complessi

I numeri complessi costituiscono un insieme che estende l'insieme dei numeri reali ed in cui, a partire dalla definizione di unità immaginaria è possibile estrarre le radici ad indice pari di numeri negativi e risolvere le equazioni di secondo grado con discriminante negativo.
- $i$ è l'unità immaginaria, definita come $i^2=-1$.
- $\mathbb{C} = \{x+iy:x,y\in \mathbb{R}\}$ = "di fatto i numeri complessi sono una coppia di numeri reali".
- $z=x+iy$ è la forma algebrica di un numero complesso.
- $x$ è la parte reale di $z$ e si scrive $Re(z)$.
- $y$ è la parte immaginaria di $z$ e si scrive $Im(z)$.
- $z=x+iy$ è il coniugato di $z$ e si scrive $\overline{z}=x-iy$.
- $|z|=\sqrt{x^2+y^2}$ è il modulo di $z$.

    **Osservazione**
    
    $\text{Im}(z) = 0 \iff z = x \iff z \in \mathbb{R}\\$
    quindi $\mathbb{R} \subset \mathbb{C}, \mathbb{R}=\{z\in\mathbb{C}:\text{Im}(z)=0\}$

    Ossia, i numeri reali sono un sottoinsieme dei numeri complessi, in particolare i numeri reali sono i numeri complessi con parte immaginaria nulla.

Su $\mathbb{C}$ non è possibile introdurre una relazione d'ordine che lo renda un campo totalmente ordinato.

Siano $z_1 = x_1 + iy_1$ e $z_2 = x_2 + iy_2$ due numeri complessi, allora:

1. **Somma:** $z_1 + z_2 = (x_1 + x_2) + i(y_1 + y_2)$
2. **Prodotto:** $z_1 \cdot z_2 = (x_1x_2 - y_1y_2) + i(x_1y_2 + x_2y_1)$

    #### Teorema
    Con queste operazioni, $\mathbb{C}$ è un campo. Inoltre...
    1. l'elemento neutro è $0+0i$
    2. l'elemento unitario è $1+0i$
    3. dato $z=x+iy$, l'opposto è $-x-iy$, e lo chiameremo $-z$
    4. dato $z=x+iy$, l'inverso è $\frac{x}{x^2+y^2}-\frac{y}{x^2+y^2}i$, e lo chiameremo $z^{-1}$

Dato $z \in \mathbb{C}$, $z = x+yi \space (\text{con }x,y \in \mathbb{R})$, chiameremo **CONIUGATO** di $z$ il numero complesso $\overline{z} = x-yi$. In altre parole, il coniugato di un numero complesso è quel numero complesso tale che la parte immaginaria è opposta a quella del numero complesso originale.

#### Teorema Fondamentale dell'Algebra

Il teorema fondamentale dell'algebra stabilisce che un qualsiasi polinomio a coefficienti reali o complessi di grado $n\geq 1$ ammette almeno una radice complessa, da cui segue un qualsiasi polinomio a coefficienti reali o complessi di grado $n$ ammette sempre $n$ radici complesse, contate con la loro molteplicità.

**Teorema:** Ogni poliinomio a coefficienti complessi di grado maggiore o uguale a 1 ammette almeno una radice complessa. 

#### Piano di Gauss

Il piano di Gaussa è un piano cartesiano leggermente modificato: l'asse $x$ è chiamato l'**asse reale**, mentre l'asse $y$ è chiamato l'**asse immaginario**. Sull'asse reale riportiamo la parte reale del numero complesso, mentre nell'asse immaginario riportiamo la parte immaginaria. Quindi, al numero complesso $z = a+bi$ si associa il punto del piano di coordinate cartesiane $(a,b) = (Re(z),Im(z))$.

Se $z \in \mathbb{C}$, $z=x+yi$ con $x,y \in \mathbb{R}$, chiamiamo **modulo** di $z$ il numero **reale** $|z| = \sqrt{x^2+y^2}$.

#### Forma Trigonometrica

La forma trigonometrica di un numero complesso è una rappresentazione che consente di esprimere qualsiasi numero complesso mediante due valori detti **modulo** e **argomento**.

##### Notazione

- $\rho = |z|$
- $\theta = \arg(z) = \text{Argomento di }z$

Chiamiamo "argomento principale di z" l'unico valore per $\arg(z)$ nell'intervallo $(-\pi,\pi]$: lo indichiamo con $\text{Arg}(z)$. Notiamo che $\arg(z)$ non è univoco, ma $\text{Arg}(z)$ lo è.

Sia $z \in \mathbb{C}$ un numero complesso, $z$ è in forma trigonometrica se si presenta nella forma $z = \rho(\cos(\theta) + i\sin(\theta))$, dove $i$ indica l'unità immaginaria, $\rho$ è un numero reale non negativo e $\theta$ è un angolo in radianti tale da soddisfare le seguenti condizioni:
$$
-\pi < \theta \leq \pi \\
\text{oppure} \\
0 \leq \theta < 2\pi
$$

Teniamo a mente le seguenti proprietà di arg:
- $\arg(z_1z_2) = \arg(z_1) + \arg(z_2)$
- $\arg\left(\frac{z_1}{z_2}\right) = \arg(z_1) - \arg(z_2)$

#### Formula di De Moivre

La formula di De Moivre è una formula che permette di calcolare la potenza n-esima di un numero complesso in forma trigonometrica. Siano $z_1,z_2 \in \mathbb{C}\backslash\{0\}$, allora:
- $z_1z_2$ ha:
  - **modulo:** $|z_1z_2| = |z_1||z_2|$
  - **argomento:** $\arg(z_1z_2) = \arg(z_1) + \arg(z_2)$
- $\frac{z_1}{z_2}$ ha:
  - **modulo:** $\left|\frac{z_1}{z_2}\right| = \frac{|z_1|}{|z_2|}$
  - **argomento:** $\arg\left(\frac{z_1}{z_2}\right) = \arg(z_1) - \arg(z_2)$

#### Funzione Esponenziale

La forma esponenziale di un numero complesso è un tipo di rappresentazione che consente di esprimere un qualsiasi numer o complesso mediante due valori reali $r$ e $\theta$, detti rispettivamente modulo e argomento, nella forma seguente:
$$
z=e^{i\theta}, \space z \in \mathbb{C}
$$
dove $e$ è il numero di Eulero, $i$ è l'unità immaginaria, $\theta$ è un angolo in radianti e $z$ è un numero complesso. Per la formula di Eulero, possiamo scrivere $z = \cos(\theta) + i\sin(\theta)$.

##### Osservazioni

- $e^{i\theta}$ ha modulo 1 $\forall \theta \in \mathbb{R}$
- $f(\theta) = e^{i(\theta)}$ è limitata e periodica (per $\theta \in \mathbb{R}$)
- Dalla formula di Eulero deduciamo che:
  $$
  e^{-i\theta} = \cos(-\theta) + i \sin(-\theta) = \cos(\theta)-i \sin(\theta) = \bar{e^{i\theta}} \\
  \text{quindi}\\
  \cos \theta = \frac{e^{i\theta}+e^{-i\theta}}{2}, \sin \theta =  \frac{e^{i\theta}-e^{-i\theta}}{2i}\\
  $$

Dato $z \in \mathbb{C}$, $z=x+yi$ con $x,y \in \mathbb{R}$, denotiamo con $e^z$ il numero complesso $e^z=e^x(\cos(y)+i\sin(y))=\rho(\cos(\theta)+i\sin(\theta))$.

### Radici n-esime

Dato $\omega \in \mathbb{C}$, sia $n \in \mathbb{N} \backslash\{0\}$, vogliamo risolvere l'equazione $z^n = \omega$. Dal teorema fondamentale dell'algebra, ci sono n soluzioni (con moltiplicità).

##### Caso Interessante ($n \geq 2, \omega \not ={0}$)

Scriviamo $z$ e $\omega$ in forma esponenziale
$$
z = re^{i\theta}, \space \omega = \rho e^{i\phi} 
$$
L'equazione diventa $(\rho e^{i\theta})^n = \rho e^{i\phi} \iff \rho^ne^{in\theta} = re^{i\phi}$.  Dalla prima condizione otteniamo $\rho=r^{1/n}$, e dalla seconda condizione otteniamo $\theta_n = \frac{\phi}{n} + \frac{2 k \pi}{n}$ con $k \in \mathbb{Z}$. Quindi, $k=0, k=n$ danno $\theta_n = \theta_0 + 2\pi$ quindi sono lo stesso argomento, basta considereare $\theta_0, \theta_1,\theta_2,\dotsc,\theta_{n-1}$.
In conclusione, le radici n-esime di $\omega$ sono i numeri complessi con modulo $|\omega|^{1/n}$ e argomenti $\frac{\arg(\omega)}{n} + \frac{2 k \pi}{n}$ per $k = 0,1,2,\cdots,n-1$.

### Equazioni di 2° grado in $\mathbb{C}$
Dato $a,b,c \in \mathbb{C}$, consideriamo l'equazione $az^2+bz+c=0$ con $a \not = 0$ e $z \in \mathbb{C}$. La soluzione di questa equazione è data dalla formula risolutiva:
$$
z = \frac{-b \pm \sqrt{b^2-4ac}}{2a}
$$
In questo caso le soluzioni sono
$$
z_1=\frac{-b+\omega_1}{2a}, \space z_2=\frac{-b-\omega_2}{2a}
$$
dove $w_1$ e $w_2$ sono le radici quadrate di $\Delta = b^2-4ac \in \mathbb{C}$, cioè le due soluzioni in $\mathbb{C}$ di $\omega^2 = b^2-4ac$.

Da notare, quando $\Delta \in \mathbb{R}$ e $\Delta \geq 0$, allora $\omega_1, \omega_2 = \pm \sqrt{b^2-4ac}$.

## Funzioni


## Limiti

### Definizione di limite

Il limite di una funzione è un concetto fondamentale dell'analisi matematica che descrive il comportamento di una funzione quando la variabile indipendente si avvicina a un certo valore. Il limite di una funzione f(x) per x che tende a un valore a è indicato con il simbolo $\lim_{x \to a} f(x)$ e si legge "il limite di f(x) per x che tende a a".

La definizione formale di limite è la seguente:

$$\lim_{x \to a} f(x) = L$$

### Teorema di unicità del limite

Se una funzione in un punto ha un limite finito, allora esso è unico.
Basta ricordare che ad ogni valore della X deve corrispondere uno e soltanto un valore della Y. Per assurdo, se $f(x)$ avesse nello stesso punto $x_0$ più di un limite, essa non sarebbe più una funzione e questo contraddice l'ipotesi del teorema.

### Permanenza del segno

Se una funzione in un punto $x_0 è dotata di limite $l\neq0$, allora esiste almeno un intorno $I$ di $x_0$ taleche per tutti i punti di $I$ (escluso $x_0$) i valori della funzione hanno lo stesso segno del limite.

### Teorema del confronto (carabinieri)

Anche noto come teorema del confronto, il teorema dei Carabinieri serve a determinare il limite di una funzione basandosi sui limiti di altre due funzioni che "incastrano" la nostra funzione.

Siano $f,g,h$ funzioni definite in un intorno di $x_0$ e tali che $f(x)\leq g(x)\leq h(x)$ per ogni $x$ nell'intorno, se $\lim_{x\to x_0}f(x)=\lim_{x\to x_0}h(x)=L$, allora $\lim_{x\to x_0}g(x)=L$.