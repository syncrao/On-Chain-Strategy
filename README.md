
# On-Chain Strategy Trading Bot 🤖📈

A high-performance on-chain trading bot that executes buy and sell decisions based on predefined strategies by directly interacting with decentralized exchanges.

---

## 🧠 What This Project Does

This project implements an automated **strategy-based trading system** that:

- Monitors on-chain prices
- Applies technical trading strategies
- Executes swaps directly on DEX smart contracts
- Runs fully non-custodial using your wallet

---

## 🏗 High-Level Architecture

```

Blockchain RPC
↓
Rust Strategy Bot
├─ Price Reader
├─ Strategy Engine
├─ Risk Manager
└─ Trade Executor
↓
On-chain DEX (Uniswap / etc.)
↓
Rust API (optional)
↓
Web Dashboard / Mobile App

```

---

## 🛠 Tech Stack

### Core Bot
- Rust
- ethers-rs
- Public RPC providers

### Trading
- DEX: Uniswap V3 (initial)
- Price source: On-chain pool data
- Execution: Direct smart contract calls

### Backend (Optional)
- Rust + Axum

### Frontend
- Next.js + TypeScript
- React Native + Expo

---

## 📦 Repository Structure

```

strategy-trading-bot/
│
├── bot/                    # Rust trading bot
│   ├── src/
│   │   ├── main.rs
│   │   ├── config.rs
│   │   ├── rpc.rs
│   │   ├── price/
│   │   │   └── uniswap.rs
│   │   ├── strategy/
│   │   │   ├── rsi.rs
│   │   │   ├── ema.rs
│   │   │   └── mod.rs
│   │   ├── risk/
│   │   │   └── risk_manager.rs
│   │   └── executor.rs
│   └── Cargo.toml
│
├── backend/                # Rust API (Axum)
│   └── src/main.rs
│
├── web/                    # Next.js web dashboard
│
├── mobile/                 # React Native mobile app
│
├── docs/
│   └── architecture.md
│
├── .env.example
├── README.md
└── LICENSE

```

---

## 📊 Example Trading Strategies

- RSI overbought / oversold
- EMA crossover
- Trend-following
- Mean reversion
- Time-based DCA

Example logic:

```

If RSI(14) < 30 → Buy
If RSI(14) > 70 → Sell

```

---

## 🔐 Why Rust?

- High-performance execution
- Safe concurrency
- Deterministic behavior for trading systems

---

## 🚧 Roadmap

- [ ] Read on-chain price from Uniswap V3
- [ ] Execute basic token swap
- [ ] Implement RSI strategy
- [ ] Implement EMA crossover strategy
- [ ] Risk management (position sizing, stop-loss)
- [ ] Paper trading mode
- [ ] Web dashboard
- [ ] Mobile notifications
- [ ] Dockerization (later)
- [ ] Multi-chain support (later)

---

## ⚠ Risk Disclaimer

This software is for educational and research purposes only.  
Cryptocurrency trading involves financial risk.  
Use at your own responsibility.

---

## 📜 License

MIT
```
