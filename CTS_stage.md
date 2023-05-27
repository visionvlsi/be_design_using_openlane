#### CTS

Clock Tree Synthesis is a technique for distributing the clock equally among all sequential parts of a VLSI design. The purpose of Clock Tree Synthesis is to reduce skew and delay. Clock Tree Synthesis is provided the placement data as well as the clock tree limitations as input. Clock Tree Synthesis (CTS) is the technique of balancing the clock delay to all clock inputs by inserting buffers/inverters along the clock routes of an ASIC design. As a result, CTS is used to balance the skew and reduce insertion latency. Before Clock Tree Synthesis, all clock pins were driven by a single clock source. Clock tree synthesis includes both clock tree construction and clock tree balance.
Clock tree inverters may be used to create a clock tree that maintains the correct transition (duty cycle), and clock tree buffers (CTB) can balance the clock tree to fulfil the skew and latency requirements. To fulfil the space and power limits, fewer clock tree inverters and buffers should be employed.

A clock tree can have different structures such as:
Fish bone
H-tree
X-tree
Multi-level clock tree
Once the Clock Tree Synthesis is complete, we must double-check the timing.
Optimizations to the clock tree are: Buffer sizing, gate sizing, HFN synthesis, and buffer relocation are used to achieve this.

What are the inputs and outputs of Clock Tree Synthesis?
Inputs Required for CTS are:
Detailed Placement Database
Buffers or inverters for creating the clock tree
Latency target if delay and skew are supplied
DRC Clock Tree (Max Tran, Max Cap, Max fanout, Max number of buffer levels)
Outputs for CTS are:
In the chip design, there is a database with a well built clock tree. Design Exchange Format (DEF),
Standard Parasitic Exchange Format (SPEF), and
Netlist are some of the outputs of clock tree synthesis.
Why are clock routes given precedence over signal nets?
Clock is propagated after placement because it requires the precise physical location of cells and modules for clock propagation, which has an impact on dealing with accurate delay and operating frequency, and clock is propagated before routing because clock routes are given higher priority than signal routes. This is due to the fact that the clock is the sole signal that changes often, acting as a source of dynamic power dissipation.

Effects of CTS are:
Clock buffers get added;
 congestion get increased;
non-clock cells get relocated to less desirable places;
Timing and maximum tran/cap violations take place.
What are the processes involved in Clock Tree Synthesis? And what is its impact on the design?
Clock Tree Synthesis refers to the process of dispersing the clock and balancing the load. Basically, the clock is delivered to all successive parts. The technique of inserting buffers or inverters along the clock pathways of an ASIC design to achieve zero/minimum skew or balanced skew is known as CTS. The clock source is the starting point for CTS, and the clock pins of subsequent cells are the ending point for CTS. The path from the Clock Source (Root) to the Clock Sinks is known as the Clock Tree (Leaf). The process of generating this Clock Path from Clock Source to Clock Sinks is known as Clock Tree Synthesis. Clock Sinks (Leaf) are all flip Flop clock pins; this is where the Clock Tree Synthesis finishes.
Skew is the most essential worry for clock networks since it can contribute over 10% of the system cycle time owing to changes in trace length, metal width and height, coupling caps, and local clock load, local power supply, local gate length and threshold, and local temperature. The timer starts at any Clock Source and tracks forward across Combinational Arcs until it hits a flop’s Clock Pin or another Clock Source.
Before a valid Leaf, all Pins/ Timing Arcs in the forward trace are regarded to be in the clock network. Sequential elements are traced through, if it is a source of the Generated Clock. Pin or Combinational Timing Arcs that trace to a non-clock pin (e.g. D pin of FF) are not part of the Clock Tree network. Clock tracing should be made aware after Case Analysis propagation. Inverters are added to the Clock Tree for improved Duty Cycle. Limit the buffer/inverter list to only 3 or 4 buf/inv sizes.

What are the limitations of the Clock Tree Synthesis?
Latency, skew, maximum transition, maximum capacitance, maximum fan-out, and a list of buffers and inverters are among the clock tree limitations. Clock Tree Synthesis has several clock buffers, which can cause congestion, crosstalk noise, and crosstalk latency, among other things.
