## 📦 Dataset

We release **380 ImageNet papers**, including **280 development**, **100 validation**, each with **ground-truth labels**.

### 📁 Directory Structure

```
project_root/
├── README.md
└── data/
       ├── dev_labels.csv        # gold labels for 280 dev papers (see table below)
       ├── val_labels.csv      # validation set (100 papers)
       ├── Supplementary_mat.pdf # full supplementary material (25 pages)
└── docs/
       ├── Supplementary_mat_p01.png  # page screenshots of supplementary PDF
       ├── Supplementary_mat_p02.png
       ├── ...
       └── Supplementary_mat_p25.png
```

### 🏷️ Columns

| Column       | Description                                                                 |
|--------------|-----------------------------------------------------------------------------|
| `arxiv_name` | PDF filename (e.g., `1312.6229v4.pdf`)                                      |
| `top1_acc`   | Reported Top-1 ImageNet accuracy (**in %**); `NA` indicates not reported    |
| `link` _(optional)_ | Direct link to the PDF (used only for non-arXiv papers)              |

> `NA` → metric absent (e.g., only Top-5 or validation results are reported).



---
### 🔍 Quick Peek

```python
import pandas as pd
df = pd.read_csv('data/val_labels.csv')
print(df.head(2))
```
---
**Example (CSV format):**

```csv
       arxiv_name                                top1_acc                             link
90  1312.6229v4.pdf                                85.82
91  CNN_Hierarchical_Deep_ICCV_2015_paper.pdf       NA          https://openaccess.thecvf.com/content_iccv_2015/papers/Yan_HD-CNN_Hierarchical_Deep_ICCV_2015_paper.pdf

```
### 🌐 External URLs for Reproducibility

To enhance reproducibility for non-arXiv papers (e.g., those from CVPR/ICCV/ECCV), we include an optional `link` column with the direct PDF link.  
For arXiv papers, this field is left blank (a canonical arXiv link can be constructed from the filename if needed).

---
## 📊 Metric Presence Summary

| Metric Presence | Development Set | Validation Set |
|------------------|-----------------|----------------|
| **Ground-truth Present** | 54 | 27 |
| **Ground-truth Absent**  | 226 | 73 |
| **Total**                | 280 | 100 |


## 🖼️ Section F – Supplementary Materials


### 📑 View Embedded PDF
> ⚠️ **Note:** GitHub does **not** support embedded PDF viewing. Upon clicking a page image below, you will be redirected to the full PDF file in your browser.

[![Page 1](docs/Supplementary_mat_p01.png)](docs/Supplementary_mat.pdf)
[![Page 2](docs/Supplementary_mat_p02.png)](docs/Supplementary_mat.pdf)
[![Page 3](docs/Supplementary_mat_p03.png)](docs/Supplementary_mat.pdf)
[![Page 4](docs/Supplementary_mat_p04.png)](docs/Supplementary_mat.pdf)
[![Page 5](docs/Supplementary_mat_p05.png)](docs/Supplementary_mat.pdf)
[![Page 6](docs/Supplementary_mat_p06.png)](docs/Supplementary_mat.pdf)
[![Page 7](docs/Supplementary_mat_p07.png)](docs/Supplementary_mat.pdf)
[![Page 8](docs/Supplementary_mat_p08.png)](docs/Supplementary_mat.pdf)
[![Page 9](docs/Supplementary_mat_p09.png)](docs/Supplementary_mat.pdf)
[![Page 10](docs/Supplementary_mat_p10.png)](docs/Supplementary_mat.pdf)
[![Page 11](docs/Supplementary_mat_p11.png)](docs/Supplementary_mat.pdf)
[![Page 12](docs/Supplementary_mat_p12.png)](docs/Supplementary_mat.pdf)
[![Page 13](docs/Supplementary_mat_p13.png)](docs/Supplementary_mat.pdf)
[![Page 14](docs/Supplementary_mat_p14.png)](docs/Supplementary_mat.pdf)
[![Page 15](docs/Supplementary_mat_p15.png)](docs/Supplementary_mat.pdf)
[![Page 16](docs/Supplementary_mat_p16.png)](docs/Supplementary_mat.pdf)
[![Page 17](docs/Supplementary_mat_p17.png)](docs/Supplementary_mat.pdf)
[![Page 18](docs/Supplementary_mat_p18.png)](docs/Supplementary_mat.pdf)
[![Page 19](docs/Supplementary_mat_p19.png)](docs/Supplementary_mat.pdf)
[![Page 20](docs/Supplementary_mat_p20.png)](docs/Supplementary_mat.pdf)
[![Page 21](docs/Supplementary_mat_p21.png)](docs/Supplementary_mat.pdf)
[![Page 22](docs/Supplementary_mat_p22.png)](docs/Supplementary_mat.pdf)
[![Page 23](docs/Supplementary_mat_p23.png)](docs/Supplementary_mat.pdf)
[![Page 24](docs/Supplementary_mat_p24.png)](docs/Supplementary_mat.pdf)
[![Page 25](docs/Supplementary_mat_p25.png)](docs/Supplementary_mat.pdf)


---

📌 **Note**: All PDFs are distributed strictly for research and benchmarking purposes. Copyright remains with the original publishers.
