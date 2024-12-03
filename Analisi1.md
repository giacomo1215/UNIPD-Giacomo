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

Siano $X$ e $Y$ due insiemi entrambi non vuoti, chiameremo **funzione** $f$ da $X$ in $Y$ una legge (o corrispondenza) che associa ad ogni elemento $x \in X$ un **unico** elemento $y \in Y$. Scriveremo $y=f(x)$ e chiameremo $y$ "valore di $f$ in $x$", e scriveremo $f:X \to Y$ per indicare che $f$ è una funzione da $X$ in $Y$.

L'insieme $X$ si dice **dominio** di $f$, l'insieme $Y$ si dice **codominio** di $f$.

Chiamiamo l'**immagine** di $f$ il sottoinsieme di $Y$:
$$
\{y \in Y : \exist \space x \in X \text{con }f(x)=y\}=Im(f)
$$
> Da notare che $Im(f) non è da confondere con la parte immaginaria di un numero complesso.

Il **grafico** di una funzione $f : X \to Y$ è il sottoinsieme di $X \times Y$:
$$
G(x) = \{(x,y) \in X \times Y : y=f(x)\}
$$

Si può definire una funzione come "il suo grafico" nel senso che una funzione con dominio $X$ e codominio $Y$ è un sottoinsieme $G$ di $X \times Y$ tale che:
$$
\forall x \in X \space \exist! y \in Y \text{ con } (x,y) \in G
$$

Sia $f:X \to Y$ una funzione, se $X \subseteq \mathbb{R}$ e $Y \subseteq \mathbb{R}$, allora $f$ è una funzione reale di variabili reali. Se $Y \subseteq \mathbb{R}$, allora diremo che $f$ è una funzione a **valori** reali.

See $f$ è una funzione a variabili reali e se il dominio non è esplicitamente indicato, allora si intende che $f$ è definita sul suo "dominio naturale", che è il sottoisneime più grande di $\mathbb{R}$ in cui la funzione è ben definita.

### Composizione di funzioni

Siano $f:X \to Y$ e $g:Y \to Z$ due funzioni e supponiamo che $f(x) \cap \forall \not= 0$, introduciamo l'insieme $\bar{X} \subseteq X$ definito da $\bar{X}:=\{x \in X : f(x) \in \mathbb{V}\}$. Possiamo definire la funzione $g \circ f$ detta "funzione composta di $g$ e $f$" così:
$$
\begin{align*}
g \circ f : \bar{X} &\to Z \\
x &\mapsto g(f(x)) \\
\\
\bar{X} &\subseteq X \to \mathbb{V} \to Z \\
&x \to f(x) \to g(f(x))
\end{align*}
$$

In generale, non è detto che se si può definire $g \circ f$, allora si possa definire $f \circ g$. Anche se si possono definire entrambe, di solito $f \circ g \not = g \circ f$.

### Funzioni iniettive, suriettive e invertibili

$f : X \to Y$ si dice:
- **Iniettiva** se $\forall y \in Y \space \exist$ al più un $x \in X$ tale che $f(x)=y$.
  - equivalentemente $x_1\not=x_2 \implies f(x_1)\not=f(x_2)$.
  - equivalentemente $f(x_1)\not=f(x_2) \implies x_1\not=x_2$.
- **Suriettiva** se $\forall y \in Y \space \exist x \in X$ tale che $f(x)=y$.
- **Biiettiva** se è sia iniettiva che suriettiva.

#### Invertibilità

Diremo che $f$ è invertibile se è biiettiva. A volte si parla di funzioni invertibili chiedendo soltanto f iniettiva: da una funzione iniettiva si ottiene in omdo canonico una funzione bigettiva regtringendo il codominio di $f$ all'immagine di $f$.

Se $f:X \to Y$ è iniettiva, possiamo considerare la funzione inversa (denotata con $f^{-1}$)nel seguente modo:
$$
f^{-1} : f(X) \to X
$$
$$
f^{-1}(y) = x \iff f(x) = y
$$

> $f^{-1}$ è l'inversa di $f$, non $\frac{1}{f}$ che di solito sono diverse.

### Restrizioni

Se $f:X \to Y$ è una funzione e $A \subseteq X$, allora la **restrizione** di $f$ ad $A$ è la funzione $f|_A : A \to Y$ definita da $f|_A(x) = f(x)$ per ogni $x \in A$.

Questa operazione può essere utile per ottenere funzioni iniettive a partire da funzioni che non lo sono.

Sia $f: domf \subset \mathbb{R} \to \mathbb{R}$, allora diciamo che:
1. $f$ è *pari* se $f(x) = f(-x) \space \forall x \in domf$.
2. $f$ è *dispari* se $f(x) = -f(-x) \space \forall x \in domf$.

### Periodicità

Sia $f: domf \subset \mathbb{R} \to \mathbb{R}$, allora diremo che $f$ è **periodica** con periodo $T$ ($T>0$) se:

$$
f(x+T) = f(x) \space \forall x \in domf
$$

Il periodo minimo di $f$ è il poiù piccolo per cui vale la condizione di periodicità.

Se $f$ e $g$ sono periodiche con periodo $T$, allora $f+g$, $f-g$, $f \cdot g$ e $f \circ g$ sono periodiche con periodo $T$.

### Monotonia

Sia $f$ una funzione, diremo che $f$ è **monotona crescente** quando:

$$
\forall x_1,x_2 \in domf \text{ con } x_1 < x_2 \implies f(x_1) < f(x_2)
$$

$f$ è strettamente crescente quando $f$ è crescente, ma viceversa è falso. 

Per esempio: $f(x) = x^3$ è strettamente crescente, ma non è crescente.
$$
\text{siano } x_1<x_2, \text{ dobbiamo mostrare che } f(x_1)<f(x_2)\\
\ \\
x_1^3 < x_2^3 \iff 0 < x_2^3 - x_1^3 = (x_2-x_1)(x_2^2+x_1x_2+x_1^2) \text{ che è vero} 
$$

### Limitatezza

Diremo che la funzione $f$ è **limitata** [superiormente/inferiormente] quando $Im(f)$ è limitata [superiormente/inferiormente].

Chiameremo maggiornate o minorante di $f$ ogni maggiorante o minorante di $Im(f)$. Analogamente per massimo, minimo, estremo superiore e inferiore. Tutte le proprietà mostrate per $\max, \min, \sup, \inf$ di insiemi valgono per funzioni perché per definizione una funzione è un insieme.

## Limiti

### Definizione di limite

Il limite di una funzione è un concetto fondamentale dell'analisi matematica che descrive il comportamento di una funzione quando la variabile indipendente si avvicina a un certo valore. Il limite di una funzione f(x) per x che tende a un valore a è indicato con il simbolo $\lim_{x \to a} f(x)$ e si legge "il limite di f(x) per x che tende a a".

La definizione formale di limite è la seguente:

$$\lim_{x \to a} f(x) = L$$

Dunque, vogliamo definire $\lim_{x \to \bar{x}} f(x)$ rendendo rigorosa l'affermazione "quando $x$ si avvicina a $\bar{x}$, $f(x)$ si avvicina ad un certo valore $L$ (che sarà il limite)".

Sia $r \in \mathbb{R}^*$, allora:
- se $r \in \mathbb{R}$ un intorno sferico centrato in $r$ è un intervallo della forma $(r-\varepsilon,r+\varepsilon)$ con $\varepsilon > 0$, oppure è tutto $\mathbb{R}$.
- se $r = +\infty$ un intorno sferico centrato in $r$ è un intervallo della forma $(M,+\infty)$ con $M \in \mathbb{R}$, oppure è tutto $\mathbb{R}$.
- se $r = -\infty$ un intorno sferico centrato in $r$ è un intervallo della forma $(-\infty,M)$ con $M \in \mathbb{R}$, oppure è tutto $\mathbb{R}$.

### Proprietà degli intorni

Sia $r \in \mathbb{R}^*$ e siano $U_1$ e $U_2$ due suoi intorni, allora $U_1 \cap U_2$ è un intorno di $r$. Inoltre, esiste la **proprietà di separazione**, che afferma che $\forall r_1, r_2 \in \mathbb{R}^*$ con $r_1 \not = r_2$, esistono due intorni $U_1$ e $U_2$ tali che $r_1 \in U_1$ e $r_2 \in U_2$ e $U_1 \cap U_2 = \emptyset$.

### Punto di accumulazione

Un punto di accumulazione di un insieme reale $E$ è un punto $x_0$ per il quale, comunque si scelga un intorno completo del punto stesso, esiste almeno un punto y dell'insieme $E$ diverso da $x_0$ e tale da appartenere all'intorno considerato. 

Sia $A \subseteq \mathbb{R}$, diremo che $r \in \mathbb{R}^*$ è un **punto di accumulazione** di $A$ quando $\forall$ intorno $U$ di $r$ vale $(A \cap U) \backslash\{r\} \not ={\emptyset}$. 

In altre parole, ogni intorno di $r$ contiene almeno un punto di $A$ diverso da $r$.

#### Punto isolato

Un punto isolato di $A$ deve appartenere ad $A$. In particolare, $+\infty$ e $-\infty$ possono essere punti d'accumulazione ma ***non*** punti isolati di $A$.

Se $f:dom \space f \rarr \mathbb{R}$, e $x_0$ è un punto d'accumulazione di $dom \space f$ e se $P$ è una proprietè che ha senso in $dom\space f$, allora diremo "f soddisfa la proprietà $P$ definitivamente per $x \rarr x_0$ quando esiste $U$ intorno di $x_0$ tale che:
$$\forall x \in U \backslash\{x_0\} \space f(x) \text{ verifica } P$$

### Definizione di limite di funzione

Il limite di una funzione è un operatore che permette di studiare il comportamento di una funzione nell'intorno di un punto, e srazie al quale possiamo stabilire a quale valore tende la funzione man mano che i valori della variabile indipendente si approssimano a quel punto.

Sia $f:dom \space f \rarr \mathbb{R}$, $x_0$ punto d'accumulazione di $dom \space f$ e $L \in \mathbb{R}*$. Diremo che $L$ è il **limite di $f$ per $x \rarr x_0$** quando:

1. $\forall U$ intorno di $L$ esiste $V$ intorno di $x_0$ tale che $f(x)\in U \space \forall x \in dom \space f \cap V \backslash \{x_0\}$
2. $\forall U$ intorno di $L$ esiste $V$ intorno di $x_0$ tale che $x \in dom \space f \cap V \backslash \{x_0\} \rArr f(x)\in U$   
3. $\forall U$ intorno di $l \space f(x)\in U$ definitivamente per $x \rarr x_0$
   1. se $l\in\mathbb{R}$ diremo che il limite è finito
   2. se $l=+\infty$ diremo che il limite è $+\infty$
   3. se $l=-\infty$ diremo che il limite è $-\infty$
   4. se $l=0$ diremo che la funzione è infinitesima


### Teorema di unicità del limite

Il teorema di unicità del limite assicura l'unicità del limite di una funzione, se quest'ultimo esiste, al tendere di $x\rarr x_0$ dove $x_0$ può essere un valore finito o indefinito.

Se $f:dom \space f \rarr \mathbb{R}$ e $x_0$ è un punto d'accumulazione di $dom \space f$ e valgono entrambi i limiti:
$$
\lim_{x \rarr x_0} f(x) = l_1 \space \text{e} \space \lim_{x \rarr x_0} f(x) = l_2
$$
allora $l_1 = l_2$.

Dunque, se una funzione in un punto ha un limite finito, allora esso è unico.
Basta ricordare che ad ogni valore della X deve corrispondere uno e soltanto un valore della Y. Per assurdo, se $f(x)$ avesse nello stesso punto $x_0$ più di un limite, essa non sarebbe più una funzione e questo contraddice l'ipotesi del teorema.

### Teorema: Limite finito implica locale limitatezza

Se il limite $\lim_{x \rarr x_0} f(x) = l \in \mathbb{R}$, cioè $l \not = \pm \infty$, allora esiste un intorno $U$ di $x_0$ e $\mathbb{N} \in \mathbb{R}$ tale che $\forall \space x \in U\cap dom \space f\backslash \{x_0\}$ vale $|f(x)| \leq N$.

### Limite destro e Limite sinistro

Un limite destro è un limite per $x$ tendente a $x_0$ con i valori di $x$ che si approssimano a $x_0$ nell'intorno destro del punto; nel caso di un limite sinistro i valori si avvicinano a $x_0$ nell'intorno sinistro del punto.

Sia $A \subset \mathbb{R}, A = \emptyset$. Un punto $r \in \mathbb{R}$ è detto punto d'accumulazione destro [sinistro] di $A$ quando $r$ è un punto di accumulazione di $A \cap (r,+\infty)$ [$A \cap (-\infty,r)$]. Chiameremo intorno destro [sinistro] di $r \in \mathbb{R}$ gli insiemi della forma $(r,r+\varepsilon)$ [$(r-\varepsilon,r)$] con $\varepsilon > 0$.

Un punto d'accumulazione destro (o sinistro) è necessariamente un punto d'accumulazione. Viceversa, un punto d'accumulazione è un punto d'accumulazione destro o sinistro, potrebbe non essere entrambi.

### Permanenza del segno

Il teorema della permanenza del segno assicura l'esistenza di un intorno di un punto c in cui la funzione $f(x)$ è concorde con il limite di $f(c)$ per $x \rarr c$, a patto che tale limite sia diverso da 0.

Dunque, se una funzione in un punto $x_0$ è dotata di limite $l\neq0$, allora esiste almeno un intorno $I$ di $x_0$ taleche per tutti i punti di $I$ (escluso $x_0$) i valori della funzione hanno lo stesso segno del limite.

### Teorema del confronto (carabinieri)

Il teorema del confronto, noto anche come il teorema dei Carabinieri, è uno strumento matematico utilizzato in analisi per determinare il limite di una funzione sfruttando il fatto che essa è "stretta" tra altre due funzioni il cui comportamento limite è noto.

#### Caso Limitato

Siano $f(x), g(x), h(x)$ definite su un certo intervallo, e vale:

- $f(x) \leq g(x) \leq h(x)$ per ogni $x$ nell'intorno di $x_0$
- $\lim_{x \rarr c} g(x) = \lim_{x \rarr c} h(x) = l \in \mathbb{R}$

allora $\lim_{x \rarr c} g(x) = l$

Immaginiamo che $f(x)$ sia un'auto intrappolata tra due pattuglie di carabinieri, rappresentate da $g(x)$ e $h(x)$. Se i carabinieri convergono allo stesso punto $l$, allora anche l'auto è costretta a raggiungere lo stesso limite $l$.

#### Caso Illimitato

Siano $f(x), g(x), h(x)$ definite su un certo intervallo, e vale:

- $0 \leq f(x) \leq g(x) \leq h(x)$ per ogni $x$ in un intervallo
- $\lim_{x\rarr c}g(x) = \lim_{x\rarr c}h(x)=\pm \infty$

allora $\lim_{x\rarr c}g(x)=\pm \infty$

Se $f(x)$ è "intrappolata tra due funzioni che crescono o decrescono all'infinito allo stesso ritmo, anche $f(x)$ sarà costretta a comportarsi allo stesso modo.

## Funzioni Iperboliche

