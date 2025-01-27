---
title: Architettura di un calcolatore (base)
date: 2025-01-24
---

<style>
    .err {
        color: LightCoral;
    }
</style>

Questo post è diverso dagli altri: non lo userò per inserire degli appunti che ho preso su un argomento ma lo uso per vedere ciò che ricordo di quel macro-argomento che ho studiato.
In futuro farò altri post di questo tipo.

Ho presente che questi argomenti, per un informatico, dovrebbero essere la base, ma io ho iniziato a venire a conoscienza di questo mondo nel 2022, quando ho iniziato il corso ITS.
Siccome molti argomenti non li ricordo bene, in vista dell'immatricolazione all'università telematica e-Campus (indirizzo _Sistemi di elaborazione e controllo_ della facoltà di [_Ingegneria Informatica_](https://uniecampus.coursecatalogue.cineca.it/corsi/2024/10026)), ho deciso di ripassare gli argomenti base (dalla parte hardware a quella software).

In questo caso andrò a trattare: "**L'architettura di Von Neumann**" (argomento studiato nuovamente e ripassato nella settimana che parte dal 20/01/2025).

Questo post lo suddivido nel seguente modo:
- [Cos'é un calcolatore](#cosé-un-calcolatore)
- [L'architettura di Von Neumann](#architettura-di-von-neumann)
- [Discussione: velocità e architettura dei processori](#discussione)
- [Fonti](#fonti)



## Cos'é un calcolatore

Un calcolatore è una macchina che esegue programmi per fornire risultati ad un utente.



## Architettura di Von Neumann

Un calcolatore è composto principalmente dalle seguenti componenti fisici:
- [Central Process Unit](#cpu)
- [Memoria centrale](#memoria-centrale)
- [Dischi](#dischi)
- [Componenti esterne](#componenti-esterne)

Oltre alle precedenti, presenta anche un ulteriore componente: il [bus di sistema](#bus-di-sistema).


### CPU

La CPU è il componente predisposto all'esecuzione dei comandi. Essa coordina i vari componenti del calcolatore, facendo sì che tutto funzioni regolarmente.

Ha 3 principali componenti:
- [Algorithm Logic Unit](#alu)
- [Control Unit](#control-unit)
- [Registri](#registri)

Oltre ai precedenti, questo componente presenta un bus ([bus interno](#bus-interno)), e un "orologio" interno ([system clock](#system-clock)).

#### ALU

L'ALU è quella componente adibita all'esecuzione delle operazione (logiche e aritmetiche).

#### Control Unit

La control unit, coordina le operazioni interne alla CPU. 

Tramite bus interno, apre i collegamenti tra:

    Control Unit - Algorithm Logic Unit - Registri

Inoltre, è quella componente che interpreta le varie istruzioni e le esegue, utilizzando i vari altri strumenti che ha a disposizione.

##### Istruzioni

Una cosa molto importante da precisare è il concetto di istruzione e programma.

Una istruzione è scritta in linguaggio macchina ed è ciò che capisce il computer per poi eseguire una o più operazioni che porteranno, all'utente, ad avere il risultato voluto.

Inoltre, è bene precisare che una istruzione è un insieme di microistruzioni, ovvero le operazioni base che il calcolatore è in grado di fare.

Un programma è un insieme di istruzioni.

Siccome è complicato scrivere in linguaggio macchina, nonostante esista una logica dietro gli insiemi di 1 e 0, è stato creato il linguaggio assembler per facilitarne la scrittura. 
Questo linguaggio è quello appena sopra quello macchina ed è l'intermezzo tra quest'ultimo e i linguaggi di più alto livello.

La sintassi si divide in più gruppi di istruzioni
- Calcolo
  - Somma i valori di A e B, salvando il risultato nel registro A
    ```
      SUM
    ```
  - Toglie, dal valore nel registro A, il valore del registro B
    ```
      DIF
    ```
  - Incrementa di 1 il valore del registro A
    ```
      INC
    ```
  - Decrementa di 1 il valore del registro A
    ```
      DEC
    ```
- Accesso alla memoria
  - Inserisce, nel registro A, il valore presente all'indirizzo "i"
    ```
    SETA i
    ```
  - Inserisce, nel registro B, il valore presente all'indirizzo "i"
    ```
    SETB i
    ```
  - Inserisce, all'indirizzo "i", il valore presente nel registro A
    ```
    STOREA i
    ```
  - Inserisce, all'indirizzo "i", il valore presente nel registro B
    ```
    STOREB i
    ```
- Salto (interrompe il funzionamento sequenziale)
  - Esegue l'istruzione contenuta all'indirizzo "i"
    ```
    JUMP i
    ```
  - Possono essere presenti anche più condizioni in base al valore nel registro A
    - = 0
      ```
      JUMPZ i
      ```
    - != 0
      ```
      JUMPNZ i
      ```
    - \> 0
      ```
      JUMPGZ i
      ```

##### Fase di fetch

Un'altra cosa molto importante da comprendere è la fase di fetch, ovvero la fase di acquisizione del dato.

Essa comprende diversi step:
- ...

#### Registri

I registri sono quella parte della CPU che memorizzano i dati utili che servono alla CPU per funzionare.

Sono memorie molto veloci (molto più della RAM di cui parlerò più avanti).

Esistono 7 tipi principali di registri all'interno della CPU:
- "A" e "B"
  - Sono quei registri che vanno a memorizzare i dati utili alle operazioni (compresi i risultati delle precedenti e gli operandi)
- Status Register
  - Questo registro contiene il risultato dell'ultima operazione di confronto
  - Potrebbe anche contenere l'eventuale overflow derivante da un'operazione aritmetica
- Program Counter
  - Contiene l'indirizzo del Byte di memoria contenente la prossima istruzione da eseguire
- Current Instruction Register
  - Contiene l'istruzione che la CU sta eseguendo
- Address Register
  - Si interfaccia con la memoria centrale
  - Mette a disposizione del bus indirizzi l'indirizzo al Byte di memoria a cui accedere
- Data Register
  - Questo registro è utile per rendere visibili i dati che devono entrare o uscire dalla CPU
  - In caso di
    - Invio
      - Viene messo il dato nel DR
      - Il bus dati, di cui parleremo dopo, vede il dato e lo preleva
        - Lo porta dove indicato dal bus indirizzi
    - Ricezione
      - Il dato, dal bus dati, viene depositato nel DR
      - La CU preleva il dato e lo pone in un altro registro
- Interrupt Register
  - Gestisce le interruzioni\*
 
\* Una interruzione è un segnale, derivante da un dispositivo quando è pronto, a cui è assegnato un numero (utile alla CU per riconoscerlo ed avviare il programma apposito per gestirlo).

#### Bus Interno

Questo bus collega le componenti interne della CPU su delle linee elettriche.

#### System Clock

Il system clock è un dispositivo, utilizzato dalla CU, per temporizzare le attività della CPU.

Produce segnali ad altizzima frequenza (a livello di GHz) di cui, ogni segnale è detto isieme di colpi di clock (quindi ogni impulso del segnale è un colpo di clock).


### Memoria Centrale

La memoria centrale è una memoria molto veloce. &Eacute; composta da una sequenza di bit, raggruppati in multipli di Byte (di cui ognuno ha una posizione ben precisa detta _indirizzo_).

Principalmente è composta da una memoria RAM (Random Access Memory). 
Essa memorizza i programmi e i dati ma, una volta tolta l'alimentazione elettrica, perde tutti i dati (per questo motivo è detta _volatile_).
Oltre alla memoria RAM, è presente una memoria minore: la ROM (Read Only Memory). 
Questo tipo di memoria non è volatile e contiene principalmente:
- ...
  - Il programma principale che, una volta avviato il computer, va a cercare il Sistema Operativo e lo esegue
- Basic Input/Output System
  - Insieme di programmi base per gestire i dispositivi esterni
 

### Dischi

I dischi hanno una capacità di memoria molto maggiore rispetto a quella della memoria centrale, ma è più lenta poichè il trasferimento di file e le modalità di lettura, richiedono più tempo.

Si dividono in due principali categorie:
- Magnetici
  - Sono modificabili
  - Vengono scritti e letti a blocchi di 1024 B
  - Si dividono a loro volta tra
    - Fissi
      - Come l'hard disk
    - Rimovibili
      - Come il floppy disk
  - Non possono essere danneggiati dalla polvere poichè chiusi in un contenitore metallico e sottovuoto
- Ottici
  - Scritti e letti tramite un laser
  - Possono essere danneggiati dalla polvere
  - Si dividono in
    - 3 Categorie
      - Compact Disk
      - Display Video Disk
      - Blu ray Disk
    - Di cui, ogni categoria, può essere distinta tra
      - -ROM
        - Se il disco non è scrivibile
      - -R
        - Se il disco può essere scritto soltanto una volta
        - I CD e DVD si dividono ulteriormente in
          - \+
          - \-
      - -RW
        - Se il disco può essere scritto più volte
  - Molto spesso sono utilizzati per tenere i dati come back-up poichè la loro velocità di
    - Lettura < disco magnetico
    - Scrittura \<< disco magnetico


### Componenti esterne 

Le due componenti principali sono il monitor, da scegliere con una buona risoluzione (ovvero la somma dei pixel e colori che può mostrare contemporaneamente), e la tastiera.

Ci sono molti dispositivi esterni, basti pensare tutti coloro che possono essere collegati al PC (fisicamente o meno).


### Bus di sistema

Il bus di sistema serve per permettere lo scambio di dati tra tutte le componenti.

Esso è suddiviso in 3 tipologie:
- Bus Dati
  - Bus che trasporta i dati ~~tra le diverse componenti del computer~~ da e verso la CPU
- Bus Indirizzi
  - Bus che trasporta l'indirizzo di memoria a cui accedere
  - <span class="err">Comunica con la memoria centrale</span>
- Bus di Controllo
  - Il bus di controllo è colui che trasporta il comando che la CPU ha imposto
  - <span class="err">In caso di</span>
    - <span class="err">Lettura</span>
      - <span class="err">Prende il dato dall'indirizzo fornito dal bus indirizzi</span>
    - <span class="err">Scrittura</span>
      - <span class="err">Memorizza il valore presente nel bus dati nell'indirizzo presente sul bus indirizzi</span>



## Discussione

Possiamo parlare di una tematica importante: la velocità di elaborazione. 
Ogni volta che si sceglie un computer, per capire la velocità basta vedere la frequenza di clock, poichè una frequenza maggiora, comporta una velocità maggiore.

Più o meno, con X colpi di clock, il processore può eseguire X &times; 0.5% microistruzioni.

Infine, possiamo distinguere 2 tecnologie riguardanti i processori:
- Complex Instruction Set Computer
  - Numero maggiore di istruzioni poichè programmi più complessi
    - CU più grande -> meno spazio per registri
  - Scrittura agevolata
- Reduced Istruction Set Computer
  - Numero minore di istruzioni -> programmi più semplici
    - CU più piccola -> più spazio per registri
- Scrittura non agevolata

Attualmente non c'è distinzione tra le due tipologie.



## Fonti

"Concetti fondamentali di informatica", V. Moriggia, G. Psaila, Esculapio
