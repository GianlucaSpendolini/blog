---
title: Google Search e le SEO
date: 2025-01-13
---

Come detto nel [precedente post](https://GianlucaSpendolini.github.io/blog/2025/01/10/Creare_un_blog.md), un sito deve essere indicizzato per poter essere visualizzato nei risultati di un motore di ricerca.

In questo post, introdurrò la ricerca di Google ed i vari processi che sono alla base, successivamente parlerò dell'argomento principale:
- [La ricerca di Google](#google-search)
- [Search Engine Optimization (SEO)](#search-engine-optimization)
- [Fonti](#fonti)


## Google Search

Per questa sezione, inizierò introducendo le nozioni base sulla ricerca, per poi seguire con una descrizione più approfondita:
- [Nozioni base](#nozioni-base)
- [Step fondamentali della ricerca](#step-fondamentali)

### Nozioni base

Gli aspetti fondamentali relativi a ciò che rende un contenuto idoneo ad essere mostrato e a funzionare
- [Requisiti tecnici](#requisiti-tecnici)
    - Ciò di cui Google ha bisogno in una pagina web per mostrarla nei risultati di ricerca;
- [Norme relative allo spam](#norme-relative-allo-spam)
    - Comportamenti e tattiche che possono portare ad un ranking inferiore/rimozione dai risultati;
- [Best practice](#best-practice)
    - Elementi principali che possono contribuire a migliorare l'aspetto del sito nei risultati;

Nonostante i precedenti aspetti vengano rispettati, non è detto che Google eseguirà la scansione, l'indicizzazione o la pubblicazione dei contenuti.


#### [Requisiti tecnici](https://developers.google.com/search/docs/essentials/technical)


#### [Norme relative allo spam](https://developers.google.com/search/docs/essentials/spam-policies)


#### [Best practice](https://developers.google.com/search/docs)

In generale esistono alcune pratiche principali che possono avere il massimo impatto sul ranking e sull'aspetto dei tuoi contenuti web:
- Creare contenuti utili, affidabili e pensati per le persone
    - Si può prendere ispirazione dal [seguente link](https://developers.google.com/search/docs/fundamentals/creating-helpful-content);
- Usa parole che le persone userebbero per cercare i tuoi contenuti 
    - Posizionale in posizioni di evidenza (come nel titolo e l'intestazione principale) o altri elementi descrittivi (come titoli alternativi delle immagini o testo dei link);
- Rendere i link sottoponibili alla scansione, in modo che Google possa trovare altre pagine sul sito tramite i link sulla pagina;
- Fai conoscere il sito
    - Partecipa alle community in cui puoi far conoscere a persone che la pensano come te i servizi e prodotti che menzioni sul sito;
- Se ho altri contenuti -> segui le best practice per far comprendere anche a loro quelle parti della pagina 
    - [Immagini](https://developers.google.com/search/docs/appearance/google-images);
    - [Video](https://developers.google.com/search/docs/appearance/video);
    - [Dati strutturati](https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data);
    - [JavaScript](https://developers.google.com/search/docs/crawling-indexing/javascript/javascript-seo-basics);
- Migliora l'aspetto nella Ricerca Google
    - Abilitando funzionalità significative per il sito;
- Se ci sono contenuti che non si vogliono mostrare nei risultati/vuoi disattivare le funzionalità
    - Controlla [come i contenuti vengono visualizzati nella Ricerca Google](https://developers.google.com/search/docs/crawling-indexing/control-what-you-share).


### Step fondamentali

Il motore di ricerca utilizza dei "web crawler" per esplorare il web e trovare pagine da aggiungere al suo indice.

Non è garantito che eseguirà la scansione della tua pagina, che la indicizzerà o la pubblicherà, anche se verranno seguite le nozioni di base.

Fasi
- [Scansione](#scansione)
    - Scaricati i testi, immagini e video dalle pagine trovate su internet tramite programmi automatizzati chiamati crawler;
- [Indicizzazione](#indicizzazione)
    - Analizzati il testo, le immagini e i file video sulla pagina e memorizza le informazioni nell'Indice Google (è un grande database);
- [Pubblicazione dei risultati di ricerca](#pubblicazione-dei-risultati)
    - Restituzione delle informazioni pertinenti alla query.

#### Scansione
- Individuazione degli URL
    - Capire quali pagine esistono sul web
        - Non esiste un registro centrale di tutte le pagine web -> Google deve costantemente cercare pagine nuove e aggiornate e aggiungerle al proprio elenco di pagine note;
    - Tramite invio di una sitemap, ovvero un elenco di pagine;
- Visita/scansione della pagina 
    - Effettuata grazie a Googlebot -> algoritmo per determinare siti che deve scansionare/frequenza della scansione/numero di pagine da recuperare in ogni sito
        - Non esegue la scansione di tutte le pagine -> [non autorizzate](https://developers.google.com/search/docs/crawling-indexing/robots/robots_txt) per la scansione (da proprietario) o non accessibili senza accesso;
        - Su quelle che scansiona 
            - Visualizza ed esegue codice JavaScript -> versione recente di Chrome -> visualizza come il browser vede la pagina che visiti -> rendering importante per vedere contenuto derivante da JavaScript;
    - Crowler programmati in base alle risposte del sito (500 è rallentamento) in modo da tentare di non eseguire troppo velocemente la scansione -> evita sovraccarico;
- Problemi che possono verificarsi
    - [Relativi al server](https://developers.google.com/search/docs/crawling-indexing/http-network-errors#http-status-codes);
    - [Di rete](https://developers.google.com/search/docs/crawling-indexing/http-network-errors#network-and-dns-errors);
    - [Regole del file robots.txt che impediscono l'accesso alla pagina](https://developers.google.com/search/docs/crawling-indexing/robots/intro).

#### Indicizzazione 
- Capire cosa tratta la pagina 
    - Elaborazione ed analisi dei contenuti tesuali e dei tag di contenuti chiave ed attributi (come <title> e attributi ALT);
- Capisce se pagina è duplicato o canonica 
    - Canonica -> mostrata nei risultati
        - Raggruppamento (clustering) delle pagine con contenuti simili trovate su internet;
        - Selezionata quella più rappresentativa;
        - Altre pagine sono versioni alternative -> pubblicate in contesti diversi (accesso da dispositivo mobile pagina specifica in quel cluster);
- Raccoglie indicatori dalla pagina canonica e contenuti -> usati nella fase di pubblicazione dei risultati 
    - Info archiviate nell'Indice di Google (grande database ospitato su migliaia di computer);
- Dipende anche dai contenuti e metadati -> problematiche
    - [Qualità bassa dei contenuti](https://developers.google.com/search/docs/essentials);
    - [Le regole dei meta tag Robots non consentono l'indicizzazione](https://developers.google.com/search/docs/crawling-indexing/block-indexing);
    - [Il design del sito potrebbe rendere difficile l'indicizzazione](https://developers.google.com/search/docs/crawling-indexing/javascript/javascript-seo-basics).

#### Pubblicazione dei risultati
- Dopo inserimento della query da parte di un utente
    - I computer cercano le pagine corrispondenti nell'indice;
    - Restituiscono i risultati ritenuti della migliore qualità e più pertinenti per quella query
        - La pertinenza viene stabilita tenendo in considerazione centinaia di fattori (come la posizione, la lingua e il dispositivo dell'utente);
    - Le funzionalità di ricerca visualizzate nella pagina dei risultati di ricerca cambiano anche in base alla query dell'utente;
- Se Search Console indica che una pagina è indicizzata ma non la vedi -> possibili cause
    - [Contenuti non pertinenti alle query degli utenti](https://developers.google.com/search/docs/fundamentals/seo-starter-guide#expect-search-terms);
    - [Qualità bassa dei contenuti](https://developers.google.com/search/docs/essentials);
    - [Le regole del meta tag Robots impediscono la pubblicazione ](https://developers.google.com/search/docs/crawling-indexing/block-indexing).


## Search Engine Optimization

...


## Fonti

Google Search
- [Nozioni di base sulla Ricerca Google](https://developers.google.com/search/docs/essentials)
- [Guida approfondita sul funzionamento di Google Search](https://developers.google.com/search/docs/fundamentals/how-search-works)

Search Engine Optimization
- [Guida introduttiva all'ottimizzazione per i motori di ricerca](https://developers.google.com/search/docs/fundamentals/seo-starter-guide)
