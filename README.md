# Optimizing Gas Cost Notes 😎
Gas is an unit of computation in the EVM that describe the fee to conduct a transaction based on its complexity. 
## Notes
This notes was taken from the [Advanced Solidity: Understanding and Optimizing Gas Costs](https://www.udemy.com/course/advanced-solidity-understanding-and-optimizing-gas-costs) made by Jeffrey Scholz
## In this notes you will see 
1. Overview 
    - [Block Limits](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/overview/notes.md#storage-slots)
    - [Opcodes](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/overview/notes.md#opcodes)
    - [Function Selector](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/overview/notes.md#function-selector)
    - [Payable Functions](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/overview/notes.md#payable-functions)
    - [Unchecked Arithmetic](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/overview/notes.md#unchecked-arithmetic)
    - [Solidity Optimizer](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/overview/notes.md#solidity-optimizer)
    - [TIPS](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/overview/notes.md#tips)

2. Storage
    - [Storage Cost](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/storage/notes.md#storage-movements)
    - [Cold access](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/storage/notes.md#cold-access)
    - [Warm Access](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/storage/notes.md#warm-access)
    - [Variables](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/storage/variables.md#variables)
    - [Moving Variables](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/storage/variables.md#variables)
    - [Uint8 or Uint128](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/storage/variables.md#smaller-integers-)
    - [Refunds](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/storage/variables.md#refunds)
    - [Blockchain Files](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/storage/variables.md#refunds)
    - [TIPS](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/storage/variables.md#tips)

3. Memory
    - [Memory vs Calldata](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/memory/notes.md#memory-vs-calldata)
    - [Memory Explosion](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/memory/notes.md#memory-explosition)
    - [TIPS](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/memory/notes.md#tips)

4. Tricks
    - [Function Names](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/tricks/notes.md#function-names)
    - [Less Than vs Less than or Equal](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/tricks/notes.md#less-than-vs-less-than-or-equal-to)
    - [Bit Shifting](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/tricks/notes.md#bit-shifting)
    - [Shot Circuiting](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/tricks/notes.md#bit-shifting)
    - [Precomputing](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/tricks/notes.md#bit-shifting)
    - [TIPS](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/tricks/notes.md#tips)

5. Excersise
    - [Gas Puzzle](https://github.com/EdwardsVO/gas-optimization-notes/blob/main/excersise-repo/pratice.md#gas-puzzles)

