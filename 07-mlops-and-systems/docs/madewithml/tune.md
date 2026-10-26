# Hyperparameter Tuning (`madewithml.tune`)

The `tune` module coordinates distributed hyperparameter optimization across clusters using Ray Tune and early-stopping schedulers.

---

## 🛠️ Key Function

### `tune_models`
```python
def tune_models(
    experiment_name: str,
    dataset_loc: str,
    initial_params: dict,
    num_workers: int = 1,
    cpu_per_worker: int = 1,
    gpu_per_worker: int = 0,
    num_runs: int = 4,
    num_epochs: int = 5,
    batch_size: int = 256,
    results_fp: str = None
) -> ray.tune.ResultGrid
```

### Search Space & Optimization Mechanics:
- **Search Spaces**: Explores continuous and categorical parameters:
  - `lr`: Uniform or log-uniform learning rate sampling (e.g., `1e-5` to `1e-3`).
  - `dropout_p`: Dropout rate exploration (e.g., `0.3` to `0.7`).
  - `lr_factor` & `lr_patience`: Learning rate scheduler decay aggressiveness.
- **ASHA Scheduler**: Employs Asynchronous Successive Halving to terminate underperforming trials early, freeing compute resources for promising configurations.
- **Trial Logging**: Tracks trial loss and validation accuracy directly into MLflow experiments.
