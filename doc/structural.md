## This is the **structural** documentation file.

# Table of Contents:

[Introduction](#Introduction)

The following components are currently documented (at least in part):

* [container](#container)
* [machine](#machine)
* [ddrwrapper](#ddrwrapper)

## Introduction

This page will give an overview of *some* of the components, especially the components at the upper levels. For lower-level components, it is recommended that state-machine diagrams or data-flow diagrams$

Contributors: please order the components within this file as they appear in Xilinx ISE.

## container
the toplevel component within the fpga design 
( [PDF](./images/container.pdf) 2Mb )
[![container](./images/container-small.jpg)](./images/container.jpg)

48MHz clock comes in, is buffered and fed to a CLKDLL
the CLKDLL outputs four clock signals that are used within the design

clk_out0 - designed to be 48MHz

clk_out1 - designed to be 24MHz

The [ddrwrapper](#ddrwrapper) component is currently not working. Its function is to provide access between the external DDR2-ram chip and the internal 'machine' component.

The [machine](#machine) component holds the significant rest of the architecture.

Other 'logic' includes signal routing, input debouncing, etc.

## machine
this component holds most of the fpga design, including CPU, Memory, VIC/SID chips

[![machine](./images/machine-small.jpg)](./images/machine.jpg)

## ddrwrapper
this component is currently not working, and will soon be removed from the design.

The End.