# Initial AURE Candlestick Bible training run

Completed October 9, 2026. This was actual continued language-model training, producing a separate experimental LoRA adapter. The original base files were verified unchanged by SHA-256 checks. No model weights, training text, or private checkpoint locations are published here.

## Method

- Existing local AURE causal-language-model checkpoint, loaded in 4-bit form.
- Rank-8 LoRA on query/value projections in the final four layers; 524,288 trainable parameters.
- One fixed pass: 117 optimizer steps, batch size 1, learning rate 0.00005, maximum sequence length 512, seed 20261009.
- Text extracted from the book, with repeated headers and page numbers removed. Pages 11-166 were considered; three pages with fewer than 25 extracted words were excluded.
- Six-page groups assigned to disjoint training, validation, and test sets before chunking; no overlapping chunks or exact duplicate text examples across splits.
- 117 training examples containing 17,018 tokens including end markers; 18 validation examples and 18 test examples.
- Test results were not used to choose settings or select a checkpoint. The final adapter from the fixed run was reloaded before evaluation.

## Measured results

Lower values mean better next-token prediction on the reserved book text.

| Measure | Original base | Base with trained adapter |
|---|---:|---:|
| Test loss | 2.631679 | 2.209259 |
| Test perplexity | 13.897078 | 9.108962 |
| Validation loss | 2.768234 | 2.298758 |
| Validation perplexity | 15.930469 | 9.961803 |

Test loss decreased by approximately 16.1%. This is not a question-answer accuracy score, a profitability result, or an external benchmark.

The saved adapter reloaded successfully. Its 16 tensors were finite, and learned update tensors were nonzero. The final adapter is approximately 2.10 MB. All ten original checkpoint files matched their pre-training fingerprints.

## Limitations and status

This first run learned from extracted text only. Chart images were not used. A small holdout from the same book shares terminology and concepts with the training set, and the original checkpoint's pretraining membership is unknown. These results do not demonstrate performance on new market data or reliable trading decisions.

Short concept probes were not formally scored and some exhausted a 256-token generation allowance while reasoning. A follow-up comparison question with a larger 1,200-token allowance still omitted the hanging-man half of a hammer-versus-hanging-man comparison. Answer completeness therefore remains a known issue; the adapter is experimental. Book statements were not independently fact-checked or corrected by this training run.

Source training and redistribution rights remain unverified. The book, extracted text, datasets, and adapter remain local and excluded from Git. The original trading system was not modified, and the future combined strategy was not implemented. No deployment or live trading changes occurred.
