# Training readiness

AURE is the intended model family for an independent candlestick-only strategy. The exact checkpoint has not been selected, and no training has started.

## Decisions before training

1. Select the AURE checkpoint and verify its identity, license, compatibility, and local availability.
2. Establish the applicable rights to use any source material in training.
3. Define the task: inputs, expected outputs, candlestick concepts, and the distinction between explaining book concepts and making market decisions.
4. Prepare a reviewed dataset with provenance and a separate held-out evaluation set. Do not publish book text or private data here.
5. Verify a feasible training method and compute budget, with all new artifacts isolated from the original model.
6. Record reproducible settings and evaluate the new version independently before considering any deployment.

Understanding instructional material does not establish trading profitability. Trading evaluation will require its own market data, time boundaries, costs, and leakage controls. No historical data period has been specified.

## Current boundaries

No model weights, private model inventories, internal infrastructure details, training datasets, or original strategy code are included. This repository does not implement a combined strategy, RAG system, or live trading integration.
