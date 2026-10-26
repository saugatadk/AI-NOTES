# Real-Time Model Serving (`madewithml.serve`)

The `serve` module provides real-time online inference serving using Ray Serve integrated with a FastAPI REST application.

---

## 🚀 Architecture & Endpoints

### `class ModelDeployment`
Ray Serve deployment class decorated with `@serve.deployment` and `@serve.ingress(app)`:
- Loads the model checkpoint and preprocessor into worker memory upon replica initialization.
- Scales horizontally across CPU or GPU replicas based on traffic load.

### REST Endpoints

#### `GET /`
- **Purpose**: Liveness and health check endpoint.
- **Response**:
  ```json
  {
    "message": "OK",
    "status-code": 200,
    "data": {}
  }
  ```

#### `GET /performance`
- **Purpose**: Returns the latest evaluation metrics (F1 score, precision, recall) for the deployed checkpoint.

#### `POST /predict`
- **Purpose**: Real-time multi-class prediction endpoint.
- **Request Body**:
  ```json
  {
    "title": "Transfer Learning with Transformers",
    "description": "Using BERT representations for downstream text classification tasks."
  }
  ```
- **Response**:
  ```json
  {
    "prediction": "natural-language-processing",
    "probabilities": {
      "computer-vision": 0.02,
      "natural-language-processing": 0.94,
      "mlops": 0.04
    }
  }
  ```
