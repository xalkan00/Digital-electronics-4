# H1 Digital-electronics-1
Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

1. First ordered list item
2. Another item
⋅⋅* Unordered sub-list. 
1. Actual numbers don't matter, just that it's a number
⋅⋅1. Ordered sub-list
4. And another item.

⋅⋅⋅You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).

⋅⋅⋅To have a line break without a paragraph, you will need to use two trailing spaces.⋅⋅
⋅⋅⋅Note that this line is separate, but within the same paragraph.⋅⋅
⋅⋅⋅(This is contrary to the typical GFM line break behaviour, where trailing spaces are not required.)

* Unordered list can use asterisks
- Or minuses
+ Or pluses



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


	

![alt text](01-gates.png "Logo Title Text 1")
c 	b 	a 	f(c,b,a)

0 	0 	0 	0

0 	0 	1 	1

0 	1 	0 	0

0 	1 	1 	0

1 	0 	0 	0

1 	0 	1 	1

1 	1 	0 	0

1 	1 	1 	0


[Hyk� playground](https://www.edaplayground.com/x/qfxM)
