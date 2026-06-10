### Principio di funzionamento degli ampl a componenti discreti

Un transistor, per poter funzionare deve essere all’interno di un circuito apposito.

![Untitled](Cap%2010/Untitled.png)

In questo caso il BJT è polarizzato e vengono applicate le tensioni $V_{BB}$ alla giunzione EB e la tensione $V_{CC}$ alla giunzione CB. Possiamo ricavare il punto di riposo dall’intersezione fra la retta di carico e la caratteristica di uscita del transistor

![Untitled](Cap%2010/Untitled%201.png)

La retta di carico ha equazione $V_{CC}=V_{CE}+R_CI_C$

La differenza con i circuiti a diodi è che la caratteristica dei BJT è formata da diversi rami, che dipendono dalla variabile di ingresso $I_B$. Questa si può ricavare dall’equazione  $V_{BB}=V_{BE}+R_BI_B$ ponendo $V_{BE}=0,7V$

IL circuito di prima praticamnete non fa niente. Per funzionare da amplificatore, c’è bisogno di qualcosa da amplificare. Quindi aggiungiamo un piccolo segnale di tensione sinusoidale sulla base.

![Untitled](Cap%2010/Untitled%202.png)

Nell’istante $t=0$, abbiamo che $v_s=0$ e il punto di riposo può essere ricavato nello stesso modo che per le caratteristiche di uscita. Per $t>0$, invece abbiamo che $v_s\neq 0$ e la retta di carico comincia ad oscillare alla stessa frequenza del segnale di ingresso. La retta trasla parallelamente a se stessa, quindi quello che cambia non le intersezioni con gli assi. Per $i_B=0$, abbiamo che $V_{BE}=V_{BB}+v_s=e_B$.

Quando $v_s$ è massima, anche $V_{BE}$ è massima, quando è al minimo, anche $V_{BE}$ lo è, quando passa per lo zero, $V_{BE}=V_{BB}$ 

![Untitled](Cap%2010/Untitled%203.png)

Si possono unire i grafici della transcaratteristica $i_c-i_b$ e quello della caratteristica d’uscita come sotto:

![Untitled](Cap%2010/Untitled%204.png)

Dall’analisi del grafico si evince che:

- Se aumenta $i_c$, diminuisce $v_{ce}$. Per questo questa configurazione viene chiamata invertente. $v_{ce}$ risulta sfasata di 180 gradi
- C’è un’amplificazione di tensione data da $\frac{v_{ce}}{v_{be}}$, con $v_{be }$ tensione in ingresso, l’altra in uscita.
- C’è un’amplificazione di corrente, data da $\frac{i_c}{i_b}$
- C’è un’amplificazione di potenza data dal prodotto delle due amplificazioni di prima

L’amplificazione è dovuta interamente alla tensione continua, mentre la tensione di ingresso serve solo a riportare la stessa frequenza in uscita.

Se per caso togliessimo la tensione continua ($V_{CC}=0$), allora la retta di carico sarebbe un punto sull’origine degli assi e non ci sarebbe segnale d’uscita.

La stessa situazione avviene se invece di utilizzare un BJT utilizzassimo un MOSFET configurato a source comune, con una tensione continua $V_{GS}$ al gate e un segnale di ingresso triangolare con ampiezza picco-picco di 1 V

![Untitled](Cap%2010/Untitled%205.png)

In assenza di segnale, il punto di riposo si trova sulla caratteristica $v_{GS}=5V$. Se viene aumentato o diminuito questo si sposterà sulla retta di carico sino ad intersecare la curva opportuna

### Limiti di funzionamento degli ampl a comp discrete

Cosa succede se aumentiamo la resistenza di drain $R_D$?

Visto che la pendenza della retta di carico è $\frac{1}{R_D}$, allora all’aumentare di $R_D$ diminuisce la pendenza. Diminuendo la pendenza, l’escursione del punto di riposo $Q$ non risulta più simmetrica rispetto al valore che si ha per $v_{GS}=5V$

Tutto questo porta l’amplificatore a distorcere il segnale di ingresso, e quindi non è più un amplificatore lineare.

Si può dimostrare, che il circuito smette di amplificare quando il punto di riposo entra nella regione di triodo o di saturazione. Basta però anche esserne sufficientemente vicini, in modo che le oscillazioni del segnale di ingresso lo portino all’interno delle suddette zone.

Il segnale quindi deve essere abbastanza piccolo da fare rimanere il punto di riposo in zona di saturazione.

I FET, per funzionare ed essere lineari devono essere polarizzati nella regione di saturazione, mentre i BJT in zona attiva

Per ottenere la massima escursione del punto di riposo, $Q$ si deve trovare al centro della regione di saturazione. Nei FET questo significa $V_{DS}$ compresa tra $V_{DS}(sat) = V_{GS} – V_t$ e $V_{DD}$, mentre per i BJT significa $V_{CE }$ compresa tra VCE(sat) ≈ 0 e $V_{CC}$

### Metodo di analisi degli amplificatori

L’analisi di un amplificatore è composta da due parti:

- analisi statica → effetto delle tensioni continue sul circuito
- analisi dinamica → effetti delle variazioni del segnale di ingresso sull’uscita

Finchè il punto di riposo si trova nella regione di linearità, si può sfruttare il principio di sovrapposizione degli effetti per eseguire le due analisi. Per fare l’analisi statica si ignora il segnale di ingresso, mentre per quella dinamica ignoriamo le tensioni di alimentazione

Di solito si deve calcolare solo l’amplificazione, quindi si può usare solo l’analisi dinamica

### Analisi statica

In un transistor, tensioni e correnti non sono indipendenti tra loro. Si solito una o più grandezze è imposta dalla rete di polarizzazione esterna (variabili indipendenti), le altre saranno le variabili dipendenti.

Queste ultime sono sempre ricavabili da

![Untitled](Cap%2010/Untitled%206.png)

per i FET

![Untitled](Cap%2010/Untitled%207.png)

per i BJT npn

Prendiamo come esempio l’amplificatore a MOSFET a svuotamento a source comune

![Untitled](Cap%2010/Untitled%208.png)

Abbiamo che la retta di carico (formata dall’alimentazione e la resistenza $R_D$) e la tensione di polarizzazione $V_{GG}$ ci servono per trovare il punto di riposo.

In realtà questo metodo fa schifo, perchè le caratteristiche dei transistor hanno elevate dispersioni.

![Untitled](Cap%2010/Untitled%209.png)

Quelle sopra sono le transcaratteristiche minime e massime di un MOSFET, quindi vediamo che anche a una tensione di polarizzazione fissa, il punto di riposo può variare.

Per migliorare la stabilità del punto di riposo, possiamo ricorrere a reti di polarizzazione alternative

![schema di polarizzazione automatica](Cap%2010/Untitled%2010.png)

schema di polarizzazione automatica

Qui il gate e posto a massa tramite la resistenza $R_G$, ed essendo la corrente di gate trascurabile, allora $V_G=0$, da cui abbiamo l’equazione alla magli di ingresso 

![Untitled](Cap%2010/Untitled%2011.png)

Questa sopra è l’equazione di una retta nel piano $I_D-V_{GS}$. L’intersezione con le due transcaratteristiche definisce sempre i due punti di riposo, ma questa volta la retta è pendente. La pendenza dipende da $R_S$, e noi vogliamo che sia minore possibile in modo da avere $I_D$ stabile. Il problema di questo metodo invece è che limitiamo eccessivamente la corrente di drain.

![Untitled](Cap%2010/Untitled%2012.png)

Uno dei metodi migliori per polarizzare un FET è tramite una rete di polarizzazione a 4 resistenze

![Untitled](Cap%2010/Untitled%2013.png)

Applichiamo il teorema di Thevenin al circuito e otteniamo il circuito equivalente

![Untitled](Cap%2010/Untitled%2014.png)

in cui 

![Untitled](Cap%2010/Untitled%2015.png)

![Untitled](Cap%2010/Untitled%2016.png)

$V_{TH}$ coincide con $V_G$, quindi possiamo scrivere $V_S=V_{TH}-V_{GS}$, da cui possiamo ricavare la corrente di drain

![10.10](Cap%2010/Untitled%2017.png)

10.10

![Untitled](Cap%2010/Untitled%2018.png)

In questo modo abbiamo ancora più diminuito la pendenza della retta, per $V_{TH}>>V_{GS}$ possiamo considerare la corrente di drain costante.

L’elemento stabilizzante del circuito a 4 resistenza è la resistenza $R_S$. Mettiamo che $I_D$ aumenti, allora diminuirà la tensione su $V_{GS}$, equilibrando l’aumento iniziale di corrente.

Anche per i BJT la rete di polarizzazione più diffusa è quella a 4 resistenze. In questo caso , lo scopo è quello di trovare un punto di riposo stabile, per il quale la corrente di uscita non varia al variare delle caratteristiche del transistor. Il parametro da controllare maggiormente è il guadagno di corrente $\beta$, poichè ha molta dispersione e varia molto con la temperatura.

![Untitled](Cap%2010/Untitled%2019.png)

Dallo schema di Thevenin ricaviamo:

![Untitled](Cap%2010/Untitled%2020.png)

![Untitled](Cap%2010/Untitled%2016.png)

E applicando la LKT nella maglia di ingresso abbiamo

![Untitled](Cap%2010/Untitled%2021.png)

e considerando che $I_B=\frac{I_C}{\beta}$abbiamo

![10.13](Cap%2010/Untitled%2022.png)

10.13

E affinchè $I_C$ risulti indipendente da $\beta$, dobbiamo avere $R_E>>\frac{R_{TH}}{\beta}$, in modo tale da avere

![10.14](Cap%2010/Untitled%2023.png)

10.14

La condizione appena vista possiamo ottenerla diminuendo molto il valore di $R_{TH}$, ma per motivi ignoti, questo non può avvenire, per l’alta impedenza che dobbiamo dare all’ingresso. Per questo dobbiamo lavorare su $R_E$, aumentandola. Possiamo dire, quindi che $R_E$ è l’elemento stabilizzatore del circuito e che lo rende indipendente da $\beta$.

Ritornando ai FET, per ridurre gli effetti delle variazioni di $V_{GS}$, possiamo modificare lo schema di polarizzazione in questo modo

![Untitled](Cap%2010/Untitled%2024.png)

chiamato polarizzazione di source. Da questo troviamo la corrente di drain:

![Untitled](Cap%2010/Untitled%2025.png)

Affinchè questa polarizzazione sia efficace, $V_{SS}>>V_{GS}$, ma siccome i valori di $V_{GS}$  variano da -5 a -1V, non è facile, ma essendo che normalmente $V_{SS}$ è maggiore di $V_{GS}$ è sempre un miglioramento.

Per rendere stabile il punto di riposo, la corrente di drain deve essere indipendente da $V_{GS}$, e per riuscirci si può ricorrere allo schema di polarizzazione tramite generatore di corrente costante

![Untitled](Cap%2010/Untitled%2026.png)

Il generatore di corrente costante può essere realizzato con un BJT

![Untitled](Cap%2010/Untitled%2027.png)

Il BJT è alimentato con una polarizzazione d’emettitore, dunque la corrente di collettore vale

![Untitled](Cap%2010/Untitled%2028.png)

Poichè il collettore del BJT è collegato direttamente al source del FET allora abbiamo $I_D=I_C=I_O$

Poichè $I_C=I_O$ è costante, i punti di riposo hanno lo stesso valore di corrente di drain, rendendola indipendente da $V_{GS}$.

![Untitled](Cap%2010/Untitled%2029.png)

I tipi di reti di polarizzazione visti fin ora vanno bene solo per i MOSFET a svuotamento. Per quelli ad arricchimento dobbiamo avere  $V_{GS}>V_t$.

### Analisi Dinamica. Amplificazione

Per l’analisi dinamica, tutti i generatori di corrente si sostituiscono con un circuito aperto, quelli di tensione costante con un cortocircuito. Questo circuito, chiamato schema dinamico, può essere semplificato sostituendo al transistor degli elementi più semplici. Questa semplificazione vale solo se il transitor lavora in zona lineare.

Se per esempio, prendiamo un FET (a source comune), in zona lineare la corrente di drain vale 

![Untitled](Capitolo%207/Untitled%2012.png)

in questo modo, può essere considerato un generatore di corrente dipendente da $v_{gs}$. Prendiamo ora solo dei piccoli segnali, ossia variazioni attorno al punto di riposo. se $v_{gs}$ è sufficientemente piccolo, la transcaratteristica $i_D-v_{GS}$ può essere linearizzata nell’intorno del punto $Q$, e $i_d=v_{gs}*\text{coefficiente della retta}$

![Untitled](Cap%2010/Untitled%2030.png)

Il coefficiente della retta rappresenta la transconduttanza $g_m$ (cap 7). Questa si può calcolare come:

![Untitled](Cap%2010/Untitled%2031.png)

Andando a sostituire la formula sotto in quella sopra,

![Untitled](Capitolo%207/Untitled%2010.png)

otteniamo

![Untitled](Cap%2010/Untitled%2032.png)

Vogliamo avere una tranconduttanza grande, e la otteniamo in due modi, o con W grande ed L piccolo oppure con $V_{GS}>V_t$, ma non dobbiamo aumentare troppo $V_{GS}$ per non modificare il segnale di uscita.

Possiamo sostituire ora nello schema dinamico, al posto del FET, il modello equivalente di sotto

![Untitled](Cap%2010/Untitled%2033.png)

Nel caso volessimo tenere conto del fatto che le caratt. di uscita non sono perfettamente orizzontali, possiamo aggiungere in parallelo una resistenza $r_o$ (parte tratteggiata)

L’uscita del modello di sopra vale anche nel caso di un BJT. Quello che cambia è l’entrata, infatti il BJT può essere pilotato sia da una tensione ($v_{be}$) che da una corrente ($i_b$). Mentre nel FET in ingresso abbiamo un circuito aperto, nel BJT abbiamo una resistenza $r_{\pi}=\frac{v_{be}}{i_b}$

![Untitled](Cap%2010/Untitled%2034.png)

Il generatore di corrente è pilotato dalla corrente $\beta i_b$, ma essendo la tensione $v_{be}$ dipendente da $i_b$, possiamo anche dire che sia pilotato da quest’ultima.

Avendo

![Untitled](Cap%2010/Untitled%2035.png)

calcoliamo la corrente $i_c$ del generatore

![Untitled](Cap%2010/Untitled%2036.png)

Il $g_m$ che abbiamo sostituito è la transconduttanza, analoga a quella del FET vista prima.

Il modello di sopra rimane valido se gli andiamo a sostituire un generatore di corrente pilotato in tensione $g_mv_{be}$

Per usare il transistor come amplificatore di piccoli segnali, lo posizioniamo tra una sorgente di segnale $v_s$ ed un utilizzatore

![Untitled](Cap%2010/Untitled%2037.png)

Le due capacità, dette di accoppiamento, servono per evitare che la corrente esca dalla rete di polarizzazione e vada alla sorgente o al carico. Oltre a questo servono a rendere indipendente il punto di riposo dalle resistenze $R_L$ ed $R_S$. Queste capacità le consideriamo infinite, in modo da poterle considerare circuiti aperti nel caso di segnali continui, o cortocircuiti nel caso di segnali alternati.

### Amplificatore a source comune e ad emettitore comune

![Untitled](Cap%2010/Untitled%2038.png)

Quello sopra è lo schema di un amplificatore a source comune. In teoria, in una configurazione del genere il source sia posto a massa, cosa che però non succede qui. La soluzione a questo problema è mettere in parallelo alla resistenza $R_S$ una capacità $C_s$, detta di bypass. Questa capacità deve avere un valore molto elevato per poter cortocircuitare un segnale a qualsiasi frequenza. Supporremo la reattanza infinita.

Notiamo che quando $v_{gs}$ aumenta, lo fa anche $i_d$, ma la tensione sul drain diminuisce. Pertanto un semiperiodo positivo della tensione in ingresso ne produce uno positivo in uscita e viceversa. L’amplificatore a source comune, di conseguenza, inverte la fase del segnale d’ingresso

![10.16b](Cap%2010/Untitled%2039.png)

10.16b

Questo sopra è lo schema equivalente dinamico. Le due resistenze $R_1$ ed $R_2$ sono in parallelo, quindi possiamo scriverle come un unica resistenza $R_G$. La tensione di uscita però è indipendente da quest’ultima, ed è uguale a 

![Untitled](Cap%2010/Untitled%2040.png)

dove il segno meno indica l’inversione di fase

La tensione di ingresso invece è $v_i=v_{gs}$

Definiamo l’amplificazione di tensione come

![Untitled](Cap%2010/Untitled%2041.png)

Vediamo ora un amplificatore ad emettitore comune

![Untitled](Cap%2010/Untitled%2042.png)

L’amplificazione è la stessa ma si sostituisce la resistenza

![10.27](Cap%2010/Untitled%2043.png)

10.27

è utile ora calcolare le resistenze di ingresso e di uscita. Per farlo possiamo guardare lo schema dinamico

![10.17b](Cap%2010/Untitled%2044.png)

10.17b

Per calcolare la resistenza di uscita cortocircuitiamo tutti i generatori di tensione indipendenti e apriamo tutti i generatori di corrente indipendenti. Sarà quindi uguale al rapporto tra la tensione e la corrente di uscita. Se cortocircuitiamo il segnale $v_i$, il generatore di corrente dipendente $g_mv_{gs}$ diventa un circuito aperto. La resistenza di uscita sarà allora $R_o=R_D$

Nel coso ad emettitore comune viceversa avremo $R_O=R_C$

Dal punto di vista di amplificazione di tensione e resistenza di uscita, non  ci sono differenze tra source ed emettitore comune. In un BJT la transconduttanza è maggiore di quella di un FET, quindi l’amplificazione risulta più grande.

I due amplificatori differiscono per quanto riguarda la resistenza di ingresso.

Per i FET (10.16b), avremo 

![10.30](Cap%2010/Untitled%2045.png)

10.30

Mentre per i BJT (10.17b)

![Untitled](Cap%2010/Untitled%2046.png)

Nel caso dei BJT, la resistenza di ingresso è limitata dalla resistenza $r_\pi$, quindi per avere la massima resistenza dimensioniamo $R_1$ ed $R_2$ in modo che siano di un ordine di grandezza maggiore di $r_\pi$

Perché è importante avere una resistenza di ingresso elevata e una di uscita piccola? andiamo a scoprirlo

Prendiamo come esempio lo schema sotto

![Untitled](Cap%2010/Untitled%2047.png)

Al coso ad emettitore comune abbiamo aggiunto in uscita una resistenza di carico $R_L$ ed in entrata un generatore di segnale reale $v_s$, Sotto c’è lo schema equivalente dinamico

![Untitled](Cap%2010/Untitled%2048.png)

L’amplificazione del circuito diventa $\frac{v_o}{v_s}$, e possiamo scriverla come

![Untitled](Cap%2010/Untitled%2049.png)

Dallo schema dinamico vediamo che $R_L$ è in parallelo  a $R_C$
, quindi la 10.27 diventa $A=g_mRC||R_L$

Rimane da calcolare il secondo rapporto. Lo possiamo fare prendendo il circuito sottostante

![Untitled](Cap%2010/Untitled%2050.png)

nel quale abbiamo sostituito la rete circuitale a ***valle*** del generatore reale con la sua resistenza $R_i$. Diventa quindi un partitore di tensione. L’amplificazione totale diventa:

![Untitled](Cap%2010/Untitled%2051.png)

La resistenza $R_S$ quindi si comporta come attenuazione del segnale. Più è piccola rispetto a $R_i$ più il rapporto del partitore tende a 1, quindi $R_S$ non ha più influenza sull’amplificazione totale.

Possiamo pensare che per non avere un’attenuazione del segnale possimao imporre $R_i>>R_S$ e $R_O<<R_L$, ma se vogliamo il massimo trasferimento di potenza dalla sorgente al carico dobbimao avere invece $R_i=R_S$ e $R_O=R_L$. Essendo che le due condizioni non si possono aveer in contemporanea, allora l’amplificazione di potenza non sarà la massima ottenibile

Riassumendo

![Untitled](Cap%2010/Untitled%2052.png)

![Untitled](Cap%2010/Untitled%2053.png)

![Untitled](Cap%2010/Untitled%2054.png)

### Amplificatore a doppio carico

Il problema precedente si può risolvere con l’amplificatore a doppio carico, ovvere un ampl. a source comune con resistenza sul source, o viceversa con l’emettitore.

![a JFET](Cap%2010/Untitled%2055.png)

a JFET

Con il suo schema dinamico:

![Untitled](Cap%2010/Untitled%2056.png)

Ponendo $R'_L=R_L\parallel R_D$ la tensione di uscita è

![Untitled](Cap%2010/Untitled%2057.png)

la tensione $v_{gs}$ la troviamo calcolando separatamente le due tensioni al source e al gate

![Untitled](Cap%2010/Untitled%2058.png)

Quindi possiamo trovare l’amplificazione

![Untitled](Cap%2010/Untitled%2059.png)

Se $g_mR_S>>1$ l’amplificazione si semplifica

![Untitled](Cap%2010/Untitled%2060.png)

La condizione $g_mR_S>>1$ è sempre verificata per i MOSFET e $g_mR_E>>1$ per i BJT. Non è sempre verificata invece per i JFET, a causa della minore transconduttanza

Per calcolare l’amplificazione totale di tensione consideriamo la resistenza di ingresso, che calcoliamo come

![Untitled](Cap%2010/Untitled%2061.png)

Troviamo l’amplificazione totale 

![Untitled](Cap%2010/Untitled%2062.png)

Per calcolare la resistenza di uscita ci aiutiamo con lo schema sotto

![Schema circuitale per il calcolo della resistenza d’uscita di un
amplificatore a FET a doppio carico](Cap%2010/Untitled%2063.png)

Schema circuitale per il calcolo della resistenza d’uscita di un
amplificatore a FET a doppio carico

in cui è riportato il generatore ausiliario e tutti i generatori indipendenti annullati

Il generatore di corrente pilotato fornisce corrente nulla, in quanto

![Untitled](Cap%2010/Untitled%2064.png)

La resistenza di uscita vale quindi $R_o=R_D$

Per i BJT il calcolo è analogo, infatti l’amplificazione varrà

![Untitled](Cap%2010/Untitled%2065.png)

e la resistenza di uscita $R_o=R_C$

Per calcolare la resistenza di ingresso ci aiutiamo con lo schema di sotto

![Schema circuitale per il calcolo della resistenza d’ingresso di un amplificatore a BJT a doppio carico](Cap%2010/Untitled%2066.png)

Schema circuitale per il calcolo della resistenza d’ingresso di un amplificatore a BJT a doppio carico

In questo schema abbiamo il transistor con il generatore pilotato dalla corrente $i_b$. La corrente che scorre su $r_\pi$ è $i_b$, se aapplichiamo la LKC al nodo E, otteniamo la corrente sulla resistenza $R_E$, che è pari a $(1+\beta)i_b$. Osservando dall’ingresso del circuito, non cambia niente se togliamo il generatore $\beta i_b$ e sostituiamo $R_E$ con una resistenza di valore $(1+\beta)R_E$. Così facendo resta una solaa maglia e la corrente $i_b$ scorrerà pure sul resistore $(1+\beta)R_E$. La resistenza di ingresso quindi è

![Untitled](Cap%2010/Untitled%2067.png)

Con un amplificatore a doppio carico, possiamo stabilire il valore dell’amplificazione scegliendo il valori delle resistenze sul drain o source. Non abbiamo molta libertà però, visto che modificando le resistenze spostiamo anche il punto di riposo, che se esce dalla zona di linearità, non ci fa amplificare più niente.

Per avere un po’ di libertà in più, si può cortocircuitare dinamicamente una parte delle resistenze sul source, o emettitore, come nello schema sotto

![Untitled](Cap%2010/Untitled%2068.png)

In questo modo possiamo ridurre il valore di $r_{E1}$ in modo da aumentare l’amplificazione, ma senza modificare il punto di riposo.

![Untitled](Cap%2010/Untitled%2069.png)

![Untitled](Cap%2010/Untitled%2070.png)

### Amplificatore a drain comune e a collettore comune

![Untitled](Cap%2010/Untitled%2071.png)

Questa configurazione risolve il problema di prima. Qui l’uscita si trova sul source ed è più o meno uguale a quella di ingresso ed in fase con essa. Per questo si chiama inseguitore di source.

In questa configurazione, visto che la resistenza d’ingresso è molto più grande di quella di uscita, il circuito richiede meno potenza al segnale di ingresso per pilotare un carico dato.

Possiamo dire che un generatore di segnale con una sua resistenza, può ora pilotare un’altra resistenza di carico paragonabile o inferiore, senza problemi di attenuazione. L’inseguitore di source ha un’amplificazione di corrente, ma non di tensione.

Calcoliamo ora l’amplificazione e resistenze di ingresso e di uscita

![Untitled](Cap%2010/Untitled%2072.png)

![Untitled](Cap%2010/Untitled%2073.png)

![Untitled](Cap%2010/Untitled%2074.png)

Nel caso ci sia un carico $R_L$ dovremo considerare $R_L\parallel R_S$ e non più solo $R_S$

L’inseguitore di source è un amplificatore a bassa distorsione (inferiore a quella di un amplificatore a source comune) pooichè la sua amplificazione tende ad 1 ed è poco sensibile a $g_m$.

La resistenza di ingresso è uguale tutte le altre volte

![Untitled](Cap%2010/Untitled%2075.png)

Per trovare la resistenza di uscita ci calcoliamo prima la tensione di uscita

![Untitled](Cap%2010/Untitled%2076.png)

Questa formula ci ricorda un partitore di tensione, il cui circuito dinamico è 

![Untitled](Cap%2010/Untitled%2077.png)

Se applichiamo il teorema di Thevenin ci troviamo il circuito 

![Untitled](Cap%2010/Untitled%2078.png)

Da qui ci troviamo la resistenza di uscita 

![Untitled](Cap%2010/Untitled%2079.png)

Lo stesso discorso si può fare per i BJT, con lo schema a collettore comune:

![Untitled](Cap%2010/Untitled%2080.png)

che chiamiamo inseguitore di emettitore. Lo schema dinamico è

![Untitled](Cap%2010/Untitled%2081.png)

Ponendo $R_L'=R_L\parallel R_E$, calcoliamo l’amplificazione

![Untitled](Cap%2010/Untitled%2082.png)

e approssimando $1+\beta\approx\beta$

![Untitled](Cap%2010/Untitled%2083.png)

La resistenza di uscita è

![Untitled](Cap%2010/Untitled%2084.png)

IL calcolo della resistenza di ingresso cambia un po’, vista la presenza di $r_\pi$, ed è

![Untitled](Cap%2010/Untitled%2085.png)

![Untitled](Cap%2010/Untitled%2086.png)

![Untitled](Cap%2010/Untitled%2087.png)

### Amplificatori multistadi

![Untitled](Cap%2010/Untitled%2088.png)

Ogni stadio è costituito da una delle configurazioni che abbiamo visto fin ora. Nell’immagine di sopra sono collegati in modo diretto.

Per come sono connessi i blocchi, l’analisi statica è facile. Essendo che la corrente in uscita è più grande di quella in entrata allo stadio successivo, allora lo studio statico può essere effettuato in modo quasi indipendente. Per essere considerati completamente indipendenti, gli stadi devono essere accoppiati con un condensatore di accoppiamento.

L’analisi dinamica è più complessa, poiché ogni stadio ha una sua amplificazione che contribuisce all’amplificazione totale, che è

![Untitled](Cap%2010/Untitled%2089.png)

L’amplificazione di ogni stadio va calcolata tenendo in considerazione l’effetto di carcio dovuto allo stadio successivo.

Ci sono due modi per calcolare l’amplificazione di un coso multistadio

![Untitled](Cap%2010/Untitled%2090.png)

Esistono vari modi per collegare gli stadi chiamati accoppiamenti:

- Accoppiamento RC
    
    ![Untitled](Cap%2010/Untitled%2091.png)
    
    Il segnale sulla resistenza di collettore passa alla base dello stadio successivo tramite il condensatore di accoppiamento. Questo condensatore fa passare la corrente alternata e blocca quella continua. Lo svantaggio è che impongono una frequenza limite inferiore, quindi per rimediare, facciamo in modo che alla frequenza più bassa prevista, la rete passa alto abbia una reattanza trascurabile.
    
- Accoppiamento diretto (o in continua)
    
    Questo tipo abbatte la barriera a bassa frequenza. Fa passare sia la corrente alternzata che continua e amplifica qualsiasi segnale.
    
    ![10.28b](Cap%2010/Untitled%2092.png)
    
    10.28b
    
    Questo tipo di accoppiamento è usato per segnali continui o lentamente variabili nel tempo. Lo svantaggio è però che i punti di riposo non si possono fissare in modo indipendente. Infatti nello schema di sopra abbiamo che la base di T2 viene polarizzata dal collettore di T1. In questo modo però  succede che una variazione del punto di riposo di T1 determina una variazione di quello di T2.
    
    Se per esempio l’amplificazione dei due stadi fosse di -10 e -40, avremmo un’amplificazione totale di 400, che trasformerebbe una variazione di 5 mV in entrata in una variazione di 2 V in uscita. Questa variazione indesiderata si chiama deriva, e in base a cosa stiamo usando può fare uscire i transistor dalla zona attiva.
    
    ### Criteri di progetto
    
    ![Untitled](Cap%2010/Untitled%2093.png)