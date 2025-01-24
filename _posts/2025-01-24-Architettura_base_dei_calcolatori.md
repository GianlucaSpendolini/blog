---
title: Architettura (base) di un calcolatore
date: 2025-01-24
---

Questo post è diverso dagli altri: non lo userò per inserire degli appunti che ho preso su un argomento ma lo uso per vedere ciò che ricordo di quel macro-argomento che ho studiato.

In futuro farò altri post di questo tipo.

In questo caso andrò a trattare: "**L'architettura di Von Neumann**".

Questo post lo suddivido nel seguente modo:
- [Cos'é un calcolatore](#cosé-un-calcolatore)
- [L'architettura di Von Neumann](#architettura-di-von-neumann)
- [Discussione: velocità e architettura dei processori](#discussione)
- [Fonti](#fonti)



## Cos'é un calcolatore

Un calcolatore è una macchina che esegue programmi per fornire risultati ad un utente.



## L'architettura di Von Neumann

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

Oltre ai precedenti, questo componente presente un bus, chiamato [bus interno](#bus-interno).

#### ALU

L'ALU è quella componente adibita all'esecuzione delle operazione (logiche e aritmetiche).

#### Control Unit

La control unit, coordina le operazioni interne alla CPU. 

Inoltre, tramite bus interno, apre i collegamenti tra:

  Ccontrol Unit - Algorithm Logic Unit - Registri

Inoltre, è quella componente che interpreta le varie istruzioni e le esegue, utilizzando i vari altri strumenti che ha a disposizione.

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



## Discussione

...



## Fonti

"Concetti fondamentali di informatica", V. Moriggia, G. Psaila, Esculapio
