# Labs 1 gates
## Part 1: link to repository
     https://github.com/xsocha00/Digital-electronics-1
     
## Part 2: Verification of De Morgan's laws of function f(c,b,a)

####  Table:
| **c** | **b** |**a** | **f(c,b,a)** | **f(c,b,a)nand** | **f(c,b,a)nor** | 
| :-: | :-: | :-: | :-: | :-: | :-: |
| 0 | 0 | 0 | 1 | 1 | 1 | 
| 0 | 0 | 1 | 1 | 1 | 1 |
| 0 | 1 | 0 | 0 | 0 | 0 |
| 0 | 1 | 1 | 0 | 0 | 0 |
| 1 | 0 | 0 | 0 | 0 | 0 |
| 1 | 0 | 1 | 1 | 1 | 1 |
| 1 | 1 | 0 | 0 | 0 | 0 |
| 1 | 1 | 1 | 0 | 0 | 0 |

#### Code:
```vhdl
architecture dataflow of gates is
begin
    f_o     <= ((not b_i) and a_i)or((not c_i) and (not b_i));
    fnand_o <= ((not b_i) nand a_i)nand((not c_i)nand(not b_i));
    fnor_o  <= not((b_i nor (not a_i))nor(c_i nor b_i));
    --fnand_o <=
    --fand_o <= a_i and b_i;
    --fxor_o <= a_i xor b_i;

end architecture dataflow;
```

####Screen:
![demorgan](https://github.com/xsocha00/Digital-electronics-1/blob/main/Labs/01-gate/Images/demorgan.png)

