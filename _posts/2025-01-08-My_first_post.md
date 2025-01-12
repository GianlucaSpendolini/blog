---
title: "Cosa portare nel blog"
date: 2025-01-08
---

Questo blog è stato creato grazie al [tutorial](https://github.com/skills/github-pages) di GitHub relativo a GitHub-Pages.

&Eacute; utile per allenarmi sia con i linguaggi classici (HTML, CSS e JavaScript) nel [sito principale](https://GianlucaSpendolini.github.io), sia con linguaggi di Markdown ed altri, per ampliare le mie conoscenze.

In futuro magari inizierò a fare post in inglese per allenarmi, però devo ancora capire cosa portare (se volessi andare avanti con questo progetto).

Magari posso portare i miei progressi nel mondo dello sviluppo, in modo da ricordarmi anche quando imparo qualcosa di nuovo e di importante (quindi non porterei quando imparo dei comandi ma quando seguo tutorial e corsi per imparare nuove cose).

---

Alla fine ho deciso: racconterò la mia esperienza nel mondo del coding :)

---

### 10/01/2025 - 18:28 (IT)

Piccola correzione: non solo nel mondo del coding, ma in quello della tecnologia (specialmente in ambito informatico).

Probabilmente correggerò, se ci sono modifiche da fare, come ho fatto ora:
- Scrivo "\-\-\-";
- Sotto riporto la modifica (non per forza sono correzioni ma anche aggiunte).

---

### 12/01/2025 - 21:34 (IT)

Già che questo è il primo post, ne approfitto per inserire, come argomento vero, ciò che ho imparato per ultimo (fino all'8 Gennaio) e grazie a cui è stato creato questo blog: Jekyll. Di seguito inserirò:
- Una breve [descrizione](#descrizione) di Jekyll, presa dal corso precedentemente citato;
- La [struttura](#struttura) di un progetto Jekyll, con, per ogni parte, una descrizione.

#### Descrizione

Jekyll uses a file titled _config.yml to store settings for your site, your theme, and reusable content like your site title and GitHub handle. 
You can check out the _config.yml file on the Code tab of your repository.

We need to use a blog-ready theme. For this activity, we will use a theme named "minima".

GitHub Pages uses Jekyll. In Jekyll, we can create a blog by using specially named files and frontmatter. 
The files must be named _posts/YYYY-MM-DD-title.md. You must also include title and date in your frontmatter.

What is frontmatter?: The syntax Jekyll files use is called YAML frontmatter

#### Struttura

    .
    ├── _config.yml
    ├── _data
    │   └── members.yml
    ├── _drafts
    │   ├── begin-with-the-crazy-ideas.md
    │   └── on-simplicity-in-technology.md
    ├── _includes
    │   ├── footer.html
    │   └── header.html
    ├── _layouts
    │   ├── default.html
    │   └── post.html
    ├── _posts
    │   ├── 2007-10-29-why-every-programmer-should-play-nethack.md
    │   └── 2009-04-26-barcamp-boston-4-roundup.md
    ├── _sass
    │   ├── _base.scss
    │   └── _layout.scss
    ├── _site
    ├── .jekyll-cache
    │   └── Jekyll
    │       └── Cache
    │           └── [...]
    ├── .jekyll-metadata
    └── index.html # can also be an 'index.md' with valid front matter

Un progetto Jekyll solitamente è strutturato come segue:
- [_config.yml](#config)
- _data
- _drafts
- _includes
- _layouts
- _posts
- _sass
- _site
- .jekyll-cache
- .jekyll-metadata
- [index.html (can also be an 'index.md' with valid front matter)](#index)

##### Config
- Utilizzato per configurare le impostazioni generiche
- Posso specificare
    - Titolo
      
            title: 'titolo'
      
    - Chi è l'autore del post
      
          author:
              name: 'nome'
              email: 'email'
      
    - Una descrizione
        
          description: >
              ...
      
    - Il tema
        - Per Minima
          
              theme: minima
              remote_theme: jekyll/minima # Se voglio ultima versione
          
    - Quali pagine inserire nell'header (nav-bar)
      
          header_pages:
              - ...
      
    - Settaggi per Minima
      
          minima: 
          
              skin: 'aspetto'
                  - classic -> Default, light color scheme.
                  - dark -> Dark variant of the classic skin.
                  - auto -> Adaptive skin based on the default classic and dark skins.
                  - solarized-light -> Light variant of solarized color scheme.
                  - solarized-dark -> Dark variant of solarized color scheme.
                  - solarized -> Adaptive skin for solarized color scheme skins.
              
              date_format: 'datetime'
                  - default -> "%b %d, %Y" (e.g. Nov 14, 2023)
                  - riferimento -> https://shopify.github.io/liquid/filters/date/
              
              social_links:
                  - { platform: devto,          user_url: "<URL>" }
                  - { platform: dribbble,       user_url: "<URL>" }
                  - { platform: facebook,       user_url: "<URL>" }
                  - { platform: flickr,         user_url: "<URL>" }
                  - { platform: github,         user_url: "<URL>" }
                  - { platform: gitlab,         user_url: "<URL>" }
                  - { platform: google_scholar, user_url: "<URL>" }
                  - { platform: instagram,      user_url: "<URL>" }
                  - { platform: keybase,        user_url: "<URL>" }
                  - { platform: linkedin,       user_url: "<URL>" }
                  - { platform: microdotblog,   user_url: "<URL>" }
                  - { platform: pinterest,      user_url: "<URL>" }
                  - { platform: stackoverflow,  user_url: "<URL>" }
                  - { platform: telegram,       user_url: "<URL>" }
                  - { platform: twitter,        user_url: "<URL>" }
                  - { platform: x,              user_url: "<URL>" }
                  - { platform: youtube,        user_url: "<URL>" }

##### Index
- Contiene il contenuto della home page (il main)
