#### Routing

Netlist: The netlist is a logical representation of the design that specifies the connections between the various logic gates and components. During the routing step, the physical connections between these components are determined.

Global routing: The global routing step determines the approximate path of each net by selecting the appropriate metal layer, routing track width, and via locations. Global routing creates a rough estimate of the routing that is then used to guide the detailed routing process.

Detailed routing: The detailed routing step determines the precise path of each net by connecting the pins of the logic gates and components using the available routing resources. The detailed routing process involves selecting the routing resources, such as the metal layers, vias, and routing track widths, that are available for each net. The routing algorithm must also consider the design rules and constraints, such as minimum spacing and maximum routing density, to ensure that the routing meets the physical design requirements.

Timing closure: The routing step can also impact the timing of the design, so timing closure is performed to ensure that the design meets its timing constraints. This involves adding buffer gates and optimizing the clock tree to minimize the timing delay and meet the required clock skew.

Crosstalk analysis: Crosstalk is the interference between adjacent signals on the same metal layer, and it can cause signal integrity issues in the design. Crosstalk analysis is performed during the routing step to identify and mitigate these issues by adding shielding or changing the routing patterns.

Design rule checking (DRC): Design rule checking is performed during the routing step to ensure that the routing meets the design rules and constraints. DRC checks for issues such as minimum metal spacing, minimum via size, and maximum routing density.

Metal fill insertion: Metal fill insertion is performed during the routing step to ensure that the design meets the metal density requirements. Metal fill is added to areas of the chip where there is insufficient routing density, and it also helps to reduce the effect of electro-migration and thermal issues.

Quality of results (QoR) metrics: The routing tool generates various QoR metrics to evaluate the quality of the routing results. These metrics may include wirelength, crosstalk, timing, power, and area. The QoR metrics can be used to compare different routing runs and select the best routing for the design.

Overall, the routing step is a critical part of the physical design process that determines the physical connectivity of the design. The routing results have a significant impact on the final chip performance and yield, making it an important step in VLSI physical design.
