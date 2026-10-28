# Strategem

**Strategem** is an open-source trading-bot framework for building, backtesting, and running transparent, rule-based trading strategies.

It is designed for developers and independent traders who want reproducible strategy logic, clear risk controls, and full visibility into how trades are selected and executed.

> **Disclaimer:** Strategem is a development and research tool, not financial advice. Trading involves substantial risk. Past performance does not guarantee future results. Always test strategies thoroughly and use appropriate risk controls.

## Features

- Modular strategy definitions
- Historical backtesting with configurable parameters
- Clear separation between signals, risk rules, and execution
- Support for paper trading before live deployment
- Structured logging for every decision and order event
- Exchange/API integration layer
- Example strategies and configuration templates
- Designed for community contributions and extensions

## Why Strategem?

Many trading tools are either black-box systems or difficult to customize. Strategem aims to make every part of the trading workflow explicit:

- What signal triggered a trade?
- What risk rules allowed or blocked it?
- What order was sent, when, and why?
- How would the same strategy have performed historically?

The goal is not to promise profits, but to provide a transparent foundation for researching and automating strategies responsibly.

## Project status

Strategem is in early development. APIs, configuration formats, and features may change.

Planned milestones:

- [ ] Core strategy interface
- [ ] Historical data loading
- [ ] Backtesting engine
- [ ] Risk-management module
- [ ] Paper-trading mode
- [ ] Exchange integrations
- [ ] Example strategies
- [ ] Documentation and contributor guide

## Installation

```bash
git clone [https://github.com/your-username/strategem.git](https://github.com/your-username/strategem.git)
cd strategem
pip install -r requirements.txt
```

## Quick start

```python
from strategem import Strategy, Backtester

class SimpleMovingAverageStrategy(Strategy):
    def generate_signals(self, data):
        # Example placeholder: define your entry and exit rules here
        pass

backtester = Backtester(
    strategy=SimpleMovingAverageStrategy(),
    initial_capital=10_000,
)

results = backtester.run(data)
print(results.summary())
```

## Risk controls

Strategem is intended to make risk management a first-class part of strategy development.

Planned controls include:

- Maximum position size
- Daily loss limits
- Stop-loss and take-profit rules
- Maximum open positions
- Trading-session restrictions
- Paper-trading mode by default

## Contributing

Contributions are welcome.

1. Fork the repository
2. Create a feature branch
3. Add tests for new behavior
4. Submit a pull request

Before contributing, please open an issue to discuss major changes.

## License

This project is licensed under the [MIT License](LICENSE).
