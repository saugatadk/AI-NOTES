# ML System Design & MLOps Architecture

A complete engineering reference guide for designing, developing, and deploying production-grade Machine Learning services with Ray, PyTorch, MLflow, and FastAPI.

---

## 🏛️ System Architecture

```
                    ┌─────────────────────────┐
                    │ Raw Datasets (CSV)      │
                    └────────────┬────────────┘
                                 │
                                 ▼
                     madewithml.data
                 (Ingestion & Tokenization)
                                 │
                                 ▼
                    madewithml.models
                    (BERT Classifier)
                                 │
             ┌───────────────────┴───────────────────┐
             │                                       │
             ▼                                       ▼
     madewithml.train                        madewithml.tune
 (Ray Train + TorchTrainer)                 (Ray Tune Search)
             │                                       │
             └───────────────────┬───────────────────┘
                                 │
                                 ▼
                        MLflow Model Registry
                                 │
             ┌───────────────────┴───────────────────┐
             │                                       │
             ▼                                       ▼
    madewithml.evaluate                     madewithml.serve
 (Slice-based Performance)               (FastAPI + Ray Serve)
```

---

## 📚 Core Modules Reference

- **[Data Pipeline (`data.md`)](madewithml/data.md)**: Ray Dataset loading, stratified train/test splitting, cleaning text, and BERT tokenization.
- **[Model Architecture (`models.md`)](madewithml/models.md)**: PyTorch BERT fine-tuning classification head with custom dropout and feedforward layers.
- **[Distributed Training (`train.md`)](madewithml/train.md)**: Multi-worker distributed training using Ray Train, TorchTrainer, and MLflow experiment logging.
- **[Hyperparameter Tuning (`tune.md`)](madewithml/tune.md)**: Distributed tuning with Ray Tune, search spaces, and ASHA early stopping schedulers.
- **[Evaluation & Diagnostics (`evaluate.md`)](madewithml/evaluate.md)**: Precision, Recall, F1, confusion matrices, and granular slice-based evaluations.
- **[Batch Prediction (`predict.md`)](madewithml/predict.md)**: High-throughput batch inference pipeline for offline scoring.
- **[Real-Time Serving (`serve.md`)](madewithml/serve.md)**: Production REST API deployment with FastAPI and Ray Serve.
- **[Utilities (`utils.md`)](madewithml/utils.md)**: Reproducible random seeding, JSON artifact persistence, and helper utilities.
