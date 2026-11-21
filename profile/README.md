# AutomaticTrading AI

**AI-powered trading research, strategy engineering, optimization, and reproducible backtesting.**

AutomaticTrading is building a research-first engineering ecosystem for systematic trading strategies. Our focus is on **experiment quality, reproducibility, risk controls, and evidence-based validation**—not promises of profits.

## Vision

Build an integrated research workflow connecting AI-assisted strategy discovery, historical market-data analysis, parameter optimization, simulation, and auditable experiment records.

## Planned architecture

```text
                     AgentTrader / OpenClaw
                              |
                      Research Orchestrator
                              |
          +-------------------+-------------------+
          |                   |                   |
      RD-Agent              Qlib               Optuna
    Research ideas      Quant research      Parameter search
          |                   |                   |
          +-------------------+-------------------+
                              |
                    Strategy Specification
                              |
                NautilusTrader / MT5 Lab
                     Backtesting only
                              |
                    Experiment Registry
                         PostgreSQL
                              |
                   Research Knowledge Layer
               Existing RAG (read-only access)
```

## Technology roadmap

| Component | Intended role |
| --- | --- |
| **OpenClaw / AgentTrader** | Agent orchestration and research workflow |
| **RD-Agent** | AI-assisted research and strategy exploration |
| **Microsoft Qlib** | Quantitative research and datasets |
| **NautilusTrader** | Event-driven strategy simulation and validation |
| **Optuna** | Reproducible hyperparameter optimization |
| **PostgreSQL** | Experiment metadata, metrics, and provenance |
| **MT5 Strategy Lab** | Linux-based experimental strategy testing |
| **RAG / knowledge retrieval** | Reuse and compare research evidence |

These are **planned or evaluated integrations**. Listing a component does not mean it is deployed or production-ready.

## Engineering principles

- **Research only:** No live trading or order execution is authorized in the initial phases.
- **Read-only infrastructure audit first:** Inspect before installing or changing existing services.
- **Protect existing knowledge:** Preserve the current ChromaDB/RAG records, vectors, collections, metadata and backups. No destructive changes or migration without explicit authorization.
- **Reproducible experiments:** Record strategy versions, datasets, assumptions, fees, slippage and evaluation results.
- **Robust validation:** Out-of-sample evaluation and walk-forward tests before interpreting a result.
- **Scoped changes:** Keep research environments isolated from operational infrastructure.

## Project status

**Architecture and integration planning.** Repositories, integrations, and deployment status will be documented as they are individually verified.

## Links

- [AutomaticTrading GitHub organization](https://github.com/AutomaticTrading)

---

*Research software only. Nothing here constitutes investment advice or a claim of trading performance.*
