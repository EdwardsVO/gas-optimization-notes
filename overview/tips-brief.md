## Tips 
- Use memory if the input need to be mutated, don't use call data becouse it will be more expensive saving the input value into a variable 
- Big memory allocations need to be separated thorugh many variables, to avoid memory explosion
- Use `unchecked {}` block when the logic doesn't need the flow validation, for example when the smart contract it's wotking with counters
- Use longer optimizer parameters to reduce the execution cost of the smart contract for the final users
- Doing storage read and then storage write costs similar to only doing a storage write
- Using smaller integers sizes will not save storage gas.
- Deleting an array can be expensive (setting to zero variables)
- Setting to zero can cost between 200 and 5000 gas.
- For every zero operation try to spend 24000 gas
- Counting down is more efficient than counting up
- Looping an array, it could save gas if the lenght it's accessed only once saving the lenght in a variable, so the SLOAD won't need to be call each time the loop check the lenght for iteration
- Make sure that gas sensitive functions and its selector is near the top of the opcodes.
- While optimizing don't change function names, becouse the gas consuption could be modified by the functions selector order.
- Change the logic check from `>=` to `<`
- Inside require statements with `AND` or `OR` logic try to operate in a way that validations only consumes the cheapest of both argument.
- Try to work with precomputed functions
- Check if pure function returning constant was precomputed by the compiler. 

