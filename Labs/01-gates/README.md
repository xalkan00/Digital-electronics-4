# H1 Digital-electronics-1
# H2 1. cvièení Digitální elektronika
[Hykš 01-Digital-electronics-1](https://github.com/mrhyks/Digital-electronics-1)

library ieee;               
use ieee.std_logic_1164.all;

entity gates is
	port(
    	a_i:in std_logic;
        b_i:in std_logic;
        c_i:in std_logic;
        f_o:out std_logic;
        fnand_o:out std_logic;
        fnor_o:out std_logic
        );
end entity gates;

architecture dataflow of gates is
begin
    f_o <= ((not(b_i) and a_i) or (not(c_i) and not(b_i)));
    fnand_o <= ((not(b_i)nand a_i) nand (not(c_i)nand not(b_i)));
    fnor_o <= (not((b_i nor not(a_i)) nor (c_i nor b_i)));

end architecture dataflow;


	

![alt text](https://raw.githubusercontent.com/mrhyks/Digital-electronics-1/main/Labs/01-gates/01-gates.png "")
| c | b | a | f(c,b,a) |

0 	0 	0 	0

0 	0 	1 	1

0 	1 	0 	0

0 	1 	1 	0

1 	0 	0 	0

1 	0 	1 	1

1 	1 	0 	0

1 	1 	1 	0

library ieee;               
use ieee.std_logic_1164.all;

entity gates is
	port(
    	a_i:in std_logic;
        b_i:in std_logic;
        c_i:in std_logic;
        f_o:out std_logic;
        fnand_o:out std_logic;
        fnor_o:out std_logic
        );
end entity gates;

architecture dataflow of gates is
begin
    f_o <= ((not(b_i) and a_i) or (not(c_i) and not(b_i)));
    fnand_o <= ((not(b_i)nand a_i) nand (not(c_i)nand not(b_i)));
    fnor_o <= (not((b_i nor not(a_i)) nor (c_i nor b_i)));

end architecture dataflow;



[Hykš 01-gates De Morganovy zákony](https://www.edaplayground.com/x/qfxM)

![alt text](https://raw.githubusercontent.com/mrhyks/Digital-electronics-1/main/Labs/01-gates/01-gates-distribuce.png "")

library ieee;               
use ieee.std_logic_1164.all;

entity gates is
	port(
    	x_i:in std_logic;
        y_i:in std_logic;
        z_i:in std_logic;
        f1_1:out std_logic;
        f1_2:out std_logic;
        f2_1:out std_logic;
        f2_2:out std_logic
        );
end entity gates;

architecture dataflow of gates is
begin
    f1_1 <= ((x_i and y_i) or (x_i and z_i));
    f1_2 <= (x_i and (y_i or z_i));
    f2_1 <= ((x_i or y_i) and (x_i or z_i));
    f2_2 <= (x_i or (y_i and z_i));

end architecture dataflow;


[Hykš 01-gates Distribuèní zákony](https://www.edaplayground.com/x/L5bX)



