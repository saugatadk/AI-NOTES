# Distributed Training Pipeline (`madewithml.train`)

The `train` module manages multi-worker distributed training using Ray Train (`TorchTrainer`), tracking experiment metrics in MLflow, and saving model checkpoints.

---

## 🛠️ Key Functions

### `train_model`
```python
def train_model(
    experiment_name: str,
    dataset_loc: str,
    train_loop_config: dict,
    num_workers: int = 1,
    cpu_per_worker: int = 1,
    gpu_per_worker: int = 0,
    num_epochs: int = 5,
    batch_size: int = 256,
    results_fp: str = None
) -> ray.train.Result
```
Main orchestrator that:
1. Loads and preprocesses the training/validation datasets with Ray Data.
2. Initializes a distributed `TorchTrainer`.
3. Coordinates workers across CPU/GPU resources.
4. Logs metrics and artifacts into MLflow.

### `train_loop_per_worker`
```python
def train_loop_per_worker(config: dict) -> None
```
Worker execution loop run on each distributed process:
- Instantiates the `FinetunedLLM` model wrapped in Ray's distributed PyTorch context.
- Configures the `AdamW` optimizer and learning rate decay scheduler.
- Runs epochs, calling `train_step` on batches, computing CrossEntropy loss, and running validation with `eval_step`.
- Emits validation metrics and checkpoints back to the Ray Train coordinator.
