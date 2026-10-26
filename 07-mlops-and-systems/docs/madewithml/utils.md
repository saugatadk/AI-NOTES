# Core Utilities (`madewithml.utils`)

The `utils` module provides shared helpers for reproducibility, artifact serialization, and tensor collations.

---

## 🛠️ Key Utilities

### `set_seeds`
```python
def set_seeds(seed: int = 42) -> None
```
Fixes random seeds across Python's `random`, `numpy`, PyTorch CPU, and PyTorch CUDA to guarantee reproducible experimentation.

### `load_dict` & `save_dict`
```python
def save_dict(d: Dict, path: str, cls: Any = None, sortkeys: bool = False) -> None
def load_dict(path: str) -> Dict
```
Safely serializes and deserializes configurations, evaluation outputs, and metadata files into human-readable JSON files with custom encoder support.

### `collate_fn` & `pad_array`
```python
def collate_fn(batch: Dict[str, np.ndarray]) -> Dict[str, torch.Tensor]
```
Prepares distributed worker batches for PyTorch model input, converting numpy arrays to PyTorch tensors and handling dynamic padding.
