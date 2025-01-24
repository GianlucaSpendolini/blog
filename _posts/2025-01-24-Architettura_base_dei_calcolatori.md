---
title: Architettura di un calcolatore (base)
date: 2025-01-24
---

Questo post è diverso dagli altri: non lo userò per inserire degli appunti che ho preso su un argomento ma lo uso per vedere ciò che ricordo di quel macro-argomento che ho studiato.

In futuro farò altri post di questo tipo.

In questo caso andrò a trattare: "_L'architettura di Von Neumann_".

Questo post lo suddivido nel seguente modo:
- [Cos'è un calcolatore](#cose-un-calcolatore)
- [L'architettura di Von Neumann](#architettura-di-von-neumann)
- [Discussione: velocità e architettura dei processori](#discussione)
- [Fonti](#fonti)



## Cos'è un calcolatore

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
  - Gestisce le interruzioni





## Discussione

...



## Fonti

"Concetti fondamentali di informatica", V. Moriggia, G. Psaila, Esculapio
