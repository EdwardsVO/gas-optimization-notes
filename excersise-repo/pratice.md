# Gas Puzzles
1. Clone this repo: https://github.com/RareSkills/gas-puzzles

2. Install with npm install

2. Optimize the contracts in the contracts folder by creating a folder inside with the path contracts/optimized_contracts/

3. Copy the contracts into the new folder

4. Prefix the contract names in the new folder with 'Optimized' e.g. contract ArraySum becomes OptimizedArraySum

5. Optimize the code until the test passes. To run the test do npx hardhat test tests/<contract_name>