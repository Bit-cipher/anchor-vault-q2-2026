# anchor-vault-q2-2026

A simple Solana smart contract built with Anchor that implements a secure on-chain vault using Program Derived Addresses (PDAs).

This project demonstrates how SOL can be securely deposited, managed, and withdrawn using program-controlled accounts on Solana.

---

## ✨ Features

The vault program allows users to:

- 🧱 **Initialize Vault**
  - Creates a PDA-based vault state account
  - Stores bump seeds and ownership metadata

- 💰 **Deposit SOL**
  - Transfers SOL from a user into the vault PDA
  - Controlled via CPI to the System Program

- 🔓 **Withdraw SOL**
  - Allows authorized withdrawal using PDA signing
  - Ensures only valid vault authority can withdraw funds

- 🧹 **Close Vault**
  - Closes the vault state account
  - Returns remaining SOL back to the user

---

## ⚙️ Tech Stack

- ⚓ Anchor Framework
- 🧠 Rust (Solana Programs)
- ⚡ Solana CLI `v3.1.15 (Agave)`
- 🧪 LiteSVM (fast local testing runtime)
- 📦 Node.js / Yarn

---

## 🧪 Testing Strategy

This project uses **LiteSVM** instead of `solana-test-validator` for fast and lightweight testing.

LiteSVM provides a minimal Solana runtime that enables:
- Faster test execution
- No need for full validator setup
- Easy program simulation

---

## ▶️ Running Tests

Run all tests using:

```bash
anchor test