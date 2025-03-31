# 🖼️ Solana NFT Creator

This project provides a minimal example of creating an NFT collection and minting an NFT that belongs to that collection on **Solana Devnet** using the Metaplex Umi SDK and Token Metadata program.

## 📁 Files

- `create-collection.ts` — creates a collection NFT.
- `create-nft.ts` — creates an individual NFT and assigns it to the previously created collection.

---

## 🚀 Getting Started

### 1. Clone the Repo

```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Prerequisites

- Node.js v18+
- A Solana wallet keypair file (`~/.config/solana/id.json` or any custom path)
- Devnet SOL (automatically airdropped)

---

## 📦 Creating a Collection

Run the script to create a collection NFT:

```bash
ts-node create-collection.ts
```

This will:

- Load your keypair
- Airdrop SOL if needed
- Initialize Umi and Token Metadata
- Create a collection NFT
- Output the collection address (save this!)

---

## 🖼️ Creating an NFT in the Collection

Update the `collectionAddress` in `create-nft.ts`:

```ts
const collectionAddress = publicKey(
  "PASTE_YOUR_COLLECTION_ADDRESS_HERE"
);
```

Then run:

```bash
ts-node create-nft.ts
```

This will:

- Load your keypair
- Airdrop SOL if needed
- Create an individual NFT
- Assign it to the collection
- Print the NFT address and Solana Explorer link

---

## 🧪 Example Output

```
Loaded user 8zX...pJ3
Set up Umi instance for user
Created Collection 📦! Address is https://explorer.solana.com/address/...
```

```
Creating NFT...
🖼️ Created NFT! Address is https://explorer.solana.com/address/...
```

---

## 🌐 Off-chain Metadata

- Collection metadata: [`nft-collection-offchain-data.json`](https://raw.githubusercontent.com/0xdmtry/sol-nft/refs/heads/main/nft-collection-offchain-data.json)
- NFT metadata: [`nft-offchain-data.json`](https://raw.githubusercontent.com/0xdmtry/sol-nft/refs/heads/main/nft-offchain-data.json)

---

## 🧰 Tools & Libraries

- [Metaplex Umi SDK](https://docs.metaplex.com/umi/)
- [Solana Web3.js](https://github.com/solana-labs/solana-web3.js)
- [@solana-developers/helpers](https://github.com/solana-developers/helpers)
