## 📦 Dataset

We release **200 ImageNet papers**, including **100 development** and **100 validation** papers, each with **ground-truth labels**.

### 📁 Directory Structure

```
data/
├── dev_labels.csv   # gold labels (see table below)
├── val_labels.csv   # validation set
```

### 🏷️ Columns

| Column       | Description                                                                 |
|--------------|-----------------------------------------------------------------------------|
| `arxiv_name` | PDF filename (e.g., `1312.6229v4.pdf`)                                      |
| `top1_acc`   | Reported Top-1 ImageNet accuracy (**in %**); `NA` indicates not reported    |
| `url` _(optional)_ | Direct link to the PDF (used only for non-arXiv papers)              |

> `NA` → metric absent (e.g., only Top-5 or validation results are reported).

---

### 🔍 Quick Peek

```python
import pandas as pd
df = pd.read_csv('data/val_labels.csv')
print(df.head(8))
```

```
       arxiv_name   top1_acc
0  1312.6229v4.pdf     85.82
1  1406.2732v1.pdf      NA
2  1412.0296v1.pdf      NA
3  1412.6598v2.pdf      NA
4  1502.03167v3.pdf     NA
5  1503.01224v2.pdf     NA
6  1506.04701v3.pdf     NA
7  1510.00921v6.pdf     NA
```

---

### 🌐 External URLs for Reproducibility

To enhance reproducibility for non-arXiv papers (e.g., those from CVPR/ICCV/ECCV), we include an optional `url` column with the direct PDF link.  
For arXiv papers, this field is left blank (a canonical arXiv link can be constructed from the filename if needed).

**Example (CSV format):**

```csv
arxiv_name,top1_acc,url
1312.6229v4.pdf,85.82,
Yan_HD-CNN_Hierarchical_Deep_ICCV_2015_paper.pdf,63.34,https://openaccess.thecvf.com/content_iccv_2015/papers/Yan_HD-CNN_Hierarchical_Deep_ICCV_2015_paper.pdf
```

---

📌 **Note**: All PDFs are distributed strictly for research and benchmarking purposes. Copyright remains with the original publishers.
