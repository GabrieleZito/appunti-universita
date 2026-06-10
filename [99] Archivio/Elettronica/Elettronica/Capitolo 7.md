# FET

E’ un dispositivo a semiconduttore con 3 terminali.

![Untitled](Capitolo%207/Untitled.png)

La tensione applicata tra i terminali 1 e 2 regola il flusso di corrente che scorre tra il 3 e l’1.

Esistono 3 tipi di FET:

1. MOSFET → il gate metallico è isolato dal semiconduttore da un film di biossido di silicio. è utilizzato per circuiti come microprocessori e memorie a semiconduttore
2. JFET → il gate è una giunzione p-n polarizzata inversamente
3. MESFET → il gate è una giunzione rettificante polarizzata inversamente

Caratteristiche:

- il funzionamento dipende dai portatori maggioritari
- sono più semplici da realizzare rispetto ai BJT
- elevata impedenza di ingresso
- hanno un rumore inferiore ai BJT
- funzionano bene come interruttori

Lo svantaggio è che non amplificano tanto quanto i BJT

## MOSFET ad arricchimento

![Untitled](Capitolo%207/Untitled%201.png)

![Untitled](Capitolo%207/Untitled%202.png)

Le regioni $n^+$ sono isolate tra di loro a meno che non venga applicata una tensione al gate in modo da creare un canale di tipo $n$. La conducibilità del canale dipende da questa tensione.

Il substrato forma delle giunzioni p-n con source e drain. Normalmente sono polarizzate inversamente. Esiste un quarto elettrodo, detto *Body,* che è normalmente connesso al source. Se il drain ha una tensione positiva rispetto al source le giunzioni source-body e drain-body sono polarizzate inversamente.

Analizziamo

Nel caso in cui abbiamo $v_G$=0 e $V_{DS}$ (tensione applicata tra drain e source) positiva le giunzioni sono polarizzate inversamente e si oppongono al passaggio della corrente.

Nel caso invece in cui $v_{DS}>0$ e $v_{GS}>0$, abbiamo che quest’ultima tensione allontana le lacune dal gate verso il body creando una regione svuotata. Questa regione viene riempita dagli elettroni delle regioni di drain e di source. Si è formato quindi un canale di tipo n che li collega. Essendo $v_{DS}$ positiva la corrente scorrerà tra S e D.

![Untitled](Capitolo%207/Untitled%203.png)

Questo tipo di MOSFET è chiamato MOSFET a canale n (NMOS). Questo canale viene formato invertendo il substrato da tipo p a tipo n, per questo viene chiamato strato di inversione.

IL valore di $v_{GS}$ sufficiente a far formare il canale di conduzione è chiamata tensione di soglia $V_t$

Esistono anche MOSFET a canale p (PMOS) in cui source e drain sono regioni $p^+$ e il substrato n, inoltre usa le lacune come portatori di cariche e $v_{GS}, v_{DS}$  e $V_t$ sono negative

![Untitled](Capitolo%207/Untitled%204.png)

### Caratteristiche corrente-tensione

Supponiamo di lavorare con $v_{DS}=0.1/0.2V$. Che il canale sia formato ($v_{GS}\ge V_t$), source e substrato connessi a massa e che le tensioni applicate agli altri due elettrodi siano riferite a massa. Se la tensione $v_{GS}$ aumenta, aumenta la conduttanza del canale. La corrente $i_D$ risulta proporzionale a $v_{GS}$ e $v_{DS}$

![Untitled](Capitolo%207/Untitled%205.png)

All’aumentare di $v_{DS}$ la tensione vale 0 in corrispondenza del source e $v_{DS}$ in corrispondenza del drain e assumendo valori intermedi nel canale. Misurando la tensione tra il gate e i vari punti del canale la tensione varia da $v_{GS}$ nel source a $(v_{GS}-v_{DS})$ nel drain

Lo spessore del canale dipende dalle due tensioni $v_{DS}$ e $v_{GS}$. Se aumentiamo $v_{DS}$ il canale si strozzerà nelle vicinanze del drain

![Untitled](Capitolo%207/Untitled%206.png)

Non appena $v_{DS}$ è sufficientemente elevata, le caratteristiche $i_d-v_{DS}$ si incurveranno.

Quando $v_{DS}=(v_{GS}-V_t)$ il canale risulta completamente strozzato. Sostituendo questo valore alla tensione sul drain $(v_{GS}-v_{DS})$ otteniamo $V_t$ . Il canale si dice in pinch-off-

Se $v_{DS}\ge (v_{GS}-V_t)$ si estende la zona dello strozzamento in direzione del source, ma sezione del canale e velocità delle cariche rimangono costanti, come la corrente $i_D$, che dipende da queste ultime.

La tensione $v_{DS(sat)}=v_{GS}-V_t$ è chiamata tensione di saturazione. Per $v_{DS}\ge v_{DS(sat)}$ il MOSFET è in regione di saturazione. Per $v_{DS}< v_{DS(sat)}$ il MOSFET è in regione di triodo. La tensione di saturazione cambia al variare di $v_{GS}$

Il MOSFET dell’immagine prima è  equivalente allo schema

![Untitled](Capitolo%207/Untitled%207.png)

essendo il gate separato dal resto del componente, $i_{G}=0$, quindi $i_D=i_S$. Poiché il source è comune a ingresso e uscita prende il nome di MOSFET a source comune.

![Untitled](Capitolo%207/Untitled%208.png)

Possiamo distinguere tre regioni:

1. $v_{GS}<V_t$ → regione di cut-off o di interdizione
    
    In questo caso non si forma il canale, quindi non passa corrente
    
2. $v_{GS}\ge V_t$ e $v_{DS}<v_{GS}-V_t$ → regione di triodo
    
     $i_d$ e $v_{DS}$ sono proporzionali, quindi la caratteristica è una retta. Aumentando $v_{DS}$ il canale inizia a strozzarsi e la caratteristica ad incurvarsi.
    
    ![Untitled](Capitolo%207/Untitled%209.png)
    
    ![Untitled](Capitolo%207/Untitled%2010.png)
    
    K → parametro di conducibilità
    
    $\mu$ → mobilità dei portatori
    
    $C_{ox}$→ capacità per unità di area del condensatore tra il gate e il substrato (detta capacità dell’ossido),
    
    W la larghezza e L la lunghezza del canale
    
    Per $v_{DS}$ piccolo trascuriamo il termine quadratico 
    
    ![Untitled](Capitolo%207/Untitled%2011.png)
    
3. $v_{GS}\ge V_t$  e  $v_{DS}\ge v_{GS}-V_t$ → regione di saturazione
    
    La corrente è indipendente da $v_{DS}$, ma non da $v_{GS}$. se vogliamo trovare il suo valore sostituiamo nella 7.5 a $v_{DS}$ il valore di confine tra le due regioni, $v_{DS(sat)}=v_{GS}-V_t$
    
    ![Untitled](Capitolo%207/Untitled%2012.png)
    
    Quest’ultima formula rappresenta la transcaratteristica del MOSFET in saturazione
    
    ![Untitled](Capitolo%207/Untitled%2013.png)
    

Le rette della transcaratteristica del mosfet in realtà non sono perfettamente orizzontali. La loro pendenza dipende dal fatto che aumentando $v_{DS}$ oltre il valore $v_{DS(sat)}$ la lunghezza del canale diminuisce, K aumenta e di conseguenza anche $i_D$

![Untitled](Capitolo%207/Untitled%2014.png)

Essendo $V_A$ non infinita, il MOSFET non si comporta come un generatore ideale di corrente.

Definiamo $g_o=\frac{I_D}{V_A}$ la conduttanza di uscita, con $I_D$ la corrente corrispondente al particolare valore di vGS per cui go è stato calcolato, ovvero la corrente nel punto di riposo .

Quadro riassuntivo:

![Untitled](Capitolo%207/Untitled%2015.png)

### MOSFET a svuotamento

In un MOSFET a svuotamento il canale è già realizzato fisicamente. Se $v_{DS}>0$ è presente una corrente $i_D$ non nulla anche se $v_{GS}=0$. Nel caso invece in cui $v_{DS}>0$ ma $v_{GS}<0$ allora il canale si assottiglia, a causa dell’allontanamento degli elettroni dal canale. Diminuendo ulteriormente $v_{GS}$ fino a raggiungere una tensione $V_T$ negativa il canale risulterà completamente svuotato di elettroni. Scendendo sotto $V_T$ avremo che $i_D=0$ anche se $v_{DS}>0$. Questa è la condizione di cut-off del dispositivo. Nel caso in cui $v_{GS}>0$ il MOSFET funzionerà ad arricchimento, quindi un MOSFET a svuotamento può funzionare ad arricchimento, ma non viceversa!

![Untitled](Capitolo%207/Untitled%2016.png)

La differenza con il simbolo del MOSFET ad arricchimento è la presenza della linea verticale che rappresenta il canale permanente.

![Untitled](Capitolo%207/Untitled%2017.png)

Sopra sono riportate le caratteristiche $i_D-v_{DS}$ del MOSFET a svuotamento

Le regioni sono le stesse di un MOSFET ad arricchimento, ma il passaggio da una regione all’altra avviene quando $v_{DS}=v_{GS}-V_T$

Come per il MOSFET ad arricchimento $i_D$ dipende da $v_{DS}$ nella regione di saturazione

![Transcaratteristica $i_D-v_{GS}$](Capitolo%207/Untitled%2018.png)

Transcaratteristica $i_D-v_{GS}$

Un parametro utile per i MOSFET a svuotamento è la corrente di drain in saturazione per $v_{GS}=0$

![Untitled](Capitolo%207/Untitled%2019.png)

![Untitled](Capitolo%207/Untitled%2020.png)