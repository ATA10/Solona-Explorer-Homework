# Create Project Folder: 
npm init -y

# Install Dependencies:
npm install @types/node typescript @solana/web3.js @project-serum/anchor
npm install --save-dev ts-node

# Initialize TypeScript Configuration:
npx tsc --init --rootDir ./ --outDir ./dist --esModuleInterop --lib ES2020 --module commonjs --resolveJsonModule true --noImplicitAny true

# Add Script Command in package.json:
"scripts": {
    "call_program": "ts-node ./call_program.ts"
}

# wallet.json:
Place your wallet's secret key in integer array format inside this file.

# Running the Project
Ensure your wallet has sufficient funds by using a Solana devnet faucet.

Run the project:
npm run call_program
