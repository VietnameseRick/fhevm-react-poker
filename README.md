# FHE Poker 🎰

**Privacy-first blockchain poker powered by Fully Homomorphic Encryption (FHE)**

Play Texas Hold'em with truly private cards. No one—not even the blockchain—can see your cards until showdown. Built with Zama's fhEVM technology for provably fair gameplay with complete privacy.

🎮 **[Play Demo](https://ghub.bet)** | 📖 **[Documentation](./packages/fhevm-poker/README.md)** | 💬 **[Discord](https://discord.com/invite/zama)**

## ✨ Features

- 🔐 **Fully Private Cards** - Cards remain encrypted on-chain until showdown
- 🎲 **Provably Fair** - FHE-powered shuffle ensures unpredictable, verifiable randomness
- ⚡ **Real-time Gameplay** - Smooth, responsive poker experience
- 💰 **Multi-player Tables** - Up to 10 players per table
- 🎨 **Cyberpunk UI** - Beautiful, modern interface with smooth animations
- 🔗 **Blockchain-Native** - All game logic runs on-chain with FHE smart contracts

## 🛠️ Technology Stack

- **Smart Contracts**: Solidity + Zama's fhEVM
- **Frontend**: Next.js 15 + React 19
- **Styling**: TailwindCSS + Custom Animations
- **Encryption**: Fully Homomorphic Encryption (FHE)
- **Wallet**: Privy + WalletConnect
- **State Management**: Zustand

## 📋 Prerequisites

- **Node.js**: Version 20 or higher
- **npm**: Version 7.0.0 or higher
- **Wallet**: MetaMask, WalletConnect, or any EIP-6963 compatible wallet

## Local Hardhat Network (to add in MetaMask)

Follow the step-by-step guide in the [Hardhat + MetaMask](https://docs.metamask.io/wallet/how-to/run-devnet/) documentation to set up your local devnet using Hardhat and MetaMask.

- Name: Hardhat
- RPC URL: http://127.0.0.1:8545
- Chain ID: 31337
- Currency symbol: ETH

## 🚀 Quick Start

### 1. Install Dependencies

```bash
# Clone the repository
git clone https://github.com/yourusername/fhe-poker.git
cd fhe-poker

# Install dependencies
npm install
```

### 2. Setup Environment Variables

```bash
# Set up Hardhat mnemonic for local development
npx hardhat vars set MNEMONIC

# (Optional) Set Infura API key for testnet deployment
npx hardhat vars set INFURA_API_KEY

# (Optional) Set Etherscan API key for contract verification
npx hardhat vars set ETHERSCAN_API_KEY
```

### 3. Run Locally (Mock Mode)

```bash
# Terminal 1: Start local Hardhat node
npm run hardhat-node

# Terminal 2: Deploy contracts and start frontend
npm run dev:mock
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### 4. Configure MetaMask for Local Network

1. Open MetaMask extension
2. Add network manually:
   - **Network Name**: Hardhat Local
   - **RPC URL**: http://127.0.0.1:8545
   - **Chain ID**: 31337
   - **Currency**: ETH

## 🌐 Deploy to Sepolia Testnet

```bash
# Deploy contracts
npm run deploy:sepolia

# Run frontend pointing to Sepolia
npm run dev

# Visit http://localhost:3000 and connect to Sepolia in MetaMask
```

## 📁 Project Structure

```
fhevm-gameplay/
├── packages/
│   ├── fhevm-poker/          # Smart contracts & Hardhat
│   │   ├── contracts/        # Solidity contracts (FHEPoker.sol)
│   │   ├── tasks/            # Hardhat tasks for testing
│   │   ├── deploy/           # Deployment scripts
│   │   ├── LICENSE-BSL       # Business Source License
│   │   └── README.md
│   │
│   └── site/                 # Next.js frontend
│       ├── app/              # Next.js 15 app directory
│       ├── components/       # React components
│       ├── hooks/            # Custom React hooks
│       ├── stores/           # Zustand state management
│       ├── abi/              # Contract ABIs
│       ├── LICENSE-BSL       # Business Source License
│       └── README.md
│
├── scripts/                  # Build & deployment scripts
└── README.md                 # This file
```

## 🎮 How to Play

1. **Create/Join Table**: Connect wallet and join an existing table or create a new one
2. **Buy-In**: Add chips to your stack (minimum buy-in set per table)
3. **Play Poker**: Standard Texas Hold'em rules apply
4. **Private Cards**: Your cards are encrypted—only you can decrypt and see them
5. **Showdown**: At showdown, cards are revealed via FHE decryption
6. **Winner Determined**: Smart contract evaluates hands and awards pot automatically

## 📚 Documentation

- **[Smart Contract Documentation](./packages/fhevm-poker/README.md)** - Contract details & Hardhat tasks
- **[Frontend Documentation](./packages/site/README.md)** - React components & hooks
- **[FHEVM Documentation](https://docs.zama.ai/protocol/)** - Learn about FHE technology
- **[Zama Discord](https://discord.com/invite/zama)** - Join the community

## 🧪 Testing

```bash
# Run smart contract tests
npm run test

# Run frontend tests
npm run test:site

# Generate coverage report
npm run coverage
```

## 🔧 Available Commands

| Command | Description |
|---------|-------------|
| `npm run hardhat-node` | Start local Hardhat node |
| `npm run dev:mock` | Run frontend in mock mode |
| `npm run deploy:sepolia` | Deploy to Sepolia testnet |
| `npm run test` | Run all tests |
| `npm run compile` | Compile smart contracts |

## 📄 License

This project uses a **dual license** structure:

### FHE Poker Implementation (Your Code)
- **License**: Business Source License 1.1 (BSL 1.1)
- **Licensor**: 0xDRick (Tra Anh Khoi)
- **Change Date**: 2029-01-01 (converts to MIT License)
- **Commercial Use**: Requires separate licensing before change date
- **Non-Commercial Use**: Free for development, testing, research, personal projects

See [LICENSE-BSL](./packages/fhevm-poker/LICENSE-BSL) for complete terms.

### Zama fhEVM Technology
- **License**: BSD 3-Clause Clear License
- **Copyright**: (c) 2025 Zama

See [LICENSE](./LICENSE) for complete terms.

### Commercial Licensing
For commercial licensing inquiries before the change date:
- **Email**: rick@thekey.studio
- **Licensor**: 0xDRick (Tra Anh Khoi)

For Zama fhEVM licensing:
- **Website**: https://www.zama.ai/contact

## 🤝 Contributing

Contributions are welcome! By contributing, you agree that your contributions will be licensed under the Business Source License 1.1.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 👨‍💻 Author

**0xDRick** (Tra Anh Khoi)
- Email: rick@thekey.studio
- GitHub: [@vietnameserick](https://github.com/vietnameserick)

## 🙏 Acknowledgments

- **Zama** for the groundbreaking fhEVM technology
- **Uniswap** for pioneering the BSL 1.1 license structure
- The FHE and blockchain communities

---

**Built with ❤️ using Zama's fhEVM**
