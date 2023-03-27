# Variables
### Changing a Non-Zero variable to Non-Zero value => Why 5000 gas 
Cost of cold storage access 2100 gas + Cost for STORE operation 2900 = 5000

## Smaller Integers ?
An space of 32 byte slot will be save for any variable type. It will always cost 20.000 gas setting a non-zero variable from zero. Ethereum treats variables as 32 bytes.

## Refunds 
Setting Non-Zero variable to Zero will refund some gas (I kind of incentive from the EVM for saving storage). It will happen only if the transaction requires 30.000 gas or more.
- With Berlin EVM it could be save till 15000 gas 
- London EVM update araises and now it could be save till 4800 gas
Setting many variables to zero can be really expensive since London update. 20% rule

## File on the blockchain
`1kb == 32 bytes == 32bytes * (22.100gas) == 707.200 gas` 
A bit expensive. Instead of uploading the complete element on the blockchain, it is recommended to upload the hash of the element or the ID.

## Structs and Strings
- Structs save every attribute in a 32 bytes memory slot costing 22100 per atributte. The attributes are trated as common variables.  
- Strings are save in a 32 bytes memory slot too, if the string reaches the 32 bytes it will be added another 32 slot to the string storage, making it more expensive. 
- Address take 20 bytes memory
- Bools take 1 byte of memory for true value and 0 for false, and these for example are packed in the slot of an address (20 bytes) 

## Variable packing 
When two variables are kept in a single 32 bytes slot.


##  Tips
- Doing storage read and then storage write costs similar to only doing a storage write
- Using smaller integers sizes will not save storage gas.
- Deleting an array can be expensive (setting to zero variables)
- Setting to zero can cost between 200 and 5000 gas.
- For every zero operation try to spend 24000 gas
- Counting down is more efficient than counting up
- Looping an array, it could save gas if the lenght it's accessed only once saving the lenght in a variable, so the SLOAD won't need to be call each time the loop check the lenght for iteration