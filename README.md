# IES Multilingual Company Website Dataset (UK & Germany)

**Version:** v1.0  
**Publication date:** 2026-02-10  
**DOI:** 10.24352/UB.OVGU-2026-022 
**Creators:** 
- Stefan Langer, Otto-von-Guericke University
- Marcel Genzmehr, Otto-von-Guericke University
- Sayantan Polley, Otto-von-Guericke University
- Andreas Nürnberger, Otto-von-Guericke University
  
**Project:** Innovation Ecosystems (IES)

---

## 1. Overview

This dataset supports the goals of the Innovation Ecosystems (IES) project by providing large-scale, multilingual company website data from Germany and the United Kingdom. It is designed to enable research on information retrieval, retrieval-augmented generation (RAG), and explainability in the context of business and innovation ecosystems.

To support the development and evaluation of the IES Platform, we constructed a harmonized corpus of structured and unstructured business information extracted from publicly accessible company websites. The dataset is intended as a reusable research resource for the broader research community.

> This dataset has been assigned the DOI https://doi.org/10.24352/UB.OVGU-2026-022 and will be presumably active at Feb 20, 2026. 

> At present, the publicly accessible files contain a representative sample of the complete dataset. The full dataset will be made available once the ongoing migration of the university library’s data infrastructure has been completed.
> 
> The sample can be accessed [here](https://cloud.ovgu.de/s/6BijmQxBgaqXbpL). Access to the complete dataset can be requested by contacting stefan1.langer@ovgu.de.

---

## 2. Dataset Description

The dataset comprises crawled content from company websites in two countries:

### United Kingsdom

The corpus is multilingual, primarily covering English and German content. Each website snapshot contains raw HTML and extracted plain text, along with associated metadata, enabling downstream tasks such as semantic retrieval, entity extraction, clustering, and explainability analysis.

The dataset represents a **single snapshot in time** and reflects the publicly available information on company websites at the time of crawling.

**Data sources**
- **United Kingdom:** 52,282 company websites
- **Germany:** 11,159 company websites

For UK companies, official company information was sourced from [Companies House](https://download.companieshouse.gov.uk/en_output.html), the United Kingdom’s government registry of companies. Companies House maintains statutory records on registered companies, including company names, registration numbers, legal status, registered addresses, and filing histories. These records were used to identify companies and obtain official metadata for inclusion in the dataset.

Company website URLs were identified using publicly available sources, including [Endole](https://endole.co.uk/). No proprietary data from Endole is redistributed as part of this dataset.

For German companies, official company information was sourced from the [Unternehmensregister](https://unternehmensregister.de/), the central online portal for company register information in Germany. The Unternehmensregister provides access to legally required company disclosures, including registration details, legal form, registered office, and published filings. These records were used to identify companies and obtain official metadata for inclusion in the dataset.
The company website URLs were identified using a combination of search engines, a web scraper, automatic filtering based on the scraped website contents, and manual work. 

---

## 3. Dataset Composition

**Data sources**
- Publicly accessible company websites
- Companies operating in Germany and the United Kingdom

**Content types**
- Raw website HTML
- Extracted textual content (plain text)
- metadata information

**Languages**
- English  
- German  

**Granularity**


**File formats**
- HTML (raw website content)
- TXT (extracted plain text)

**Total size**
Approximate size:
- **United Kingdom**: 110 GB (unzipped)
- **Germany**: 38 GB (unzipped)

---

## 4. Data Collection and Processing

**Crawling methodology**
- Websites were crawled using automated tools in **July 2025** for United Kingdom companies and between **March 2024** and **September 2024** for German companies.
- We downloaded the Homepage of the website and subpages directly linked from the homepage
- To ensure comprehensive text extraction from modern web applications, we used Puppeteer, a headless browser automation framework. This allowed dynamic rendering of JavaScript-driven websites, including progressive web applications built with frameworks such as React and Vue.js. By executing client-side scripts during crawling, we captured rendered content that would not be available through static HTML retrieval alone.
- Only publicly accessible content was collected.
- No authentication, paywalled, or private content was accessed.

**Preprocessing**
- Extraction of plain text from HTML
- Basic cleaning and normalization of text
- Association of extracted text with source URLs and crawl metadata

**Limitations and biases**
- Coverage depends on web presence and crawlability of companies.
- Small and medium-sized enterprises (SMEs) may be underrepresented in certain sectors.
- Website content may be incomplete, outdated, or primarily promotional.
- The dataset reflects a snapshot and does not capture subsequent website changes.



### 4. Data Collection and Processing

### Crawling Methodology

- Websites of United Kingdom companies were crawled in **July 2025**.
- Websites of German companies were crawled between **March 2024** and **September 2024**.
- Crawling was conducted using automated tools.
- For each company, the homepage and subpages directly linked from the homepage were downloaded.
- Both raw HTML files and rendered page content were collected.
- To capture dynamically generated content, we used **Puppeteer**, a headless browser automation framework.
- Puppeteer executed client-side JavaScript to render modern web applications, including progressive web applications (PWAs) built with frameworks such as React and Vue.js.
- This enabled extraction of textual content that would not be available through static HTML retrieval alone.
- Only publicly accessible content was collected.
- No authentication mechanisms were bypassed, and no paywalled or restricted content was accessed.

### Preprocessing

- Plain text was extracted from the downloaded HTML files.
- Basic cleaning and normalization were applied to remove markup artifacts and non-textual elements.
- Extracted text was stored in TXT format.
- Text files were associated with source URLs and crawl metadata.

### Limitations and Biases

- Coverage depends on the web presence and crawlability of companies.
- Small and medium-sized enterprises (SMEs) may be underrepresented in certain sectors.
- Website content may be incomplete, outdated, or primarily promotional in nature.
- The dataset represents a snapshot in time and does not reflect subsequent changes to company websites.


---

## 5. Intended Use

The dataset is suitable for:
- Retrieval-augmented generation (RAG) research
- Explainable AI and model interpretability
- Semantic search and information retrieval
- Analysis of innovation ecosystems and business landscapes

The dataset is **not** intended for:
- Legal, financial, or compliance assessments of individual companies
- Commercial profiling or ranking of companies without additional validation

---

### 6. Legal Considerations

### License

This dataset is released under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license.

License details are available at:
https://creativecommons.org/licenses/by/4.0/

A copy of the license text is included in the [`LICENSE`](./LICENSE) file of this repository.

The CC BY 4.0 license applies to the dataset as a compilation, including its structure, metadata, and the preprocessing performed by the authors.

### Third-Party Content

Copyright of the original website content (including raw HTML and extracted textual content) remains with the respective website owners. The dataset does not claim ownership of third-party website content.

Users of this dataset are responsible for ensuring that their use complies with applicable copyright law and any rights associated with the original content providers. The authors make no representations regarding rights clearance beyond the compilation of the dataset itself.

### Personal Data

The dataset may incidentally contain personal data that was publicly available on company websites (e.g., names of contact persons). No personal data was intentionally collected, enriched, or annotated.

Users are responsible for ensuring that their use of the dataset complies with applicable data protection regulations.

---

## 7. Access and Availability

The dataset is publicly available via this repository and the associated DOI.

**Download**
- Links to dataset files are provided via the DOI landing page or repository interface.

**Access conditions**
- Open access

**Technical requirements**
- Storage: sufficient disk space for HTML and text files
- Processing: standard data processing tools (e.g. Python, text and HTML parsers)

---

## 8. Relationship to the IES Platform

The dataset was created as part of the Innovation Ecosystems (IES) project and is used to develop and evaluate components of the IES Platform, including retrieval, ranking, and explanation modules. The dataset can be used independently of the platform and does not require access to the IES system.

---

## 9. Citation

If you use this dataset, please cite it as follows:

**Plain text**

Langer, Stefan; Genzmehr, Marcel; Polley, Sayantan; N{\"u}rnberger}, Andreas (2026). *IES Multilingual Company Website Dataset (UK & Germany), v1.0*. DOI: 10.24352/UB.OVGU-2026-022 

**BibTeX**
```bibtex
@dataset{ies_company_websites_2025,
  title   = {IES Multilingual Company Website Dataset (UK & Germany)},
  author  = {Stefan Langer and Marcel Genzmehr and Sayantan Polley and Andreas N{\"u}rnberger},
  year    = {2026},
  version = {1.0},
  doi     = {10.24352/UB.OVGU-2026-022}
}
```

## 10. Versioning and Updates

- v1.0: Initial public release
- Future updates: no updates planned

## 11. Contact

For questions, issues, or corrections, please contact:

- Maintainer: Stefan Langer
- Email: stefan1.langer@ovgu.de
