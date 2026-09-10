# FA550 sample data

Public data files for FA550 Data Visualization Applications, Stevens Institute
of Technology. These exist so course snippets can load them straight from a URL,
with nothing to download and nothing to upload.

## 311-sample.csv

900 synthetic service requests shaped like NYC 311 data. Nothing here describes
a real person or a real request.

| Column | What it holds |
|---|---|
| `borough` | One of five boroughs |
| `complaint` | Heat, Noise, Water, Street or Parking |
| `date` | Request date across 2024 |
| `crew` | Crew size assigned, 1 to 5 |
| `hours` | Hours taken to close the request |
| `lat`, `lon` | Approximate location |
| `reopened` | Whether the request came back |

Load it directly.

```python
import pandas as pd
url = "https://raw.githubusercontent.com/hosl-research/fa550-data/main/311-sample.csv"
df = pd.read_csv(url, parse_dates=["date"])
```

```r
url <- "https://raw.githubusercontent.com/hosl-research/fa550-data/main/311-sample.csv"
df <- read.csv(url)
```
