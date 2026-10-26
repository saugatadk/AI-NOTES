# Model Architecture (`madewithml.models`)

The `models` module encapsulates the neural network architectures used for classification tasks.

---

## 🧠 Architectures

### `class FinetunedLLM(nn.Module)`

```python
class FinetunedLLM(nn.Module):
    def __init__(self, llm_flag: str, num_classes: int, dropout_p: float = 0.5):
        ...
```

A transfer-learning architecture that attaches a fine-tuning classification head onto a pretrained transformer backbone.

#### Components:
1. **Transformer Backbone**:
   - Pretrained Hugging Face transformer (e.g., `allenai/scibert_scivocab_uncased` or standard BERT).
   - Extracts contextual embeddings from the `[CLS]` token position.
2. **Dropout Regularization**:
   - Configurable dropout probability (`dropout_p`) applied to token representations before classification.
3. **Classification Head**:
   - Linear projection layer mapping hidden dimension size (`hidden_size`) to the target number of output classes (`num_classes`).

#### Forward Pass:
```python
def forward(self, batch: Dict[str, torch.Tensor]) -> torch.Tensor
```
Takes a dictionary containing `input_ids` and `attention_mask` tensors, executes the transformer forward pass, and returns raw prediction logits.
