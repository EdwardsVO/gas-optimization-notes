# Variables
## Changing a Non-Zero variable to Non-Zero value 
### Why 5000 gas 
Cost of cold storage access 2100 gas + Cost for STORE operation 2900 = 5000

## Smaller Integers ?
An space of 32 byte slot will be save for any variable type. It will always cost 20.000 gas setting a non-zero variable from zero. Ethereum treats variables as 32 bytes.

## Refunds 
Setting Non-Zero variable to Zero will refund some gas (I kind of incentive from the EVM for saving storage). It will happen only if the transaction requires 30.000 gas or more.
- With Berlin EVM it could be save till 15000 gas 
- London EVM update araises and now it could be save till 4800 gas
Setting many variables to zero can be really expensive since London update. 20% rule
##  Tips
- Using smaller integers sizes will not save storage gas.
- Deleting an array can be expensive (setting to zero variables)
- Setting to zero can cost between 200 and 5000 gas.
- For every zero operation try to spend 24000 gas
- Counting down is more efficient than counting up