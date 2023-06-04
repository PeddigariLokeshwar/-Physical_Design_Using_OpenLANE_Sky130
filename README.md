# Advanced Physical Design Using OpenLANE/Sky130

![workshop_banner](https://user-images.githubusercontent.com/86701156/123913967-7b330980-d99c-11eb-81cf-37c61edde8c7.JPG)

## Table of Contents
1. [About](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#about)
2. [Day 1: Inception of Opensource EDA](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#day-1-inception-of-opensource-eda)
   - [How to Talk to computers?](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#how-to-talk-to-computers)
   - [SOC Design & OpenLANE](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#soc-design--openlane)
     - [Components of opensource digital ASIC design](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#components-of-opensource-digital-asic-design)
     - [Simplified RTL2GDS Flow](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#simplified-rtl2gds-flow)
     - [OpenLANE ASIC Flow](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#openlane-asic-flow)
   - [Opensource EDA tools](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#opensource-eda-tools)
     - [OpenLANE Files](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#openlane-files)
     - [Invoking OpenLANE](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#invoking-openlane)
     - [Design Preparation Step](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#design-preparation-step)
     - [Review of files & Synthesis step](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#design-preparation-step#review-of-files-&-synthesis-step)
     - [Characterization of synthesis results](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#characterization-of-synthesis-results)
3. [Day 2: Floorplanning and library cells](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#day-2-floorplanning-and-library-cells)
   - [Floorplanning considerations](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#floorplanning-considerations)
     - [Utilization Factor & Aspect Ratio](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#utilization-factor--aspect-ratio)
     - [Pre-placed cells](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#pre-placed-cells)
     - [Decoupling capacitors](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#decoupling-capacitors)
     - [Power Planning](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#power-planning)
     - [Pin Placement](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#pin-placement)
     - [Floorplan run on OpenLANE & view in Magic](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#floorplan-run-on-openlane--view-in-magic)
   - [Placement](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#placement)
     - [Placement Optimization](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#placement-optimization)
     - [Placement run on OpenLANE & view in Magic](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#placement-run-on-openlane--view-in-magic)
   - [Standard Cell Design Flow](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#standard-cell-design-flow)
   - [Standard Cell Characterization Flow](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#standard-cell-characterization-flow)
   - [Timing Parameter Definitions](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#timing-parameter-definitions)
4. [Day 3: Design library cell](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#day-3-design-library-cell)
   - [SPICE Deck creation & Simulation](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#spice-deck-creation--simulation)
   - [CMOS inverter Switching Threshold Vm](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#cmos-inverter-switching-threshold-vm)
   - [16 Mask CMOS Fabrication](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#16-mask-cmos-fabrication)
   - [Inverter Standard cell Layout & SPICE extraction](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#inverter-standard-cell-layout--spice-extraction)
   - [Inverter Standard cell characterization](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#inverter-standard-cell-characterization)
   - [Magic Features & DRC rules](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#magic-features--drc-rules)
5. [Day 4: Timing Analysis & CTS](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#day-4-timing-analysis--cts)
   - [Standard Cell LEF generation](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#standard-cell-lef-generation)
   - [Integrating custom cell in OpenLANE](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#integrating-custom-cell-in-openlane)
   - [Post-synthesis timing analysis](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#post-synthesis-timing-analysis)
   - [Clock Tree Synthesis](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#clock-tree-synthesis)
6. [Day 5: Final steps in RTL2GDS](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#day-5-final-steps-in-rtl2gds)
   - [Power Distribution Network generation](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#power-distribution-network-generation)
   - [Routing](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#routing)
7. [Differences from older OpenLANE versions](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#differences-from-older-openlane-versions)
8. [Future Scope](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#future-scope)
9. [References](https://github.com/aasthadave9/Advanced-Physical-Design-Using-OpenLANE-Sky130/blob/main/README.md#references)

## About
OpenLANE is an opensource tool or flow used for opensource tape-outs. The OpenLANE flow comprises a variety of tools such as Yosys, ABC, OpenSTA, Fault, OpenROAD app, Netgen and Magic which are used to harden chips and macros, i.e. generate final GDSII from the design RTL. The primary goal of OpenLANE is to produce clean GDSII with no human intervention. OpenLANE has been tuned to function for the Google-Skywater130 Open Process Design Kit.

## Day 1: Inception of Opensource EDA

### How to talk to computers?
The RISC-V Instruction Set Architecture (ISA) is a language used to talk to computers whose hardware is based on RISC-V core. If a user wishes to run a certain application software on a computer, its corresponding C/C++/Java program must be converted into instructions by the compliler. The ouput of the compiler is hardware dependent. These instructions go as inputs to the assembler which outputs binary language that the hardware logic in the chip layout can make sense of. According the the bits received, the digital logic consisting of gates performs the function required by the user of the application software.

### SoC Design & OpenLANE

#### Components of opensource digital ASIC design
The design of digital Application Specific Integrated Circuit (ASIC) requires three enablers or elements - Resistor Transistor Logic Intellectual Property (RTL IPs), Electronic Design Automation (EDA) Tools and Process Design Kit (PDK) data.

![ASIC](https://user-images.githubusercontent.com/86701156/124005001-35a32a80-d9f6-11eb-8fcc-0917ad337699.PNG)
- Opensource RTL Designs: github, librecores, opencores
- Opensource EDA tools: QFlow, OpenROAD, OpenLANE
- Opensource PDK data: Google Skywater130 PDK

The ASIC flow objective is to convert RTL design to GDSII format used for final layout. The flow is essentially a software also known as automated PnR (Place & route).

#### Simplified RTL2GDS Flow
![RTL2GDS flow](https://user-images.githubusercontent.com/86701156/124006238-a139c780-d9f7-11eb-8da9-6069b055fbe0.PNG)

- Synthesis: RTL Converted to gate level netlist using standard cell libraries (SCL)
- Floor & Power Planning: Planning of silicon area to ensure robust power distribution
- Placement: Placing cells on floorplan rows aligned with sites
  - Global Placement: for optimal position of cells
  - Detailed Placement: for legal positions
- Routing: Valid patterns for wires
- Signoff: Physical (DRC, LVS) and Timing verifications (STA)

#### OpenLANE ASIC Flow
![openlane asic flow](https://user-images.githubusercontent.com/86701156/124007394-f62a0d80-d9f8-11eb-9d46-7cc885c0eff6.PNG)
### Opensource EDA tools
OpenLANE utilises a variety of opensource tools in the execution of the ASIC flow:
Task | Tool/s
------------ | -------------
RTL Synthesis & Technology Mapping | [yosys](https://github.com/YosysHQ/yosys), abc
Floorplan & PDN | init_fp, ioPlacer, pdn and tapcell
Placement | RePLace, Resizer, OpenPhySyn & OpenDP
Static Timing Analysis | [OpenSTA](https://github.com/The-OpenROAD-Project/OpenSTA)
Clock Tree Synthesis | [TritonCTS](https://github.com/The-OpenROAD-Project/OpenLane)
Routing | FastRoute and [TritonRoute](https://github.com/The-OpenROAD-Project/TritonRoute) 
SPEF Extraction | [SPEF-Extractor](https://github.com/HanyMoussa/SPEF_EXTRACTOR)
DRC Checks, GDSII Streaming out | [Magic](https://github.com/RTimothyEdwards/magic), [Klayout](https://github.com/KLayout/klayout)
LVS check | [Netgen](https://github.com/RTimothyEdwards/netgen)
Circuit validity checker | [CVC](https://github.com/d-m-bailey/cvc)


#### OpenLANE Files

- skywater-pdk: contains PDK files provided by foundry
- open_pdks: contains scripts to setup pdks for opensource tools 
- sky130A: contains sky130 pdk files

#### Invoking OpenLANE
Openlane can be invoked using docker command followed by opening an interactive session.
flow.tcl is a script that specifies details for openLANE flow.

```
docker
./flow.tcl -interactive
package require openlane 0.9
```
![openlane invoke ](https://github.com/PeddigariLokeshwar/-Physical_Design_Using_OpenLANE_Sky130/assets/105622389/6176987f-0d3e-4a93-bfe6-88d865eb5b89)

#### Design Preparation Step
This project is based on the reference SoC design of PicoRV32 which is a CPU core that implements RISC-V instruction set.
 Various packages are initialized followed by preparation of the picorv32a design.
 ```
 prep -design picorv32a
 ```
![preparation command](https://github.com/PeddigariLokeshwar/-Physical_Design_Using_OpenLANE_Sky130/assets/105622389/7520b333-4e4f-47c8-9076-ab6edcd20b55)

#### Review of files & Synthesis step
A "runs" folder is generated within the picorv32a folder.

![folder with date](https://github.com/PeddigariLokeshwar/-Physical_Design_Using_OpenLANE_Sky130/assets/105622389/6d78fbd8-c0a8-4df6-8354-d40819922714)

Since today's date is 30th May, a folder titled "30-05..." is created within the picorv32a directory:

![review runs folder](https://github.com/PeddigariLokeshwar/-Physical_Design_Using_OpenLANE_Sky130/assets/105622389/5896173a-df54-4142-b091-5f9d3f1d0574)

The merged file is created during the merging operation in the pircorv32a design preparation (it merges lef and techlef files)

![merged lef ](https://github.com/PeddigariLokeshwar/-Physical_Design_Using_OpenLANE_Sky130/assets/105622389/a0d2516b-133f-4bb8-8994-09c2a0794b6c)

Next, we run the synthesis of picorv32a design in the openlane interactive terminal:
`run_synthesis`

![run synthesis command](https://github.com/PeddigariLokeshwar/-Physical_Design_Using_OpenLANE_Sky130/assets/105622389/08c839a3-3e47-4c88-a031-66c2d671a845)

The yosys and ABC tools are utilised to convert RTL to gate level netlist

Calcuation of Flop Ratio:
```
Flop ratio = Number of D Flip flops 
             ______________________
             Total Number of cells
```

![no of cells](https://github.com/PeddigariLokeshwar/-Physical_Design_Using_OpenLANE_Sky130/assets/105622389/d917bab9-e7da-4867-b87f-c28371c6f46b) ![no of dflops](https://github.com/PeddigariLokeshwar/-Physical_Design_Using_OpenLANE_Sky130/assets/105622389/7a73981b-3665-4e4b-b3df-12a6db84c419)
```
dfxtp_4 = 1613,
Number of cells = 14876,
Flop ratio = 1613/14876 = 0.1084 = 10.84%
```

#### Characterization of synthesis results
We may check the success of the synthesis step by checking the synthesis folder for the synthesised netlist file (.v file)
![sysnthesis file ss](https://github.com/PeddigariLokeshwar/-Physical_Design_Using_OpenLANE_Sky130/assets/105622389/02302c8c-b3b1-4966-95aa-3f3a1bac8ab4)

The synthesis statistics report can be accessed within the reports directory. It is usually the last yosys file since files are listed chronologically by date of modification

![synthesis report](https://github.com/PeddigariLokeshwar/-Physical_Design_Using_OpenLANE_Sky130/assets/105622389/7fb0ca79-d572-4f7e-9026-c3a6af1bb5d9)

## Day 2: Floorplanning and library cells

### Floorplanning considerations

#### Utilization Factor & Aspect Ratio  

Two parameters are of importance when it comes to floorplanning namely, Utilisation Factor and Aspect Ratio. They are defined as follows:

```
Utilisation Factor =  Area occupied by netlist
                     __________________________
                        Total area of core
```

```
Aspect Ratio =  Height
               ________
                Width
```
                                  
A Utilisation Factor of 1 signifies 100% utilisation leaving no space for extra cells such as buffer. However, practically, the Utilisation Factor is 0.5-0.6. Likewise, an Aspect ratio of 1 implies that the chip is square shaped. Any value other than 1 implies rectanglular chip.

#### Pre-placed cells

Once the Utilisation Factor and Aspect Ratio has been decided, the locations of pre-placed cells need to be defined. Pre-placed cells are IPs comprising large combinational logic which once placed maintain a fixed position. Since they are placed before placement and routing, the are known as pre-placed cells.

#### Decoupling capacitors

Pre-placed cells must then be surrounded with decoupling capacitors (decaps). The resistances and capacitances associated with long wire lengths can cause the power supply voltage to drop significantly before reaching the logic circuits. This can lead to the signal value entering into the undefined region, outside the noise margin range.  Decaps are huge capacitors charged to power supply voltage and placed close the logic circuit. Their role is to decouple the circuit from power supply by supplying the necessary amount of current to the circuit. They pervent crosstalk and enable local communication

#### Power Planning

Each block on the chip, however, cannot have its own decap unlike the pre-placed macros. Therefore a good power planning ensures that each block has its own VDD and VSS pads connected to the horizontal and vertical power and GND lines which form a power mesh.

#### Pin Placement

The netlist defines connectivity between logic gates. The place between the core and die is utilised for placing pins. The connectivity information coded in either VHDL or Verilog is used to determine the position of I/O pads of various pins. Then, logical placement blocking of pre-placed macros is performed so as to differentiate that area from that of the pin area.

#### Floorplan run on OpenLANE & view in Magic

Files of importance in increasing priority order:
1. ```floorplan.tcl``` - System default envrionment variables
2. ```conifg.tcl```
3. ```sky130A_sky130_fd_sc_hd_config.tcl```

Floorplan envrionment variables or switches:
1. ```FP_CORE_UTIL``` - floorplan core utilisation
2. ```FP_ASPECT_RATIO``` - floorplan aspect ratio
3. ```FP_CORE_MARGIN``` - Core to die margin area
4. ```FP_IO_MODE``` - defines pin configurations (1 = equidistant/0 = not equidistant)
5. ```FP_CORE_VMETAL``` - vertical metal layer
6. ```FP_CORE_HMETAL``` - horizontal metal layer

***Note: Usually, vertical metal layer and horizontal metal layer values will be 1 more than that specified in the files***
 
 To run the picorv32a floorplan in openLANE:
 ```
 run_floorplan
 
 ```
![run floorplan command](https://github.com/PeddigariLokeshwar/-Physical_Design_Using_OpenLANE_Sky130/assets/105622389/f4de2196-29f2-4ffe-9b25-f15fd5bb579d)

Post the floorplan run, a .def file will have been created within the ```results/floorplan``` directory. We may review floorplan files by checking the ```floorplan.tcl```. The system defaults will have been overriden by switches set in ```conifg.tcl``` and further overriden by switches set in ```sky130A_sky130_fd_sc_hd_config.tcl```.
 
To view the floorplan, Magic is invoked after moving to the ```results/floorplan``` directory:
```
magic -T /home/aastha/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.floorplan.def &

```

![entire floorplan ](https://github.com/PeddigariLokeshwar/-Physical_Design_Using_OpenLANE_Sky130/assets/105622389/a8758cd2-acb4-4399-b771-c02c1e683543)
 
One can zoom into Magic layout by selecting an area with left and right mouse clcik followed by pressing "z" key. Here, equidistant input pins (FP_IO_MODE = 1) can be viewed:
 
![equidistant IO](https://github.com/PeddigariLokeshwar/-Physical_Design_Using_OpenLANE_Sky130/assets/105622389/7fd470e0-2545-4985-8747-3251f400b86b)
 
Various components can be identified by using the ```what``` command in tkcon window after making a selection on the component:

  ![IO slection in tkcon ](https://github.com/PeddigariLokeshwar/-Physical_Design_Using_OpenLANE_Sky130/assets/105622389/d3198b8c-dd9f-4f90-a9a3-ffa460286558)

Zooming in also provides a view of decaps present in picorv32a chip:

  ![decap cells](https://github.com/PeddigariLokeshwar/-Physical_Design_Using_OpenLANE_Sky130/assets/105622389/71195a37-af3b-4915-b344-7f455292c2af)

The standard cell can be found at the bottom left corner:

  ![cell in bottom left](https://github.com/PeddigariLokeshwar/-Physical_Design_Using_OpenLANE_Sky130/assets/105622389/bb910b7c-8bb7-4bf5-86d2-5c177c7ec5be)


### Placement 

#### Placement Optimization

The next step in the OpenLANE ASIC flow is placement. The synthesized netlist is the be placed on the floorplan. Placement is perfomed in 2 stages:

1. Global Placement: It finds optimal position for all cells which may not be legal and cells may overlap. Optimization is done through reduction of half parameter wire length
2. Detailed Placement: It alters the position of cells post global placement so as to legalise them

Legalisation of cells is important from timing point of view. 

#### Placement run on OpenLANE & view in Magic

Congestion aware placement using RePIAce:
```
run_placement

```
The objective of placement is the convergence of overflow value. If overflow value progressively reduces during the placement run it implies that the design will converge and placement will be successful. Post placement, the design can be viewed on magic within ```results/placement``` directory:

```
magic -T /home/aastha/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.placement.def &

```
![placement entire](https://github.com/PeddigariLokeshwar/-Physical_Design_Using_OpenLANE_Sky130/assets/105622389/07d3739e-1512-4442-b947-c3f576422ba5)

Zoomed-in views of the standard cell placement:

![placement zoomed in](https://github.com/PeddigariLokeshwar/-Physical_Design_Using_OpenLANE_Sky130/assets/105622389/309bc7dd-7613-43d8-bdce-9dec0eba9b41)
![placement more zoomed in](https://github.com/PeddigariLokeshwar/-Physical_Design_Using_OpenLANE_Sky130/assets/105622389/ffa1d0b3-f0b4-432a-be98-906328d7fbd3)
***Note: Power distribution network generation is usually a part of the floorplan step. However, in the openLANE flow, floorplan does not generate PDN. The steps are - floorplan, placement CTS and then PDN***


### Standard Cell Design Flow

Standard cell design flow involves the following:
1. Inputs: PDKs, DRC & LVS rules, SPICE models, libraries, user-defined specifications 
2. Design steps: Circuit design, Layout design (Art of layout Euler's path and stick diagram), Extraction of parasitics, Characterization (timing, noise, power)
3. Outputs: CDL (circuit description language), LEF, GDSII, extracted SPICE netlist (.cir), timing, noise and power .lib files

### Standard Cell Characterization Flow

A typical standard cell characterization flow includes the following steps:
1. Read in the models and tech files
2. Read extracted spice netlist
3. Recognise behaviour of the cell
4. Read the subcircuits
5. Attach power sources
6. Apply stimulus to characterization setup
7. Provide necessary output capacitance loads
8. Provide necessary simulation commands

The opensource software called GUNA can be used for characterization. Steps 1-8 are fed into the GUNA software which generates timing, noise and power models.

### Timing Parameter Definitions

Timing defintion | Value
------------ | -------------
slew_low_rise_thr  | 20% value
slew_high_rise_thr |  80% value
slew_low_fall_thr | 20% value
slew_high_fall_thr | 80% value
in_rise_thr | 50% value
in_fall_thr | 50% value
out_rise_thr | 50% value
out_fall_thr | 50% value

```
rise delay =  time(out_fall_thr) - time(in_rise_thr)

Fall transition time: time(slew_high_fall_thr) - time(slew_low_fall_thr)

Rise transition time: time(slew_high_rise_thr) - time(slew_low_rise_thr)
```

A poor choice of threshold points leads to neative delay value. Therefore a correct choice of thresholds is very important

## Day 3: Design library cell

OpenLANE allows users to make changes to environment variables on the fly. For instance, if we wish to change the pin placement from equidistant to some other style of placement we may do the following in the openLANE flow:
```
set ::env(FP_IO_MODE) 2
```

### SPICE Deck creation & Simulation

A SPICE deck includes information about the following:
1. Model description
2. Netlist description
3. Component connectivity
4. Component values
5. Capacitance load
6. Nodes
7. Simulation type and parameters
8. Libraries included

### CMOS inverter Switching Threshold Vm

Thw sitching threshold of a CMOS inverter is the point on the transfer characteristic where Vin equals Vout (=Vm). At this point both PMOS and NOMOS are in ON state which gives rise to a leakage current

### 16 Mask CMOS Fabrication
The 16-mask CMOS process consists of the following steps:
1. Selection of subtrate: Secting the body/substrate material
2. Creating active region for transistors: Isolation between active region pockets by SiO2 and Si3N4 deposition followed by photolithography and etching
3. N-well and P-well formation: Ion implanation by Boron for P-well and by Phosphorous for N-well formation
4. Formation of gate terminal: NMOS and PMOS gates formed by photolithography techniques
5. LDD (lightly doped drain) formation: LDD formed to prevent hot electron effect
6. Source & drain formation: Screen oxide added to avoid channelling during implants followed by Aresenic implantation and annealing
7. Local interconnect formation: Removal of screen oxide by HF etching. Deposition of Ti for low resistant contacts
8. Higher level metal formation: CMP for planarization followed by TiN and Tungsten deposition. Top SiN layer for chip protection

### Inverter Standard cell Layout & SPICE extraction

The Magic layout of a CMOS inverter will be used so as to intergate the inverter with the picorv32a design. To do this, inverter magic file is sourced from [vsdstdcelldesign](https://github.com/nickson-jose/vsdstdcelldesign) by cloning it within the ```openlane_working_dir/openlane``` directory as follows:
```
git clone https://github.com/nickson-jose/vsdstdcelldesign
```
This creates a vsdstdcelldesign named folder in the openlane directory. The repo's contents after cloning appear as follows:

To invoke magic to view the ```sky130_inv.mag``` file, the sky130A.tech file must be included in the command along with its path. To ease up the complexity of this command, the tech file can be copied from the magic folder to the vsdstdcelldesign folder.
![files in vsdstdcelldesign](https://github.com/PeddigariLokeshwar/-Physical_Design_Using_OpenLANE_Sky130/assets/105622389/890202a8-bf52-4afb-b3d8-69c858f37ec5)

The sky130_inv.mag file can then be invoked in Magic very easily:
```
magic -T sky130A.tech sky130_inv.mag &
```
![magic inverter layout](https://github.com/PeddigariLokeshwar/-Physical_Design_Using_OpenLANE_Sky130/assets/105622389/e68ed062-08c9-4785-b554-17a4ddd6da9a)

In Sky130 the first layer is called the local interconnect layer or Locali as shown above.

To verify whether the layout is that of CMOS inverter, verification of P-diffusiona nd N-diffusion regions with Polysilicon can be observed:
![verifying pdiff intersection with poly](https://user-images.githubusercontent.com/86701156/124420751-a4c5a980-dd7d-11eb-81df-df3a88eed34e.PNG)

Other verification steps are to check drain and source connections. The drains of both PMOS and NMOS must be connected to output port (here, Y) and the sources of both must be connected to power supply VDD (here, VPWR.

**LEF or library exchange format:**
A format that tells us about cell boundaries, VDD and GND lines. It contains no info about the logic of circuit and is also used to protect the IP.

**SPICE extraction:**
Within the Magic environment, following commands are used in tkcon to achieve .mag to .spice extraction:
```
extract all
ext2spice cthresh 0 rethresh 0
ext2spice
```
![spice extraction commands](https://github.com/PeddigariLokeshwar/-Physical_Design_Using_OpenLANE_Sky130/assets/105622389/fd08d29f-01b7-40b6-8d0e-b15db2649aed)

This generates the ```sky130_in.spice``` file as shown above. This SPICE deck is edited to include ```pshort.lib``` and ```nshort.lib``` which are the PMOS and NMOS libraries respectively. In addition, the minimum grid size of inverter is measured from the magic layout and incorporated into the deck as: ```.option scale=0.01u```. The model names in the MOSFET definitions are changed to ```pshort.model.0``` and ```nshort.model.0``` respectively for PMOS and NMOS. Finally voltage sources and simulation commands are defined as follows:
```
VDD VPWR 0 3.3V
VSS VGND 0 0
Va A VGND PUSLE(0V 3.3V 0 0.1ns 0.1 ns 2ns 4ns)
.tran 1n 20n
.control
run 
.endc
.end
```

For simulation, ngspice is invoked in ther terminal:
```
ngspice sky130_inv.spice
```
The output "y" is to be plotted with "time" and swept over the input "a":
```
plot y vs time a
```

The waveform obtained is as shown:

![inverter waveform](https://user-images.githubusercontent.com/86701156/124429304-561f0c00-dd8b-11eb-98fa-1fd7ab385e16.PNG)

The spikes in the output at switching points is due to low capacitance loads. This can be taken care of by editing the spice deck to increase the load capacitance value.

### Inverter Standard cell characterization

Four timing parameters are used to characterize the inverter standard cell:
1. Rise transition: Time taken for the output to rise from 20% of max value to 80% of max value
2. Fall transition- Time taken for the output to fall from 80% of max value to 20% of max value
3. Cell rise delay = time(50% output rise) - time(50% input fall)
4. Cell fall delay  = time(50% output fall) - time(50% input rise)

The above timing parameters can be computed by noting down various values from the ngspice waveform.

![rise time calc](https://user-images.githubusercontent.com/86701156/124429861-09880080-dd8c-11eb-83db-0183bf4d6c76.PNG) 
```Rise transition = (2.23843 - 2.17935) = 59.08ps```

![fall time calc](https://user-images.githubusercontent.com/86701156/124430314-a3e84400-dd8c-11eb-9759-753929e215ff.PNG)
```Fall transition = (4.09291 - 4.05004) = 42.87ps```

![cell rise delay calc](https://user-images.githubusercontent.com/86701156/124430430-cbd7a780-dd8c-11eb-8382-9a758ce9451b.PNG)
```Cell rise delay = (2.20636 - 2.15) = 56.36ps```

![cell fall delay calc](https://user-images.githubusercontent.com/86701156/124430661-0fcaac80-dd8d-11eb-8f32-1fda5750491a.PNG)
```Cell fall delay = (4.07479 - 4.05) = 24.79ps```

### Magic Features & DRC rules
The technology file is a setup file that declares layer types, colors, patterns, electrical connectivity, DRC, device extraction rules and rules to read LEF and DEF files.
Magic layouts can be sourced from [opencircuitdesign.com](https://opencircuitdesign.com/) using the command:
```
wget http://opencircuitdesign.com/open_pdks/archive/drc_tests.tgz
tar xfz drc_tests.tgz
```

The ```.magicrc``` loads the tech file required by the user. Since this file sets up the tech file, sky130.tech need not be mentioned in the command used to invoke Magic. Hecen Magic can be invoked more conveniently now:
```
magic -d XR
```

##### DRC Errors
To analyse DRC errors, magic is invoked and the met3.mag file is opened either from the software as ```file-> open-> met3.mag``` or by running command in tkcon as ```magic -d XR met3```. DRC errors can be found by selecting a component and typing: ```drc why``` in tkcon.

![drc error checking in magic](https://user-images.githubusercontent.com/86701156/124431912-a0ee5300-dd8e-11eb-8cca-b0cb8a114305.PNG)

met3.6 is the name of a DRC rule. The descriptions of DRC rules can be found in the [SKY130 PDK’s documentation](https://skywater-pdk--136.org.readthedocs.build/en/136/rules.html)

To check for vias in the metal3 layer, make a rectangluar selection in an empty space and paint it with the m3contact color from the color palette by clicking middle mouse button. The vias can be viewed by: ```cif see VIA2```

![vias](https://user-images.githubusercontent.com/86701156/124432365-2c67e400-dd8f-11eb-8736-053ced3bf279.PNG)

In this fashion, one can search for DRC errors, read up their descriptions and resolve them by editing the technology file.

## Day 4: Timing Analysis & CTS

A requirement for ports as specified in ```tracks.info``` is that they should be at intersection of horizontal and vertical tracks. The CMOS Inverter ports A and Y are on li1 layer. It needs to be ensured that they're on the intersection of horizontal and vertical tracks. We access the tracks.info file for the pitch and direction information:

![tracks info file for route info](https://user-images.githubusercontent.com/86701156/124445507-3e508380-dd9d-11eb-8313-b45244931a86.PNG)

To ensure that ports lie on the intersection point, the grid spacing in Magic (tkcon) must be changed to the li1 X and li1 Y values. Convergence of grid and tracks can be achieved using the following command:
```
grid 0.46um 0.34um 0.23um 0.17um
```
### Standard Cell LEF generation
Before the CMOS Inverter standard cell LEF is extracted, the purpose of ports must be defined:
Select port A in magic:
```
port class input
port use signal
```
Select Y area
```
port class output
port class signal
```
Select VPWR area
```
port class inout
port use power
```

Select VGND area
```
port class inout
port use ground
```

LEF extraction can be carried out in tkcon as follows:
```
lef write
```
This generates ```sky130_vsdinv.lef``` file.

### Integrating custom cell in OpenLANE

In order to include the new standard cell in the synthesis, copy the sky130_vsdinv.lef file to the ```designs/picorv32a/src``` directory  
Since abc maps the standard cell to a library abc there must be a library that defines the CMOS inverter. The ```sky130_fd_sc_hd_typical.lib``` file from ```vsdstdcelldesign/libs``` directory needs to be copied to the ```designs/picorv32a/src``` directory (Note: the slow and fast library files may also be copied).

Next, ```config.tcl``` must be modified:
```
set ::env(LIB_SYNTH) "$::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130/sky130_fd_sc_hd__typical.lib"
set ::env(LIB_SLOWEST) "$::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130/sky130_fd_sc_hd__slow.lib"
set ::env(LIB_FASTEST) "$::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130/sky130_fd_sc_hd__fast.lib"
set ::env(LIB_TYPICAL) "$::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130/sky130_fd_sc_hd__typical.lib"

set ::env(EXTRA_LEFS) [glob $::env(OPENLANE_ROOT)/designs/$::env(DESIGN_NAME)/src/*.lef]
```

In order to integrate the standard cell in the OpenLANE flow, invoke openLANE as usual and carry out following steps:

```
prep -design picorv32a -tag 02-07_07-56 -overwrite
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs
run_synthesis
```
During the synthesis run, several instances of the sky130_vsdinv cell can be observed:
![vsdinv in run_synthesis step - success](https://user-images.githubusercontent.com/86701156/124448257-de0f1100-dd9f-11eb-8a2a-efcc418997da.PNG)
![synthesis of std cell](https://user-images.githubusercontent.com/86701156/124448454-19a9db00-dda0-11eb-9a31-d44105a14738.PNG)

Next floorplan is run, followed by placement:

```
init_floorplan
run_placement
```

To check the layout invoke magic from the ```results/placement``` directory:

```
magic -T /home/aastha/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.placement.def
```

Since the custom standard cell has been plugged into the openLANE flow, it would be visible in the layout:
![zoomed in layout - view of vsdinv std cell](https://user-images.githubusercontent.com/86701156/124449266-e6b41700-dda0-11eb-97e6-c27d031decf5.PNG)
![expanded layout view of cmos inv](https://user-images.githubusercontent.com/86701156/124449276-e87dda80-dda0-11eb-9823-bcfe9bd536bc.PNG)

### Post-synthesis timing analysis

Timing analysis is carried out outside the openLANE flow using OpenSTA tool. For this, a new file ```pre_sta.conf``` is created. This file would be reqiured to carry out the STA analysis. Invoke OpenSTA outside the openLANE flow as follows:
```
sta pre_sta.conf
```
![slack at the end of STA](https://user-images.githubusercontent.com/86701156/124452411-fbde7500-dda3-11eb-91f0-01fbc584e443.PNG)

Since clock tree synthesis has not been performed yet, the analysis is with respect to ideal clocks and only setup time slack is taken into consideration. The slcak value is the difference between data required time and data arrival time. The worst slack value must be greater than or equal to zero. If a negative slack is obtained, following steps may be followed:
1. Change synthesis strategy, synthesis buffering and synthesis sizing values 
2. Review maximum fanout of cells and replace cells with high fanout

![large fanout at net 11344 - affects delay](https://user-images.githubusercontent.com/86701156/124451312-e3ba2600-dda2-11eb-9b40-984fafc7f2c0.PNG)


### Clock Tree Synthesis

The purpose of building a clock tree is enable the clock input to reach every element and to ensure a zero clock skew. H-tree is a common methodology followed in CTS.
Before attempting a CTS run in TritonCTS tool, if the slack was attempted to be reduced in previous run, the netlist may have gotten modified by cell replacement techniques. Therefore, the verilog file needs to be modified using the ```write_verilog``` command. Then, the synthesis, floorplan and placement is run again. To run CTS use the below command:

```
run_cts
```
The CTS run adds clock buffers in therefore buffer delays come into picture and our analysis from here on deals with real clocks. Setup and hold time slacks may now be analysed in the post-CTS STA anlysis in OpenROAD within the openLANE flow:
```
openroad
write_db pico_cts.db
read_db pico_cts.db
read_verilog /openLANE_flow/designs/picorv32a/runs/03-07_11-25/results/synthesis/picorv32a.synthesis_cts.v
read_liberty $::env(LIB_SYNTH_COMPLETE)
link_design picorv32a
read_sdc /openLANE_flow/designs/picorv32a/src/my_base.sdc
set_propagated_clock (all_clocks)
report_checks -path_delay min_max -format full_clock_expanded -digits 4
```

Slack at the end of STA for typical corner:

![slack at end of sta via openroad - for typical corner](https://user-images.githubusercontent.com/86701156/124453238-ce45fb80-dda4-11eb-8b32-de78c261cc76.PNG)

One may also check how the timing gets affected if clock buffers are replaced. Below, clkbuf_1 was replaced:
![altering clk buf_list to exclude buf_1 (assign2)](https://user-images.githubusercontent.com/86701156/124453733-49a7ad00-dda5-11eb-8039-dcb19372469b.PNG)

## Day 5: Final steps in RTL2GDS

### Power Distribution Network generation

Unlike the general ASIC flow, Power Distribution Network generation is not a part of floorplan run in OpenLANE. PDN must be generated after CTS and post-CTS STA analyses:

```
gen_pdn
```

We can confirm the success of PDN by checking the current def environment variable: ``` echo $::env(CURRENT_DEF) ```

### Routing 
OpenLANE uses the TritonRoute tool for routing. There are 2 stages of routing:
1. Global routing: Routing region is divided into rectangle grids which are represented as course 3D routes (Fastroute tool)
2. Detailed routing: Finer grids and routing guides used to implement physical wiring (TritonRoute tool)

Features of TritonRoute:
1. Honouring pre-processed route guides
2. Assumes that each net satisfies inter guide connectivity
3. Uses MILP based panel routing scheme
4. Intra-layer parallel and inter-layer sequential routing framework

Running routing step in TritonRoute as part of openLANE flow:

```
run_routing
```

Routing typically uses up a lot of memory:
![huge amount of memory used in detailed routing](https://user-images.githubusercontent.com/86701156/124459606-ed945700-ddab-11eb-83e1-7df005822489.PNG)


At the end of routing, one may see a few DRC violations. In such cases, better routing stratgies may be employed, however, this compromises on time and memory. Once routing is completed, parasitic resistances and capacitances associated with routes come into picture. These parasitics can be extracted into a SPEF file. In newer openLANE versions, SPEF extraction is a part of routing run. Following this, post-route STA may be carried out.

## Differences from older OpenLANE versions
- In the new version, FP_CORE_UTIL, FP_CORE_VMETAL and FP_CORE_HMETAL environment variables are missing in ```ioPlacer.log``` and ```config.tcl```. They need to be included in ```config.tcl``` file.
- ```run_floorplan``` fails after the STA analysis in the new version. An alternate command can be used: ```init_floorplan```
- SPEF extraction need not be externally performed in the new version. It has been integrated into the OpenLANE flow

Note: In the new version following commands may be used for an error-free flow:

```
init_floorplan 
place_io
global_placement_or
detailed_placement 
tap_decap_or
detailed_placement
gen_pdn
run_routing
```

## Future Scope
- Design of custom standard cells such as NAND, OR, clock buffers and integrating them in the openLANE flow.
- Detailed IP characterization for all corner models

## References 
- [The OpenROAD Project](https://github.com/The-OpenROAD-Project/OpenLane)
- [Nickson Jose](https://github.com/nickson-jose/vsdstdcelldesign)
- [Kunal Ghosh](https://github.com/kunalg123)
 







