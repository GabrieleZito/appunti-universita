### Diodi elettroluminescenti

In un diodo a giunzione p-n polarizzato direttamente, gli elettroni dal lato n si spostano alla zona p e le lacune si spostano dal lato p al lato n, entrambe diventando portatori minoritari. Essendoci un alta concentrazione di elettroni e lacune in prossimità della giunzione, c’è un’alta probabilità di ricombinazione

Quando un elettrone passa dalla banda di valenza a quella di conduzione avviene un rilascio di energia. La quantità di energia rilasciata dipende dal gap di energia $E_G=E_C-E_V$

L’energia può essere ceduta all’esterno sotto forma di calore, o di luce. La prima avviene con diodi al silicio, mentre la seconda con diodi di altri materiali. Per quanto riguarda la luce, la sua lunghezza d’onda è dipendente dal gap di energia secondo la seguente legge

![9.1](Cap%209/Untitled.png)

9.1

h → costante di Planck 

c → velocità della luce

f → frequenza della luce

$\lambda$ → lunghezza d’onda della luce

Sviluppando i calcoli si può arrivare ad ottenere la seguente formula

![9.2](Cap%209/Untitled%201.png)

9.2

![Untitled](Cap%209/Untitled%202.png)

Un diodo ad emissione di luce (LED) è un dispositivo a semiconduttore basato su una giunzione p-n polarizzata direttamente e ad emissione di luce visibile

![Untitled](Cap%209/Untitled%203.png)

![Untitled](Cap%209/Untitled%204.png)

Il primo grafico è a caratteristica tensione-corrente, che è uguale a quella di un diodo p-n ma con la tensione di soglia più elevata (1.3-3.3V). L’intensità della luce dipende dalla corrente, e sono proporzionali. I valori tipici di corrente sono 10-20 mA con un minimo di 5 mA per l’accensione.

I LED non sopportano tensioni inverse troppo elevate (3-5V max) né correnti dirette troppo elevate (30-40 mA max). Per questo motivo si usa una resistenza in serie col diodo.

![Untitled](Cap%209/Untitled%205.png)

Dal circuito sopra possiamo ricavare il valore della resistenza di protezione con la formula

![Untitled](Cap%209/Untitled%206.png)

e scegliendo $i_d$.

### Fotodiodi

Prendiamo una giunzione p-n e polarizziamola inversamente. Sappiamo che c’è una piccola corrente inversa dovuta alla energia termica. Se illuminiamo la giunzione, si verranno a creare coppie elettrone-lacuna, che, se create nella zona di svuotamento, si separano (elettrone va verso zona n e lacuna verso zona p) creando una ***fotocorrente***.

![Untitled](Cap%209/Untitled%207.png)

Simboli del fotodiodo

![Untitled](Cap%209/Untitled%208.png)

Il fotodiodo per funzionare deve essere polarizzato inversamente. La corrente aumenta con l’intensità luminosa, ed è tipicamente di qualche $\mu A$. Esiste una corrente, detta corrente di buio, che scorre anche in assenza di luce, dovuta al flusso dei portatori minoritari generati termicamente.

Per evitare la ricombinazione dei portatori, la giunzione dovrebbe essere vicina alla superficie e più larga possibile. Per ottenere quest’ultimo, si può utilizzare un fotodiodo pin, cioè un diodo in cui le regioni p ed n sono separate da un semiconduttore intrinseco.

![Untitled](Cap%209/Untitled%209.png)

Questo sopra è il grafico della fotocorrente. Possiamo dire che la corrente è indipendente dalla tensione inversa.

Il materiale più comune usato per i fotodiodi è il silicio, poichè permette elevata efficienza

Quella sotto è la curva di risposta :

![Untitled](Cap%209/Untitled%2010.png)

La responsivity è la quantità di corrente generata dal diodo per ogni WATT di potenza irradiata.

Il taglio alle alte lunghezze d’onda è dovuto al gap del silicio, mentre il taglio di quelle basse è dovuto alle irregolarità del semiconduttore, che cattura le cariche generate.

### Fototransitor

Funziona allo stesso modo di un BJT, con la differenza che la regione di base può essere esposta ad una radiazione incidente. Il funzionamento è simile al fotodiodo, ma la corrente prodotta è più elevata.

Polarizzando il transistor in modo che la giunzione CB sia polarizzata inversamente, la corrente di uscita sarà data dalla corrente di base $i_b$ moltiplicata per il guadagno del transistor $\beta$. Avremo che la corrente di uscita $i_e$ sarà $\beta$  volte più grande di quella del fotodiodo.

![Untitled](Cap%209/Untitled%2011.png)

La luce assorbita dalla base genera una corrente di emettitore che scorre sulla resistenza di carico $R_L$ e produce una caduta di tensione ($V_{out}$) su essa.

I fototransistor sono più sensibili dei fotodiodi, ma a scapito della velocità. La corrente di uscita di un fotodiodo è sui $\mu A$ e i tempi di commutazione sui $ns$, mentre nei fototransistor la corrente è in $mA$ e i tempi in $\mu s$

### Fotoresistenze (LDR)

Quando un semiconduttore viene irradiato da una radiazione elettromagnetica può assorbire energia sufficiente a fare passare alcuni elettroni dalla banda di valenza a quella di conduzione. Da questo ne deriva che la resistenza del semiconduttore diminuisce.

Tale fenomeno dipende:

- dal semiconduttore adoperato;
- dalla concentrazione di impurità droganti presenti all’interno del cristallo semiconduttore;
- dalla lunghezza d’onda della radiazione incidente.

Per avere una fotoresitenza più sensibile, dobbiamo catture più fotoni. Per fare ciò aumentiamo la superficie, ma facendolo aumentiamo la probabilità che le coppie elettrone-lacuna create dalla luce si ricombinino. Quindi per evitarlo si realizzano elettrodi a forma di pettine per ridurre il più possibile la distanza percorsa.

![Untitled](Cap%209/Untitled%2012.png)

La relazione tra resistenza e radiazione incidente è del tipo 

![Untitled](Cap%209/Untitled%2013.png)

L → quantità di radiazione incidente misurata in lux

a e $\alpha$ → costanti

Differenza tra fotodiodo e fotoresistenza:

- fotodiodo → giunzione p-n che se polarizzata inversamente eroga corrente
- fotoresistenza → barretta di semiconduttore che anche se polarizzata non eroga corrente