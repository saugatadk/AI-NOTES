# Batch & Offline Inference (`madewithml.predict`)

The `predict` module provides high-throughput inference utilities for loading model checkpoints and generating class probabilities for unseen data.

---

## 🛠️ Key Classes & Functions

### `class TorchPredictor`
Custom predictor class wrapping a loaded PyTorch model and fitted preprocessor:
```python
def predict_proba(self, batch: pd.DataFrame) -> np.ndarray
```
Applies tokenization preprocessing and returns normalized softmax probabilities across all classes.

### `predict`
```python
def predict(run_id: str, title: str = "", description: str = "") -> Dict
```
Utility function for quick single-sample inference from the command line or scripts given a run ID and input text.

### `get_best_run_id` & `get_best_checkpoint`
```python
def get_best_run_id(experiment_name: str = "", metric: str = "", mode: str = "") -> str
def get_best_checkpoint(run_id: str) -> ray.train.torch.TorchCheckpoint
```
Queries the MLflow model registry to locate the optimal run ID based on validation metrics (e.g., minimum `val_loss`) and retrieves the saved weights artifact.

### `format_prob` & `decode`
Decodes numeric prediction indices back to human-readable category strings using the fitted class mapping.
