### Diodo a semiconduttore

![Untitled](Cap%206/Untitled.png)

La caratteristica del diodo è la seguente:

![Untitled](Cap%206/Untitled%201.png)

- Polarizzazione diretta → corrente molto alta, ma la tensione deve essere almeno 0,6 V (tensione di soglia)
- Polarizzazione inversa → corrente molto bassa dovuta solo alla corrente inversa, cioè corrente di saturazione e di perdita superficiale

La relazione del tratto a destra della zona di rottura è descritto dalla relazione

![Untitled](Cap%206/Untitled%202.png)

dove 

![Untitled](Cap%206/Untitled%203.png)

$k$  costante di Boltzmann, $T$ la temperatura assoluta, $q$ la carica dell’elettrone, $I_s$ la corrente inversa di saturazione, $\eta$ un fattore di idealità (=2 per bassa corrente, =1 per alta corrente).

### Il diodo come elemento circuitale

![Untitled](Cap%206/Untitled%204.png)

Il circuito sopra può essere descritto con la relazione $v=v_i-R_Li$. Questa rappresenta una retta nel piano $(v, i)$con pendenza $-\frac1{R_L}$. 

![Untitled](Cap%206/Untitled%205.png)

I punti di intersezione tra la retta di carico e la caratteristica del diodo vengono chiamati punti di riposo o lavoro, cioè il valore di tensione e corrente per quel diodo. 

### Modelli del diodo

Quello che abbiamo visto prima era il modo grafico per trovare i punti di riposo. esiste anche un metodo analitico, ma implicherebbe risolvere un sistema con equazioni trascendenti, il ché non è una cosa fattibile.

Per questo abbiamo un terzo metodo, ovvero quello della linearizzazione del diodo. Introduciamo il concetto di resistenza dinamica del diodo, definita come la derivata della tensione rispetto alla corrente nell’intorno del punto di riposo.

![Untitled](Cap%206/Untitled%206.png)

Se si considerano piccole variazioni di tensioni $\Delta V$ sulla caratteristica (e le corrispondenti variazioni di corrente $\Delta I$) allora la resistenza dinamica $R_f$ è circa uguale a $\frac{\Delta V}{\Delta I}$

Per $V>V_\gamma$ possiamo sostituire il tratto della caratteristica con un tratto rettilineo di pendenza $\frac{1}{R_f}$, mentre per $V<V_\gamma$ la corrente inversa è debole, quindi il diodo può essere pensato come un circuito aperto.

![Untitled](Cap%206/Untitled%207.png)

Possiamo continuare ad approssimare la caratteristica, come nei grafici sopra. Nel grafico b abbiamo ignorato la resistenza diretta della caratteristica, in quello c anche la tensione di soglia 

Per $V<V_\gamma$ possiamo considerare tutti e tre i modelli come circuiti aperti, mentre dobbiamo differenziare per $V>V_\gamma$. Nel primo caso sarà un generatore di tensione $V_\gamma$  in serie ad una resistenza $R_f$, nel secondo caso solo una sorgente di tensione, mentre nel terzo un cortocircuito.

### Circuiti raddrizzatori

![Untitled](Cap%206/Untitled%208.png)

Considerando la tensione in entrata $v_i$ come sinusoidale di ampiezza $V_{iM}$, abbiamo che:

- se $v_i>V_\gamma$ il diodo è in stato di conduzione e quindi $v_o=v_i-V_\gamma$
- se $v_i<V_\gamma$ il diodo è in stato di interdizione e quindi $v_o=0$

![Untitled](Cap%206/Untitled%209.png)

- b grafico della tensione in entrata
- c grafico della tensione in uscita prendendo il modello 6.5b
- d grafico della tensione in uscita prendendo il modello 6.5c

![Untitled](Cap%206/Untitled%2010.png)

La transcaratteristica del diodo può essere ricavata anche in modo grafico, proiettando i valori di $v_i$ sulla transcaratteristica del circuito

L’applicazione più comune per i raddrizzatori sono gli alimentatori. Questi trasformano la tensione alternata in tensione continua di valore più basso. Necessitano quindi di un trasformatore. Possiamo vedere tre tipi di alimentatori:

![Untitled](Cap%206/Untitled%2011.png)

Questo è uguale al circuito visto prima ma $v_i$ dipende dall’uscita del trasformatore. il valore medio della tensione di uscita è $\frac{V_{sM}}{\pi}$

![Untitled](Cap%206/Untitled%2012.png)

Questo si chiama raddrizzatore a doppia semionda e richiede un trasformatore a presa centrale. Quando $v_i$  è positiva $D_1$ conduce, mentre quando è negativa conduce $D_2$. Le correnti $i_1$ ed $i_2$ percorrono $R_L$ nello stesso verso, quindi la corrente $i_L=i_!+i_2$ è tale da avere sempre una tensione positiva. Il valore medio della tensione in uscita è $2\frac{V_{sM}}{\pi}$

![Untitled](Cap%206/Untitled%2013.png)

Questo viene chiamato raddrizzatore a doppia semionda a ponte di Graetz. Durante il semiciclo positivo di $v_s$, la corrente scorre in $D_1$, prosegue su $R_L$, infine si chiude su $D_2$ ($D_3$ e D4 sono polarizzati inversamente). Durante il semiciclo negativo di vs, la corrente scorre in D3, prosegue su RL, infine si chiude su D4 (D1 e D2 sono polarizzati inversamente). Il valore medio della tensione è ancora pari a $2\frac{V_{sM}}{\pi}$

### Circuiti limitatori

vengono usati per selezionare, in una forma d’onda, solo le parti che si trovano al di sopra, al di sotto, o comprese fra delle tensioni di riferimento

Analizziamo ora il circuito seguente

![Untitled](Cap%206/Untitled%2014.png)

![Untitled](Cap%206/Untitled%2015.png)

- per $v_i<V_R+V_\gamma$  il diodo è interdetto, quindi circuito aperto. $v_o$  segue l’andamento di $v_i$
- per $v_i>V_R+V_\gamma$  il diodo è in conduzione. Se $R_f=0$ la tensione ai capi del diodo è $V_\gamma$. Se invece $R_f=\frac{dV}{dI}$ la tensione di uscita è

![Untitled](Cap%206/Untitled%2016.png)

La transcaratteristica sarà l’unione dei due casi. Nel primo è una retta bisettrice del primo e terzo quadrante ($v_o=v_i$), mentre nel secondo è una retta con coefficiente angolare $\frac{R_f}{R+R_f}$

![Untitled](Cap%206/Untitled%2017.png)

la pendenza del secondo tratto della caratteristica è dovuta al fatto che $R_f\neq0$, ma se lo fosse la retta sarebbe orizzontale ($v_o=V_R+V_\gamma$). Il valore di $R$ non deve essere talmente grande da essere comparabile con la resistenza inversa del diodo, in quel caso va cambiato il modello del diodo scelto.

Ci possono essere diverse configurazioni dei circuiti limitatori

![Untitled](Cap%206/Untitled%2018.png)

Si possono anche combinare più limitatori per ottenere degli slicer

![Untitled](Cap%206/Untitled%2019.png)

### Circuiti logici a diodi

I diodi agiscono come interruttori elettronici e ci permettono di realizzare circuiti logici a diodi, come AND e OR.

![Untitled](Cap%206/Untitled%2020.png)

- OR - Se uno dei due diodi è connesso ad un livello alto, allora sarà in conduzione, portando in uscita il livello alto. Se entrambi sono a livello basso allora saranno entrambi interdetti e in uscita ci sarà un livello basso

![Untitled](Cap%206/Untitled%2021.png)

- AND - Se uno degli ingressi è a livello basso, il diodo conduce e porta in uscita il livello basso. Se sono entrambi alti, allora i diodi non conducono e in uscita ci sarà l’alimentazione $V_a$

Una delle applicazioni dell’OR a diodi è il comparatore a finestra

![Untitled](Cap%206/Untitled%2022.png)

E’ formato da un comparatore invertente e uno non invertente, connessi all’ingresso $V_{in}$ e a delle tensioni di riferimento

![Untitled](Cap%206/Untitled%2023.png)

### Diodi Zener

I diodi Zener sono diodi che funzionano nella regione di breakdown. Hanno una tensione di breakdown (tensione di Zener) sulla quale la caratteristica I-V è quasi verticale. Vengono usati come stabilizzatori o regolatori di tensione

![Untitled](Cap%206/Untitled%2024.png)

Nel circuito sopra il diodo Zener è polarizzato inversamente funziona come stabilizzatore della tensione di uscita $V_o$. Usiamo degli stabilizzatori perché per quanto lavoriamo sulla tensione di ingresso questa potrà sempre avere delle oscillazioni e soprattutto il carico potrebbe anche non essere una semplice resistenza ma può anche cambiare nel tempo.

Supponiamo che vogliamo stabilizzare la tensione di uscita ad un valore $V_X$, allora dovremo scegliere un diodo Zener con una tensione di breakdown uguale a $V_X$. Dobbiamo trovare un valore per $R$ in modo tale che il diodo lavori in zona di breakdown e dove la resistenza dinamica $r_d$ sia molto piccola. Supponendo che la tensione in ingresso aumenti, allora aumenta anche la corrente $I_Z$ e $I_R$, se diminuisce, diminuisce anche $I_Z$. Finché però queste variazioni rimangono all’interno della zona verticale della caratteristica, la tensione in uscita non cambia. Se invece la tensione di ingresso rimane costante ma a cambiare è la corrente assorbita dal carico, allora cambia $I_Z$ ma l’uscita non cambia.

Possiamo considerare il diodo Zener come un generatore di tensione con valore $V_Z$ ma con i terminali invertiti.

Calcoliamo quindi la resistenza $R$. Partiamo dal trovare la corrente che scorre sulla resistenza stessa.

![Untitled](Cap%206/Untitled%2025.png)

Essendo che la resistenza $r_d$ è molto piccola, possiamo dire che $V_o=V_Z$. Da qui abbiamo $I_L = \frac{V_Z}{R_L}$

Infine possiamo ricavare $I_Z=I_R-I_L$. Per trovare la resistenza quindi combiniamo le formule di prima. Dobbiamo imporre però un valore alla corrente di Zener che deve essere compresa fra $I_{ZK}$ (corrente di ginocchio) e $I_{Zmax}$

il diodo zener si basa sull’effetto valanga, ma questo effetto si verifica solo nei diodi in cui la tensione di zener è poco maggiore di 6V. Per tensione minore di 6V invece, il breakdown è causato dall’effetto Zener (il drogaggio molto intenso comporta una giunzione molto stretta e un campo elettrico molto intenso che rompe numerosi legami covalenti provocando una considerevole corrente anche con tensioni esterne ridotte). Il coefficiente di temperatura ossia la variazione di VZ per ogni grado di variazione di temperatura, è negativo per diodi basati su breakdown di tipo Zener, mentre risulta positivo per breakdown con effetto valanga.

### Alimentatori

Si usano per dare alimentazione di tensione continua ai circuiti. Esistono di 3 tipi:

- non stabilizzati
- stabilizzati
- a commutazione o switching

### Alimentatori non stabilizzati

Sono formati da un trasformatore, un raddrizzatore e da un filtro. in base al tipo si raddrizzatore abbiamo tre tipi di alimentatore:

- a semionda

![Untitled](Cap%206/Untitled%2026.png)

![Untitled](Cap%206/Untitled%2027.png)

viene usato quando servono basse potenza e basse correnti di carico. Quando la tensione $v_s$ supera la tensione del condensatore $v_o$ il diodo conduce. Il resto del tempo, la corrente è fornita dal condensatore. La carica del condensatore è rapida poiché la costante di tempo dipende dalla resistenza del diodo in conduzione, mentre la scarica è lenta poiché dipende dalla resistenza di carico. Questo tipo di alimentatore presenta un ripple elevato e un forte picco di corrente $i_D$ che serve per caricare il condensatore.

- a doppia semionda

![Untitled](Cap%206/Untitled%2028.png)

abbiamo un raddrizzatore che permette la carica del condensatore ad ogni semiperiodo. Si comporta in modo diverso per quanto riguarda la massima tensione inversa PIV (peak inverse voltage). La PIV si può calcolare considerando la maglia comprendente i due diodi. Se il diodo D1 è interdetto, il D2 risulta cortocircuitato, e quindi ai capi del diodo D1 la massima tensione inversa risulta $2V_{sM}$

- a ponte

![Untitled](Cap%206/Untitled%2029.png)

In questo tipo, se supponiamo che i $D_1$ siano interdetti e i $D_2$ in conduzione, otteniamo che $PIV=V_{sM}$. Il vantaggio di questo tipo è che i diodi devono sopportare la metà della PIV, per questo sono quelli più usati. Con questo tipo di raddrizzatore si possono realizzare anche alimentatori duali, cioè con tensioni in uscita simmetriche.

![Untitled](Cap%206/Untitled%2030.png)

### Alimentatori stabilizzati

esistono di due tipi, lineari e a commutazione. Quello lineare è formato da uno non stabilizzato a cui viene collegato un circuito stabilizzatore. Questo circuito confronta la tensione di uscita con una tensione di riferimento stabile e agisce su un elemento di controllo (transistor in serie o parallelo al carico) per mantenere l’uscita stabile. Il circuito stabilizzatore più comune è quello con il diodo zener. il suo limite è la bassa escursione che può avere la corrente di uscita. La resistenza R e la corrente I che scorre in essa sono costanti. Da questo deriva che se si riduce $I_L$ aumenta (della stessa quantità) $I_Z$ e viceversa.