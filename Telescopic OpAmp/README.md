#**Telescopic CMOS Operational Amplifier Design & AC Analysis**

##**Technology**: SkyWater 130nm (Sky130A)
##**Tools**: Xschem, NGSpice

##📘 **Project Description**

This work focuses on the design and frequency-domain analysis of a Telescopic CMOS Operational Amplifier implemented using the SkyWater 130nm (Sky130A) Process Design Kit.
The circuit schematic is created using Xschem, while all electrical simulations are performed in NGSpice.

The primary aim of this project is to analyze the small-signal AC performance of the telescopic op-amp and to observe how parameters such as bias voltages, tail current, and transistor aspect ratios (W/L) influence gain and bandwidth.

##**🧰 Software & Technology Stack**

Xschem – Schematic entry and circuit visualization

NGSpice – Analog circuit simulation

SkyWater Sky130A PDK – CMOS device models

Linux OS – Simulation environment

##**🏗️ Amplifier Architecture**

The telescopic operational amplifier is a single-stage, high-gain topology that employs cascode transistors to improve output resistance and voltage gain.

##🔸 **Major Circuit Blocks**

NMOS differential input stage

NMOS and PMOS cascode devices

Constant current tail bias source

Single-ended output node

##🔸 **Key Features**

High voltage gain due to cascoding

Low power dissipation

Reduced output swing compared to multi-stage amplifiers

Well suited for high-speed analog applications

##⚙️ Simulation Methodology
AC Small-Signal Analysis

To evaluate the frequency response of the amplifier, AC analysis is performed using the following command:

.ac dec 100 1 1e9


This sweep allows observation of gain behavior from low to high frequencies.

##**📂 Model File Inclusion**

The Sky130 device models are included in the netlist using:

.lib <path_to_sky130_models>/sky130.lib.spice tt


Ensure the correct path to the Sky130 model library is specified.

##📊 **Simulation Observations**
##🔹** Initial Frequency Response**

Moderate DC gain

Early gain roll-off

Bandwidth limited by initial biasing and transistor sizing

##🔹 **Optimized Frequency Response**

After adjusting:

Bias voltages

Tail current magnitude

Transistor W/L ratios

The following improvements were observed:

Higher DC gain

Extended bandwidth

Overall enhancement in AC performance

##✅ **Qualitative Performance Summary**
Parameter	Observation
DC Gain	Increased after parameter optimization
Bandwidth	Improved
Power Consumption	Low (single-stage architecture)
Stability	Stable due to dominant single pole

##🧠** Design Takeaways**

Cascoding significantly boosts output resistance, leading to higher gain

Accurate biasing is essential to:

Maintain saturation of all MOS devices

Achieve maximum amplifier performance

Telescopic op-amps offer high speed and gain at the cost of output voltage swing

Single-stage topology eliminates the need for Miller compensation

##🎓** Learning Outcomes**

Practical understanding of telescopic op-amp operation

Experience working with the Sky130A PDK

Insight into the effects of biasing and transistor sizing

Hands-on AC analysis using NGSpice

##📄 **Usage Notice**

This project is developed strictly for educational and academic purposes.

##🔍 **Locating the Sky130 Model File on Linux**

To find the Sky130 model library (sky130.lib.spice) on your system, use:

sudo find / -type f -name "sky130.lib.spice" 2>/dev/null


Once located, copy the correct file path and include it in your schematic or netlist.

##📈 **Plotting the Frequency Response in NGSpice**

After running the simulation, execute the following command in the NGSpice terminal:

plot db(v(vout)/v(vip))


Replace vout and vip with the actual node names used in your schematic.
