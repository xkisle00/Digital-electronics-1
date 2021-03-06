# **Lab assignment**

## 1. Link to my repository :
https://github.com/xkisle00/Digital-electronics-1



## 2. Verification of De Morgan's laws :

#### Code :

```vhdl

architecture dataflow of gates is
begin
    f_o     <= ((not b_i) and a_i) or ((not c_i)and (not b_i));
    fnand_o <= not (not (not b_i and a_i) and not (not b_i and not c_i));
    fnor_o  <= not (b_i or not a_i) or not (c_i or b_i);

end architecture dataflow;

```
#### Screeshot :
![De Morganov zakon](/obrazky/screen1.png)

#### Table :

| **c** | **b** |**a** | **f(c,b,a)** |
| :-: | :-: | :-: | :-: |
| 0 | 0 | 0 | 1 |
| 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 0 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 0 | 0 |
| 1 | 0 | 1 | 1 |
| 1 | 1 | 0 | 0 |
| 1 | 1 | 1 | 0 |

#### Link na EDA playground :
https://www.edaplayground.com/x/KWay


## 3. Verification of Distributive laws :

#### Code :
```vhdl

architecture dataflow of gates is
begin
    f1_o     <= (x_i and y_i)or(x_i and z_i);
    f2_o     <= (x_i and (y_i or z_i));
    f3_o     <= (x_i or y_i) and (x_i or z_i);
    f4_o     <= (x_i or (y_i and z_i));

end architecture dataflow;

```

#### Screeshot :
![Distributive laws](/obrazky/screen2.png)

#### Link na EDA playground :
https://www.edaplayground.com/x/7urf
