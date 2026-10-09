# Training readiness

AURE is the selected model family for an independent candlestick-only strategy. An initial local checkpoint was selected and fingerprinted, and a text-only LoRA training run completed. See the [training report](training-run-2026-10-09.md). Exact private checkpoint locations remain outside the public repository.

## Requirements for further development

1. Preserve the selected checkpoint identity and separate adapter; verify model lineage and applicable licensing before distributing derivatives.
2. Establish the applicable rights to use any source material in training.
3. Define the task: inputs, expected outputs, candlestick concepts, and the distinction between explaining book concepts and making market decisions.
4. Prepare a reviewed dataset with provenance and a separate held-out evaluation set. Do not publish book text or private data here.
5. Verify a feasible training method and compute budget, with all new artifacts isolated from the original model.
6. Record reproducible settings and evaluate the new version independently before considering any deployment.

Understanding instructional material does not establish trading profitability. Trading evaluation will require its own market data, time boundaries, costs, and leakage controls. No historical data period has been specified.

## Current boundaries

No model weights, private model inventories, internal infrastructure details, training datasets, or original strategy code are included. This repository does not implement a combined strategy, RAG system, or live trading integration.
