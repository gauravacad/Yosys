## Yosys: A primer on digital circuit synthesis
### About in details of Yosys Usages

- Yosys is specific only for Verilog HDL synthesis tool. 
- This means that it takes a behavioural design description as input and generates an RTL, logical gate or physical gate level description of the design as output.
- Yosys’ main strengths are behavioural and RTL synthesis.
- A wide range of commands (synthesis passes) exist within Yosys that can be used to perform a wide range of synthesis tasks within the domain of behavioural, RTL and logic synthesis.
- Yosys is designed to be extensible and therefore is a good basis for implementing custom synthesis tools for specialised tasks.

### Interactive design investigation

- lets's take a very simple circuit

```verilog


### Levels of abstraction

> Digital circuits can be represented at different levels of abstraction. 
> During the design process a circuit is usually first specified using a higher level abstraction.

<img width="511" height="259" alt="image" src="https://github.com/user-attachments/assets/da1f6fce-e27b-46ea-8570-2432d44edbc3" />
---

### Behavioural level
At the behavioural abstraction level a language aimed at hardware description such as Verilog or VHDL is used to describe the circuit, but so-called behavioural modelling is used in at least part of the circuit description. 
In behavioural modelling there must be a language feature that allows for imperative programming to be used to describe data paths and registers. This is the always-block in Verilog and the process-block in VHDL.

### Register-Transfer Level (RTL)
On the Register-Transfer Level the design is represented by combinatorial data paths and registers (usually d-type flip flops). 
> Note that RTL is the first abstraction level in which the circuit is represented as a graph of circuit elements (registers and combinatorial cells) and signals. Such a graph, when encoded as list of cells and connections, is called a netlist.

### Logical gate level
At the logical gate level the design is represented by a netlist that uses only cells from a small number of single-bit cells, such as basic logic gates (AND, OR, NOT, XOR, etc.) and registers (usually D-Type Flip-flops).
A number of netlist formats exists that can be used on this level, e.g. the Electronic Design Interchange Format (EDIF), but for ease of simulation often a HDL netlist is used.

### Physical gate level
On the physical gate level only gates are used that are physically available on the target architecture. In some cases this may only be NAND, NOR and NOT gates as well as D-Type registers. 
