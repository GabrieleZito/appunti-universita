carica → grandezza elettrica fondamentale, indicata con $q$, misurata in Coulomb (C), $1\ C=6.24*10^18$ elettroni. Una carica che si sposta crea una corrente. Per convenzione le cariche che si spostano sono quelle positive

$i=\frac{dq}{dt}$ si misura in Ampere( = 1 Coulomb/secondo)

Ad ogni carica è associata un’energia $w$. L’energia per unità di carica è chiamata potenziale: $V=\frac{w}{q}$

Se una carica si sposta, cambia la sua energia. Se si sposta da un punto $a$ ad un punto $b$, chiamiamo tensione. o differenza di potenziale, la quantità 

$$
v_{ab}=\frac{w(a)-w(b)}{q}=V(a)-V(b)
$$

e dipende solo dalle posizioni a e b, e non dalla quantità di carica né dal percorso

La tensione si misura in Volt (=1 Joule/Coulomb)

Nodo → punto di connessione tra 2 o più elementi

Maglia → sequenza di nodi che inizia e termina sullo stesso nodo, ogni nodo incontrato una volta sola

Anello → Maglia che non contiene altre maglie

Lato → tratto di rete che rappresenta un bipolo con i conduttori ideali direttamente collegati ai suoi terminali. Il numero di lati coincide con il numero di bipoli

### Legge di OHM   v=Ri

### LKC - Legge di Kirchhoff per le correnti

La somma algebrica delle correnti che entrano (o escono) in un nodo è nulla

### LKT - Legge di Kirchhoff sulle tensioni

La somma algebrica delle tensioni lungo una maglia è nulla

Potenza → energia perduta per unità di tempo $p=\frac{\Delta w}{\Delta t}$. che diventa $p=vi=Ri^2=\frac{v^2}{R}$. Si misura in Watt (=1 Joule/secondo)

Conservazione della potenza → La somma algebrica delle potenze assorbite da tutti gli elementi di un circuito è nulla in ogni istante

### Circuiti Resistivi

Resistore → Bipolo caratterizzato dalla relazione $v=Ri$. $R$ è la resistenza. si misura in Ohm (= 1 Volt/ampere). proprietà dei materiali di opporre resistenza al passaggio della corrente.

Si può scrivere anche $i = \frac1Rv=Gv$. G è chiamata Conduttanza, si misura in Siemens

Corto circuito → Resistore di resistenza nulla, indicato con una linea continua, v=0

Circuito aperto → resistore con resistenza infinita (conduttanza nulla), i=0

Generatore indipendente di tensione

Elemento caratterizzato dalla relazione $v=v_s(t)$, che può essere costante, oppure una funzione nota del tempo. 

La tensione non dipende dalla corrente

Generatore indipendente di corrente

Elemento caratterizzato dalla relazione $i=i_s(t)$, costante o funzione nota del tempo. La corrente non dipende dalla tensione

resistori in serie→ resistori attraversati dalla stessa corrente $i$. si possono sostituire con un resistore di resistenza la somma delle resistenze

resistori in parallelo → resistori con la stessa tensione

resistori a stella e triangolo

![Untitled](Elettrotecnica/imgs/Untitled.png)

Passaggio da triangolo a stella

![Untitled](Elettrotecnica/imgs/Untitled%201.png)

Passaggio da stella a triangolo

![Untitled](Elettrotecnica/imgs/Untitled%202.png)

Principio di sovrapposizione → in un circuito resistivo lineare, qualunque tensione o corrente è la somma degli effetti dei singoli generatori indipendenti, quando agiscono uno alla volta → studiare il circuito tenendo solo accesso un generatore alla volta. quelli di tensione si sostituiscono con un corto circuito, quelli di corrente con un circuito aperto. Sommare quindi tutti i risultati

### Partitore di tensione

![Untitled](Elettrotecnica/imgs/Untitled%203.png)

Per la LKT otteniamo che $v_G=v_1+v_2$. Sostituendo $v=Ri$ otteniamo $v_g=(R_1+R_2)i$. Ci troviamo la corrente $i=\frac{v_g}{R_1+R_2}$ che se sostituiamo in $v=Ri$ otteniamo

$$
v_1=v_g\frac{R_1}{R_1+R_2}\qquad v_2=v_g\frac{R_2}{R_1+R_2}
$$

### Partitore di corrente

![Untitled](Elettrotecnica/imgs/Untitled%204.png)

Stesso svolgimento del partitore di tensione

$$
i_G=i_1+i_2\rightarrow i_1=G_1v,\ i_2=G_2v\Rightarrow i_G=(G_1+G_2)v\Rightarrow v=\frac{i_g}{G_1+G_2}
$$

$$
i_1=i_G\frac{G_1}{G_1+G_2}\qquad i_2=i_G\frac{G_2}{G_1+G_2}
$$

Principio di sostituzione → A e B due parti di un circuito. se vogliamo studiare solo la parte A, possiamo sostituire B con un generatore di tensione di valore $v$, o con uno di corrente di valore $i$

![Untitled](Elettrotecnica/imgs/Untitled%205.png)

Trasformatore Ideale → dispositivo a 4 terminali costituito da due avvolgimenti attorno ad un nucleo comune. Uno degli avvolgimenti è di solito chiuso su un generatore indipendente, ed è chiamato primario, mentre l’altro, secondario, su un carico passivo.

![Untitled](Elettrotecnica/imgs/Untitled%206.png)

![Untitled](Elettrotecnica/imgs/Untitled%207.png)

Relazioni costitutive

- $\frac{v_1}{v_2}=n$   se le tensioni sono concorde, altrimenti $\frac{v_1}{v_2}=-n$
- $\frac {i_1}{i_2}=-\frac 1n$ se le correnti sono concorde, altrimenti $\frac {i_1}{i_2}=\frac 1n$

Sia correnti che tensioni misurate nei terminali contrassegnati

Proprietà

- il trasformatore è trasparente alla potenza
    
    $p=v_1i_1+v_2i_2=0$ se sostituiamo il primo addendo con le relazioni di prima
    
    $p=nv_2(-\frac 1ni_2)+v_2i_2=0$
    
- Trasformazione delle resistenze
    - Mettiamo a sinistra un generatore qualsiasi e a destra una resistenza
        
        ![Untitled](Elettrotecnica/imgs/Untitled%208.png)
        
        Quanto vale la resistenza vista dai terminali 1 e 1’?
        
        $$
        R_{11'}=\frac{v_1}{i_1}\ e\ v_2=-R_2i_2\Rightarrow -\frac{v_2}{i_2}=R_2
        $$
        
        $$
        R_{11'}=\frac{v_1}{i_1}=\frac{nv_2}{-\frac{i_2}{n}}=-n^2(-\frac{v_2}{i_2})=n^2R_2
        $$
        
    - Viceversa invece avremo
        
        ![Untitled](Elettrotecnica/imgs/Untitled%209.png)
        
        $$
        R_{22'}=\frac{v_2}{i_2}\ e\ v_1=-R_1i_1\Rightarrow R_1=-\frac{v_1}{i_1}
        $$
        
        $$
        R_{22'}=\frac{\frac{v_1}{n}}{-ni_1}=-\frac{v_1}{i_1}\frac{1}{n^2}=\frac{R_1}{n^2}
        $$
        

### Teorema di Thevenin

![Untitled](Elettrotecnica/imgs/Untitled%2010.png)

Un circuito resistivo lineare, accessibile da due terminali, è equivalente ad un generatore indipendente di tensione in serie ad un resistore. La tensione $v_t$ del generatore è la tensione che si ha tra i terminali quando sono aperti (a vuoto). La resistenza $R_T$ è la resistenza equivalente al circuito con i generatori indipendenti spenti

Teorema di Norton → Duale di Thevenin ( generatore di corrente in parallelo ad un resistore, con corrente la corrente dei terminali in corto circuito, e resistenza la resistenza eq. al circuito con i generatori spenti)

Dimostrazione

Applichiamo il principio di sostituzione:

![Untitled](Elettrotecnica/imgs/Untitled%2011.png)

Applichiamo il principio di sovrapposizione

Spegniamo prima il generatore di corrente

![Untitled](Elettrotecnica/imgs/Untitled%2012.png)

e abbiamo $i'=0$ e $v'=v_{CA}$

Poi spegniamo tutti i generatori in A

![Untitled](Elettrotecnica/imgs/Untitled%2013.png)

troviamo $i''=i$  e $v''=-R_{eq}i''$

Per il principio di sovrapposizione abbiamo

$$
i=i'+i''=i\qquad v=v'+v''=v_{CA}-R_{eq}i
$$

Quindi per qualche motivo si può fare la sostituzione.

### Teorema del massimo trasferimento di potenza

Un generatore di resistenza interna $R_s$ fornisce la massima potenza di carico, di resistenza $R_L$, quando $R_L=R_s$

$R_L$ scelta liberamente

![Untitled](Elettrotecnica/imgs/Untitled%2014.png)

Ho il circuito di sopra, come scelgo $R_L$ in modo che la potenza assorbita da esso sia massima?

Abbiamo che $p_L=v_li$, $v_L=R_Li\Rightarrow p_L=R_Li^2=R_L(\frac{V_{CA}}{R_{TH}+R_L})^2$

Possiamo vederla come una funzione dipendente da $R_L$, quindi studiamo i punti di massimo con la derivata prima

$$
\frac{dp_L}{dR_L}= V_{CA}^2\frac{(R_{TH}+R_L)-2(R_{TH}+R_L)R_L}{(R_{TH}+R_L)^4}=0
$$

E la condizione di sopra può essere vera se e solo se $R_L=R_{TH}$

E in questo caso abbiamo che la potenza è $p_{Lx}=V_{CA}^2\frac{R_L}{(R_L+R_{TH})^2}=\frac{V_{CA}^2}{4R_{TH}}$, mentre la potenza erogata dal generatore è $p_{gx}=V_{CA}i=\frac{V_{CA}^2}{2R_{TH}}$

E avremo un rendimento di $\eta=\frac{\text{potenza utilizzatore}}{\text{potenza generatore}}=\frac{p_{Lx}}{p_{gx}}=\frac12$

$R_L$ fissa

Cosa inserisco in mezzo per avere la massima potenza su $R_L$?

Un trasformatore ideale, visto che è trasparente alla potenza

![Untitled](Elettrotecnica/imgs/Untitled%2015.png)

visto che $R_{11'}=n^2R_L$ e che vogliamo che dalla porta si veda $R_{TH}$, $\Rightarrow\ R_{TH}=n^2R_L$

dobbiamo scegliere un trasformatore con rapporto $n=\sqrt{\frac{R_{TH}}{R_L}}$ 

Rendimento in funzione di $R_L$

$$
\eta=\frac{p_L}{p_g}=\frac{V_{CA}^2\frac{R_L}{(R_{TH}+R_L)^2}}{V_{CA}^2\frac{1}{R_{TH}+R_L}}=\cdots=\frac1{\frac{R_{TH}}{R_L}+1}\Rightarrow\begin{cases}
\lim\limits_{R_L\to0}\eta=0\\
\lim\limits_{R_L\to\infty}\eta=1
\end{cases}
$$

### Generatori controllati

Generatori la cui caratteristica dipende da un’altra variabile del circuito

Porta → Coppia di terminali in cui la corrente che entra è uguale a quella che esce

Doppio Bipolo → circuito accessibile da due porte

### Thevenin e Norton con reti di N porte

![Untitled](Elettrotecnica/imgs/Untitled%2016.png)

### Sostituzione di doppi bipoli resistivi

In un doppio bipolo abbiamo 4 variabili:  $v_1,\ i_1,\ v_2,\ i_2$ 

Per risolvere il circuito abbiamo 4 possibilità

- $i_1$ ed $i_2$ indipendenti, $v_1$ e $v_2$ dipendenti - Matrice delle induttanze a circuito aperto [Z]
- $v_1$ ed $v_2$ indipendenti, $i_1$ e $i_2$ dipendenti - Matrice delle ammettenze in corto circuito [Y]
- $i_1$ ed $v_2$ indipendenti, $v_1$ e $i_2$ dipendenti - Matrice ibrida diretta [H]
- $v_2$ ed $i_2$ indipendenti, $v_1$ e $i_1$ dipendenti - Matrice di trasmissione diretta [T] o [ABCD]

### Matrice delle induttanze a circuito aperto

Devo riuscire a scrivere $v_1\ e\ v_2$ in funzione di $i_1$ ed $i_2$

$$
\begin{bmatrix}
z_{11}&z_{12}\\
z_{12}&z_{22}
\end{bmatrix}\begin{bmatrix}
i_1\\ i_2
\end{bmatrix}=
\begin{bmatrix}
v_1\\ v_2
\end{bmatrix}
$$

$$
\begin{cases}
v_1=z_{11}i_1+z_{12}i_2\\
v_2=z_{21}i_1+z_{22}i_2
\end{cases}
\qquad z_{ij}\rightarrow\text{impedenze a circuiti aperti}
$$

Troviamo i coefficienti:

$$
\text{Ponendo }i_2=0\begin{cases}
z_{11}=\frac{v_1}{i_1}\\
z_{21}=\frac{v_2}{i_1}
\end{cases}\quad
\text{Ponendo }i_1=0\begin{cases}
z_{12}=\frac{v_1}{i_2}\\
z_{22}=\frac{v_2}{i_2}
\end{cases}
$$

E otteniamo il circuito equivalente:

![Untitled](Elettrotecnica/imgs/Untitled%2017.png)

### Matrice delle ammettenze in corto circuito

Devo riuscire a scrivere $i_1$ ed $i_2$  in funzione di $v_1\ e\ v_2$

$$
\begin{cases}
i_i=y_{11}v_1+y_{12}v_2\\
i_2=y_{21}v_1+y_{22}v_2
\end{cases}
\qquad y_{ij}\rightarrow\text{ammettenze a circuiti chiusi}
$$

Calcoliamo i coefficienti

$$
\text{Ponendo }v_2=0\begin{cases}
y_{11}=\frac{i_1}{v_1}\\
y_{21}=\frac{i_2}{v_1}
\end{cases}\quad
\text{Ponendo }v_1=0\begin{cases}
y_{12}=\frac{i_1}{v_2}\\
y_{22}=\frac{i_2}{v_2}
\end{cases}
$$

E il circuito diventa:

![Untitled](Elettrotecnica/imgs/Untitled%2018.png)

### Matrice ibrida diretta

Devo riuscire a scrivere $v_1$ ed $i_2$  in funzione di $i_1\ e\ v_2$

$$
\begin{cases}
v_1=h_{11}i_1+h_{12}v_2\\
i_2=h_{21}i_1+h_{22}v_2
\end{cases}
$$

Troviamo i coefficienti:

$$
\text{Ponendo }v_2=0\begin{cases}
h_{11}=\frac{v_1}{i_1}\\
h_{21}=\frac{i_2}{i_1}
\end{cases}\quad
\text{Ponendo }i_1=0\begin{cases}
h_{12}=\frac{v_1}{v_2}\\
h_{22}=\frac{i_2}{v_2}
\end{cases}
$$

E il circuito equivalente:

![Untitled](Elettrotecnica/imgs/Untitled%2019.png)

### Matrice di trasmissione diretta

Devo riuscire a scrivere $v_1$ ed $i_2$  in funzione di $v_2\ e\ -i_2$

$$
\begin{cases}
v_1=Av_2+B(-i_2)\\
i_1=Cv_2+D(-i_2)
\end{cases}
$$

Trovare i coefficienti A, B, C, D, è impossibile, quindi troviamo gli inversi

$$
\text{Per }-i_2=0,\quad \frac 1A=\frac{v_2}{v_1}\qquad \text{Per }v_2=0,\quad \frac1B=\frac{-i_2}{v_1}\\
\text{Per }-i_2=0,\quad \frac 1C=\frac{v_2}{i_1}\qquad \text{Per }v_2=0,\quad \frac1D=\frac{-i_2}{i_1}
$$

Non si può generalizzare un circuito equivalente

Reciprocità → la risposta di un sistema non cambia se ingresso e uscita vengono invertiti

I bipoli lineari sono sempre reciproci

### Interconnessione di Doppi bipoli

In un bipolo ricordiamo che i 4 terminali devono comportarsi come 2 porte, in caso contrario non è un bipolo

### SERIE - SERIE

![Untitled](Elettrotecnica/imgs/Untitled%2020.png)

$$
v_1=v_1'+v_2''\\
v_2=v_1''+v_2''\\
i_1=i_1'=i_1''\\
i_2=i_2'=i_2''
$$

Per il doppio bipolo risultante vale la relazione $[Z]=[Z']+[Z'']$

Per verificare che il circuito risultante sia un bipolo dobbiamo verificare le condizioni:

![Untitled](Elettrotecnica/imgs/Untitled%2021.png)

Se sono valide, allora possiamo dimostrare la relazione di prima

$$
\begin{bmatrix}
v_1'\\ v_2'
\end{bmatrix}=\begin{bmatrix}
Z'
\end{bmatrix}\begin{bmatrix}
i_1'\\ i_2'
\end{bmatrix}
\qquad e\qquad
\begin{bmatrix}
v_1''\\ v_2''
\end{bmatrix}=\begin{bmatrix}
Z''
\end{bmatrix}\begin{bmatrix}
i_1''\\ i_2''
\end{bmatrix}\Rightarrow
$$

$$
\Rightarrow\begin{bmatrix}
v_1\\ v_2
\end{bmatrix}=\begin{bmatrix}
v_1'\\ v_2'
\end{bmatrix}+\begin{bmatrix}
v_1''\\ v_2''
\end{bmatrix}=\begin{bmatrix}
Z'
\end{bmatrix}\begin{bmatrix}
i_1'\\ i_2'
\end{bmatrix}+\begin{bmatrix}
Z''
\end{bmatrix}\begin{bmatrix}
i_1''\\ i_2''
\end{bmatrix}\Rightarrow
$$

$$
\Rightarrow\text{poichè  }\quad\begin{matrix}
i_1=i_1'=i_1''\\
i_2=i_2'=i_2''
\end{matrix}\Rightarrow\begin{bmatrix}
v_1\\ v_2

\end{bmatrix}=\underbrace{\begin{bmatrix}
Z'
\end{bmatrix}+\begin{bmatrix}
Z''
\end{bmatrix}}_{\begin{bmatrix}Z\end{bmatrix}}\begin{bmatrix}
i_1\\ i_2
\end{bmatrix}
$$

### PARALLELO - PARALLELO

![Untitled](Elettrotecnica/imgs/Untitled%2022.png)

$$
i_1=i_1'+i_1''\\
i_2=i_2''+i_2''\\
v_1=v_1'=v_1''\\
v_2=v_2'=v_2''
$$

Prove di validità:

![Untitled](Elettrotecnica/imgs/Untitled%2023.png)

Dimostriamo che $\begin{bmatrix}
Y
\end{bmatrix}=\begin{bmatrix}
Y'
\end{bmatrix}+\begin{bmatrix}
Y''
\end{bmatrix}$

$$
\begin{bmatrix}
i_1'\\ i_2'
\end{bmatrix}=\begin{bmatrix}
Y'
\end{bmatrix}\begin{bmatrix}
v_1'\\ v_2'
\end{bmatrix}\qquad e\qquad
\begin{bmatrix}
i_1''\\ i_2''
\end{bmatrix}=\begin{bmatrix}
Y''
\end{bmatrix}\begin{bmatrix}
v_1''\\ v_2''
\end{bmatrix}\Rightarrow
$$

$$
\Rightarrow \begin{bmatrix}
i_1\\ i_2
\end{bmatrix}=\begin{bmatrix}
i_1'\\ i_2'
\end{bmatrix}+\begin{bmatrix}
i_1''\\ i_2''
\end{bmatrix}=\begin{bmatrix}
Y'
\end{bmatrix}\begin{bmatrix}
v_1'\\ v_2'
\end{bmatrix}+\begin{bmatrix}
Y''
\end{bmatrix}\begin{bmatrix}
v_1''\\ v_2''
\end{bmatrix}\Rightarrow
$$

$$
\Rightarrow\text{Poichè }\quad
\begin{matrix}
v_1=v_1'=v_1''\\
v_2=v_2'=v_2''
\end{matrix}\Rightarrow
\begin{bmatrix}
i_1\\ i_2
\end{bmatrix}=\underbrace{\begin{bmatrix}
Y'
\end{bmatrix}+\begin{bmatrix}
Y''
\end{bmatrix}}_{\begin{bmatrix}
Y
\end{bmatrix}}\begin{bmatrix}
v_1\\ v_2
\end{bmatrix}
$$

### SERIE - PARALLELO

![Untitled](Elettrotecnica/imgs/Untitled%2024.png)

$$
v_1=v_1'+v_1''\\
i_1=i_1'=i_1''\\
v_2=v_2'=v_2''\\
i_2=i_2'+i_2''
$$

Prove di validità:

![Untitled](Elettrotecnica/imgs/Untitled%2025.png)

Dimostriamo che $\begin{bmatrix}
H
\end{bmatrix}=\begin{bmatrix}
H'
\end{bmatrix}+\begin{bmatrix}
H''
\end{bmatrix}$

$$
\begin{bmatrix}
v_1'\\ i_2'
\end{bmatrix}=\begin{bmatrix}
H'
\end{bmatrix}\begin{bmatrix}
i_1'\\ v_2'
\end{bmatrix}\qquad e\qquad
\begin{bmatrix}
v_1''\\ i_2''
\end{bmatrix}=\begin{bmatrix}
H''
\end{bmatrix}\begin{bmatrix}
i_1''\\ v_2''
\end{bmatrix}\Rightarrow
$$

$$
\Rightarrow \begin{bmatrix}
v_1\\ i_2
\end{bmatrix}=\begin{bmatrix}
v_1'\\ i_2'
\end{bmatrix}+\begin{bmatrix}
v_1''\\ i_2''
\end{bmatrix}=\begin{bmatrix}
H'
\end{bmatrix}\begin{bmatrix}
i_1'\\ v_2'
\end{bmatrix}+\begin{bmatrix}
H''
\end{bmatrix}\begin{bmatrix}
i_1''\\ v_2''
\end{bmatrix}\Rightarrow
$$

$$
\Rightarrow\text{Poichè }\quad
\begin{matrix}
i_1=i_1'=i_1''\\
v_2=v_2'=v_2''
\end{matrix}\Rightarrow
\begin{bmatrix}
v_1\\ i_2
\end{bmatrix}=\underbrace{\begin{bmatrix}
H'
\end{bmatrix}+\begin{bmatrix}
H''
\end{bmatrix}}_{\begin{bmatrix}
H
\end{bmatrix}}\begin{bmatrix}
i_1\\ v_2
\end{bmatrix}
$$

### CASCATA

![Untitled](Elettrotecnica/imgs/Untitled%2026.png)

Per questa connessione non c’è bisogno di prove di validità

$$
v_1=v_1'\\
i_1=i_1'\\\ \\
v_2'=v_1''\\
-i_2'=i_1''\\\ \\
v_2=v_2''\\
i_2=i_2''
$$

Dimostriamo $\begin{bmatrix}
T
\end{bmatrix}=\begin{bmatrix}
T'
\end{bmatrix}\begin{bmatrix}
T''
\end{bmatrix}$

$$
\begin{bmatrix}
v_1'\\ i_1'
\end{bmatrix}=\begin{bmatrix}
T'
\end{bmatrix}\begin{bmatrix}
v_2'\\ -i_2'
\end{bmatrix}\qquad e\qquad
\begin{bmatrix}
v_1''\\ i_1''
\end{bmatrix}=\begin{bmatrix}
T''
\end{bmatrix}\begin{bmatrix}
v_2''\\ -i_2''
\end{bmatrix}\Rightarrow
$$

$$
\Rightarrow\begin{bmatrix}
v_1\\ i_1
\end{bmatrix}=\begin{bmatrix}
T'
\end{bmatrix}\begin{bmatrix}
v_2'\\-i_2'
\end{bmatrix}=\begin{bmatrix}
T'
\end{bmatrix}\begin{bmatrix}
T''
\end{bmatrix}\begin{bmatrix}
v_2''\\ -i_2''
\end{bmatrix}=\begin{bmatrix}
T'
\end{bmatrix}\begin{bmatrix}
T''
\end{bmatrix}\begin{bmatrix}
v_2\\-i_2
\end{bmatrix}
$$

$$
\begin{bmatrix}
v_1\\ i_1
\end{bmatrix}=\underbrace{\begin{bmatrix}
T'
\end{bmatrix}\begin{bmatrix}
T''
\end{bmatrix}}_{\begin{bmatrix}
T
\end{bmatrix}}\begin{bmatrix}
v_2\\ -i_2
\end{bmatrix}
$$

### Condensatore

Simbolo

![Untitled](Elettrotecnica/imgs/Untitled%2027.png)

La caratteristica del condensatore è la capacità (C>0), misurata in Farad (1 F = 1 Coulomb/Volt)

$$
q=Cv
$$

Per esprimere la tensione in funzione della corrente

$$
C=\frac qv\\
\frac{dq}{dt}=i(t)=C\frac{dv}{dt}
$$

$$
dv=\frac 1C idt\Rightarrow v(t)=v(t_0)+\frac 1C\int\limits_{t_0}^ti(x)dx
$$

La tensione dipende anche dal passato

Proprietà

- A tensione costante il condensatore equivale ad un circuito aperto, infatti $i(t)=C\frac{dv}{dt}\Rightarrow i=0$
- La tensione ai capi di un condensatore è una funzione continua
- Il condensatore non dissipa energia, ma può immagazzinarla

### Circuito RC

![Untitled](Elettrotecnica/imgs/Untitled%2028.png)

- Carica del condensatore - Risposta con stato zero
    
    Determiniamo $v(t)\Rightarrow -E_0+v_R+v(t)=0\Rightarrow E_0=iR+v(t)$
    
    ma $i=C\frac{dv}{dt}$ quindi $RC\frac{dv}{dt}+v(t)=E_0$
    
    $$
    \begin{cases}
    RC\frac{dv}{dt}+v(t)=E_0\\
    v(0)=0\ 
    \end{cases}\Rightarrow \text{dopo i calcoli }\ v(t)=E_0(1-e^{-\frac{t}{RC}}),\ t\ge0\\\ \\
    \text{e quindi }i(t)=\frac{E_0}{R}e^{-\frac{t}{RC}}
    $$
    
- Scarica del condensatore - Risposta con ingresso zero
    
    analogo a sopra ma cambia la condizione iniziale
    
    $$
    \begin{cases}
    \frac{dv}{dt}+\frac1{RC}v(t)=0\\
    v(0)=E_0
    \end{cases}\Rightarrow \begin{cases}
    v(t)=E_0e^{-\frac{t}{RC}},\ \ t\ge0\\
    i(t)=-\frac{E_0}{R}e^{-\frac{t}{RC}}
    \end{cases}
    $$
    
- Risposta completa - ingresso e stato non nulli
    
    $$
    \begin{cases}
    \frac{dv}{dt}+\frac{v}{RC}=E\\
    v(0)=V_0
    \end{cases}\Rightarrow\ v(t)=\underbrace{V_0e^{-\frac{t}{\tau}}}_{\text{ingresso zero}}+E_0\underbrace{(1-e^{-\frac{t}{\tau}})}_{\text{ingresso nullo}}=(V_0-E)e^{-\frac{t}{\tau}}+E_0
    $$
    

### Condensatori in serie

Sostituzione con un unico condensatore di capacità $C_T$

$$
\frac1{C_T}=\sum\limits_{k=1}^N\frac1{C_k}
$$

### Condensatori in parallelo

Sostituzione con un unico condensatore di capacità $C_T$

$$
C_T=\sum\limits_{k=1}^NC_k
$$

### Forme d’onda notevoli di un condensatore

- Gradino unitario

$$
u(t)=\begin{cases}
0, & t<0\\
1, &t\ge0
\end{cases}
$$

![Untitled](Elettrotecnica/imgs/Untitled%2029.png)

- Gradino unitario traslato

$$
u(t-t_0)=\begin{cases}
0,&t<t_0\\
1, & t\ge t_0
\end{cases}
$$

![Untitled](Elettrotecnica/imgs/Untitled%2030.png)

Risposta al gradino $v(t)=(1-e^{-\frac{t}{\tau}})u(t)$

- Impulso finito di durata finita

$$
p_\Delta(t)=\begin{cases}
0, & t<0\\
\frac1\Delta, &0\le t<\Delta\\
0,&t\ge\Delta
\end{cases}
$$

![Untitled](Elettrotecnica/imgs/Untitled%2031.png)

Risposta all’impulso $p_\Delta=\frac1\Delta(u(t)-u(t-\Delta))$

### Induttore

![Untitled](Elettrotecnica/imgs/Untitled%2032.png)

$$
L=\text{induttanza (costante)}\\
v=L\frac{di(t)}{dt}\\
i(t)=i(t_0)+\frac1L\int\limits^t_{t_0}v(x)dx
$$

### Induttori in serie

Un induttore di induttanza

$$
L_S=\sum\limits_{k=1}^NL_k
$$

### Induttori in parallelo

$$
\frac1{L_P}=\sum\limits_{k=1}^N\frac1{L_k}
$$

### Circuito RL parallelo

- Risposta con stato zero

![Untitled](Elettrotecnica/imgs/Untitled%2033.png)

$$
i_L(0)=0\\
LKC\rightarrow I_S=i_R+i_L\Rightarrow I_S=\frac LR\frac{di_L(t)}{dt}+i_L
$$

Sia $\tau=\frac LR$

$$
\begin{cases}
\frac{di_L}{dt}+\frac{i_L}{\tau}=\frac{I_L}{\tau}\\
i_L(0)=0
\end{cases}\Rightarrow
i_L=I_S(1-e^{-\frac t\tau}),\ t\ge0
$$

- Risposta con ingresso zero

![Untitled](Elettrotecnica/imgs/Untitled%2034.png)

$$
i_L(0)=I_0\\
LKC\rightarrow i_R+i_L=0\Rightarrow\frac vR+i_L=0\Rightarrow\frac LR\frac{di}{dt}+i_L=0
$$

$$
\begin{cases}
\frac{di_L}{dt}+\frac{i_L}{t}=0\\
i(0)=I_0
\end{cases}\Rightarrow
i_L(t)=I_0e^{-\frac t\tau}
$$

- Risposta completa

![Untitled](Elettrotecnica/imgs/Untitled%2035.png)

$$
i_L(0)=0
$$

$$
\begin{cases}
\frac{di_L}{dt}\frac{i_L}{t}=\frac{I_g}{t}\\
i(0)=I_0
\end{cases}\Rightarrow
i_L(t)=\underbrace{I_0e^{-\frac t\tau}}_{\text{ing. zero}}+\underbrace{I_g(1-e^{-\frac t\tau})}_{\text{stato zero}}=(I_0-I_g)e^{-\frac t\tau}+I_g,\ t\ge0
$$

### Circuito RLC

![Untitled](Elettrotecnica/imgs/Untitled%2036.png)

$$
i_L(0)=I_0\qquad v(0)=V_0
$$

$$
v_C=v=v_L\Rightarrow\ v_L=L\frac{di(t)}{dt}=v
$$

inoltre

$$
i_C=C\frac{dv_C}{dt}=C\frac{dv_L}{dt}=CL\frac{d''i(t)}{dt^2}
$$

$$
LKC\rightarrow i_r+i_c+i_l=0\Rightarrow\frac LR\frac{di(t)}{dt}+CL\frac{d''i(t)}{dt^2}+i_l(t)=0
$$

Quindi

$$
\begin{cases}
\frac{d''i_l(t)}{dt^2}+\frac1{RC}\frac{di_l(t)}{dt}+i_l(t)=0\\
i_l(0)=I_0\\
\frac{di_l(0)}{dt}=\frac{v_L}{L}=\frac{V_0}{L}
\end{cases}
$$

Siano $\frac1{RC}=2\alpha$  e  $\frac1{LC}=\omega_0^2$

L’equazione caratteristica è del tipo

$$
s^2+2\alpha s+\omega^2_0\Rightarrow s_{1,2}=-\alpha\pm\sqrt{\alpha^2-\omega_0^2}
$$

La soluzione si divide in 4 casi:

1. $\alpha>\omega_0\Rightarrow$ 2 frequenze reali negative distinte
2. $\alpha=\omega_0\Rightarrow$ 2 frequenze reali negative coincidenti
3. $\alpha<\omega_0\Rightarrow$  2 frequenze complesse coniugate
4. $\alpha\to0\Rightarrow$ senza perdite, ideale

Caso 1: $\alpha >\omega_0$    con sovrasmorzamento

La soluzione è del tipo: $i_l(t)=k_1e^{s_1t}+k_2e^{s_2t}$, $t\ge0$

$k_1$ e $k_2$ le trovo imponendo le condizioni iniziali

$$
\begin{cases}
I_0=k_1e^0+k_2e^0\Rightarrow k_1+k_2=I_0\\
\frac{V_0}{L}=k_1s_1+k_2s_2
\end{cases}
$$

Facendo i calcoli per sostituzione trovo $k_1$ e $k_2$

Caso 2: $\alpha<\omega_0$   con smorzamento critico

La soluzione è del tipo $i_l(t)=(k_1+k_2t)e^{st}$

Condizioni iniziali per trovare $k_1$ e $k_2$

$$
\begin{cases}
I_0=k_1\\
\frac{V_0}{L}=k_2+k_1s
\end{cases}
$$

Caso 3: $\alpha<\omega_0$   sottosmorzato

Soluzione del tipo: $i_l(t)=k_1e^{s_1t}+k_2e^{s_2t}$, $t\ge0$

Ma $k_1$ e $k_2$ sono complessi e coniugati, difficili da trovare, quindi sono equivalenti le forme:

$$
i_l(t)=A_1e^{-\alpha t}\cos(\omega_dt)+A_2e^{-\alpha t}\sin(\omega_dt)
$$

oppure

$$
i_l(t)=Be^{-\alpha t}\cos(\omega_d t+\theta)
$$

con $\omega_d=\frac{2\pi}{T_d}$, $T_d$ pseudoperiodo

Caso 4: $\alpha\to0$   Ideale, oscillazione permanente

$s_{1,2}=\pm j\omega_0$

Soluzioni:

$$
i_l(t)=k_1e^{s_1t}+k_2e^{s_2t}\\
i_l(t)=A_1\cos(\omega_0 t)+A_2\sin(\omega_0t)\\
i_l(t)=A\cos(\omega_0t+\theta)
$$

### Risposta Completa RLC

![Untitled](Elettrotecnica/imgs/Untitled%2037.png)

$$
i_L(0)=I_0\\
v_c(0)=V_0
$$

Sappiamo che $i_L(t)=k_1e^{s_1t}+k_2e^{s_2t}+I_S$, $t\ge0$

Impongo le condizioni iniziali

$$
\begin{cases}
I_0=k_1+k_2+I_s\\
\frac{V_0}{L}=k_1s_1+k_2s_2
\end{cases}
$$

Risposta completa = risposta stato zero + risposta ingresso zero

### Funzioni Periodiche

Definizione $x(t+kT)=x(t)$, con $T$= periodo, $f=\frac1T$= frequenza

Valore medio in un periodo $X_m=\frac1T\int\limits_{t}^{t+T}x(t')dt'$

Valore efficace $X=\sqrt{\frac1T\int\limits_t^{t+T}x^2(t')dt'}$

Quando il valore medio è 0, si parla di funzioni alternative

$$
X_m'=\frac1{\frac T2}\int\limits_{t_0}^{t_0+\frac T2}x(t')dt\qquad\text{ con }t_0\text{ scelto in modo da massimizzare il risultato}
$$

Fattore di forma: $K_f=\frac{\text{valore efficace}}{\text{valore medio in }\frac T2}=\frac X{X'_m}$

### Funzioni sinusoidali

Sottoclasse delle funzioni alternative

Funzioni del tipo $a(t)=A_M\sin(\omega t+\alpha)$   

$A_M\to\text{Ampiezza}$, $\text{pulsazione angolare }\omega=\frac{2\pi}{T}=2\pi f$, $\alpha\to \text{fase propria/iniziale}$

Valore efficace: $A=\frac{A_M}{\sqrt{2}}$

Valore medio: $A'_m=\frac2\pi A_M$

Fattore di forma: $K_f=\frac\pi{2\sqrt{2}}\approx 1.11$

Una funzione sinusoidale dipende da $A_M,\ \omega,\ \alpha$. Per le sinusoidi isofrequenziali ($\omega$  uguale), possiamo usare il piano di Gauss per rappresentarle

![Untitled](Elettrotecnica/imgs/Untitled%2038.png)

Per questo le sinusoidi isofrequenziali possono essere messe in corrispondenza biunivoca con i numeri complessi.

$$
a(t)=A_M\sin(\omega t+\alpha)\Leftrightarrow  A_M e^{j\alpha}=\overline{A}
$$

Il numero complesso prende il nome di FASORE

Con i fasori si possono scrivere le funzioni 

$$
a(t)=A_M\sin(\omega t+\alpha)=Im[\overline Ae^{j\omega t}]\\
b(t)=B_M\cos(\omega t+\beta)=Re[\overline Be^{jwt}]
$$

### Derivata e primitiva di un fasore

Sia $a(t)=A_M\sin(\omega t+\alpha)$

Derivata

$$
\frac{da}{dt}=A_M\cos(\omega t+\alpha)=A_M\omega\sin(\omega t+\alpha+\frac\pi2)
$$

Sia $\overrightarrow A$ il fasore della derivata

$$
\overrightarrow A=\omega A_Me^{j(\alpha+\frac\pi2)}=\omega A_Me^{j\alpha}\overbrace{e^{j\frac\pi2}}^j=j\omega A_Me^{j\alpha}\quad \text{quindi}\quad \overrightarrow A=j\omega\overline A
$$

Integrale

$$
\int a(t)dt=\int A_M\sin(\omega t+\alpha)dt=-\frac1\omega A_M\cos(\omega t+\alpha)=\frac{A_M}\omega\sin(\omega t+\alpha-\frac\pi2)
$$

Sia $\overrightarrow A$ il fasore della primitiva

$$
\overrightarrow A=\frac{A_M}\omega e^{j(\alpha-\frac\pi2)}=\frac{A_M}\omega e^{j\alpha}e^{-j\frac\pi2}=\frac1{\omega e^{j\frac\pi2}}A_Me^{j\alpha}=\frac1{j\omega}\overline A\quad\text{quindi }\overrightarrow A=\frac1{j\omega}
$$

$$
\frac d{dt}\Rightarrow j\omega\qquad \int(\cdot)dt\Rightarrow \frac1{j\omega}
$$

### Relazioni costitutive simboliche dei bipoli nel dominio fasoriale

Resistore

$$
v(t)=Ri(t)\quad\text{diventa }\quad \overline V=R\overline I;\ \overline I=G\overline V
$$

Condensatore

$$
i(t)=C\frac{dv(t)}{dt}\quad\text{diventa}\quad \overline I=Cj\omega\overline V
$$

Induttore

$$
v(t)=L\frac{di(t)}{dt}\quad\text{diventa}\quad \overline V=Lj\omega\overline I
$$

Impedenza

Operatore complesso $\dot Z=\frac{\overline V}{\overline I_s}$

Ammettenza

Operatore complesso $\dot Y=\frac{\overline I}{\overline V}$

Reattanza:  $X=Im[\dot Z]$

Suscettanza:  $B=Im[\dot Y]$

Resistori

$$
\overline V=R\overline I\\
\Downarrow\\
\dot Z=R\\

$$

$$
\overline I=G\overline V\\
\Downarrow\\
\overline Y=G
$$

Induttori

$$
\overline V=j\omega L\overline I\\
\Downarrow\\
\dot Z=j\omega L\\
X=\omega L >0\\
\dot Z_L=jX_L
$$

$$
\overline I=-\frac{j}{\omega L}\overline V\\
\Downarrow\\
\dot Y=-\frac{j}{\omega L}\\
B=-\frac{1}{\omega L}<0\\
\dot Y_L=jB_L
$$

Condensatori

$$
\overline I=j\omega C\overline V\\
\Downarrow\\
\dot Y=j\omega C\\
B_c=\omega C\\
Y=jB_c
$$

$$
\overline V=-\frac{j}{\omega C}\overline I\\
\Downarrow\\
\dot Z=-\frac{j}{\omega C}\\
X_c=-\frac{1}{\omega C}\\
\dot Z = jX_c
$$

### Circuito RC

![Untitled](Elettrotecnica/imgs/Untitled%2039.png)

$$
\text{Ipotesi: }\begin{cases}
v_s(t)=V_M\sin(\omega t)\\
LKT:\ v_s=v_R+v_c
\end{cases}
$$

Vediamo anche  $i_R=C\frac{dv_c}{dt}=i=i_c$

Quindi andiamo a sostituire:

$$
\begin{cases}
v_s=RC\frac{dv_c}{dt}+v_c\\
v_c(0)=V_0
\end{cases}\Rightarrow
RC\frac{dv_c}{dt}+v_c=V_M\sin(\omega t)\Rightarrow v_c(t)=V_{ch}(t)+V_{cp}(t)
$$

Con $V_{cp}=V_{CM}\sin(\omega t+\theta)$ e $V_{CM}$ e $\theta(\text{fase)}$ da determinare, ed è $V_{cp}$ che andiamo a trovare con il circuito simbolico:

![Untitled](Elettrotecnica/imgs/Untitled%2040.png)

Calcoliamo:

$$
\overline I=\frac{\overline V_s}{R-\frac{j}{\omega C}}
$$

$$
v_{cp}(t)=\overline V_c=-\frac{j}{\omega C}\overline I=-\frac{j}{\omega C}\frac{\overline V_s}{R-\frac{j}{\omega C}}
$$

### Diagramma Fasoriale

Da fare

### Circuito RL Parallelo

![Untitled](Elettrotecnica/imgs/Untitled%2041.png)

$$
\text{Ipotesi }\begin{cases}
i_s(t)=I_M\sin(\omega t)\rightarrow \overline I_S=I_Me^{j0}=I_M\\
\dot Z_R=R\\
\dot Y_R=G\\
\dot Z_L=j\omega L\\
\dot Y_L=-\frac{j}{\omega L}
\end{cases}
$$

Con la LKC : $\overline I_S=\overline I_R+\overline I_L$

E da definizione abbiamo $\dot Z=\frac{\overline V}{\overline I_S};\ \dot Z\overline I_S=\overline V$ 

Ricaviamo caviamo 

$$
\dot Y=G+(-\frac{j}{\omega L})=|\dot Y|e^{j\phi_y}\qquad |\dot Y|=\sqrt{G^2+\bigg(\frac{1}{\omega L}\bigg)^2}\qquad \phi_y=\arctan(-\frac{1}{\omega L G})
$$

$$
\dot Z=\frac1{\dot Y}=\frac{1}{G-\frac j{\omega L}}=|Z|e^{j\phi_z}\qquad |Z|=\frac{1}{|Y|}=\frac{1}{\sqrt{G^2+\bigg(\frac{1}{\omega L}\bigg)^2}}\qquad \phi_z=-\phi_y=\arctan(\frac1{\omega LG})
$$

### Diagramma Fasoriale

Da fare

### Circuito RLC

![Untitled](Elettrotecnica/imgs/Untitled%2042.png)

$$
\text{Ipotesi }\begin{cases}
v_0(t)=V_M\sin(\omega t)\rightarrow \overline V_S=V_M\\
\dot Z_R=R\\
Z_c=\frac{1}{j\omega C}=-\frac{j}{\omega C}\\
Z_L=j\omega L
\end{cases}
$$

Per la LKT: $\overline V_S=\overline V_R+\overline V_C+\overline V_L$

E Calcoliamo

$$
\dot Y=\frac1{\dot Z}\quad \dot Z=R+j\omega L-\frac j{\omega C}\\\ \\
\dot Y=\frac1{R+j\omega L-\frac j{\omega C}}=\frac1{R+j(\omega L-\frac 1{\omega C})}
$$

Caso 1: $\omega L>\frac1{\omega C}$ IL generatore vedrà una ammettenza ohmico-induttiva

$$
X_{eq}=\omega L-\frac{1}{\omega C}>0
$$

Caso 2: $\omega L<\frac1{\omega C}$   Il generatore vedrà una ammettenza ohmico-capacitiva

$$
X_{eq}=\omega L-\frac{1}{\omega C}<0
$$

Caso 3: $\omega L=\frac1{\omega C}\Rightarrow\omega=\omega_0=\frac1{\sqrt{LC}}$ Il generatore vedrà una ammettenza puramente ohmica

$$
X_{eq}=0
$$

Il bipolo LC è equivalente ad un corto circuito

### Potenza di un bipolo

![Untitled](Elettrotecnica/imgs/Untitled%2043.png)

$$
\text{Ipotesi }\begin{cases}
v(t)=V_M\sin(\omega t+\phi_v)\rightarrow \overline V=V_Me^{j\omega \phi_v}\\
i(t)=I_M\sin(\omega t+\phi_i)\rightarrow \overline I=I_Me^{j\omega \phi_i}
\end{cases}
$$

La potenza sarà:

$$
p(t)=v(t)i(t)=V_M\sin(\omega t+\phi_v)I_M\sin(\omega t+\phi_i)
$$

Ricordando che $\sin(\alpha)\sin(\beta)=\frac12[\cos(\alpha-\beta)-\cos(\alpha+\beta)]$

$$
p(t)=\frac12V_MI_M\cos(\phi_v-\phi_i)-\frac12V_MI_M\cos(2\omega t+\phi_v+\phi_i)
$$

Dalla definizione di impedenza abbiamo $\phi_Z=\phi_v-\phi_i=\phi$, e definiamo $\cos(\phi)$ fattore di potenza

$$
p(t)=\frac12V_MI_M\cos(\phi)-\frac12V_MI_M\cos(2\omega t+\phi_v+\phi_i)
$$

Si osserva che la potenza è una funzione sinusoidale con pulsazione doppia sommata ad una costante. Si dimostra che la costante equivale alla potenza media.

Infatti

$$
P=\frac1T\int\limits_t^{t+T}p(t)dt=\frac12V_MI_M\cos(\phi)
$$

Quindi

$$
p(t)=\underbrace{P}_{\text{pot. media}}-\underbrace{\frac12V_MI_M\cos(2\omega t+\phi_v+\phi_i)}_{\text{pot. fluttuante}}
$$

### Potenza nel resistore

$$
\overline V=R\overline I\Rightarrow\phi_v=\phi_i\Rightarrow\phi=\phi_v-\phi_i=0\Rightarrow\cos(\phi)=1
$$

$$
p(t)=\frac12V_MI_M[1-\cos(2\omega t+2\phi_v)]\ge0
$$

dove $\frac12V_MI_M=\frac12RI_M^2$

### Potenza nell’induttore

$$
\overline V=j\omega LI\Rightarrow\phi_v=\frac\pi2+\phi_i\Rightarrow\phi=\phi_v-\phi_i=\frac\pi2\Rightarrow\cos(\phi)=0
$$

$$
p(t)=-\frac12V_MI_M\cos(2\omega t+2\phi_i+\frac\pi2)
$$

dove $\frac12V_MI_M=\frac12\omega LI_M^2$

### Potenza nel condensatore

$$
\overline V=-\frac j{\omega C}\overline I_M\Rightarrow\phi_v=\phi_i-\frac\pi2\Rightarrow\phi=-\frac\pi2\Rightarrow\cos\phi=0
$$

$$
p(t)=-\frac12V_MI_M\cos(2\omega t+2\phi_i-\frac\pi2)
$$

dove $\frac12V_MI_M=\frac12V_M^2\omega C$

### Energia in un intervallo temporale $\Delta t>>t$

$$
\Epsilon(\Delta t)=\int\limits_{\Delta t}p(t)dt=\int\limits_{\Delta t}Pdt-\int\limits_{\Delta t}\frac12V_MI_M\cos(2\omega t+\phi_v+\phi_i)dt=\\\ \\
=P\Delta t-\frac12V_MI_M\frac1{2\omega}\sin(2\omega t+\phi_v+\phi_i)\big|_{\Delta t}=\\\ \\
=P\Delta t-\frac{V_MI_M}{8\pi}T\sin\underbrace{(2\omega t+\phi_v+\phi_i)}_{-1<...<1}
$$

Quindi

$$
E(\Delta t)\le P\Delta t+\frac{V_MI_M}{8\pi}T=\frac12V_MI_M\cos(\phi)\Delta t+\frac12V_MI_M\frac{T}{4\pi}=\\\ \\
=\frac12V_MI_M\bigg[\cos(\phi)\Delta t+\frac T{4\pi}\bigg]
$$

$$
E(\Delta t)\simeq P\Delta t
$$

### Potenza Complessa

![Untitled](Elettrotecnica/imgs/Untitled%2044.png)

Definiamo potenza complessa $\dot S=P+jQ$

Ricordiamo (?) che $V_{eff}=\frac{V_M}{\sqrt{2}}$ ed $\frac{I_M}{\sqrt{2}}$, allora

$$
|\dot S|=\frac 12V_MI_M=V_{eff}I_{eff}\\\ \\
\tan\phi_S=\frac QP=\frac{\sin\phi}{\cos\phi}\Rightarrow\phi_S=\phi
$$

Per dimostrare la seguente uguaglianza $\dot S=\frac12\overline V\ \overline I^*$

$$
\dot S=\frac12V_Me^{j\phi_v}I_Me^{-j\phi_i}=\frac12V_MI_Me^{j(\phi_v-\phi_i)}=\frac12V_MI_Me^{j\phi}=P+jQ
$$

Resistore $Z=R,\ Y=G$

$$
P_R=\frac12R|I|^2=RI^2=\frac12G|V|^2=GV^2\\
Q_r=0
$$

Induttore $Z=j\omega L,\ Y=-\frac j{\omega L}$

$$
P_L=0\\
Q_L=\frac12|I|^2\omega L=\frac12|V|^2\frac1{\omega L}>0
$$

Condensatore $Z=-\frac{j}{\omega C},\ Y=j\omega C$

$$
P_c=0\\
Q_c=-\frac12\frac{|I|^2}{\omega C}=-\frac12|V|^2\omega C<0
$$

### Potenza Attiva e Reattiva

$$
p(t)=P-\frac12V_MI_M\cos(2\omega t+\phi_v+\phi_i-\phi_i+\phi_i)=\\
=P-\frac12V_MI_M\cos[\phi+(2\omega t+2\phi_i)]=\\
=\frac12V_MI_M\cos\phi-\frac12V_MI_M[\cos\phi\cos(2\omega t+2\phi_i)-\sin\phi\sin(2\omega t+2\phi_i)]=\\
=\frac12V_MI_M\cos\phi[1-\sin(2\omega t+2\phi_i)]+\frac12V_MI_M\sin\phi[1-\sin(2\omega t+2\phi_i)]
$$

Posto 

$$
P=\frac12V_MI_M\cos\phi\quad\text{Potenza attiva}\\
Q=\frac12V_MI_M\sin\phi\quad\text{Potenza reattiva}
$$

$$
p(t)=\underbrace{P[1-\cos(2\omega t+2\phi_i)]}_{\text{pot. attiva istantanea}}+\underbrace{Q\sin(2\omega t+\phi_i)}_{\text{pot. reattiva istantanea}}
$$

### Teorema di Boucherot

![Untitled](Elettrotecnica/imgs/Untitled%2045.png)

$$
\dot S_1=\dot S_C\\
\dot S_2=\dot S_C+\dot S_B=\dot S_B+\dot S_1\\
\dot S_3=\dot S_A+\dot S_B+\dot S_C=\dot S_A+\dot S_2
$$

### Rifasamento

Il rifasamento consiste nel cercare di fornire localmente all’utilizzatore la potenza reattiva necessaria, così da lasciare al distributore solo l’onere di fornire la potenza attiva

### Rifasamento a tensione costante (circuito ohmico-induttivo)

![Untitled](Elettrotecnica/imgs/Untitled%2046.png)

Per ipotesi $X>0$

Stabiliamo inoltre che:

1. $R+jX$ non può cambiare
2. $P_u$ non può cambiare e deve essere fornita dal distributore
3. $\overline I_L$ dovrà mantenere costante la sua componente in fase con $\overline V_S$

L’obiettivo è trovare un condensatore che eroghi la potenza reattiva necessaria, ovvero $|Q_C|=Q\Rightarrow|Q_C|=\omega CV_S^2\Rightarrow$ 

$$
\Rightarrow C=\frac{Q}{\omega V_S^2}=\frac{P\tan\phi}{\omega V_S^2}
$$

![Untitled](Elettrotecnica/imgs/Untitled%2047.png)

### Rifasamento parziale

In questo caso non forniamo localmente tutta la potenza reattiva

$$
Q=P\tan\phi;\ Q'=P\tan\phi'\Rightarrow\omega CV_S^2=P\tan\phi-P\tan\phi'\\\ \\
C=\frac{P[\tan\phi-\tan\phi']}{\omega V_S^2}
$$

### Potenza Massima in regime sinusoidale

![Untitled](Elettrotecnica/imgs/Untitled%2048.png)

$$
P=\frac12Re(Z)|I|^2\quad I=\frac{\overline E_T}{\dot Z_T+\dot Z}\\\ \\
\overline Z_T=Re(Z_T)+jX_T
$$

L’obiettivo è trovare $\dot Z$ in modo da massimizzare $P$

$$
I=\frac{\overline E_T}{Z_T+Z}=\frac{\overline E_T}{Re(Z_T)+jX_T+Re(Z)+jX}=\frac{\overline E_T}{Re(Z_T+Z)+j(X_T+X)}
$$

$$
P=\frac12Re(Z)\frac{\overline E_T^2}{[Re(Z_T+Z)]^2+(X_T+X)^2}
$$

Otteniamo una $P$  maggiore se $X_T+X=0\Rightarrow X=-X_T$

Passando alla parte reale

$$
P=\frac12|E_T|^2\frac{Re(Z)}{[Re(Z_T)+Re(Z_T)]^2}
$$

Studio la derivata ponendola a zero

$$
\frac{dP}{dRe(Z)}=\frac12|E_T|^2\frac{[Re(Z_T)+Re(Z)]^{\cancel 2}-2Re(Z)\cancel{[Re(Z_T)+Re(Z)]}}{[Re(Z_T)+Re(Z)]^{\cancel 4\ 3}}=0
$$

$$
\frac12|E_T|^2\frac{Re(Z_T)-Re(Z)}{[Re(Z_T)+Re(Z)]^3}=0\Leftrightarrow Re(Z)=Re(Z_T)
$$

Quindi $P$ è massima $\Leftrightarrow\ Z=Re(Z_T)+j(-X_T)=Z_T^*$

E per calcolare il rendimento

$$
P_{max}=\frac12|E_T|^2\frac{Re(Z_T)}{4Re(Z_T)^2}=\frac{|E_T|^2}{8Re(Z_T)}\\
P_{genx}=\frac12|E_T||I|\cos \underbrace{(E_T\land I)}_{=\ 0}=\frac12|E_T|\frac{|E_T|}{2Re(Z_T)}=\frac{|E_T|^2}{4Re(Z_T)}
$$

$$
\mu=\frac{P_{max}}{P_{genx}}=\frac12
$$

### Sistema trifase

Sistema di 3 grandezze sinusoidali isofrequenziali, di uguale ampiezza e sfasate di 120 gradi

Generatore trifase:

![Untitled](Elettrotecnica/imgs/Untitled%2049.png)

Con

$$
a=E_M\sin(\omega t)\\
b=E_M\sin(\omega t+\frac23\pi)\\
c=E_M\sin(\omega t+\frac43\pi)
$$

![Untitled](Elettrotecnica/imgs/Untitled%2050.png)

$$
\text{Tensioni di fase:}\begin{cases}
\overline E_1=E_Me^{j0}\\
\overline E_2=E_Me^{j\frac23\pi}\\
\overline E_3=E_Me^{j\frac43\pi}
\end{cases}\\\ \\
\text{Tensioni di linea:}\begin{cases}
\overline V_{12}=\overline E_1-\overline E_2\\
\overline V_{23}=\overline E_2-\overline E_3\\
\overline V_{31}=\overline E_3-\overline E_1
\end{cases}
$$

### Carico trifase a stella

![Untitled](Elettrotecnica/imgs/Untitled%2051.png)

Per il teorema di Millman otteniamo

$$
V_{oo'}=\frac{\frac{\overline E_1}{Z}+\frac{\overline E_2}{Z}+\frac{\overline E_3}{Z}}{\frac1Z+\frac1Z+\frac1Z}=\frac{\frac1Z(\overline E_1+\overline E_2+\overline E_3)}{\frac1Z+\frac1Z+\frac1Z}=0
$$

$$
\overline I_1=\frac{\overline E_1}{Z},\qquad \overline I_2=\frac{\overline E_2}{Z},\qquad \overline I_3=\frac{\overline E_3}{Z}
$$

### Carico trifase e triangolo

![Untitled](Elettrotecnica/imgs/Untitled%2052.png)

$$
\begin{cases}
\overline I_{12}=\frac{\overline V_{12}}{\dot Z}\\
\overline I_{23}=\frac{\overline V_{23}}{\dot Z}\\
\overline I_{31}=\frac{\overline V_{31}}{\dot Z}
\end{cases}\Rightarrow
\begin{cases}
\overline I_1=\overline I_{12}-\overline I_{31}\\
\overline I_2=\overline I_{23}-\overline I_{23}\\
\overline I_3=\overline I_{31}-\overline I_{23}
\end{cases}
$$

### Carico trifase squilibrato a stella

![Untitled](Elettrotecnica/imgs/Untitled%2053.png)

$$
V_{oo'}=\frac{\frac{\overline E_1}{Z_1}+\frac{\overline E_2}{Z_2}+\frac{\overline E_3}{Z_3}}{\frac1{Z_1}+\frac1{Z_2}+\frac1{Z_3}}\neq0
$$

$$
\overline I_1=\frac{\overline E_1'}{Z_1},\qquad \overline I_2=\frac{\overline E_2'}{Z_2},\qquad \overline I_3=\frac{\overline E_3'}{Z_3}
$$

$$
\overline E_1'=\overline E_1-V_{oo'}\qquad \overline E_2'=\overline E_2-V_{oo'}\qquad \overline E_3'=\overline E_3-V_{oo'}
$$

Sistema non utilizzabile in un sistema di distribuzione, poichè non si possono garantire tensioni nominali in un range predefinito

### Carico trifase squilibrato a stella e conduttore neutro

![Untitled](Elettrotecnica/imgs/Untitled%2054.png)

Introduciamo il conduttore neutro

$$
V_{oo'}=\frac{\frac{\overline E_1}{Z_1}+\frac{\overline E_2}{Z_2}+\frac{\overline E_3}{Z_3}}{\frac1{Z_1}+\frac1{Z_2}+\frac1{Z_3}+\frac1{Z_N}}=\dot Z_N\overline I_N
$$

Con $Z_N$ piccola $V_{oo'}\to0\Rightarrow$

$$
\Rightarrow\begin{cases}
\overline E_1'=\overline E_1-V_{oo'}\simeq\overline E_1\\
\overline E_2'=\overline E_2-V_{oo'}\simeq\overline E_2\\
\overline E_3'=\overline E_3-V_{oo'}\simeq\overline E_3
\end{cases}
$$

In questo caso possiamo garantire che al tensione di linea sia in un determinato range a prescindere dai carichi

### Carico trifase squilibrato a triangolo

![Untitled](Elettrotecnica/imgs/Untitled%2055.png)

$$
\begin{cases}
I_{12}=\frac{\overline V_{12}}{\dot Z_{12}}\\
I_{23}=\frac{\overline V_{23}}{\dot Z_{23}}\\
I_{31}=\frac{\overline V_{31}}{\dot Z_{31}}
\end{cases}\Rightarrow\begin{cases}
\overline I_1=\overline I_{12}-\overline I_{31}\\
\overline I_2=\overline I_{23}-\overline I_{12}\\
\overline I_3=\overline I_{31}-\overline I_{23}
\end{cases}
$$

### Potenza trifase

![Untitled](Elettrotecnica/imgs/Untitled%2056.png)

Nel caso generale abbiamo

$$
\begin{cases}
e_1=E_M\sin(\omega t)\\
e_2=E_M\sin(\omega t - \frac23\pi)\\
e_3=E_M\sin(\omega t-\frac 43\pi)
\end{cases}\quad e\quad
\begin{cases}
i_1=I_{M_1}\sin(\omega t+\phi_1)\\
i_2=I_{M_2}\sin(\omega t+\phi_2-\frac23\pi)\\
i_3=I_{M_3}\sin(\omega t+\phi_3-\frac43\pi)
\end{cases}
$$

Sappiamo che $p(t)=e_1i_1+e_2i_2+e_3i_3\Rightarrow$

$$
\Rightarrow p(t)=E_MI_{M_1}\sin(\omega t)\sin(\omega t+\phi_1)+E_MI_{M_2}\sin(\omega t-\frac23\pi)\sin(\omega t+\phi_2-\frac23\pi)+\\
+E_MI_{M_3}\sin(\omega t-\frac43\pi)\sin(\omega t+\phi_3-\frac43\pi)=
$$

ricordando che $\sin\alpha\sin\beta=\frac12[\cos(\alpha-\beta)-\cos(\alpha+\beta)]$

$$
=\frac12E_MI_{M_1}[\cos(\phi_1)-\cos(2\omega t+\phi_1)]+\\
+\frac12E_MI_{M_2}[\cos(\phi_2)-\cos(2\omega t+\phi_2-\frac43\pi)]+\\
+\frac12E_MI_{M_3}[\cos(\phi_3)-\cos(2\omega t+\phi_3-\frac83\pi)]
$$

Vediamo che 

$$
P=P_1+P_2+P_3=\frac12E_MI_{M_1}\cos(\phi_1)+\frac12E_MI_{M_2}\cos(\phi_2)+\frac12E_MI_{M_3}\cos(\phi_3)
$$

$$
Q=Q_1+Q_2+Q_3=\frac12E_MI_{M_1}\sin(\phi_1)+\frac12E_MI_{M_2}\sin(\phi_2)+\frac12E_MI_{M_3}\sin(\phi_3)
$$

$$
\dot S=\frac12\overline E_1\overline I_1^*+\frac12\overline E_2\overline I_2^*+\frac12\overline E_3\overline I_3^*=P+jQ
$$

### Potenza trifase con carico simmetrico ed equilibrato

Nel caso simmetrico equilibrato abbiamo

$$
\begin{cases}
e_1=E_M\sin(\omega t)\\
e_2=E_M\sin(\omega t - \frac23\pi)\\
e_3=E_M\sin(\omega t-\frac 43\pi)
\end{cases}\quad e\quad
\begin{cases}
i_1=I_{M}\sin(\omega t+\phi)\\
i_2=I_{M}\sin(\omega t+\phi-\frac23\pi)\\
i_3=I_{M}\sin(\omega t+\phi-\frac43\pi)
\end{cases}
$$

La potenza sarà

$$
p(t)=E_MI_M\sin(\omega t)\sin(\omega t+\phi)+E_MI_M\sin(\omega t-\frac23\pi)\sin(\omega t+\phi-\frac23\pi)+E_MI_M\sin(\omega t-\frac43\pi)\sin(\omega t+\phi-\frac43\pi)=
$$

ricordando che $\sin\alpha\sin\beta=\frac12[\cos(\alpha-\beta)-\cos(\alpha+\beta)]$

$$
=\frac12E_MI_M[\cos(\phi)-\underline{\cos(2\omega t+\phi)}]+\\
+\frac12E_MI_M[\cos(\phi)-\underline{\cos(2\omega t+\phi-\frac43)}]+\\
+\frac12E_MI_M[\cos(\phi)-\underline{\cos(2\omega t+\phi-\frac83\pi)}]
$$

*queste sinusoidi sono isofrequenziali $(2\omega t+\phi)$, ma sfasate di $120^o$, quindi la loro somma è nulla

Vediamo che la potenza istantanea coincide con la potenza media

$$
P=P_1+P_2+P_3=3[\frac12E_MI_M\cos(\phi)]\Rightarrow\text{passando ai valori efficaci}\Rightarrow\\
\Rightarrow P=3EI\cos(\phi)
$$

quindi $p(t)=P=3EI\cos(\phi)$  costante nel tempo

Per calcolare la potenza reattiva si deve andare a vedere nel circuito specifico

### Potenza massima con adattamento

Avendo

![Untitled](Elettrotecnica/imgs/Untitled%2057.png)

Con $\dot Z\neq\dot Z_T^*$

Come otteniamo il massimo trasferimento di potenza?

Aggiungiamo un trasformatore ideale e il problema diventa:

![Untitled](Elettrotecnica/imgs/Untitled%2058.png)

dimensionare $n$ e $B$ tali che $\dot Z_{11}=\dot Z_T^*$

Ricordando le relazioni del trasformatore: $\frac{\overline V_1}{\overline V_2}=n\quad \frac{\overline I_1}{\overline I_2}=-\frac1n\quad \dot Z_{11'}=n^2\dot Z_{22'}$

$$
\dot Z_{11}=\frac1{\dot Y_{22'}}=\frac1{jB+\frac1{\dot Z}}=\frac1{jB+\dot Y}
$$

Imponiamo $\dot Z_{11}=\dot Z_T^*=Re(\dot Z_T)-jIm(\dot Z_T)$

E otteniamo 

$$
\dot Z_{11}=n^2\dot Z_{22'}=Re(\dot Z_T)-jIm(\dot Z_T)
$$

$$
\frac{n^2}{\frac1{\dot Z}+jB}=Re(Z_T)-jIm(Z_T)\\\ \\
\frac{n^2}{Re(Y)+jIm(Y)+jB}=Re(Z_T)-jIm(Z_T)\\\ \\
\frac{n^2[Re(Y)-jIm(Y)]}{Re^2(Y)+[Im(Y)+B]^2}=Re(Z_T)-jIm(Z_T)
$$

Trasformiamo questa relazione vettoriale in un sistema

$$
\begin{cases}
\frac{n^2Re(Y)}{Re^2(Y)+[Im(Y)+B]^2}=Re(Z_T)\\
\frac{n^2Im(Y)}{Re^2(Y)+[Im(Y)+B]^2}=Im(Z_T)
\end{cases}
$$

sistema a 2 incognite con 2 equazioni. B si trova facendo il rapporto delle equazioni, n di conseguenza.

### Induttori accoppiati

![Untitled](Elettrotecnica/imgs/Untitled%2059.png)

Due bobine vicine creano un accoppiamento magnetico. Le correnti di ogni bobine generano un campo magnetico che attraversa entrambe le bobine.

Distinguiamo in vari flussi: $\phi_{ij},$ flusso attraverso la bobina $i$ dovuto alla corrente $j$

$$
\phi_{11}=L_1i_1,\quad \phi_{12}=M_{12}i_2,\quad \phi_{21}=M_{21}i_1,\quad \phi_{22}=L_2i_2
$$

Supponendo entrambe le correnti attive

$$
\begin{matrix}
\phi_1=L_1i_1+Mi_2\\
\phi_2=Mi_1+L_2i_2
\end{matrix}\quad\text{dove}\quad
\begin{matrix}
L_i:\text{auto induttanza dedlla bobina }i\\
M:\text{mutua induttanza}
\begin{cases}
M>0\Leftarrow i_1\ e\ i_2\text{ concordi}\\
M<0\Leftarrow i_1\ e\ i_2\text{ discordi}
\end{cases}
\end{matrix}
$$

Per la legge di Faraday

$$
\begin{cases}
v_1(t)=\frac{d\phi_1}{dt}=L_1\frac{di(t)}{dt}+M\frac{di(t)}{dt}\\
v_2(t)=\frac{d\phi_2}{dt}=L_2\frac{di(t)}{dt}+M\frac{di(t)}{dt}
\end{cases}
$$

Da cui possiamo ricavare le relazioni inverse

$$
\begin{bmatrix}
V_1\\
V_2
\end{bmatrix}=\begin{bmatrix}
L_1&M\\
M&L_2
\end{bmatrix}\begin{bmatrix}
\frac{di_1(t)}{dt}\\
\frac{di_2(t)}{dt}
\end{bmatrix}\Rightarrow
\begin{bmatrix}
\frac{di_1(t)}{dt}\\
\frac{di_2(t)}{dt}
\end{bmatrix}=\frac1{\Delta}\begin{bmatrix}
L_2&-M\\
-M&L_1
\end{bmatrix}\begin{bmatrix}
V_1\\
V_2
\end{bmatrix}\Rightarrow\\\ \\
\Rightarrow\begin{cases}
i_1(t)=i(0)+\frac1\Delta\int\limits_0^tL_2v_1(t)-Mv_2(t')dt'\\
i_2(t)=i(0)+\frac1\Delta\int\limits_0^t-Mv_1(t)+L_1v_2(t')dt'
\end{cases}
$$

Definendo le seguenti induttanze reciproche:

$$
\begin{matrix}
\Gamma_{11}=\frac{L_2}{\Delta}&
\Gamma_{12}=-\frac{M}{\Delta}\\
\Gamma_{21}=-\frac{M}{\Delta}&
\Gamma_{22}=\frac{L_1}{\Delta}
\end{matrix}\Rightarrow
\begin{cases}
i_1(t)=i_1(0)+\Gamma_{11}\int\limits_0^tv_1(?)dt' + \Gamma_{12}\int\limits_0^tv_2(t')dt'\\
i_2(t)=i_2(0)+\Gamma_{21}\int\limits_0^tv_1(?)dt' + \Gamma_{22}\int\limits_0^tv_2(t')dt'
\end{cases}
$$

Energia immagazzinata nel sistema:

$$
E(t)=\int\limits_0^t(v_1i_i+v_2i_2)dt=\int\limits_2^?(L_1i_1di_1+Mi_1di_2)+(Mi_2di_1+L_2i_2di_2)=\\\ \\
=\int\limits_o^{I_1}L_1i_1di_1+\int\limits_0^{I_1I_2}Md(i_1i_2)+\int\limits_0^{I_2}L_2i_2di_2=\\\ \\
=\frac12L_1I_1^2+MI_1I_2+\frac12L_2I_2^2
$$

Affinché l’energia non sia negativa $\Rightarrow |M|<\sqrt{L_1L_2}$

Definiamo $k$ misura dell’accoppiamento magnatico $k=\frac{|M|}{\sqrt{L_1L_2}}$

$k=0\Rightarrow M=0\Rightarrow$ non c’è accoppiamento magnetico

$k=1\Rightarrow$ coincide con la media geometrica di $L$

$k\to1\Rightarrow$ caso ideale: accoppiamento perfetto  

![Untitled](Elettrotecnica/imgs/Untitled%2060.png)

### Risposta in frequenza

è lo studio della funzione di rete al variare della pulsazione che ci permette di determinare il comportamento filtrante del circuito