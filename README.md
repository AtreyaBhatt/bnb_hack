# How to Run the ProofNest Project Locally

## Prerequisites
- **Node.js** (v16 or higher) and **npm**
- **Dfinity SDK (DFX)**: [Install instructions](https://internetcomputer.org/docs/current/developer-docs/setup/install)
- **Git** (for cloning the repository)

---

## Steps

### 1. Clone the Repository
```bash
git clone <repository-url>
cd Proofnest-main
```

### 2. Start the Internet Computer Local Replica
```bash
dfx start --clean --background
```

### 3. Deploy Backend Canisters
```bash
cd proofnest
dfx deploy
```

### 4. Install Frontend Dependencies
```bash
cd src/proofnest_frontend
npm install
```

### 5. Start the Frontend Development Server
```bash
npm start
```
- The frontend will be available at [http://localhost:3000](http://localhost:3000).

---

## Notes

- **Authentication:**  
  Internet Identity works best on mainnet. For local development, you may need to deploy a local Internet Identity canister. See [Internet Identity local setup](https://github.com/dfinity/internet-identity#local-development).

- **Reset Local State:**  
  If you encounter issues, reset the replica:
  ```bash
  dfx stop
  dfx start --clean
  ```

- **Environment Variables:**  
  Ensure your `.env` files are configured for local development.

---

## Troubleshooting

- Check terminal and browser console for errors.
- Make sure all dependencies are installed.
- Ensure DFX is running before deploying or starting the frontend.

---

## Useful Links

- [Dfinity SDK Documentation](https://internetcomputer.org/docs/current/developer-docs/setup/install)
- [Internet Identity Local Setup](https://github.com/dfinity/internet-identity#local-development)
