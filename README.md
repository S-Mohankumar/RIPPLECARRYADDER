# RIPPLECARRYADDER
# AIM:
To simulate and synthesis of ripplecarryadder using vivado 2023.

# APPARATUS REQUIERED:
vivado 2023.1

# PROCEDURE:
STEP:1 Start the vivado software, Select and Name the New project.

STEP:2 Select the device family, device, package and speed.

STEP:3 Select new source in the New Project and select Verilog Module as the Source type.

STEP:4 Type the File Name and module name and Click Next and then finish button. Type the code and save it.

STEP:5 Select the run simulation and then run Behavioral Simulation in the Source Window and click the check syntax.

STEP:6 Click the simulation to simulate the program and give the inputs and verify the outputs as per the truth table.

STEP:7 compare the output with truth table.

![image](https://github.com/RESMIRNAIR/RIPPLECARRYADDER/assets/154305926/62459000-90cb-4c43-a221-7b8cf1d419b0)
![image](https://github.com/RESMIRNAIR/RIPPLECARRYADDER/assets/154305926/24ea1940-0b55-4f8a-be6a-a7ac5daf2919)
# Full Adder
![image](https://github.com/RESMIRNAIR/RIPPLECARRYADDER/assets/154305926/3208d46f-2fd4-4d6a-987f-63102c173ca0)
# Program:
```
module fa(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = a^b^c;
assign carry=(a&b)|(b&c)|(c&a);
endmodule
module rca(a,b,cin,sum,cout);
input [3:0]a,b;
input cin;
output [3:0]sum;
output cout;
wire c1,c2,c3;
fa fa1(a[0],b[0],cin,sum[0],c1);
fa fa2(a[1],b[1],c1,sum[1],c2);
fa fa3(a[2],b[2],c2,sum[2],c3);
fa fa4(a[3],b[3],c3,sum[3],cout);
endmodule
```
# Output
![WhatsApp Image 2024-05-11 at 21 25 29_c0e2e491](https://github.com/S-Mohankumar/RIPPLECARRYADDER/assets/163832108/0ed59495-2d7a-46db-a82d-de8177cf5085)
# RESULT:
Thus the simulation and synthesis of ripplecarryadder using vivado 2023.1 is successfully executed and verified.
