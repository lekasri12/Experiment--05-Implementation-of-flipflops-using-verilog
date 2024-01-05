# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
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
/* write all the steps invloved */



### PROGRAM 

Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: LEKA SRI G
RegisterNumber:  212223100025
![286804807-cf2b82d4-70f5-4309-880e-54adc7897cbf](https://github.com/lekasri12/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037427/f16330e6-9033-4283-85e5-f888f9a8d42f)
![286805019-55f3012b-975a-47e6-91d6-033ccd2d68fb](https://github.com/lekasri12/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037427/4d45d2ff-5d17-401f-a68d-9510a6be9722)
![286805124-bb7b57ea-2c21-412f-84fb-42850b3b72ef](https://github.com/lekasri12/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037427/9f5d484f-f154-4bfa-a21a-bafe7dd8f232)
![286805165-46a67e4f-b26f-427d-a832-8511218042fa](https://github.com/lekasri12/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037427/f13acb3c-05e6-43ec-926c-4646c43544d1)
![286805211-96721648-6266-481e-a5fd-0ce15f96ab99](https://github.com/lekasri12/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037427/07d26408-d6d1-4a7b-a681-e35a7f725e5a)
![286805248-249c14fc-4746-4d9b-bd4b-58c364c022f2](https://github.com/lekasri12/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037427/0ee99ddd-78f4-46b9-a842-c34eee3feca8)
![286805425-41de9279-2bc7-45e1-b250-67c6e2912b65](https://github.com/lekasri12/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037427/bfe93896-bdbf-4dd2-aca7-bd7cb6a541e6)
![286805470-6dd5d998-4e22-440c-8f71-f53e5125051b](https://github.com/lekasri12/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037427/8c42585f-51dd-4377-b51a-ea1bfeeea97e)

### RTL LOGIC FOR FLIPFLOPS
![286805837-6a6864d7-799c-46ef-be5f-6e8fb78f7f14](https://github.com/lekasri12/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037427/b08ca8e9-e2e4-4bab-8c04-eb680e0c1353)
![286805948-b4d111d5-6b92-4503-9340-812fb412f2be](https://github.com/lekasri12/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037427/23563fc2-796b-4ca8-b27c-80d447b4bfc8)
![286806077-9dd21d8d-dce4-402b-803f-63ccc1bd37ca](https://github.com/lekasri12/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037427/6da86d5e-9e27-4370-9a2c-c3e984625758)
![286806240-9324ba88-87f7-4a56-a7cb-a2a3e03d52b7](https://github.com/lekasri12/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037427/8850ec49-2d50-4625-a122-364050390aa4)


### TIMING DIGRAMS FOR FLIP FLOPS 
![286806403-75e4c4ea-39c1-43f8-8a4d-d35259a77461](https://github.com/lekasri12/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037427/f8a79edc-9677-4bd8-bc95-4bc8c3366371)
![286806448-52de785d-11b7-4e48-9202-d802887bf838](https://github.com/lekasri12/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037427/bc015b4a-eab0-4eec-9cee-87ff4defbeb5)
![286806550-0be2bf79-32d6-499d-9253-83bb2ed8fd9e](https://github.com/lekasri12/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037427/5a7ca998-9b2d-4a7b-a28c-168d50f4fff9)
![286806672-de20783f-9e10-4a84-84bd-0b6cf6ea2861](https://github.com/lekasri12/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149037427/de1d0ea4-9b75-4e4c-a26f-7770515b4b53)









### RESULTS 
