# Model Evaluation & Diagnostics (`madewithml.evaluate`)

The `evaluate` module handles model validation on holdout datasets, computing global accuracy, per-class F1-scores, and granular slice-based diagnostics.

---

## 🛠️ Key Functions

### `evaluate`
```python
def evaluate(
    run_id: str,
    dataset_loc: str,
    results_fp: str = None
) -> Dict[str, Any]
```
Loads the specified model checkpoint from MLflow, runs inference across the holdout dataset, and aggregates evaluation metrics.

### `get_overall_metrics`
```python
def get_overall_metrics(y_true: np.ndarray, y_pred: np.ndarray) -> Dict
```
Computes global performance statistics including macro/weighted Precision, Recall, and F1-score across all test samples.

### `get_per_class_metrics`
```python
def get_per_class_metrics(y_true: np.ndarray, y_pred: np.ndarray, class_to_index: Dict) -> Dict
```
Generates a breakdown of precision, recall, and sample support for every individual target category.

### `get_slice_metrics`
```python
def get_slice_metrics(y_true: np.ndarray, y_pred: np.ndarray, ds: ray.data.Dataset) -> Dict
```
Performs behavioral and slice-based testing:
- **Length Slicing**: Evaluates accuracy on short vs long text inputs (`short_text`).
- **Domain Slicing**: Evaluates accuracy on specific topic keywords (`nlp_llm`).
- Ensures model does not degrade on high-priority edge cases.
