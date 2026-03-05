# Spore Burner 🔥

**Melt Spore DOBs on Nervos CKB and reclaim locked capacity.**

→ **Live demo:** https://toastmanau.github.io/spore-burner

## What it does

Spore DOBs lock CKB capacity inside the cell. When you no longer want a DOB, you can **melt** it — permanently destroying the NFT and returning the locked CKB to your wallet.

No CLI, no Node.js, no setup. Runs entirely in your browser.

## Features

- 🔥 Burn one or many DOBs in a single session
- ✅ Works on both **mainnet** and **testnet**
- 👛 Connects via **JoyID** (passkey wallet)
- 📋 Shows each DOB's ID and locked CKB amount
- 🔒 Confirm dialog before any irreversible action
- 🌐 No backend — pure browser app using CCC

## Usage

1. Open `index.html` (or use the live GitHub Pages link above)
2. Select **Mainnet** or **Testnet** in the top-right
3. Click **Connect JoyID**
4. Click **Load My DOBs**
5. Click the DOBs you want to burn (checkbox select)
6. Click **🔥 Burn Selected** → confirm → sign in JoyID
7. CKB lands back in your wallet

## Tech

- [`@ckb-ccc/core`](https://github.com/ckb-ecofund/ccc) — CKB client + transaction builder
- [`@ckb-ccc/spore`](https://github.com/ckb-ecofund/ccc) — `meltSpore()` implementation
- [`@ckb-ccc/connector`](https://github.com/ckb-ecofund/ccc) — JoyID wallet connector
- All loaded via [esm.sh](https://esm.sh) — zero build step required

## Deploy your own

This is a single HTML file with zero dependencies to install. Just serve `index.html` anywhere:

```bash
# GitHub Pages — fork the repo and enable Pages from Settings
# Or just open locally:
open index.html
```

## Security

- Your private key never leaves JoyID
- This page never sees your key — it only builds and submits transactions
- The `meltSpore` call is constructed client-side; you sign it in JoyID
- Verify the source code before use

## License

MIT
