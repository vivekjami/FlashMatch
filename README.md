# ⚡ FlashMatch

**FlashMatch** is a high-performance, fully onchain Central Limit Order Book (CLOB) built on the **Solana blockchain** with **MagicBlock** integration. It combines the speed of centralized exchanges (CEXs) with the security and transparency of decentralized finance (DeFi), enabling high-frequency trading with sub-50ms latency.

FlashMatch leverages ephemeral rollups, an onchain matching engine, and a responsive UI to deliver a seamless trading experience for assets like SOL/USDC and BTC/USDC.

---

## ✨ Features

- ⚡ **Sub-50ms Trade Execution**  
  Ultra-low latency achieved through MagicBlock’s ephemeral rollups for high-frequency trading.  
- 🛠️ **Onchain Matching Engine**  
  Decentralized order matching implemented as a Solana program for transparency and auditability.  
- 📊 **Real-Time UI**  
  Responsive frontend with live order book updates and market data streams.  
- 💱 **Multi-Asset Support**  
  Trade popular pairs such as `SOL/USDC`, `BTC/USDC`, and more, with easy configuration for additional pairs.  
- 🔒 **Secure & Decentralized**  
  All trades are settled onchain, ensuring cryptographic verifiability and user custody of funds.

---

## 📂 Project Structure

```
FlashMatch/
├── programs/                # Solana smart contracts for the CLOB
│   └── clob_engine/         # Rust-based matching engine logic
├── frontend/                # React-based trading UI with WebSocket integration
├── rollups/                 # Ephemeral rollup service for offchain processing
├── indexer/                 # Real-time event indexer for state synchronization
├── tests/                   # Integration and unit tests
└── README.md                # Project documentation
```

---

## 🛠️ Tech Stack

- **Blockchain**: Solana  
- **Rollups**: MagicBlock Ephemeral Rollups  
- **Frontend**: React, TypeScript, TailwindCSS, WebSockets  
- **Backend**: Node.js, Express (for rollup and indexer services)  
- **Smart Contracts**: Rust, Anchor Framework (Solana Program Library)  

---

## 🔍 How It Works

1. **Order Submission**: Traders place orders (buy/sell) through the frontend UI.  
2. **Rollup Processing**: Orders are batched and validated offchain by the ephemeral rollup engine.  
3. **Onchain Matching**: Valid orders are relayed to the Solana CLOB smart contract for matching and settlement.  
4. **Real-Time Updates**: Trade executions, cancellations, and order book updates are streamed to the UI via WebSockets.  
5. **Settlement**: All trades are finalized onchain, ensuring transparency and security.

---

## 🚀 Getting Started

### Prerequisites

- [Solana CLI](https://docs.solana.com/cli/install-solana-cli-tools) (v1.18.4 or higher)  
- [Anchor Framework](https://www.anchor-lang.com/docs/installation) (v0.29.0 or higher)  
- [Node.js](https://nodejs.org/) (v18 or higher)  
- [Yarn](https://yarnpkg.com/) (v1.22 or higher) or npm  
- [Rust](https://www.rust-lang.org/tools/install) (v1.77 or higher)  

### Installation

1. **Clone the Repository**  
   ```bash
   git clone https://github.com/your-org/FlashMatch.git
   cd FlashMatch
   ```

2. **Install Dependencies**  
   Ensure all subdirectories have their dependencies installed.

### Steps to Run

#### 1. Build and Deploy the Smart Contract
```bash
cd programs/clob_engine
anchor build
anchor deploy --provider.cluster devnet
```

#### 2. Start the Rollup Engine
```bash
cd rollups
yarn install
yarn start
```

#### 3. Start the Indexer
```bash
cd indexer
yarn install
yarn start
```

#### 4. Launch the Frontend
```bash
cd frontend
yarn install
yarn dev
```
The frontend will be available at `http://localhost:3000`.

---

## 📈 Supported Trading Pairs

- `SOL/USDC`  
- `BTC/USDC`  
- `ETH/USDC`  

To add more pairs, update the `market-config.json` file in the `frontend` directory.

---

## 🤝 Contributing

Contributions are welcome! Please read our [CONTRIBUTING.md](CONTRIBUTING.md) for details on how to submit pull requests, report issues, or suggest features.

---

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 🙌 Acknowledgements

- [MagicBlock](https://magicblock.xyz) for ephemeral rollup infrastructure  
- [Solana Labs](https://solana.com) for high-performance blockchain technology  
- [Anchor Framework](https://www.anchor-lang.com) for streamlined Solana smart contract development  

---

## 📧 Contact

For inquiries, reach out to `dev@flashmatch.xyz` or open an issue on GitHub.
