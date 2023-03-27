# Overview of Gas Cost 
Gas is an unit of computation in the EVM that describe the fee to conduct a transaction based on its complexity. 
The minimum gas amount that cost a simple transaction inside Ethereum is `21.000 gas` that is the amount sended when transfering Ether to an account.

## Block limits 
- Bitcoin has limited the block size to 1MB 
- Ethereum limits the amount of computations per block, the gas, each computation has a gas cost 
- The Block Limit is `30 Million Gas` == `1.428` simple transfers 
- Ethereum has an average of 13 transations per second.

## Storage Slots 
The location where a variable of any type lives, those slots are fixed with the position of the variables. Slot 0 will be the first variable, slot 1 the second, slot 2 the third and continue.  

## Opcodes 
When solidity code it's compiled the compiler outputs the assembly that will be processed by the EVM 

## Function Selector 
Functions names are stored in the opcodes as the first four bytes of the hash keccak256, names of the arguments aren't stored. 
`"ed18f0a7": "blue()"` 
These bytes will be the function selector of a specific function inside the compiler output.

## Payable functions 
Payable functions has less opcodes than the non-payable, the non-payable has more opcodes for transaction value verification.

## Unchecked Arithmetic
`Solidity 0.8` solve the overflow and underflow vulnerabilities with variables, that was solved adding more opcodes in the solidirty compiler to check if there was and under/overflow in the function output making arithmetic operations more expensive.

## Solidity Optimizer 
It is a tool that helps with the contract optimization in two ways: 

1. Reducing the size of contract deployment 
2. Reducing the gas cost when calling functions 

It exist a tradeoff parameter between code size and code execution cost 

- A parameter of "1" will produce short but expensive code 
- A longer parameter will produce longer but gas efficient code 

## Tips
- Use `unchecked {}` block when the logic doesn't need the flow validation, for example when the smart contract it's wotking with counters
- Use longer optimizer parameters to reduce the execution cost of the smart contract for the final users


