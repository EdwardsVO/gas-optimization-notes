
# Overview
## Storage movements

- Setting storage to - to non-zero value cost 20.000 gas 
- Setting storage to non-zero to non-zero value cost 5.000 gas 
- Setting to non-zero to 0 refund the gas 
- First time accesing a variable will cost 2.100 gas, for cold storage fee 

###  Cold access 
First time acccessing a variable 
- 2100 gas
### Warm access
Access a variable already accessed
- 100 gas

### Example 
#### Read + Write
2100(Read + Cold Access) + 20100(Write + Warm Access) = 22200 gas
#### Writw without read 
22100(Write + Cold Access) = 22100 gas
