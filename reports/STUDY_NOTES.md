# Study Notes and Source Provenance

**Source:** Universitas Airlangga 2024 three-person Mass Communication Theory project poster, *Analisis Representasi Generative AI pada Media Massa Online*, and the historical `ANALISIS_DETIK.ipynb` notebook.

## Quantitative information recorded in the poster

| Metric | detikcom | CNBC Indonesia | CNN Indonesia |
|---|---:|---:|---:|
| Articles | 74 | 60 | 35 |
| Total word count (*Total Kosa Kata*) | 36,550 | 30,551 | 16,838 |
| Average words/article (*Average Kosa Kata per-Berita*) | 493.92 | 509.18 | 481.09 |
| Innovation | 34 | 43 | 27 |
| Education | 20 | 2 | 2 |
| Challenges | 10 | 10 | 1 |
| Regulation | 5 | 5 | 2 |
| Social | 3 | 0 | 2 |
| Crime | 2 | 0 | 1 |

The labels and counts are historical and were not independently reprocessed from full three-outlet datasets. `Total Kosa Kata` is treated as poster-reported total word count, not proven unique vocabulary size. Percentage denominators in the poster's example phrase counts are unspecified, and identical Detik phrase text appears with different counts; the README records these without attempting to reconcile them.

## Three poster conclusions

1. *Tidak terdapat perbedaan dalam tema pemberitaan*: understood here as **overlap of broad news themes**, rather than identical numerical distributions; CNBC had no recorded Social or Crime articles in this sample.
2. *Berita berfokus pada edukasi & inovasi*: supported by 104 Innovation and 24 Education articles across 169 recorded articles; Education appears most often in Detik.
3. *Terdapat perbedaan visual, bahasa & framing*: based on descriptive group observations of technical language, headlines, quotations, readability, layouts, and illustrations; no numeric scoring or causal claim.

## Publication and reproducibility

- Notebook: detikcom original historical workflow, cell outputs cleared; sample implementation that may be adapted to other datasets, not evidence of identical runs for all outlets.
- No original articles, source CSV, or poster bearing student numbers are distributed.
- The theme chart is generated from the poster's tabulated counts; it is not a new data-driven model output.
- The study did not implement a supervised sentiment classifier and should not be described as one.
