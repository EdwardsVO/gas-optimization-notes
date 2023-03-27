# Solidity Tricks 
Optimizing the way the compiler processes the functions inside a solidity file.

## Function Names 
Adding functions inside a solidity file will increase the cost of call each function. To check what function was called inside the transaction data, the compiler will sort the functions selectors in hexadecimal order, then the data will be compared with each hexadecimal functions names consuming gas. So more functions more opcodes to run. 
- 22 gas per function added increasing in a linear way in hexadecimal order, being the most expensive the last function selector.

## Less than vs Less than or Equal to 
Strict inequalities only require one opcode.
- `< >` are always more efficient tham `<= >=`
- `<= >=` require two more opcodes for comparison 

## Bit Shifting
When multiplying or dividing what is really happening is bit shifting.
- Multipliying by two fill shift to the left
`5 = 00101`
`10 = 01010`
- Dividing by two will shift to the right 
`5 = 00101`
`2 = 00010`
- So dividing by two:
Solidity:  
`n*2 == n << 1`
`n/2 == n >> 1` 

## Reverting Early
Revert as early as possible will save a lot of gas, no storage will be touched 

## Short Circuiting 
Order inside a require statement, the first argument will be the first in executing
- `require( X || Y, "invalid)` In this example if the `X` true the sencond argument won't be executed because the final result will be true 
- `require( X && Y, "invalid")` Here both arguments need to be calculated to be true, but if the first arugment is false the final result will be false

## Precomputing 
Pure functions that not require logic as a simple `return 3 * 7` will hardcode the result inside the opcodes. Also work with address keccak256 will
hardcode too the result.
Sometimes this optimization cannot happen, because the solidity compiler doesn't recognize the operation, for exmaple using expresions to store a constant and then return the expresion plus 2. It is needed to find the cheapest way working with precomputation and pure functions 

## Tricks 
- Make sure that gas sensitive functions and its selector is near the top of the opcodes.
- While optimizing don't change function names, becouse the gas consuption could be modified by the functions selector order.
- Change the logic check from `>=` to `<`
- Inside require statements with `AND` or `OR` logic try to operate in a way that validations only consumes the cheapest of both argument.
- Try to work with precomputed functions
- Check if pure function returning constant was precomputed by the compiler. 

