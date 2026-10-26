# Data Processing Pipeline (`madewithml.data`)

The `data` module provides distributed ingestion, preprocessing, cleaning, and tokenization utilities designed to work seamlessly with Ray Datasets.

---

## 🛠️ Key Functions & Classes

### `load_data`
```python
def load_data(dataset_loc: str, num_samples: int = None) -> ray.data.Dataset
```
Loads raw CSV data from local storage or cloud object stores into a Ray Dataset with random shuffling.

### `stratify_split`
```python
def stratify_split(ds: Dataset, stratify: str, test_size: float, shuffle: bool = True, seed: int = 1234) -> Tuple[Dataset, Dataset]
```
Splits a distributed Ray Dataset into training and testing partitions while preserving label distributions across classes.

### `clean_text`
```python
def clean_text(text: str, stopwords: List = STOPWORDS) -> str
```
Normalizes raw input text by stripping special characters, links, and redundant stopwords to standardize vocabulary.

### `tokenize`
```python
def tokenize(batch: Dict) -> Dict
```
Applies Hugging Face's BERT Tokenizer across batches in parallel, padding and truncating sequences into tensor arrays (`input_ids`, `attention_mask`).

### `class CustomPreprocessor`
Stateful preprocessor that fits on the training partition:
- Maps string category labels into integer class indices (`class_to_index`).
- Transforms raw text columns using `clean_text` and `tokenize`.
- Preserves tokenization metadata for deployment reproducibility.
