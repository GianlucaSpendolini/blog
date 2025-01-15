---
title: Google Search e la SEO
date: 2025-01-13
---

Come detto nel [precedente post](https://GianlucaSpendolini.github.io/blog/2025/01/10/Creare_un_blog.html), un sito deve essere indicizzato per poter essere visualizzato nei risultati di un motore di ricerca.

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

La SEO serve ad aiutare i motori di ricerca a comprendere i tuoi contenuti, nonché aiutare gli utenti a trovare il tuo sito e decidere se visitarlo tramite un motore di ricerca.

Non è garantito che un determinato sito venga aggiunto all'indice di Google, ma hanno maggiori probabilità di comparire nei risultati di ricerca di Google.

La SEO riguarda il passo successivo: impegnarsi per migliorare la presenza del tuo sito nella Ricerca
- Se vengono seguite le best practice, magari sarà più facile per i motori di ricerca (non solo Google) eseguire la scansione, indicizzare e comprendere i tuoi contenuti.

Di seguito riporterò:
- [Tempistiche per vedere gli effetti](#tempistiche-per-i-risultati)
- [Aiutare Google nella ricerca](#aiutare-google-nella-ricerca)
- [Organizzazione del sito](#organizzare-il-sito)
- [Creare un sito utile ed interessante](#creare-un-sito-utile-ed-interessante)
- [Influenzare l'aspetto del sito](#influenzare-laspetto-del-sito)
- [Aggiungere immagini ed ottimizzarle](#aggiungere-immagini-ed-ottimizzarle)
- [Ottimizzazione dei video](#ottimizzazione-dei-video)
- [Promuovere il sito web](#promuovere-il-sito-web)
- [Aspetti su cui non soffermarsi](#aspetti-su-cui-non-soffermarsi)
- [Consigli extra](#consigli)


### Tempistiche per i risultati

Non è immediato. Le modifiche sono di diversi tipi e richiedono diverso tempo. Si possono aspettare un paio di settimane e, se non si vedono effetti, è possibile ripetere le modifiche.


### Aiutare Google nella ricerca

Prima di tutto, controlla se Google ha già trovato i contenuti, così da non fare altro se non qualche piccola modifica per aumentarne il ranking. Inizia usando l'operatore "site" nella barra di ricerca come segue:

    site:<URL>

Se sono nell'indice di Google, vedrai i risultati nella pagina di ricerca, altrimenti puoi controllare i [requisiti tecnici](https://developers.google.com/search/docs/essentials/technical) per constatare che sia altro.

Se non è nemmeno un problema tecnico, è meglio adottare qualche piccola modifica. Google spesso trova le pagine tramite link da pagine di cui ha già eseguito la scansione. Infatti è molto comodo avere pagine che
rimandano al tuo sito e, per farlo, puoi promuovere il sito, invitando le persone a [scoprire i contenuti che porti](https://developers.google.com/search/docs/fundamentals/seo-starter-guide#promoting).
Un altro modo è inviare una [sitemap](https://developers.google.com/search/docs/crawling-indexing/sitemaps/overview), ovvero un file contenente tutti gli URL del sito importanti. E' possibile che alcuni CMS lo 
facciano già, però è sempre meglio far conoscere il proprio sito. 

Di seguito:
- [Verificare se Google può vedere una pagina come la vede l'utente](#vedere-la-pagina-come-lutente)
- [Se non si vuole che una pagina venga visualizzata nei risultati di ricerca](#se-non-si-vuole-far-comparire-una-pagina-nei-risultati)

#### Vedere la pagina come l'utente
- In una scansione dovrebbe vedere la pagina come la vedrebbe l'utente -> meglio se fosse in grado di accedere alle stesse risorse del browser dell'utente
    - Se il sito nasconde componenti importanti (come CSS e JavaScript) -> potrebbe non riuscire a comprendere le pagine -> non mostrate/pessimo ranking
- Se le pagine contengono informazioni diverse a seconda dell'ubicazione dell'utente -> meglio assicurarsi che siano soddisfatte le informazioni che vede Google dal suo crawler (Stati Uniti)
    - E' possibile usare uno [strumento](https://support.google.com/webmasters/answer/9012289) per verificare come Google vede la pagina

#### Se non si vuole far comparire una pagina nei risultati
- E' possibile farlo attraverso [diversi modi](https://developers.google.com/search/docs/crawling-indexing/control-what-you-share#how-to-block-content)


### Organizzare il sito

Se il sito è organizzato in modo logico, è utile per gli utenti e i motori di ricerca a comprendere la correlazione tra le pagine ed il resto del sito.
- Consigli utili a lungo termine
- Se non lo è -> i motori di ricerca comprenderanno le pagine (indipendentemente da com'è organizzato)

Di seguito:
- [URL descrittivi](#url-descrittivi)
- [Raggruppare le pagine nelle directory](#raggruppare-le-pagine-nelle-directory)
- [Ridurre i contenuti duplicati](#ridurre-i-contenuti-duplicati)

#### URL descrittivi
<table style="border: none; padding-left: 0;">
    <tr>
        <td style="border: none; width: auto;">
            Delle parti possono essere visualizzate nei risultati come breadcrumb (parte grigio-chiaro accanto a 'dominio' > ...).
            Ciò permette agli utenti di utilizzare anche gli URL per capire se un risultato sarà utile per loro.
            <br /><br />
            Inoltre, Google viene a conoscenza automaticamente dei breadcrumb in base alle parole nell'URL.
            I breadcrumb possono anche essere influenzati con i dati strutturati se si hanno le competenze tecniche necessarie.
            Una cosa molto utile è quella di provare a includere nell'URL parole che potrebbero essere utili per gli utenti.
        </td>
        <td style="border: none; padding-right: 0; width: 200px;">
            <img 
                alt="Illustrazione che mostra un risultato di testo nella Ricerca Google con callout che etichettano elementi visivi dell'URL visibili specifici, tra cui dominio e breadcrumb" 
                src="https://developers.google.com/static/search/docs/images/text-result.png" 
                style="max-width: 100%; height: auto;"
            />
        </td>
    </tr>
</table>

#### Raggruppare le pagine nelle directory

<table style="border: none;">
    <tr>
        <td style="border: none; padding-left: 0; width: auto;">
            Il modo in cui vengono organizzati i contenuti potrebbe influire su come Google esegue la scansione e l'indicizzazione del sito.
            <br /><br />
            L'uso di directory (o cartelle) per raggruppare argomenti simili può aiutare Google a capire la frequenza con cui cambiano gli URL nelle singole directory.
            <br /><br />
            Inoltre Google può apprendere queste informazioni ed eseguire la scansione delle varie directory a frequenze diverse.
            Un consiglio potrebbe essere quello di avere le <a 
                href="https://developers.google.com/search/docs/specialty/ecommerce/help-google-understand-your-ecommerce-site-structure"
            >strutture</a> dei siti ottimizzate per la ricerca, poichè avere un'efficace struttura degli URL ha un'importanza molto rilevante.
        </td>
        <td style="border: none; padding-right: 0; width: 200px;">
            <img 
                alt="Illustrazione di come raggruppare le pagine nelle directory" 
                src="https://developers.google.com/static/search/docs/images/grouping-pages-in-directories.png" 
                style="max-width: 100%; height: auto;"
            />
        </td>
    </tr>
</table>

#### Ridurre i contenuti duplicati
- Evitare di fare come molti siti che mostrano gli stessi contenuti ma con URL diversi poichè i motori di ricerca sceglieranno solo quello canonico da registrare
    - Per questo, è meglio verificare se è possibile [specificare una versione canonica](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls) (al posto di far sprecare risorse di scansione su URL che non interessano)
- Per lavorare alla canonicalizzazione, assicurati che ogni contenuto sia accessibile tramite 1 solo URL (altrimenti può crearsi confusione)
    - Se si hanno più pagine con le stesse informaizoni -> reindirizzamento ad un URL che rappresenti al meglio le informazioni 
    - Se non è possibile fare il reindirizzamento -> si può usare l'elemento link con la proprietà rel="canonical"

            <link rel="canonical" />

### Creare un sito utile ed interessante

Ovviamente, creare contenuti "interessanti ed utili" varia di persona in persona, ma è molto utile per permettere la presenza del tuo sito nei risultati. Inoltre, i contenuti "interessanti ed utili" hanno delle cose in comune:
- Il testo è facile da leggere e ben organizzato
    - Redigere i contenuti in modo naturale e assicurarsi che siano ben scritti
        - Facili da seguire
        - Privi di errori ortografici e grammaticali
    - Suddividere i contenuti lunghi in paragrafi e sezioni
    - Fornire intestazioni per aiutare gli utenti a navigare le pagine 
- Crea contenuti unici
    - Quando si scrivono nuovi contenuti -> non copiare quelli di altri ma scrivili in base a ciò che sai a riguardo (non limitarti a [rimaneggiare contenuti già pubblicati](https://developers.google.com/search/docs/essentials/spam-policies#scraped-content))
- Aggiorna i contenuti
    - Controlla e aggiorna in base alle necessità OPPURE elimina se non sono più rilevanti
- Riporta contenuti [utili, affidabili e pensati per le persone](https://developers.google.com/search/docs/fundamentals/creating-helpful-content)
    - Assicurarsi di scrivere contenuti che gli utenti ritengono affidabili (anche riportando le fonti da cui si sono prese le notizie)
 
Di seguito
- [Pensare ai termini di ricerca usati dai lettori](#pensare-ai-termini-di-ricerca-usati-dai-lettori)
- [Evitare pubblicità che distraggono](#evitare-pubblicità-che-distraggono)
- [Inserire link a risorse pertinenti](#inserire-link-a-risorse-pertinenti)

#### Pensare ai termini di ricerca usati dai lettori
- Ogni utente può utilizzare diversi termini per cercare i contenuti
    - Utenti esperti potrebbero utilizzare parole chiave diverse rispetto a quelle impiegate dai neofiti
    - Prevedere queste differenze nei comportamenti di ricerca e scrivere pensando ai lettori potrebbe avere effetti positivi sulle prestazioni del tuo sito nei risultati di ricerca
- Però se non si prevedono tutti i termini, non bisogna preoccuparsi, poichè i sistemi di corrispondenza delle lingue di Google sono sofisticati e sono in grado di comprendere in che modo la tua pagina è correlata a molte query

#### [Evitare pubblicità che distraggono](https://developers.google.com/search/docs/appearance/avoid-intrusive-interstitials)
- Evitare che distraggano eccessivamente o che impediscano di leggere i contenuti

#### Inserire link a risorse pertinenti
<div align="center">
    <img 
        alt="Illustrazione che mostra la parte di testo di un link"
        src="https://developers.google.com/static/search/docs/images/what-is-link-text.png"
        width="50%"
    />
</div>

- I link sono molto utili per collegare gli utenti e i motori di ricerca ad altre parti del tuo sito o a pagine pertinenti su altri siti
    - I link possono aggiungere valore anche collegando gli utenti e Google ad un'altra risorsa che conferma ciò di cui scrivi
- Il testo del link ([anchor text](https://developers.google.com/search/docs/crawling-indexing/links-crawlable#write-good-anchor-text))
    - Parte testuale di un link che puoi vedere
        - Comunica informazioni sulla pagina a cui rimanda il link
    - Utenti e motori di ricerca possono comprendere facilmente cosa contengono le pagine collegate prima di visitarle
- Inserire il link quando necessario
    - Possono fornire più contesto su un argomento, sia per gli utenti che per i motori di ricerca
        - Potrebbe aiutare a dimostrare le tue conoscenze su un argomento
    - Quando inserisci link a pagine al di fuori del tuo controllo, assicurati che la risorsa a cui indirizza il link sia attendibile
        - Se non ritieni attendibili i contenuti e vuoi comunque creare un link che vi rimandi, aggiungi un'annotazione "nofollow" o simile al link per evitare l'associazione con quello a cui rimandi
        - Ciò evita potenziali conseguenze negative sul tuo ranking nella Ricerca Google
    - Se si accettano contenuti generati dagli utenti, assicurati che in ogni link pubblicato dagli utenti sia presente nofollow o un'annotazione simile 
        - Aggiunta automaticamente dal tuo CMS
        - Magari non vuoi che il tuo sito venga associato ciecamente ai siti a cui gli utenti rimandano tramite link
            - Può anche scoraggiare gli spammer dall'utilizzare il tuo sito web in modo illecito

### Influenzare l'aspetto del sito

Pagina dei risultati è composta da alcuni [elementi visivi](https://developers.google.com/search/docs/appearance/visual-elements-gallery) che si possono influenzare per aiutare gli utenti se visitare il sito.

Di seguito
- [Influenzare i link dei titoli](#influenzare-i-link-dei-titoli)
- [Controllare gli snippet](#controllare-gli-snippet)

#### Influenzare i link dei titoli
<table style="border: none;">
    <tr>
        <td style="border: none; padding-left: 0; width: auto;">
            Parte del titolo dei risultati di ricerca può aiutare le persone a fare click.
            <br /><br />
            Ci sono fonti che Google usa per generare il link del titolo tramite le parole inserite nel tag <code>title</code> ed altre intestazioni della pagina.
            Il testo del titolo può essere usato anche per il titolo mostrato nei browser web e nei preferiti.
            <br /><br />
            Per criverne <a
                             href="https://developers.google.com/search/docs/appearance/title-link"
             >uno efficace</a> si possono tenere a mente questi dettagli:
            <ul>
                <li>
                    Unico per la pagina
                </li>
                <li>
                    Chiaro
                </li>
                <li>
                    Conciso
                </li>
                <li>
                    Ne descriva accuratamente i contenuti
                </li>
            </ul>
        </td>
        <td style="border: none; padding-right: 0; width: 200px;">
            <img 
                alt="Illustrazione di un risultato di testo nella Ricerca Google, con un riquadro evidenziato intorno alla parte del link del titolo" 
                src="https://developers.google.com/static/search/docs/images/blank-title-link.png" 
                style="max-width: 100%; height: auto;"
            />
            <img 
                alt="Illustrazione dell'aspetto del testo del titolo in una pagina web e nel codice HTML" 
                src="https://developers.google.com/static/search/docs/images/titles-on-page-html.png" 
                style="max-width: 100%; height: auto;"
            />
        </td>
    </tr>
</table>

#### Controllare gli snippet
<table style="border: none;">
    <tr>
        <td style="border: none; padding-left: 0; width: auto;">
            Gli snippet non sono altro che una descrizione della pagina di destinazione.
            Si trovano sotto il link del titolo e aiutano gli utenti a decidere se fare click.
            <br /><br />
            Il testo è estratto dai contenuti della pagina a cui rimanda il risultato di ricerca, mediante:
            <ul>
                <li>
                    Controllo sulle parole che possono essere usate per generare lo snippet;
                </li>
                <li>
                    Estrazione dei contenuti del tag della <a
                                                               href="https://developers.google.com/search/docs/appearance/snippet#meta-descriptions"
                                                           >meta descrizione</a>
                    <ul>
                        <li>
                            Breve riepilogo della pagina di 1/2 frasi;
                        </li>
                        <li>
                            Unica per determinata pagina;
                        </li>
                        <li>
                            Include i punti più significativi della pagina.
                        </li>
                    </ul>
                </li>
            </ul>
        </td>
        <td style="border: none; padding-right: 0; width: 200px;">
            <img 
                alt="Illustrazione di un risultato di testo nella Ricerca Google, con un riquadro evidenziato intorno alla riga della parte dello snippet" 
                src="https://developers.google.com/static/search/docs/images/blank-snippet.png" 
                style="max-width: 100%; height: auto;"
            />
        </td>
    </tr>
</table>

### Aggiungere immagini ed ottimizzarle

Molte persone effettuano ricerche visive
- Le immagini possono rappresentare il modo in cui gli utenti trovano il sito per la prima volta
- Se aggiungi immagini -> assicurati che le persone ed i motori di ricerca siano in grado di trovarle e comprenderle

Di seguito
- [Aggiungere immagini di alta qualità accanto al testo pertinente](#immagini-di-alta-qualità-accanto-al-testo)
- [Aggiungere testo alternativo descrittivo all'immagine](#aggiungere-testo-alternativo-descrittivo-allimmagine)

#### Immagini di alta qualità accanto al testo
- Meglio fornire agli utenti contesto e dettagli sufficienti per decidere quale immagine corrisponde meglio a ciò che stavano cercando
- Usa immagini nitide e chiare, e posizionale vicino al testo pertinente all'immagine
    - Il testo accanto alle immagini può aiutare Google a comprendere meglio l'argomento dell'immagine e il suo significato nel contesto della tua pagina

#### Aggiungere testo alternativo descrittivo all'immagine
- Il testo alternativo è una porzione di testo breve ma descrittiva che spiega la relazione tra l'immagine e i tuoi contenuti
- Aiuta i motori di ricerca a capire l'argomento dell'immagine e come è correlata alla tua pagina
    - E' importante aggiungere [testo alternativo efficace](https://developers.google.com/search/docs/appearance/google-images#descriptive-alt-text)

### [Ottimizzazione dei video](https://developers.google.com/search/docs/appearance/video)
- Le persone potrebbero anche riuscire a scoprire il tuo sito tramite i risultati di video nella Ricerca Google
- Crea contenuti video di alta qualità
    - Incorpora il video in una pagina autonoma, vicino a del testo pertinente al video
    - Scrivi un testo descrittivo nei campi dei titoli e della descrizione di un video 
        - Il titolo di un video è sempre un titolo, quindi puoi applicare le best practice per la scrittura dei titoli anche in questo caso

### [Promuovere il sito web](https://developers.google.com/search/docs/essentials/spam-policies)
- Promozione sui social media
- Coinvolgimento della community
- Pubblicità, sia offline che online
    - Come stampare il sito su bigliettini da visita 
- Passaparola e molti altri metodi
    - [Risorse per ampliare e coinvolgere il pubblico](https://creators.google/en-us/content-creation-guides/audience-engagement/)

### Aspetti su cui non soffermarsi
- Meta tag keywords
    - La [ricerca Google non usa i meta-tag keywords](https://developers.google.com/search/blog/2009/09/google-does-not-use-keywords-meta-tag)
- Parole chiave in eccesso
    - Ripetere eccessivamente le stesse parole (anche in varianti) possono stancare gli utenti ed essere viste dal motore di ricerca come [violazione relativa allo spam](https://developers.google.com/search/docs/essentials/spam-policies#keyword-stuffing)
- Parole chiave nel nome di dominio o nel percorso dell'URL 
    - Fai ciò che è meglio per l'azienda
        - Usa le best practice per il marketing
    - Per il ranking
        - Utilizzo di parole chiave nel nome del dominio/nell'URL -> quasi nessun effetto se non nel [breadcrumb](https://developers.google.com/search/docs/appearance/visual-elements-gallery#breadcrumb)
        - Per i nomi di dominio di primo livello
            - Importante solo se scegli come target gli utenti di un paese specifico e, anche in questo caso, di solito è un indicatore a basso impatto
            - Altrimenti non infleunza il ranking
- Lunghezza minima o massima dei contenuti
    - Se si prende in considerazione solo questo parametro -> non conta 
    - Se si usano varianti delle parole (scrivendo in modo naturale per evitare le ripetizioni), si hanno maggiori possibilità di comparire nella Ricerca semplicemente perché si utilizzano più parole chiave
- Sottodomini e sottodirectory
    - Fare tutto ciò che è utile all'attività
    - Puoi
        - Gestire il sito se è segmentato per sottodirectory
        - Suddividere gli argomenti in sottodomini, a seconda dell'argomento o del settore del sito
- [PageRank](https://developers.google.com/search/docs/appearance/ranking-systems-guide#link-analysis)
    - Utilizza i link ed è uno degli algoritmi fondamentali di Google 
    - La ricerca prende in considerazione anche altri indicatori di ranking
- "Penalità" per contenuti duplicati
    - Se alcuni dei tuoi contenuti sono accessibili da più URL, non è un problema
    - Non è efficiente MA non è causa di azione manuale
        - Diversamente se si [copiano i contenuti di altri siti](https://developers.google.com/search/docs/essentials/spam-policies#scraped-content)
- Numero e ordine delle intestazioni
    - L'ordine semantico è ottimo per gli screenreader ma non importa nulla per la ricerca Google 
        - Solitamente non usa HTML valido -> ricerca spesso non dipende da significati semantici nell'HTML 
    - Non esiste una quantità magica e ideale di intestazioni che una determinata pagina dovrebbe avere
        - Se ci sono troppi link, diminuiscine il numero 
- Pensare che i criteri EEAT costituiscano un fattore di ranking
    - [Expertise, Authoritativeness, Trustworthiness](https://developers.google.com/search/docs/fundamentals/creating-helpful-content#eat)

### Consigli
- Utilizza [Search Console](https://developers.google.com/search/docs/monitor-debug/search-console-start)
    - Configurare un account Search Console ti consente di monitorare e ottimizzare le prestazioni del tuo sito web sulla Ricerca Google
- [Gestire la SEO del tuo sito web nel tempo](https://developers.google.com/search/docs/fundamentals/get-started)
    - Attività e scenari più approfonditi relativi alla SEO
- Migliorare l'aspetto del tuo sito nei risultati della Ricerca Google
    - [Dati strutturati](https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data) validi sulle tue pagine le rendono idonee anche per molte funzionalità speciali nei risultati della Ricerca Google
        - Stelle delle recensioni
        - Caroselli
        - ...
    - Molto utile è la [galleria](https://developers.google.com/search/docs/appearance/structured-data/search-gallery) dei tipi di risultati di ricerca per i quali le pagine possono essere idonee


## Fonti

Google
- Google Search
    - [Nozioni di base sulla Ricerca Google](https://developers.google.com/search/docs/essentials)
    - [Guida approfondita sul funzionamento di Google Search](https://developers.google.com/search/docs/fundamentals/how-search-works)
- Search Engine Optimization
    - [Guida introduttiva all'ottimizzazione per i motori di ricerca](https://developers.google.com/search/docs/fundamentals/seo-starter-guide)

Salvatore Aranzulla
- [Come funziona](https://www.aranzulla.it/seo-come-funziona-1290285.html)
- [Indicizzare un sito](https://www.aranzulla.it/come-indicizzare-un-sito-27237.html)
- [Essere i primi su Google](https://www.aranzulla.it/come-essere-primi-su-google-1092179.html)
- [Link Building](https://www.aranzulla.it/come-fare-link-building-1266246.html)
