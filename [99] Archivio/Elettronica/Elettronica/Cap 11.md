
La tecnologia usata oggi per la realizzazione dei dispositivi integrati è la tecnologia planare, le cui fasi sono:

- formazione dello strato epitassiale
- formazione dello strato di biossido di silicio;
- rimozione selettiva del biossido tramite fotolitografia;
- diffusione o impiantazione ionica delle impurità droganti
- metallizzazione

Ma come vengono realizzate le fette di silicio ?

### Crescita del monocristalli

si parte con la scelta dei materiali, che devono essere estremamente puri, con una tolleranza non superiare ad un atomo ogni 5 mld di atomi di silicio. Inoltre non ci devono essere difetti nella struttura cristallina.

Per la crescita di materiali semiconduttori e con il grado di purezza necessario, si usa il metodo Czochralsky.

- Mettiamo del silicio policristallino in un contenitore non reattivo (assieme alla voluta percentuale di elementi droganti) e lo facciamo fondere
- Prendiamo un campione di silicio (seme), lo portiamo a contatto con la superficie fusa e lo facciamo ruotare
- Man mano che ruota viene anche fatto sollevare dalla superficie
- Raffreddandosi si viene a creare la “carota”, fino a 30 cm di diametro
- La carota viene fatta a fette di 0.5 mm e levigate e lucidate

![Untitled](Cap%2011/Untitled.png)

## Tecnologia planare

### Formazione strato epitassiale

Questo processo serve a realizzare sulla fetta di silicio un sottile strato monocristallino con spessore e drogaggio opportuni. Va fatto nel caso in cui si voglia sovrapporre due strati con drogaggi diversi o quando serve un controllo preciso dei profili di drogaggio.

Per deporre gli atomi di silicio sulla fetta si usa il gas $SiCl_4$ (tetracloruro di silicio). Per avere uno strato di tipo $p$, si aggiunge l’idrogeno del diborano, mentre per quelli $n$, si aggiunge della fosfina.

Lo spessore dipende dalla temperatura, che a 1200 C assicura la crescita monocristallina dello strato.

### Formazione dello strato di biossido di silicio

Per creare lo strato di biossido di silicio, si fa fluire dell’ossigeno sulla superficie della fetta, portata ad alta temperatura. Per evitare contaminazioni, viene messa all’interno di un contenitore di quarzo

### Rimozione selettiva del biossido tramite fotolitografia

Il motivo per cui si aggiunge lo strato di biossido sul silicio è che questo fa da maschera per l’introduzione selettiva delle impurità droganti, aprendo una finestra nella zona di interesse.

Per aprire la finestra si usano le maschere fotolitografiche. Si usa un materiale fotosensibile detto “fotoresist”, che viene sparso per tutta la fetta.

Al di sopra della fetta viene posta una maschera di vetro che blocca o fa passare la luce ultravioletta in specifiche zone. il fotoresist nelLe zone esposte alla luce diventa solubile, e può essere rimosso tramite un solvente (idrossido di potassio). tolto questo lo strato di biossido rimane scoperto. Per eliminare questa parte scoperta viene usato l’acido fluoridrico, che crea a sua volta una finestra nello strato di silicio. Il fotoresist può essere tolto del tutto.

### Diffusione o impiantazione ionica delle impurità droganti

Si può drogare il silicio in due modi, diffusione o impiantazione ionica

- Diffusione → si depositano le impurità sulla fetta e si porta ad alta temperatura, alla quale le impurità si diffondono nel silicio. La diffusione nel silisio avviene per due meccanismi:
    - Impurità sostituzionali → si mettono in un posto vuoto non occupato dal silicio
    - Impurità interstiziali → si collocano tra un atomo ed un altro per effetto della maggiore distanza interatomica esistente ad alta temperatura, ma nel successivo raffreddamento anch'esse si stabiliscono in siti reticolari del Si.
- Impiantazione ionica → un fascio di ioni viene sparato contro il silicio, controllando l’intensità e la profondità del drogaggio attraverso la corrente del fascio. Il vantaggio è che viene eseguita a basse temperature, lo svantaggio è che danneggia la superficie del silicio.

### Metallizzazione

I collegamenti elettrici tra i dispositivi vengono realizzati tramite un film sottile di alluminio. Questo viene depositato tramite condensazione sulla fetta di silicio. Per farlo si usano sempre le tecniche di fotoresist e maschere di prima

![Untitled](Cap%2011/Untitled%201.png)

![Untitled](Cap%2011/Untitled%202.png)

### Carico attivo

Esistono anche circuiti integrati analogici. tuttavia ci sono limitazioni, come ad esempio il non poter usare resistenza di alto valore. Per questo si usano carichi attivi, ossia FET.

![Untitled](Cap%2011/Untitled%203.png)

Quello sopra è un amplificatore con carico a svuotamento. Poiche il MOSFET ha il gate e il source allo stesso potenziale, allora la sua caratteristica sarà

![Untitled](Cap%2011/Untitled%204.png)

che non è più una retta, ma una curva di carico, che poi sovrapponiamo alle caratteristiche del transistor T1

![Untitled](Cap%2011/Untitled%205.png)

Viene tracciata partendo dal punto $V_{DD}$ sull’asse $v_o$ e disegnandola specchiata.

Se entrambi i dispositivi si trovano in zona lineare, allora lo schema equivalente è

![Untitled](Cap%2011/Untitled%206.png)

in cui sono presenti le resistenze dei due MOSFET, $r_{o1}$ ed $r_{o2}$

Poiché il gate e il source del transistor di carico sono cortocircuitati, allora vgs2 = 0, pertanto il
generatore di corrente dipendente gm2vgs2 si annulla

L’amplificazione è allora la stessa di un amplificatore a source comune

![Untitled](Cap%2011/Untitled%207.png)

In questo caso caso, però, $A$ risulta maggiore.

### Evoluzione delle famiglie logiche

i dispositivi digitali vengono suddivisi in famiglie logiche. Oggi i dispositivi logici vengono costruiti con la tecnologia dei circuiti integrati monolitici, e a seconda del numero di porte logiche su di essi si classificano in:

1. Circuiti SSI (Small Scale Integration), i quali contengono un massimo di dieci porte logiche
2.  Circuiti MSI (Medium Scale Integration), i quali contengono tipicamente da dieci a cento
porte logiche.
3. Circuiti LSI (Large Scale Integration), i quali contengono tipicamente da cento a mille porte
logiche.
4. Circuiti VLSI (Very Large Scale Integration), i quali contengono un numero di porte logiche
superiore a mille.

![Untitled](Cap%2011/Untitled%208.png)

### Caratteristiche generali delle famiglie logiche integrate

![Untitled](Cap%2011/Untitled%209.png)

![Untitled](Cap%2011/Untitled%2010.png)

![Untitled](Cap%2011/Untitled%2011.png)

![Untitled](Cap%2011/Untitled%2012.png)

![Untitled](Cap%2011/Untitled%2013.png)

![Untitled](Cap%2011/Untitled%2014.png)

![Untitled](Cap%2011/Untitled%2015.png)

![Untitled](Cap%2011/Untitled%2016.png)

### Funzionamento del BJT in commutazione

Studiamo ora il funzionamento del BJT quando lascia la zona attiva. Le zone di interdizione e di saturazione ci servono se vogliamo fare funzionare il BJT come un interruttore.

![Untitled](Cap%2011/Untitled%2017.png)

Nella zona attiva il BJT si comporta come amplificatore di corrente e $\frac{I_C}{I_B}=\beta$. Se il punto di riposo si sposta su $M$, la corrente $I_C$ non cresce ulteriormente e si mantiene stabile all’incirca a $\frac{V_{CC}}{R_C}$ e il BJT è in saturazione.

In questa regione la relazione fondamentale del transistor diventa

![Untitled](Cap%2011/Untitled%2018.png)

$V_{CE}$ assume valori molto bassi (0.2 V) e la corrente di collettore risulta 

![Untitled](Cap%2011/Untitled%2019.png)

$V_{BE}$ assume valori più alti (0.8 V)

In saturazione entrambe le giunzioni sono polarizzate direttamente. Normalmente il circuito viene progettato in modo tale che IB sia più alta di IB(sat) di un fattore che varia da 2 a 10 (denominato fattore di overdrive)

Diminuendo $V_{BE}$, $I_B$ e $I_C$ diminuiscono anch’esse; non appena $V_{BE}<V_\gamma$, le correnti risultano trascurabili. Il BJT si trova in zona di interdizione.

Anche le tensioni di base negative mantengono il BJT in interdizione. Bisogna stare attenti solo alla tensione di breakdown fra base ed emettitore $V_{EBO}$

In interdizione entrambe le giunzioni del BJT sono polarizzate inversamente.

Per lavorare in commutazione, il BJT lavora tra l’interdizione e la saturazione. Il motivo dell’uso di queste due regioni è che correnti e tensioni sono definite e non dipendono da parametri instabili come $\beta$ e che la potenza dissipata è molto bassa.

Vediamo ora come funziona il BJT da interruttore

Mettiamo di avere in ingresso un segnale che può avere solo due livelli, alto ($V_{CC}$) o basso (0).

Se in ingresso arriva il livello alto, la giunzione BE è polarizzata direttamente, e anche BC, se le due resistenza sono opportunamente dimensionate. L’uscita $V_o$ coincide con $V_{CE(sat)}=0$. Il BJT è un interruttore chiuso.

Se in ingresso abbiamo il livello basso, le giunzioni BE e BC sono interdette, e il segnale di uscita sarà a livello alto. Il BJT è un interruttore aperto.

Il circuito si comporta pertanto da porta logica NOT ed è detto invertitore a transistor.

A differenza della zona attiva, non dobbiamo stabilizzare il punto di riposo, poiché i M ed N sono intrinsecamente stabili.

Ovviamente le commutazioni tra i due stati non sono istantanee, ma ci sono i tempi $t_{ON}$ (il tempo necessario affinché la corrente IC si porti al 90% del suo valore massimo di saturazione) e $t_{OFF}$ (il tempo necessario affinché la corrente IC si porti dal suo valore di saturazione al 10% di tale valore)

### Funzionamento del MOSFET in commutazione

![Untitled](Cap%2011/Untitled%2020.png)

Il MOSFET lavora come amplificatore di segnale in zona di saturazione, Mentre in commutazione passa da uno stato di interdizione (punto N) ad uno stato di conduzione (punto M) nella zona resistiva

Per $V_{GS}<V_t$, il canale non è formato, $I_D=0$, il MOS è interdetto e il punto di funzionamento cade in N ($V_{DS}=V_{DD}$)

Mentre per $V_{GS}>V_t$, nel canale inizia a scorrere corrente, $V_{DS}$ inizia a diminuire e il punto di riposo passando dalla zona di saturazione arriva al punto M, nel quale il MOS si comporta come una resistenza $r_{ON}$

Quando il MOSFET è ON, non abbiamo tensione nulla, né si può considerare un interruttore chiuso, ma si comporta come una resistenza.

Le resistenze $R_D$ e $r_{ON }$ formano un partitore di tensione, che fornisce in uscita una frazione di $V_{DD}$. Se però prendiamo $R_D$ molto più grande di $r_{ON}$, allora la frazione di $V_{DD}$ si può ignorare e consideriamo il MOSFET un cortocircuito

Il circuito di Fig. 11.13a si comporta allora da porta NOT ed è chiamato invertitore a MOSFET (logica NMOS).

### La famiglia CMOS

![Untitled](Cap%2011/Untitled%2021.png)

I CMOS sono composti da un NMOS e da un PMOS, in serie con i drain connessi insieme

L’NMOS conduce quando $V_{GS}>V_t$, mentre il PMOS quando $V_{GS}<V_t$, ma in questo caso $V_t$ è negativa e in valore assoluto pari alla soglia dell’NMOS.

Nel momento in cui $V_i=0$, si ha $V_{GS1}=0$ e $V_{GS2}=-V_{DD}$, quindi T1 è OFF, e t2 è ON, e risulta che $V_o=V_{DD}$

Nel caso in cui $V_i=V_{DD}$, si ha $V_{GS1}=V_{DD}$ e $V_{GS2}=0$, quindi T1 è ON, e t2 è OFF, e risulta che $V_o=0$

Analizziamo il funzionamento con il grafico sopra, con diverse tensioni di alimentazione.

Quando $V_i$ super la tensione di soglia di T1, questo conduce, e avviene una partizione di $V_{DD}$ sulle resistenze dei due MOS. All’aumentare di $V_i$, la resistenza di T1 diminuisce, mentre quella di T2 aumenta. Abbiamo quindi che per $V_i=\frac{V_{DD}}{2}$ le resistenze sono uguali e $V_o=\frac{V_{DD}}{2}$

Aumentando ancora $V_i$, la resistenza di T2 supera quella di T1, così facendo $V_o$  si abbassa fino a 0V, fino a quando, per $V_i=V_{DD}-1.5V$, T2 va in OFF

![Untitled](Cap%2011/Untitled%2022.png)

L’ingresso è isolato dal dispositivo dallo strato di ossido di silicio. I due MOS li possiamo rappresentare come due interruttori posti in serie alla resistenza $r_{ON}$. Per evitare di danneggiare il componente, vengono inseriti dei diodi limitatori che impediscono alla tensione sugli ingressi di salire oltre $V_{DD}+V_\gamma$ e scendere al di sotto $-V_\gamma$

![Untitled](Cap%2011/Untitled%2023.png)

In condizioni statiche il CMOS non dissipa potenza, infatti sia la corrente di ingresso che di uscita è nulla, poiché uno dei due MOS è interdetto

Durante la commutazione, per breve tempo i MOS sono entrambi in conduzione, quindi ci sarà una corrente  $I_{DD}$ che scorre verso massa. Questa corrente raggiunge il valore massimo quando $V_i=\frac{V_{DD}}{2}$

![Untitled](Cap%2011/Untitled%2024.png)

La potenza dissipata dipende da: durata della commutazione, resistenza dei canali, quadrato di $V_{DD}$ e numero di commutazioni al secondo, cioè frequenza di funzionamento

### Porte Open Drain

Sono circuiti integrati simili a quelli visti prima, con la differenza che presentano in uscita un MOS con il drain aperto, non connesso all’alimentazione

![Untitled](Cap%2011/Untitled%2025.png)

Se connettiamo uscita e alimentazione con una resistenza detta di pull-up, si comporta come una porta ordinaria

![Untitled](Cap%2011/Untitled%2026.png)

Vantaggi degli open drain:

- Possibilità di alimentare la resistenza di pull-up $R_C$ con una tensione diversa da quella propria della porta logica. In tal caso la resistenza va dimensionata opportunamente.
- Possibilità di realizzare un AND cablato, ossia collegando le uscite di più open drain insieme

![Untitled](Cap%2011/Untitled%2027.png)

### Buffer Driver

Sono porte periferiche che vengono interposte fra il sistema logico e i dispositivi esterni. A volte hanno delle uscite potenziate in tensione e corrente in modo da pilotare i dispositivi esterni, quindi chiamati anche driver

### Trigger di Schmitt

Sono circuiti di commutazione con due tensioni di soglia. L’uscita cambia di stato quando, l’ingresso passando dallo stato basso a quello alto supera la tensione di soglia superiore, oppure quando, passando da alto a basso, super la tensione di soglia inferiore.

Di solito vengono usati per squadrare segnali di forma d’onda qualsiasi oppure per rendere i segnali digitali esenti da jitter.

![Untitled](Cap%2011/Untitled%2028.png)