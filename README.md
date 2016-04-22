# buybackcalc
Nushares buyback and Peercoin reserve operations calculator

This calculator script computes the weekly [Nushares buyback](https://discuss.nubits.com/t/passed-motion-to-begin-nsr-buyback-immediately/2654) amount. The official calculation thread is [here](https://discuss.nubits.com/t/nsr-buyback-calculations/3347).

## install
The calculator is written so that it can be run on any generic unix computer, and has been tested on
 * Ubuntu linux
 * Raspbian on a Raspberry Pi
 * Cygwin on Windows

## run the calculator
* On linux or Cygwin, just run

`./buybackcalc`

if execution permission is set for the script. 

* By default the calculator uses https://alix.coinerella.com/panel/api/?getinfo to get Nubits moneysupply online. If alix cannot be used, the calculators can communicate with a running Nu server (`nud`) to get current Nubits moneysupply. In this case when running the calculator, `nud` should be running and synchronized with Nu network. You should edit the code at line

`NUD=../daemon/nd`

to add the command line that runs `nud` on your computer. For example `../daemon/nd` is how I run `nud` on Windows command line. After these change, you can run the calculator using `nud`

`buybackcalc -n`

* If you want to set the Nubits moneysupply by hand, you can run the calculator

`buybackcalc -m _<moneyspply>_`
