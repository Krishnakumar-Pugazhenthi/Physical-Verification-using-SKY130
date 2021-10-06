# **Physical Verification using SKY130**

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY1/PV.jpeg)

## Table of Contents

Day 1 - Introduction to SkyWater SKY130 and Open-Source EDA Tools.
Day 2 - Design Rule Checks and Layout Vs. Simulation.
Day 3 - Design Rule Checking.
Day4 - Openlane Flow
Day 5 - Running Layout Vs. Schematic.


## *Day 1 - Introduction to SkyWater SKY130 and Open-Source EDA Tools*



**SKY130 Layers:**

Metal Layers

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY1/metal%20layer.png)

There are 5 Layer of Aluminium metal


Metal Layers and Via is called Backend Layers

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY1/backendlayers.jpg)

The local interconnects, wells are called as Front-end layers.The local interconnect is used to connect VDD and Gnd  and cannot be used for Routing

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY1/frontendlayers.jpg)

The other layers are High voltage layer and Mim Cap layers.


MAGIC

```
magic -d XR
```
We can change the values of the components in the parameter box

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY1/magic_param.jpg)


![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY1/magic_eg.jpg)

Opening Xschem

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY1/xschem_open.jpg)

Choosing MOS symbols from Library

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY1/mosfromlib.jpg)

Renaming the Pins

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY1/renaming%20fet.jpg)

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY1/renamefet_2.jpg)


Xschem Inverter Diagram

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY1/xschem_3.jpg)

Inverter Symbol

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY1/symbol_inv.jpg)

Inverter Spice 

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY1/inv_spice.jpg)

Inverter Waveform

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY1/inv_waveform.jpg)

Opening Inverter.spice file in Magic

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY1/spiceinmagic.jpg)

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY1/inv_1.jpg)

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY1/inv_2.jpg)


## *Day 2 - Design Rule Checks and Layout Vs. Simulation*

### GDS read and Input Styles

Listing styles

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/cifstyles.jpg)

Vendor Style

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/vendorstyle.jpg)

Default Style
 ![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/default%20style.jpg)

Cell manager to add a cell

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/addgate%20_cellmanager.jpg)

GDS read

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/gdsread.jpg)

Checking for duplicates

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/duplicates.jpg)

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/duplicate%20result.jpg)


### Ports and Port Indexes

Lef Read

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/lefread.jpg)

 
![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/lefspiceexecuted.jpg)


![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/moreports.jpg)

Port Name, Class, Use

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/port_def.jpg)


Abstract View

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/abstractgate_select.jpg)

Readspice to change Port 3 name from X

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/changeport.jpg)

Port 3 is changed to gnd after readspice

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/changedtovgnd.jpg)


### Basic Extraction

Extraction

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/extract_1.jpg)

Spice file created from extraction

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/extractfile_2.jpg)

Extracting with parasitic capacitance

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/cthres0_3.jpg)

Reduce the number of parasitics in the netlist

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/cthres0.1_4.jpg)

spice file

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/ngspice_thres_5.jpg)

Running a full R-C extraction

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/extresist_6.jpg)

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/extresist_7.jpg)

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/extresist_8.jpg)

The spice netlist consist of both R and C

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/extresist_9.jpg)

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/extresist_10.jpg)


DRC Check

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/drcevaluate_11.jpg)

DRC error 

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/rcerror_12.jpg)

DRC checked is changed to 7 in DRC tab in the layout

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/drcchange_13.jpg)

The type of error is displayed

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/error_display_14.jpg)

LVS Command 

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/lvs_16.jpg)

Netlist Match

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/lvsfile_17.jpg)

Loading AND

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/xor_load_18.jpg)

Erase Polysil

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/erase_19.jpg)

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY2/erase_shown.jpg)



# *Day 3 - Design Rule Checking*

### Width and Spacing Rules

Width rule error

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/drcerrortype_1.jpg)

The error is not shown when only the metal is selected

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/noerror_onlymetal2.jpg)

Criteria for the error to be solved

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/criteria_3.jpg)

Width is corrected

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/widthcorrected_4.jpg)

Spacing between metal error

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/spacinferror_5.jpg)

Spacing error rule is corrected

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/spacingcorrected_6.jpg)

### Wide Spacing and Notch Rules

Wide spacing error

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/widespaceerror_7.jpg)

Wide Spacing error is corrected

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/widespaceresolved_8.jpg)

Notch rule

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/notchrule_9.jpg)

### Contact Cuts (Via) and its DRC Errors

Via error

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/viasize_10.jpg)

Via error Corrected

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/viasizecoorected_11.jpg)

Types of Contact Cuts

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/contactcuttypes_12.jpg)

Multiple contact cuts

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/seecontactcuts_13.jpg)

Single contact cut

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/onecutcontact_14.jpg)

No room for contact cut

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/noroomforcontactcut_15.jpg)

Metal overlap on local interconnect

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/metaloverlaperror_16.jpg)

Metal overlap error corrected

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/overlaperrorfixed_17.jpg)

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/overlapsolved_18.jpg)

### Minimum Area and Minimum Hole Rule

Minimum area rule

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/actualerror_20.jpg)

Error in area

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/minarea_19.jpg)


Minimum area rule corrected

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/rectify_21.jpg)

Minimum Hole error

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/minholeerror_22.jpg)

Minimum Hole error corrected

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/errorcorrect_23.jpg)

### Wells and Deep N-Wells

Set DRC type to full before checking for Wells

Nwell error

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/nwelerror_24.jpg)

Error after creating a tap to correct a well error

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/taperror_25.jpg)

Error is Corrected
![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/fixall_26.jpg)

Pwell has to be connected if it has a tap

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/pwellconnectedtap_27.jpg)

Deep well error

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/deepwellerror_28.jpg)

Deep well error corrected

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/deepwellfixed_29.jpg)

### Derived Layers

NMOS LVT

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/nmoslvt_30.jpg)

NMOS

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/nmos_31.jpg)

Cif Commands

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/ciffsee_32.jpg)

See LVTN

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/seelvtn_33.jpg)

High Voltage Implant

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/cifseehvi_34.jpg)

NDSM HVI

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/ndsmhvi_35.jpg)

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/final_36.jpg)

Cif see NPC

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/npc_37.jpg)


Satisfies all width and spacing rule for NPC 

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/satisfiesall_38.jpg)


Different arrangement

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/diffarrangement_39.jpg)

### Parameterised and PDK Devices

Metal minimum area error

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/parametererror_40.jpg)

Error Corrected

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/errorcorrected_41.jpg)

Cell points to valid GDS file with property command

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY3/property_42.jpg)



# *Day 4: OpenLane Flow*


**OPENLANE**

Openlane creates an automated GDSII file.The openlane automates from RTL synthesis stage till verification after which a GDSII file is created. GDSII file contains the entire design architecture such as memory, design , IP's in a binary file format.

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Advanced-Physical-Design-using-OpenLANE-SKY130/blob/main/DAY1/openlane_flow.jpg)

**Synthesis:**

RTL is converted to gate level representation using the synthesis tools

-   `Yosys`  - Performs RTL synthesis
-   `abc`  - Performs technology mapping
-   `OpenSTA`  - Performs static timing analysis on the resulting netlist to generate timing reports

**Floorplanning:**

It is the arrangement of logical blocks such as Logic gates, multiplexers and even macros.

**Placement:**

It is the process of placing the standard cells in the suitable physical location on the floor plan area.

**Routing:**

In the routing stage all the interconnections are made and precise paths for each nets is determined. There are two types of routing namely Global and Detailed Routing.

**RC Parasitic extraction** is done by magic.

**Physical verification** is done by Magic, Klayout, Netgen

Invoke the docker to open OpenLANE
```
/Desktop/work/tools/openlane_working_dir/openlane$ docker
```

The following command is to open it in an interactive mode where we can execute in a step by step manner.

```
bash-4.2$ ./flow.tcl -interactive
```


# *DAY 5- Running LVS*

### Introduction to LVS

Invoking Netgen

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/invokenetgen_1.jpg)

LVS of netA.spice and netB.spice

![!\[enter image description here\](https://github.com/Krishnakumar-](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/spicefiles_2.jpg)

Since there are no subcell definitions in the spice netlist, the following error is occurs during simulation

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/cannotrunspice_3.jpg)

However, since LVS considers only  the difference between netlists of  Layout and Schematic here it matched successfully

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/success_4.jpg)

Comp.out file

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/comp_5.jpg)

Changes are made to netA.spice file

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/changespice_6.jpg)

We get a mismatch while running netgen

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/netlistmismatch_7.jpg)


While running the netlist again with LVS we have to either reinitialize or quit and open a new netgen tab

Comp.out file

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/spiceoutput_8.jpg)

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/spiceoutput_9.jpg)



### LVS with Subcircuits

Subcircuits in spice files

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/subckt_10.jpg)

Running the LVS

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/nodevice_11.jpg)

Execute at Subcircuit level

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/subckt_12.jpg)

Netlist matched successfully

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/subcktnetlistmatch_13.jpg)

Comp.out file

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/comp_14.jpg)

Changing Pin order in netA.spice

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/pinorder_15.jpg)

But the netlist matches

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/stillmatch_16.jpg)

Swapping pins A and C

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/swappins_17.jpg)

Netlist matches but cells matching failed

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/cellsmismtach_18.jpg)

Comp.out file

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/cout_19.jpg)


### LVS with Blackbox Subcircuits

The below netlists are executed for LVS with the following command
```
./run_lvs.sh
```
Netlist with empty Subcircuit definitions

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/emptysubcircuit_20.jpg)

Information about each subcell is printed when LVS is run from terminal

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/info_21.jpg)
 
 Disconnected Nodes in Comp.out file
 
![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/disconnectednode_22.jpg)

Changing Pin order at Subcircuit level

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/changepinorder_23.jpg)

Netlist is mismatched

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/netlistmismatch_24.jpg)

Comp,out file

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/cout_25.jpg)

Edit netA.spice with pins ABD

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/changetoabd_26.jpg)

Netlist not matched

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/netnotmatch_27.jpg)

Comp.out file

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/cout_28.jpg)

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/cout_29.jpg)

Changing the cell name in net A.edit file

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/cellnamechange_30.jpg)

Comp.out file

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/cout_31.jpg)

### LVS with SPICE Low Level Components

Subcircuits with Resistors and Capacitors

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/addcomponent_32.jpg)

LVS run

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/runlvs_33.jpg)

After swapping the pins to CBA in netA.spice the netlist mismatches
 
![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/swappins_34.jpg)

To allow cell swapping we must intimate the netgen which can be done by the below command in the run_lvs.sh script

```
permute "-circuit1 cell1" A C
permute "-circuit2 cell1" A C
```
![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/allowswap_35.jpg)


### LVS For Power-On-Reset Circuit

Changing directory to open Xschem

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/analog_36.jpg)

Xschem File

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/xschem_37.jpg)

Power on Reset circuit

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/poweron_38.jpg)

In the netlist spice file the subcircuit is present as a comment

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/subcrctcomment_39.jpg)

Selecting LVS netlist  to  Top level is subcircuit 

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/fixerror_40.jpg)

After running the netlist below is the output in spice file

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/fixed_41.jpg)

user_analog_project_wrapper.mag in Magic

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/poweroninmagic_41.jpg)

Extracting the file

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/extract_42.jpg)

Netlist mismatch after LVS

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/afterwrapper_43.jpg)

The standard cells are not included in the netlist and they are treated as blackboxes. 

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/probelminstdcell_44.jpg)

Comp.out file 

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/proxyinnetlist_45.jpg)

Analog wrapper file in Xschem

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/rerun_46.jpg)

### Layout Vs. Verilog for Standard Cell

Since netlist is compared to Verilog there is no schematic capture.

Extraction

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/verilog_47.jpg)

Digital.pll file

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/digitallpll_48.jpg)

Netlist mismatch in LVS check

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/lvs_49.jpg)

Mismatch in Comp.out file

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/mismatch%2050.jpg)

FILLER_0_11 present in Verilog

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/fillcell_51.jpg)

FILLER_0_11 not  present in Spice

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/notinspice_52.jpg)

FILLER_0_11 in magic

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/magic_53.jpg)


![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/emptymagic_54.jpg)

### LVS for Digital PLL Design

Extract the netlist 

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/lvsdigital_55.jpg)

LVS run

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/runlvs_56.jpg)

Comp.out file

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/cout_57.jpg)

Diode Mismatch in comp.out
![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/diodemismtach_58.jpg)

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/diode_59.jpg)

It is not present in Verilog file

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/notverliog_60.jpg)

Selecting cell to find out the node

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/slecetcell_61.jpg)

Node connection is found with commands in tkcon window

![enter image description here](https://github.com/Krishnakumar-Pugazhenthi/Physical-Verification-using-SKY130/blob/main/DAY5/last_62.jpg)
