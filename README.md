## NAME : AVINASH T

## ROLL NO : 23014109


# Experiment 05 Implementation of flipflops using verilog

### AIM:
 To implement all the flipflops using verilog and validating their functionality using their functional tables

## EQUIPMENTS REQUIRED 
 HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
 SOFTWARE REQUIRED:   Quartus prime
 
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167910294-bb550548-b1dc-4cba-9044-31d9037d476b.png)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167910648-ced88e69-869c-42e2-9718-a285a3902446.png)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167908180-5fc9d589-1cb5-41f5-b2c8-927e04f5f387.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167908214-25b30a54-db20-4bcb-9385-5f93a1982a09.png)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![image](https://user-images.githubusercontent.com/36288975/167910378-d2d984a7-2815-4d17-8c41-ee4bdf59ec24.png) 

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167908575-59c35afb-50d3-46a2-888c-47478a3179d5.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/167908688-fa93c3e9-8323-4864-947d-c11d163d5a90.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure


The SR flip-flop is the simplest type of flip-flop. It has two inputs, S (Set) and R (Reset), and two outputs, Q and Q' (not Q). The output of the SR flip-flop is set to 1 when the S input is high and the R input is low. The output is reset to 0 when the R input is high and the S input is low. If both inputs are high, the output is unpredictable.The JK flip-flop is more versatile than the SR flip-flop. It has two inputs, J and K, and two outputs, Q and Q'. The output of the JK flip-flop toggles (changes from 0 to 1 or 1 to 0) when both inputs are high. When one input is high and the other is low, the output remains unchanged. When both inputs are low, the output depends on the previous state of the flip-flop.
The D flip-flop is also known as a data flip-flop. It has one data input, D, and two outputs, Q and Q'. The output of the D flip-flop follows the data input on the rising edge of the clock pulse.
The T flip-flop is also known as a toggle flip-flop. It has one input, T, and two outputs, Q and Q'. The output of the T flip-flop toggles on the rising edge of the clock pulse.


### PROGRAM 


## SR FLIPFLOP
module flipflops(S,R,clk,Q,Qbar);

input S,R,clk;

output reg Q;

output reg Qbar;

initial Q=0;

initial Qbar=1;

always @(posedge clk)

begin

Q=S|((~R)&Q);

Qbar=R|((~S)&(Qbar));

end

endmodule



## D FLIPFLOP
module experiment5(d,clk,q,qbar);

input d,clk;

output q,qbar;

reg q,qbar;

always @(posedge clk)

begin 

q<=d;

qbar<=~q;

end 

endmodule 


## JK FLIPFLOP

module flipflops(J,K,clk,Q,Qbar);

input J,K,clk;

output reg Q;

output reg Qbar;

initial Q=0;

initial Qbar=1;

always @(posedge clk)

begin

Q=(J&(~Q))|((~K)&Q);

Qbar=((~J)&(Qbar))|K&(~Qbar);

end

endmodule




## T FLIPFLOP
 
module exp_5c(clk,T,q,qbar);

input clk,T;

output q,qbar;

reg q,qbar;

always @(posedge clk)

begin

q<=(T&~q)|(~T&q);

qbar<=~q;

end 

endmodule





## RTL REALIZATION

## SR FLIPFLOP
![image](https://github.com/AVINASH05T/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151514286/7f24ab1e-6be0-4eb7-acbd-8380151bc9bd)



## D FLIPFLOP 
![image](https://github.com/AVINASH05T/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151514286/e140a1b8-b4c3-4650-b3fa-cb17633bf316)



## JK FLIPFLOP
![image](https://github.com/AVINASH05T/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151514286/e8b1f1be-c450-4f2b-9202-f0b75c57ee9a)


## T FLIPFLOP
![image](https://github.com/AVINASH05T/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151514286/cad19860-15a9-42c3-bb3e-9a03d2c574cc)





## TRUTH TABLE

## SR FLIPFLOP

![image](https://github.com/AVINASH05T/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151514286/b7d427c9-132b-4329-9eff-df0386e546e9)


## D FLIPFLOP
![image](https://github.com/AVINASH05T/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151514286/9dba2998-a50e-42a6-9682-4527f488f0fb)



## JK FLIPFLOP

![image](https://github.com/AVINASH05T/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151514286/efdc37e6-7829-403d-b867-b7c127563c08)



## T FLIPFLOP

![image](https://github.com/AVINASH05T/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151514286/76da2e8f-1632-4471-becd-aa9796016806)






## TIMING DIAGRAM


## SR FLIPFLOP

![image](https://github.com/AVINASH05T/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151514286/f279d870-bde0-4440-b48a-c5cfa0c0851a)


## D FLIPFLOP
![image](https://github.com/AVINASH05T/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151514286/f01fd230-285a-4e02-a1ff-baa084805d54)



## JK FLIPFLOP
![image](https://github.com/AVINASH05T/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151514286/93a24668-0be2-4848-961f-a72470b8657b)



## T FLIPFLOP
![image](https://github.com/AVINASH05T/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151514286/b21c9e16-91ac-414f-8c1e-63e802749ae2)






### RESULTS 
Thus, the implementation of SR,JK,D and T flipflops using nand gates are done sucessfully
