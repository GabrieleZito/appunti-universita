Il funzionamento è simile a quello dei MOSFET, ma la differenza principale è che la corrente che scorre tra drain e source è controllata non solo dalla tensione sul gate, ma anche dalla corrente. Nel caso del BJT la resistenza di ingresso sarà bassa, per fare passare la corrente, anche se molto piccola.

Il termine bipolare indica che la conduzione coinvolge sia portatori maggioritari che minoritari. Lo scopo del transistor (transfer-resistor) è quello di trasferire una variazione di corrente da una resistenza bassa ad una di valore più elevato, amplificando così la tensione.

![Untitled](Cap%208%20-%20BJT/Untitled.png)

Il BJT è formato da tre regioni, Emettitore, base e collettore. Ogni regione è connessa ad un terminale, in modo da avere tre elettrodi. Ci sono 2 giunzioni p-n che in base alla polarizzazione definiscono diversi modi di funzionamento del BJT.

![Untitled](Cap%208%20-%20BJT/Untitled%201.png)

Usiamo per esempio il BJT come in figura sopra. La giunzione EB polarizzata direttamente e la giunzione CB inversamente. UN BJT polarizzato in questo modi si dice in zona attiva.

La giunzione EB fa passare la corrente, in particolare gli elettroni vanno nella base e le lacune vanno nell’emettitore. Ma nell’emettitore ci sono tanti elettroni e nella base poche lacune. La corrente di emettitore è dominata dalla corrente degli elettroni. Questi elettroni arrivati nella base non hanno il tempo di ricombinarsi, quindi verranno presi dal collettore, essendo la zona di svuotamento molto ampia

### Caratteristiche del BJT

Corrente di collettore $i_C$ → è data dal flusso di elettroni che attraversa la giunzione EB, e che poi viene spazzata via dal campo elettrico della zona di svuotamento della giunzione CB. Ignorando i pochi elettroni che si ricombinano nella regione di base, la corrente di collettore coincide con la corrente del diodo base-emettitore la cui espressione è la seguente 

![6.1](Cap%208%20-%20BJT/Untitled%202.png)

6.1

$i_c$ è proporzionale a $e^{\frac{V_{BE}}{V_T}}$

Corrente di base $i_B$ → è composta da due componenti. La prima è un flusso di cariche maggioritarie che attraversa la giunzione di un diodo polarizzato direttamente (è anch’essa proporzionale a $e^{\frac{V_{BE}}{V_T}}$). La seconda dipende dalle lacune perse durante la ricombinazione (anche questa è proporzionale a $e^{\frac{V_{BE}}{V_T}}$).

Essendo la corrente di base formata da componenti proporzionali alla stessa quantità, anche  $i_c$ e $i_B$ sono proporzionali tra di loro. Definiamo la costante di proporzionalità $\beta$:

![8.1](Cap%208%20-%20BJT/Untitled%203.png)

8.1

Corrente di emettitore $i_E$ → è la corrente che esce dal BJT e si può calcolare come $i_E=i_C+i_B$.

Sostituendo questa nella 8.1 si ottiene 

![Untitled](Cap%208%20-%20BJT/Untitled%204.png)

[https://www.notion.so](https://www.notion.so)

Poniamo 

![Untitled](Cap%208%20-%20BJT/Untitled%205.png)

abbiamo che $i_C=\alpha i_E$

Avendo che $\alpha\simeq 1$ allora $i_C\simeq i_E$

![Untitled](Cap%208%20-%20BJT/Untitled%206.png)

Lo schema sopra è una configurazione ad emettitore comune. Abbiamo il parametro $\beta=\frac{i_C}{i_B}$ che prende il nome di guadagno di corrente ad emettitore comune

![Untitled](Cap%208%20-%20BJT/Untitled%207.png)

Quella sopra è la transcaratteristica. In zona attiva, la funzione è rettilinea, con coeff. angolare $\beta$, ma superato un certo valore di $V_{CE}$ si incurva. La caratteristica non passa per l’origine, ma parte da una certa tensione di soglia, al di sotto della quale l’unica corrente che passa è quella dei due diodi polarizzati inversamente.

Le caratteristiche di uscita possono essere controllate sia dalla corrente che dalla tensione in entrata. vediamolo per la corrente $i_B$:

![Untitled](Cap%208%20-%20BJT/Untitled%208.png)

Quando $V_{CE}$ è maggiore di qualche decimo di volt, si ha una corrente costante $i_C$ che dipende solo da $i_B$. La tensione $V_{CE}$ è data da $V_{CE}=V_{CB}+V_{BE}$, ma essendo che $V_{BE}$ è la tensione di soglia del diodo BE (0,6-0,7V), allora dipenderà quasi esclusivamente da $V_{CB}$. Questa non andrà a cambiare la corrente ma solo la larghezza della zona di svuotamento CB, in modo che gli elettroni vengano spostati più velocemente verso il collettore. In realtà è presente una piccola dipendenza di $i_C$ da $v_{CE}$, dovuta alla dimensione più grande della zona di svuotamento, che cattura qualche elettrone in più. Per questo la caratteristica è leggermente inclinata. Questo fenomeno prende il nome di effetto Early, che è lo stesso che abbiamo visto nei FET.

Oltre un certo valore di $V_{CE}$ la corrente aumenta rapidamente e CB entra in breakdown. Al di sotto invece di un certo valore la corrente $i_c$ diminuisce rapidamente sino a zero. Questo avviene quando la giunzione Cb non è più polarizzata inversamente. Diminuendo $v_{CE}$ si restringe la zona di svuotamento e il campo elettrico non riesce più a spostare gli elettroni. In pratica avviene quando $V_{CE}\simeq0$, $V_{BE}\simeq0,7V$ e $V_{CB}=-V_{BC}=-0,7V$, cioè quando entrambe le giunzioni sono polarizzate direttamente.

La corrente $i_C$ è invece sempre uguale a 0 se $i_B=0$ e questo si ha quando $V_{BE}<0,7V$. Questo corrisponde ad avere entrambe le giunzioni polarizzate inversamente

![Untitled](Cap%208%20-%20BJT/Untitled%209.png)