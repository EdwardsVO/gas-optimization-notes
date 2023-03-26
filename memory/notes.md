# Memory 
## Memory vs Calldata
Memory could be mutated, calldata its readonly 
- Memory it's more expensive than call data 

## Memory explosition 
Quadratric growth associated to memory allocations as early the quadratic breach it's reached with big memory number.
- It only can be used 30 million gas per blockchain block
## Memory it's never cleared
 Soldity hasn't garbage collector, it is needed to be carefull how the memory it's allocated
## Tips 
- Use memory if the input need to be mutated, don't use call data becouse it will be more expensive saving the input value into a variable 
- Big memory allocations need to be separated thorugh many variables, to avoid memory explosion