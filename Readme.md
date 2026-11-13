# IVUS Text Datasets

CSV descriptions for IVUS captioning, lesion description, and report-generation research.

## Published files

| File | Records | Columns |
| --- | ---: | --- |
| `ivus_cad_rad_2175.csv` | 2,175 | `description` |
| `ivus_lesion_caps_2175.csv` | 2,175 | `description` |
| `ivus_reportgen_2175.csv` | 2,175 | `description` |

Each file contains a header and one text description per record. The release currently provides description text. Image identifiers, image-to-row pairing, dataset split metadata, and annotation-generation details remain undocumented.

## Reading the CSVs

The files can be read with Python's standard CSV reader.

```python
import csv

with open("ivus_lesion_caps_2175.csv", newline="", encoding="utf-8-sig") as handle:
    descriptions = [row["description"] for row in csv.DictReader(handle)]

print(len(descriptions))
```

## Image source

The original repository identifies the following Roboflow IVUS search as its image source. Individual dataset versions, image mappings, and applicable terms need to be established from the source datasets. [Roboflow IVUS search](https://universe.roboflow.com/search?q=ivus)
