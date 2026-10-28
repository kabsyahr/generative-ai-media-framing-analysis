# Generative AI in Indonesian Online Media | Text Mining & Framing Analysis

**Academic group project · Mass Communication Theory · Universitas Airlangga · 2024**  
**Focus:** Media analytics · Indonesian text mining · Thematic content analysis · Cross-outlet comparison

## 1. Project Overview

How do Indonesian online news outlets represent generative AI, and how do their topics, language, and editorial presentation differ? This three-person academic project examined articles from **detikcom, CNBC Indonesia, and CNN Indonesia** through quantitative text exploration and qualitative framing observations.

The work describes **news coverage**, not audience sentiment. The project did not train a machine-learning sentiment classifier or measure changes in public opinion.

## 2. Research Problem and Objectives

As generative AI became a recurring subject of media coverage, the team sought to understand **which aspects received attention** and **how the same technology was presented differently** across news outlets.

The analysis addressed four practical questions:

1. What topics were discussed, and how frequently did they appear in each outlet?
2. What words and expressions were prominent in the reviewed articles?
3. How did the outlets differ in technical language, headlines, source quotations, and framing?
4. How did layout, readability, and imagery contribute to editorial presentation?

## 3. Dataset and Scope

The final team poster reported the following article counts:

| Outlet | Articles | Poster-reported total word count | Average words per article |
|---|---:|---:|---:|
| detikcom | **74** | 36,550 | 493.92 |
| CNBC Indonesia | **60** | 30,551 | 509.18 |
| CNN Indonesia | **35** | 16,838 | 481.09 |
| **Total** | **169** | **83,939** | — |

**Interpretation:** CNBC Indonesia had the highest reported average article length (**509.18 words**), followed by detikcom (**493.92**) and CNN Indonesia (**481.09**). These are **descriptive sample averages**; they do not establish differences in readability or quality. The total word-count field follows the poster's *Total Kosa Kata* figure; the original counting script for every outlet is not available to independently confirm its tokenization definition.

*Source: 2024 group poster. Article-level files for the full three-outlet sample are not published in this repository.*

## 4. Analytical Workflow

1. **Collect and categorize news articles** across the three selected outlets.
2. **Code articles by six themes:** Innovation, Education, Challenges, Regulation, Social, and Crime.
3. **Explore article text:** basic normalization, selected stopword removal, frequent-word extraction, and n-gram exploration.
4. **Compare descriptive metrics:** article counts, category distributions, frequently occurring terms, and reported article lengths.
5. **Review qualitative presentation:** technical language, headline style, use of interview/source quotations, layout, and illustrations.
6. **Synthesize findings** into a group comparison poster.

### Notebook Implementation

The repository includes a **sample implementation using detikcom articles** in [`notebooks/detik_text_mining_original.ipynb`](notebooks/detik_text_mining_original.ipynb). It documents text preprocessing, word-frequency analysis, and n-gram exploration. The analytical approach **can be adapted** to other news outlets after adjusting the source dataset and relevant processing logic.

The **three-outlet comparison below comes from the group's historical poster**, not from an execution of the included notebook on all three outlets. The available notebook is presented as a technical example, not proof that a single unchanged script reproduced all published figures.

## 5. Findings and Analytical Insights

### 5.1. Topic Distribution Across the Three Outlets

Six themes were recorded in the group poster:

| Theme | detikcom (n=74) | CNBC Indonesia (n=60) | CNN Indonesia (n=35) | Total |
|---|---:|---:|---:|---:|
| Innovation | 34 | 43 | 27 | **104** |
| Education | 20 | 2 | 2 | **24** |
| Challenges | 10 | 10 | 1 | **21** |
| Regulation | 5 | 5 | 2 | **12** |
| Social | 3 | 0 | 2 | **5** |
| Crime | 2 | 0 | 1 | **3** |
| **Total** | **74** | **60** | **35** | **169** |

![Theme distribution by outlet](images/theme_distribution_by_outlet.png)

**Analytical insights**

- **Innovation was the largest theme in all three samples:** detikcom **34/74 (45.9%)**, CNBC Indonesia **43/60 (71.7%)**, and CNN Indonesia **27/35 (77.1%)**. Across all outlets, **104/169 articles (61.5%)** were coded as Innovation.
- **Education was much more prominent in the detikcom sample:** **20/74 (27.0%)**, compared with **2/60 (3.3%)** for CNBC Indonesia and **2/35 (5.7%)** for CNN Indonesia. Together, Innovation and Education accounted for **128/169 (75.7%)** reviewed articles.
- **Challenges appeared in both detikcom and CNBC Indonesia** (**10 articles each**), versus **1 article** in CNN Indonesia. The remaining categories were less frequent.
- **Shared broad themes did not mean identical coverage proportions.** The poster's takeaway of no fundamental difference in news themes is best understood as *overlapping areas of coverage*; specific category representation varied, and the poster recorded **zero Social and Crime articles for CNBC Indonesia** in the sample.

*Themes are historical content-coding categories, not machine-learning predictions. No inferential significance test was reported.*

### 5.2. Frequently Appearing Words

The group poster lists these ten prominent terms for each outlet, in the displayed order:

| detikcom | CNBC Indonesia | CNN Indonesia |
|---|---|---|
| mahasiswa | galaxy | telkomsel |
| teknologi | indonesia | indonesia |
| indonesia | s24 | teknologi |
| data | fitur | persen |
| perusahaan | samsung | galaxy |
| meningkatkan | teknologi | digital |
| digital | digital | samsung |
| tugas | video | bri |
| dosen | telkomsel | microsoft |
| aplikasi | pengguna | fitur |

**Analytical insight:** The detikcom list contains terms related to higher education (e.g., *mahasiswa*, *dosen*, *tugas*), while CNBC Indonesia and CNN Indonesia show technology product and company terms such as *Galaxy*, *Samsung*, and *Telkomsel*. These are **observed word lists**, not sufficient evidence by themselves to infer the editorial intent or sentiment of every article.

### 5.3. Reported Terms and Illustrative Expressions

The poster includes examples of expressions observed in each outlet. The counts and percentages below are **transcribed as reported**, rather than independently recalculated. They are **examples**, not a complete ranked keyword-frequency dataset.

| Outlet | Poster example | Reported count | Reported percentage |
|---|---|---:|---:|
| detikcom | “Google Cloud” | 21 words | 0.28% |
| detikcom | “Mahasiswa Dosen” | 34 words | 0.40% |
| detikcom | “Mahasiswa Dosen” (second poster entry) | 13 words | 0.47% |
| detikcom | “Ditjen Dikti” | 6 words | 0.69% |
| detikcom | “Elon Musk” | 12 words | 1.64% |
| detikcom | “Foto Mesum” | 7 words | 2.06% |
| CNBC Indonesia | “Entitas Ekonomi” | 18 words | 0.72% |
| CNBC Indonesia | “Tony Blair” | 11 words | 0.92% |
| CNBC Indonesia | “Galaxy S” | 198 words | 1.43% |
| CNBC Indonesia | “Digiland Conference” | 6 words | 1.08% |
| CNN Indonesia | “hoaks pemilu” | 6 words | 1.81% |
| CNN Indonesia | “jcio community” | 5 words | 0.87% |
| CNN Indonesia | “tenaga kerjanya” | 3 words | 1.01% |
| CNN Indonesia | “samsung galaxy” | 33 words | 0.45% |
| CNN Indonesia | “keterampilan digital” | 3 words | 0.34% |
| CNN Indonesia | “media sosial” | 5 words | 0.95% |

**Interpretation:** These examples point to differences in contextual references—from education and public figures to consumer devices, employment, and digital skills. **The poster does not specify a consistent denominator for the percentages**, so they should not be treated as directly comparable cross-outlet rates. The detikcom poster repeats “Mahasiswa Dosen” with two different figures; both historical entries are retained above rather than silently corrected.

### 5.4. Language, Headlines, and Framing

The poster describes qualitative differences in presentation:

| Aspect | detikcom | CNBC Indonesia | CNN Indonesia |
|---|---|---|---|
| **Technical language** | Uses relevant technical terms, sometimes without extensive lay explanation | More formal language, data/statistics emphasis, and technical terminology | Simpler explanations and added context for technical terms |
| **Headlines and subheadlines** | Some titles or subheadlines described as *clickbait* | More factual, technical and information-oriented headlines | Informative and relevant headlines, with less emphasis on clickbait |
| **Source quotations** | Quotes from companies and government officials | Professional sources supporting technical or strategic claims | Technology experts, public officials, and academics cited for explanatory context |

**Analytical insight:** Different presentation styles can shape **how readers encounter** the same subject. These observations are **qualitative team assessments** of the reviewed articles; they are not scored readability indices, experimentally measured framing effects, or claims about every article published by these outlets.

### 5.5. Visual Presentation and Readability

The poster also evaluates article appearance—not only text:

| Aspect | detikcom | CNBC Indonesia | CNN Indonesia |
|---|---|---|---|
| **Layout and readability** | Clean, organized structure with short paragraphs; described as comfortable to scan | Clean, organized layout and a reading-friendly structure | Structured, responsive layout with short paragraphs and spacing between text, images, and advertisements |
| **Images and illustrations** | Relevant images of prominent technology figures, companies, or events | Illustrations generally relevant to the news and supportive of the narrative | Generally relevant imagery, although some visuals were described as emphasizing appeal rather than fully representing the article content |

**Analytical insight:** The group's interpretation was that **visual design, language, and framing differed** across the outlets, even where major discussion topics overlapped. The poster did not provide a numerical readability test or image-relevance scoring, so these observations remain descriptive.

### 5.6. Consolidated Takeaways from the Team Poster

The original poster emphasized three conclusions. The table below preserves their intent while making the evidence explicit:

| Poster conclusion | Evidence-supported interpretation |
|---|---|
| **No fundamental difference in news themes** | All three outlets discussed generative AI through overlapping broad topics, especially Innovation. **Their category distributions were not identical**. |
| **Coverage focused on Education and Innovation** | Innovation was the dominant category (**104 articles**) and Education contributed **24**, together representing **128/169 articles (75.7%)**. Education was concentrated in detikcom's sample. |
| **Differences in visual, language, and framing** | Qualitative comparisons reported differences in headline style, technical explanations, source quotations, layout, and image use. |

## 6. Media Analytics Implications

The project illustrates how a combined **quantitative and qualitative content-analysis workflow** can support:

- **Topic monitoring:** Track which editorial topics dominate a defined news sample and identify differences in their shares across outlets.
- **Keyword exploration:** Use repeated terms and n-grams to identify article contexts worth examining in greater depth.
- **Cross-outlet comparison:** Combine frequency tables with structured reading of headlines, quotations, and visual presentation.
- **Communication research:** Describe media coverage with traceable evidence rather than treating word frequency as a substitute for framing analysis.

**Key takeaway:** The central value of this project is not an automated sentiment score. It is the combination of **169 historically documented article classifications** with **word-level exploration and contextual interpretation** to compare how three outlets presented generative AI.

## 7. Repository Contents

- **[Sample Detik text-mining notebook](notebooks/detik_text_mining_original.ipynb)** — original workflow, with saved cell outputs removed; can be adapted to other news datasets.
- **[Theme comparison chart](images/theme_distribution_by_outlet.png)** — visualizes the reported three-outlet coded-topic counts.
- **[Study notes](reports/STUDY_NOTES.md)** — data provenance, important terminology, and documentation boundaries.
- **[Python requirements](requirements.txt)** — dependencies associated with the notebook.

### Running the Sample Notebook

The historical notebook expects a local file named `berita lokal - LABEL DETIK.csv` containing at least the columns `Teks`, `Label`, and `Tanggal publikasi`. That file is **not** distributed with the repository. Use only appropriately authorized data.

```bash
pip install -r requirements.txt
```

The original environment setup and paths may require adjustment before execution. **No new results are claimed from rerunning the notebook.**

## 8. Team Attribution and Study Limitations

This is a **three-member Universitas Airlangga academic group project** (2024). The analysis, poster, and findings are attributed to the group, not claimed as individually authored. The original poster is not republished because it includes members' personal identification details.

- The cross-outlet figures and observations are **transcribed from the group's final poster**; only the Detik notebook is included as a **sample technical implementation**.
- The underlying article datasets, complete article list, and original coding decisions cannot be fully audited from this public repository.
- Historical percentages for individual expressions are retained as printed in the poster, including entries with unclear denominators or repeated phrases.
- Theme labels are based on **content analysis**, not machine-learning topic classification.
- Findings are descriptive of the **reviewed samples**. The project does not establish public sentiment, readership effects, causality, or statistical population-level differences.
