# buybackcalc
Nushares buyback and Peercoin reserve operations calculator

This calculator script computes the weekly [Nushares buyback](https://discuss.nubits.com/t/passed-motion-to-begin-nsr-buyback-immediately/2654) amount. The official calculation thread is [here](https://discuss.nubits.com/t/nsr-buyback-calculations/3347).

## install
The calculator is written so that it can be run on any generic unix computer, and has been tested on
 * Ubuntu linux
 * Raspbian on a Raspberry Pi
 * Cygwin on Windows
 * DOS `cmd` window on Windows.

The calculators needs to communicate with a running Nu server (`nud`) to get current Nubits moneysupply. So when running the calculator, `nud` should be running and synchronized with Nu network. You should edit the code on line

`NUD=./daemon/nd`

to add the command line that runs `nud` on your computer. For example `./daemon/nd` is how I run `nud` on Windows command line.

## run the calculator
* On linux or Cygwin, just run

`./buybackcalc`

if execution permission is set for the script. 

* In a DOS `cmd` window, I run the script with

`bash buybackcalc` 

where bash is Cygwin binary.

* If nud is not running and you know the Nubits moneysupply, you can uncomment the line

`#totalNBT=`

and add Nubits moneysupply by hand. The calculation results would be correct.
