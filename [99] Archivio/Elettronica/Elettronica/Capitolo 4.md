# Capitolo 4

Amplificatore : un amplificatore è un circuito biporta in grado di innalzare il livello del segnale d’ingresso conferendo ad esso una potenza maggiore rispetto a quella che aveva in ingresso

L’amplificatore funziona con due ingressi, uno con tensione alternata, che è il segnale da amplificare, e il secondo in tensione continua che è quello che fornisce potenza all’amplificatore

elemento attivo: componente che da in uscita una potenza maggiore di quella in ingresso

elemento passivo : no

relazione di un amplificatore : $v_o(t)=Av_i(t)$ $A$ è il guadagno dell’amplificatore. Siccome vogliamo che l’ampl. sia lineare, deve essere costante

La resistenza di ingresso ($R_L$) di un amplificatore deve essere tendente a infinito così che l’amplificatore assorba tutta la potenza del generatore. E al contrario $R_S$ deve essere molto più piccola.

![Untitled](Capitolo%204/Untitled.png)

Un amplificatore operazionale è fondamentalmente un circuito integrato. 

Idealmente, presenta amplificazione di tensione (AOL) infinita, resistenza d’ingresso (Ri) infinita e resistenza d’uscita (Ro) nulla.

![Untitled](Capitolo%204/Untitled%201.png)

La relazione di un amplificatore operazionale è $v_o=A_{OL}(v_+-v_-)=-A_{OL}v_i$ con $v_i=v_--v_+$

### Funzionamento ad anello aperto

Si collega l’ingresso invertente a massa e si applica all’ingresso non invertente un segnale $v_s$. La transcaratteristica è : $v_o=A_{OL}(v_+-v_-)=A_{OL}v_s$

![Untitled](Capitolo%204/Untitled%202.png)

L’uscita di un amplificatore è limitata tra $-V_{SAT}$ e $V_{SAT}$ che sono tensioni di 1 o 2 V più piccole delle tensioni di alimentazione

Questo funzionamento è più adatto ad essere usato come comparatore, e non come amplificatore.

### Funzionamento ad anello chiuso

Visto che un amplificatore da solo non è buono per amplificare, dobbiamo inserire una rete di reazione negativa, che ci permette di rendere $A_{OL}$ stabile. 

![Untitled](Capitolo%204/Untitled%203.png)

Prendiamo l’amplificazione dell’amplificatore $A=\frac{v_o}{v_i}$ e quella del quadripolo di reazione $\beta=\frac{v_o}{v_f}$. Troviamo che la tensione di uscita corrisponde a $v_o=Av_i=A(v_s-\beta v_o)$

Quindi l’amplificazione di tutto il sistema è $A_f=\frac{v_o}{v_s}=\frac{A}{1+\beta A}$

![Untitled](Capitolo%204/Untitled%204.png)

Analizzando il funzionamento di questo sistema, ci accorgiamo che l’amplificazione risulta stabile. Assumendo che $v_s$ e $\beta$ siano costanti, nel caso in cui $A$ aumenti, abbiamo un aumento di $v_o$, che a sua volta comporta un aumento di $v_f$. Dato però che in entrata all’amplificatore $A$ c’è $v_i=v_s-v_f$, $v_i$ diminuirà e causerà un decremento di $v_o$ che nel complesso equilibrerà gli sbalzi di valore di $A$

Per un valore di A(o $\beta$) molto elevato si ha $\beta A >>1$ da cui otteniamo $A_f=\frac{A}{1+\beta A}=\frac{1}{\beta}$

L’amplificazione ad anello chiuso ha due caratteristiche:

- essendo la resistenza di ingresso molto elevata, la corrente in ingresso è trascurabile
- essendo $A_{OL}$ sempre molto elevata, qualsiasi valore della tensione d’uscita in zona lineare (-Vsat < $v_o$ < Vsat) presuppone che la tensione $v_i$ fra l’ingresso invertente e l’ingresso non invertente sia molto piccola e quindi trascurabile.

Pertanto, in zona di funzionamento lineare, i due ingressi sono sostanzialmente allo stesso potenziale, ovvero,  fra gli ingressi esiste un cortocircuito virtuale. Siccome spesso uno degli ingressi è posto a massa, si parla di massa virtuale

### Amplificatore Invertente

![Untitled](Capitolo%204/Untitled%205.png)

Fornisce in uscita un segnale amplificato invertito di fase rispetto al segnale in ingresso. 

La rete di reazione è costituita dalle resistenze R1 e R2: in particolare la resistenza R2 riporta l’uscita sull’ingresso invertente in modo tale che la reazione risulti negativa. Il circuito dell’amplificatore è equivalente al circuito seguente:

![Untitled](Capitolo%204/Untitled%206.png)

Studiando il circuito si trovano:

$$
v_o=-R_2i\\
v_s=R_1i
$$

dalle quali si ottiene: $A_f=\frac{v_o}{v_s}=\frac{-R_2i}{R_1i}=-\frac{R_2}{R_1}$

Se prendiamo come amplificatore quello con il circuito sotto riportato:

![Untitled](Capitolo%204/Untitled%207.png)

La resistenza di ingresso dell’amplificatore invertente è $R_1$. La resistenza di uscita si calcola come $\frac{v_o}{i_{sc}}$:

$$
v_o=-\frac{R_2}{R_1}v_s\\ i_{sc}=i_f-i_o=\frac{v_s}{R_1+R_2}-A_{OL}\frac{v_i}{r_o}\sim -A_{OL}\frac{v_i}{r_o}=-\frac{A_{OL}}{r_o}v_s\frac{R_2}{R_1+R_2}
$$

Quindi:

![Untitled](Capitolo%204/Untitled%208.png)

Avendo che $\frac{R_2}{R_1}>>1$, allora $R_o=r_o\frac{A_f}{A_{OL}}$

Per regolare l’amplificazione dell’amplificatore si possono dimensionare le resistenze $R_1$ ed $R_2$, ma ci sono delle considerazioni da fare:

- $R_1$ troppo basso → $R_i$  troppo bassa e quindi l’amplificatore caricherebbe troppo la sorgente $v_s$, e quindi meno amplificazione
- $R_2$ troppo basso → implica ovviamente un valore di R1 ancora più basso (se si vuole amplificazione). Inoltre, poiché un punto di R2 è connesso a massa virtuale, allora R2 si può considerare in parallelo all’uscita e se essa è confrontabile o più piccola di ro, la tensione d’uscita cade maggiormente su ro piuttosto che su R2: in tali condizioni non è più vero che vo = AOL·vi e si può facilmente dimostrare che non è più neanche vero che Af = R2 / R1;
- $R_2/R_1$ troppo alto → non si può più considerare la massa virtuale e l’effetto di reazione scompare

### Amplificatore non invertente

![Untitled](Capitolo%204/Untitled%209.png)

In questo caso il segnale in ingresso è applicato all’ingresso non invertente. La tensione all’ingresso invertente è la seguente:

$$
v_-=v_o\frac{R_1}{R_1+R_2}
$$

L’amplificazione del circuito è:

$$
A_f=\frac{v_o}{v_s}=\frac{R_1+R_2}{R_1}=1+\frac{R_2}{R_1}
$$

con $v_+=v_s$

Prendendo sempre come schema dell’amplificatore quello seguente

![Untitled](Capitolo%204/Untitled%2010.png)

Troviamo la resistenza di ingresso $R_i$

![Untitled](Capitolo%204/Untitled%2011.png)

![Untitled](Capitolo%204/Untitled%2012.png)

![Untitled](Capitolo%204/Untitled%2013.png)

### Circuiti lineari ad amplificatori operazionali

### Buffer

Adatta l’impedenza tra due circuiti

![Untitled](Capitolo%204/Untitled%2014.png)

### Amplificatore differenziale

![Untitled](Capitolo%204/Untitled%2015.png)

Per calcolare $v_o$ dobbiamo usare il principio di sovrapposizione degli effetti

- poniamo $v_1$ a 0 e troviamo la tensione di uscita $v_{o2}$, e il circuito diventa:
    
    ![Untitled](Capitolo%204/Untitled%2016.png)
    
    Quindi $v_{o2}=-\frac{R_2}{R_1}v_2$
    
- poniamo $v_2$ a zero e troviamo la tensione di uscita $v_{o1}$, e il circuito diventa:
    
    ![Untitled](Capitolo%204/Untitled%2017.png)
    
    ![Untitled](Capitolo%204/Untitled%2018.png)
    

Quindi per trovare la tensione di uscita si sommano le due parziali

$$
v_o=v_{o1}+v_{o2}=\frac{R_2}{R_1}(v_1-v_2)
$$

### Sommatore

Abbiamo due tipi di sommatori, invertente e non.

![Untitled](Capitolo%204/Untitled%2019.png)

Per quello invertente, sfruttando la massa virtuale, abbiamo che $v_o=-Ri$. Ma 

![Untitled](Capitolo%204/Untitled%2020.png)

quindi, 

![Untitled](Capitolo%204/Untitled%2021.png)

Ponendo tutte le resistenze uguali, possiamo scrivere $v_o=-\sum\limits_{i=1}^nv_{si}$

![Untitled](Capitolo%204/Untitled%2022.png)

Per quello non invertente, scriviamo che $v_o=\sum\limits_{i=1}^nv_{si}$, ponendo $R_1=R_n$ e $R=\frac{R_f}{n-1}$

### Convertitore Corrente-Tensione

![Untitled](Capitolo%204/Untitled%2023.png)

È utile per convertire i segnali provenienti da dei sensori che producono corrente. Idealmente fornisce una tensione proporzionale alla corrente in entrata, indipendentemente dalla resistenza interna Rs del generatore d’ingresso e della resistenza di carico RL. L’amplificatore ha resistenza d’ingresso e di uscita nulle. La prima in modo tale che la corrente ignori la resistenza $R_s$ del generatore, la seconda per non fare passare la corrente dal carico, poichè entra dal terminale di uscita e si chiude a massa.

La tensione di uscita vale $v_o=-R_2i_s$

### Integratore

![Untitled](Capitolo%204/Untitled%2024.png)

Sfruttando la massa virtuale, si può ottenere la tensione come $v_o=-\frac1C\int i\ dt$. Sostituendo $i=\frac {v_s} R$ ricaviamo  

![Untitled](Capitolo%204/Untitled%2025.png)

Se si applicano più ingressi con il rispettivo resistore ad un integratore si ottiene un sommatore integratore.

### Derivatore

![Untitled](Capitolo%204/Untitled%2026.png)

Anche in questo caso per la massa virtuale possiamo scrivere che $v_o=-Ri$, alla quale sostituiamo $i=C\frac{dv_s}{dt}$ e otteniamo

![Untitled](Capitolo%204/Untitled%2027.png)

### Comparatore

![Untitled](Capitolo%204/Untitled%2028.png)

Un comparatore così fatto, cioè un operazionale ad anello aperto, in uscita avrà $V_{SAT}$ se $v_s<V_R$, altrimenti $-V_{SAT}$.

Questo tipo di comparatore però è limitato e poco efficiente, per quanto riguarda tempi di risposta, alimentazione e sensibilità al rumore.

Un comparatore fatto bene è l’integrato 311

![Untitled](Capitolo%204/Untitled%2029.png)

Il componente all’uscita dell’operazionale è un BJT e si comporta da interruttore aperto se il terminale B è negativo (si dice che il BJT è in interdizione), mentre da interruttore chiuso se B è positivo (si dice che il BJT è in saturazione).

Il terminale C è l’uscita del sistema. Quando $IN_+$  è più grande di $IN_-$ allora il potenziale in B è $-V_{SAT}$, il chè comporta che all’uscita avremo la tensione che alimenta il transistore stesso. Mentre se $IN_+<IN_-$ allora l’uscita sarà collegata al terminale E, che di solito è a massa.