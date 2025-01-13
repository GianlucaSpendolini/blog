---
title: Google Search e le SEO
date: 2025-01-13
---

Come detto nel [precedente post](./2025-01-08-Creare_un_blog.md), un sito deve essere indicizzato per poter essere visualizzato nei risultati di un motore di ricerca.

In questo post, introdurrò la ricerca di Google ed i vari processi che sono alla base, successivamente parlerò dell'argomento principale:
- [La ricerca di Google](#google_search)
- [Search Engine Optimization (SEO)](#search_engine_optimization)
- [Fonti](#fonti)


## Google Search

Per questa sezione, inizierò introducendo le nozioni base sulla ricerca, per poi seguire con una descrizione più approfondita:
- [Nozioni base](#nozioni_base)
- [Step fondamentali della ricerca](#step_fondamentali)

### Nozioni base

Gli aspetti fondamentali relativi a ciò che rende un contenuto idoneo ad essere mostrato e a funzionare
    - [Requisiti tecnici](#requisiti_tecnici)
        - Ciò di cui Google ha bisogno in una pagina web per mostrarla nei risultati di ricerca 
    - [Norme relative allo spam](#norme_relative_allo_spam)
        - Comportamenti e tattiche che possono portare ad un ranking inferiore/rimozione dai risultati
    - [Best practice](#best_practice)
        - Elementi principali che possono contribuire a migliorare l'aspetto del sito nei risultati

Nonostante i precedenti aspetti vengano rispettati, non è detto che Google eseguirà la scansione, l'indicizzazione o la pubblicazione dei contenuti.


#### [Requisiti tecnici](https://developers.google.com/search/docs/essentials/technical)


#### [Norme relative allo spam](https://developers.google.com/search/docs/essentials/spam-policies)


#### [Best practice](https://developers.google.com/search/docs)

In generale esistono alcune pratiche principali che possono avere il massimo impatto sul ranking e sull'aspetto dei tuoi contenuti web:
    - Creare contenuti utili, affidabili e pensati per le persone
        - https://developers.google.com/search/docs/fundamentals/creating-helpful-content
    - Usa parole che le persone userebbero per cercare i tuoi contenuti 
        - posizionale in posizioni di evidenza (come nel titolo e l'intestazione principale) o altri elementi descrittivi (come titoli alternativi delle immagini o testo dei link)
    - Rendere i link sottoponibili alla scansione, in modo che Google possa trovare altre pagine sul sito tramite i link sulla pagina 
    - Fai conoscere il sito
        - partecipa alle community in cui puoi far conoscere a persone che la pensano come te i servizi e prodotti che menzioni sul sito 
    - Se ho altri contenuti -> segui le best practice per far comprendere anche a loro quelle parti della pagina 
        - immagini
            - https://developers.google.com/search/docs/appearance/google-images
        - video
            - https://developers.google.com/search/docs/appearance/video
        - dati strutturati
            - https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data
        - JavaScript
            - https://developers.google.com/search/docs/crawling-indexing/javascript/javascript-seo-basics
    - Migliora l'aspetto nella Ricerca Google
        - abilitando funzionalità significative per il sito
    - Se ci sono contenuti che non si vogliono mostrare nei risultati/vuoi disattivare le funzionalità
        - Controlla come i contenuti vengono visualizzati nella ricerca google (https://developers.google.com/search/docs/crawling-indexing/control-what-you-share)


### Step fondamentali

Il motore di ricerca utilizza dei "web crawler" per esplorare il web e trovare pagine da aggiungere al suo indice.

Non è garantito che eseguirà la scansione della tua pagina, che la indicizzerà o la pubblicherà, anche se verranno seguite le nozioni di base.

Fasi
    - Scansione
        - Scaricati i testi, immagini e video dalle pagine trovate su internet tramite programmi automatizzati chiamati crawler
    - Indicizzazione 
        - Analizzati il testo, le immagini e i file video sulla pagina e memorizza le informazioni nell'Indice Google (è un grande database)
    - Pubblicazione dei risultati di ricerca 
        - Restituzione delle informazioni pertinenti alla query

SCANSIONE
    - individuazione degli URL
        - capire quali pagine esistono sul web
            - non esiste un registro centrale di tutte le pagine web -> Google deve costantemente cercare pagine nuove e aggiornate e aggiungerle al proprio elenco di pagine note
        - tramite invio di una sitemap, ovvero un elenco di pagine 
    - visita/scansione della pagina 
        - effettuata grazie a Googlebot -> algoritmo per determinare siti che deve scansionare/frequenza della scansione/numero di pagine da recuperare in ogni sito
            - non esegue la scansione di tutte le pagine -> non autorizzate (https://developers.google.com/search/docs/crawling-indexing/robots/robots_txt) per la scansione (da proprietario) o non accessibili senza accesso
            - su quelle che scansiona 
                - visualizza ed esegue codice JavaScript -> versione recente di Chrome -> visualizza come il browser vede la pagina che visiti -> rendering importante per vedere contenuto derivante da JavaScript
        - crowler programmati in base alle risposte del sito (500 è rallentamento) in modo da tentare di non eseguire troppo velocemente la scansione -> evita sovraccarico
    - problemi che possono verificarsi
        - server
            - https://developers.google.com/search/docs/crawling-indexing/http-network-errors#http-status-codes
        - rete 
            - https://developers.google.com/search/docs/crawling-indexing/http-network-errors#network-and-dns-errors
        - regole del file robots.txt -> impediscono l'accesso alla pagina 
            - https://developers.google.com/search/docs/crawling-indexing/robots/intro

INDICIZZAZIONE 
    - Capire cosa tratta la pagina 
        - elaborazione ed analisi dei contenuti tesuali e dei tag di contenuti chiave ed attributi (come <title> e attributi ALT)
    - Capisce se pagina è duplicato o canonica 
        - canonica -> mostrata nei risultati
            - raggruppamento (clustering) delle pagine con contenuti simili trovate su internet
            - selezionata quella più rappresentativa
            - altre pagine sono versioni alternative -> pubblicate in contesti diversi (accesso da dispositivo mobile pagina specifica in quel cluster)
    - Raccoglie indicatori dalla pagina canonica e contenuti -> usati nella fase di pubblicazione dei risultati 
        - Info archiviate nell'Indice di Google (grande database ospitato su migliaia di computer)
    - Dipende anche dai contenuti e metadati -> problematiche
        - Qualità bassa dei contenuti
            - https://developers.google.com/search/docs/essentials
        - Le regole dei meta tag Robots non consentono l'indicizzazione
            - https://developers.google.com/search/docs/crawling-indexing/block-indexing
        - Il design del sito potrebbe rendere difficile l'indicizzazione 
            - https://developers.google.com/search/docs/crawling-indexing/javascript/javascript-seo-basics

PUBBLICAZIONE DEI RISULTATI
    - Dopo inserimento della query da parte di un utente
        - I computer cercano le pagine corrispondenti nell'indice
        - Restituiscono i risultati ritenuti della migliore qualità e più pertinenti per quella query
            - La pertinenza viene stabilita tenendo in considerazione centinaia di fattori (come la posizione, la lingua e il dispositivo dell'utente)
        - Le funzionalità di ricerca visualizzate nella pagina dei risultati di ricerca cambiano anche in base alla query dell'utente
    - Se Search Console indica che una pagina è indicizzata ma non la vedi -> possibili cause
        - Contenuti non pertinenti alle query degli utenti
            - https://developers.google.com/search/docs/fundamentals/seo-starter-guide#expect-search-terms
        - Qualità bassa dei contenuti
            - https://developers.google.com/search/docs/essentials
        - Le regole del meta tag Robots impediscono la pubblicazione 
            - https://developers.google.com/search/docs/crawling-indexing/block-indexing


## Search Engine Optimization

...


## Fonti

Google Search
- [Nozioni di base sulla Ricerca Google](https://developers.google.com/search/docs/essentials)
- [Guida approfondita sul funzionamento di Google Search](https://developers.google.com/search/docs/fundamentals/how-search-works)

Search Engine Optimization
- [Guida introduttiva all'ottimizzazione per i motori di ricerca](https://developers.google.com/search/docs/fundamentals/seo-starter-guide)
