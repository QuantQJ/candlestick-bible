# Candlestick Bible

Independent candlestick-only strategy research and preparation for training an AURE-based model using concepts from *The Candlestick Trading Bible*.

## Project status

This project is at the documentation and planning stage. AURE is the intended model family; the exact checkpoint and training configuration remain pending. No model has been trained here, and no strategy implementation, backtest, or deployment has been completed. No trading-performance claims are made.

## Scope

- Develop and evaluate an independent candlestick-only strategy.
- Preserve the existing original trading system without changing its models, strategies, configuration, or trading state.
- Reserve any combination of original and candlestick strategies for a third, separate future version.
- Choose the training approach after confirming the model, data, and evaluation requirements. No RAG architecture is assumed.

## Source and data

[Source provenance](docs/source-provenance.json) records the source URL, verified 168-page count, and file fingerprint. The PDF, extracted book text, datasets, and model weights are excluded from this repository. Source authorship and training/redistribution rights remain unverified. Public availability alone does not establish those rights.

See [training readiness](docs/training-discovery.md) for the remaining decisions. Paid compute, live trading changes, and publication of source data require separate authorization.

## Collaborating

Start with [CONTRIBUTING.md](CONTRIBUTING.md). You can read this public repository and propose documentation changes or evaluation ideas through issues and pull requests. There is no runnable training application yet.

Public visibility does not automatically connect this repository to ChatGPT or grant write access. Each collaborator must configure their own supported GitHub connection and permissions.
