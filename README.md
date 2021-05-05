# CROSTATUS' IDEA
## OVERVIEW
La mia idea si basava su un gioco rogue-lite (“con run”) non hardcore basato sulla **raccolta di minerali, conquista di zone e gestione del proprio esercito**.

Con **grafica 2D e visuale isometrica**, giochi nei panni di **leader di una colonia** che deve espandersi e sopravvivere *(tipo ape regina)*.

## LA MAPPA
La mappa è divisa in settori e, **partendo dal settore centrale**, lo scopo è quello di raggiungere una qualsiasi zona laterale per vincere.  

*Ecco un esempio di mappa 9x9:*


X | X | X | X | X | X | X | X | X
--- | - | - | - | - | - | - | - | -
**X** |  |  |  |  |  | **B** |  | **X**
**X** |  | **B** |  |  |  |  |  | **X**
**X** |  |  |  |  |  |  |  | **X**
**X** |  |  |  | **S** |  |  |  | **X**
**X** |  |  |  |  |  | **B** |  | **X**
**X** |  | **B** |  |  |  |  |  | **X**
**X** |  |  |  |  |  |  |  | **X**
**X** | **X** | **X** | **X** | **X** | **X** | **X** | **X** | **X**

- **S = START**: Settore principale dal quale inizia ogni partita, e contiene le strutture fondamentali per gestire risorse e unità.
- **B = BOSS**: Sparsi casualmente per la mappa, in una quantità dipendente dalla grandezza della mappa.
- **X = SETTORE FINALE**: Giunti in una qualsiasi di queste caselle bisognerà affrontare una sfida finale e poi, se superata, partono i titoli di coda.
- **CASELLA VUOTA**: Area standard con nemici e risorse da scavare. Una volta che sono stati uccisi tutti i nemici al suo interno la zona rimane non ostile per tutta la durata della partita.  

Ogni zona ha un ingresso sui quattro lati per potersi spostare nelle zone adiacenti (sopra, sotto, sx, dx). La zona nella minimappa è **rappresentata come un quadrato ma in gioco non deve avere per forza tale forma**.

## MINERALI DA TROVARE
Ogni casella contiene una **quantità stabilita di risorse per ogni tipo**. Una volta che una zona è stata prosciugata è praticamente inutile, ma c'è sempre spazio per nuove idee.  
I tipi di minerali scavabili sono 5:  
  - **ROSSO**: Carburante dell' intera colonia, serve a:
    - Ripristinare salute
    - Ripristinare stamina
    - Ricaricare armi
  - **VERDE**: Minerale che si può incubare per spawnare un' unità di tipo **Scout**
  - **BLU**: Minerale che si può incubare per spawnare un' unità di tipo **Scienziato**
  - **ROSSO**: Minerale che si può incubare per spawnare un' unità di tipo **Guerriero**
  - **VIOLA**: Minerale che si può incubare per spawnare un' unità di tipo **Minatore**

*(Serviranno ovviamente nomi più fantasiosi!)*  

**I minerali servono anche per completare le ricerche.**  

## TIPI DI UNITA'
Tutte le unità hanno **perma-death** ma dovrebbero essere sostituibili con forze nuove non troppo difficilmente.  
Le unità utilizzano stamina per effettuare qualsiasi operazione, se la stamina scende a zero tornano alla base.
 - **LEADER**: ce n'è uno solo per l' intera partita, se muore hai perso. Il leader si muove nella base operativa e decide come impegnare le risorse ottenute e quali ricerche effettuare. Per rendere tutto un pò più teso per vincere dovrà affrontare un boss finale. Le statistiche del leader per l' ultima battaglia dipendono dalle azioni intraprese durante tutto l' arco della partita, es:  
  - minerali scavati => stamina
  - operazioni di scouting => velocità di movimento
  - uccisioni => danni
  - ricerche completate => hp massimi

- **SCOUT**: Unità veloce ma debole, può essere spedito nelle caselle adiacenti per rilevare informazioni utili alla prossima scelta da intraprendere come quali/quanti minerali sono presenti, presenza o no di boss, numero di nemici.

- **MINATORE**: Scava e trasporta i minerali alla base.
- **SCIENZIATO**: Topo da laboratorio che permette di avviare le ricerche. Le ricerche possono chiedere task (es: uccisioni) e/o risorse per progredire.
- **GUERRIERO**: Può essere melee o ranged, mena la gente.  

## GAMEPLAY
Il loop principale per progredire dovrebbe essere:  
  1. **Scouting** delle zone limitrofe
  2. **Assalto** alla zona scelta per ripulirla dai nemici
  3. **Raccolta** risorse
  4. **Gestione** su come investire le risorse e ricerche
  5. Ripeti

La fase 3 è fatta per forza dalla CPU *(troppo noiosa)*, mentre la 4 viene eseguita solo dal giocatore.   
Invece la 1 e 2 possiamo scegliere se **affidarla alle unità in maniera autonoma o giocarla di persona**, vestendo i panni delle unità in tale missione.    
Ciò permette al giocatore di svolgere più di un' attività alla volta.   
Se si **delega** un' operazione alla CPU, si dovrà scegliere quante unità affidare e affidarsi ad **un po' di RNG** per i risultati (successo/insuccesso, quante unità morte).    
*(Wow grazie per aver letto fino a qua)*   
Se invece si decide di giocarle di persona queste missioni, dovremmo :    
- pulire la zona "*alla Binding of Isaac*" nel caso dei guerrieri   
-  scoprire la mappa in modo stealth, notare risorse e disattivare trappole in caso dello scouting.


### CONTRO
  - A volte mi sembra carino e a volte la cosa più noiosa che abbia mai sentito.
  - Non so se l' abbinamento di elementi gestionali con il rogue ci azzeccano qualcosa.
  - Sembra difficile da bilanciare per non essere o estremamente facile (troppe risorse) o troppo stressante.

### PRO
  - Non c'è da trovare lore
  - La mappa così formata permette a te di scegliere come giocare. Vuoi speedrunnare ? vai tutto a dritto. Vuoi uccidere roba ? Pulisci tutte le stanze. Vuoi un gioco carino? Non chiedere a me.
