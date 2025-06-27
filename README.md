<div id="top">

<!-- HEADER STYLE: CLASSIC -->
<div align="center">

# Biologia Computazionale - Progetto d'esame
<em>

Progetto per l'esame di _Biologia Computazionale[145375]_ dell'**Università di Trento** a.a. 2024/2025.
<br>
Docenti: **Dassi Erik** e **Asnicar Francesco**
</em>

</div>
<br>


## Indice

- [Panoramica](#Panoramica)
- [Progetto](#progetto)
    - [Struttura delle cartelle](#struttura-delle-cartelle)
        - [Grafici](#grafici)
        - [Dati](#dati)
- [Il progetto TCGA-ESCA](#il-progetto-tcga-esca)
    - [Casistiche del progetto](#casistiche-del-progetto)
    - [Analisi Svolte su TCGA-ESCA](#analisi-svolte-su-tcga-esca)
    - [Terapie Coinvolte e Approcci Clinici](#terapie-coinvolte-e-approcci-clinici)
        - [Terapia Standard](#terapia-standard)
        - [Terapie mirate e immunoterapia](#terapie-mirate-e-immunoterapia)
    - [Altri Dati Clinici Disponibili](#altri-dati-clinici-disponibili)
- [Fonti](#fonti)
- [Autori](#autori)
- [Licenza](#licenza)

---

# Panoramica

L'obbiettivo del progetto è identificare e caratterizzare vari geni differenzialmente espressi per la tipologia di tumore specifico. Tutte le analisi necessarie sono state svolte utilizzando il dataset del progetto TCGA.

# Progetto
Il le analisi del progetto sono state realizzate mediante un `R Notebook`, in modo da rendere il codice pulito e leggibile. Il file R per le analisi è il seguente: [ESCA.Rmd](./ESCA.Rmd).

> All'interno del file sono spiegate le varie a analisi, sia dal punto di vista tecnico, sia dal punto di vista dei risultati ottenuti.

## Struttura delle cartelle
```sh
└── BioComp2025-ESCA/
    ├── ESCA.Rmd
    ├── graph
    ├── data
    ├── BioComp2025-ESCA.Rproj
    ├── LICENSE
    └── README.md
```

### Grafici
I grafici sono contenuti nella cartella [graph](./graph/) e sono numerati per l'analisi fatta. Per una ricerca veloce cercate il numero del grafico all'interno del file [ESCA.Rmd](./ESCA.Rmd), questo vi porterà all'analisi corrispondente.

### Dati
I dati elaborati si trovano nella cartella [data](./data/).

> Non tutti i dati sono numerati per esperimento, consiglio di cercare direttamente il nome del file e vi troverete dove è stato generato.

---

# Il progetto TCGA-ESCA

TCGA-ESCA è il progetto del _The Cancer Genome Atlas_ (TCGA) dedicato al carcinoma esofageo. Questo tumore può essere suddiviso in due sottotipi principali:

- **Esophagus Squamous Cell Carcinoma (ESCC)**: originato dalle cellule squamose che rivestono l'esofago.
- **Esophagus Adenocarcinoma (EAC)**: si sviluppa dalle ghiandole mucose, spesso associato a esofago di Barrett.


## Casistiche del progetto

All'interno del progetto sono presenti dati per un numero di pazienti pari a 185.

I dati si distribuiscono in:
- ~90 ESCC
- ~95 EAC

I campioni provengono da diversi centri oncologici negli Stati Uniti. Sono stati raccolti vari tessuti tra cui: tumori primari, tessuti normali adiacenti e in alcuni casi metastasi.


## Analisi Svolte su TCGA-ESCA

TCGA ha eseguito una profilazione multi-omica dei campioni. Le principali analisi includono:
1. Genomica
    - Whole exome sequencing (WES): per identificare mutazioni somatiche.
    - Copy number alterations (CNA): utilizzando SNP arrays.
    - Mutazioni frequenti:
        - ESCC: TP53, NFE2L2, KEAP1, PIK3CA
        - EAC: TP53, CDKN2A, ERBB2, KRAS

2. Epigenomica
    - Methylation arrays: per l'analisi dello stato epigenetico.

3. Trascrittomica
    - RNA-Seq: per valutare l’espressione genica.
    - Splicing alternativo
    - Analisi di espressione differenziale tra tessuti tumorali e normali.

4. Proteomica
    - Reverse Phase Protein Array (RPPA): per la quantificazione di proteine e fosfoproteine.


## Terapie Coinvolte e Approcci Clinici
### Terapia Standard:

ESCC:
- Chemio-radioterapia (es. cisplatino + 5-FU)
- Chirurgia in casi selezionati

EAC:
- Chirurgia (esofagectomia)
- Chemoterapia (es. FOLFOX, paclitaxel)
- Targeted therapy per mutazioni specifiche (es. HER2 amplificato)

### Terapie mirate e immunoterapia:
In casi avanzati, si stanno testando:
- Inibitori di checkpoint immunitari (es. anti-PD1/PD-L1)
- Terapie mirate su ERBB2, MET, ecc.

## Altri dati clinici disponibili

I metadati clinici raccolti da TCGA includono:

| Categoria            | Dettagli                                                                           |
| :------------------- | :--------------------------------------------------------------------------------- |
| **Età**              | 33-90 anni, mediana \~60-65                                                        |
| **Sesso**            | Prevalenza maschile                                                                |
| **Stadio Tumorale**  | I-IV, con staging TNM incluso                                                      |
| **Grado Istologico** | Ben differenziato, moderato, poco differenziato                                    |
| **Follow-up**        | Informazioni su sopravvivenza globale (OS), sopravvivenza libera da malattia (DFS) |
| **Recidive**         | Data di recidiva e localizzazione                                                  |
| **Trattamenti**      | Tipo di trattamento (chemioterapia, radioterapia, chirurgia), date e durata        |


# Fonti
- [cBioPortal](https://www.cbioportal.org/study/summary?id=esca_tcga)
- [GDC Data Portal](https://portal.gdc.cancer.gov/projects/TCGA-ESCA)
- [UCSC Xena Browser](https://xenabrowser.net)
- [Cancer Genomics Cloud](https://docs.cancergenomicscloud.org/docs/tcga-data)
- recount3 e Bioconductor: accesso agli RNA-Seq pre-processati.

---

## Esame

Progetto per l'esame di `Biologia Computazionale [145375]` dell'**Università di Trento** a.a. 2024/2025.

Docenti:
- **Dassi Erik**
- **Asnicar Francesco**


## Autori

- ***Eva Jovanovska***
- ***Lara Baggio***
- ***Sofia Paiusco***
- ***Pietro Rocchio***

## Licenza

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.
<div align="left"><a href="#top">⬆ Torna in alto</a></div>
