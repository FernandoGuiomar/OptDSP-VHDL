# FIR Filter VHDL Implementation
## Block Operation
### Generic
* **bitWidth**    : Input/Output data bitwidth
* **coeffFiles**  : *.txt file with values of the coefficients stored (obtained from MATLAB). The path of the coefficients file is obtain in relation to the origin (project/project.scr/new/).
* **nTaps**       : Total number of taps of the FIR filter         
### Port
* **clk**         : Input clock port
* **inputData**   : Input data bus port
* **outputData**  : Output data bus port         
## Description
![FIR_Filter](https://github.com/FernandoGuiomar/OptDSP-VHDL/blob/main/Figs/FIR_Filter.png)

The operation of the FIR filter can be described in three different parts:
* Multiplication of the input signal by the different values of the coefficients of the filter (signal array multOut in the figure)
* The sum of the signal arrays from the multiplication operation (multOut) with the values from the previous clock cycle (regOut). 
* The transition of the values from the previous clock cycle (sumOut array signal) to the level of the ongoing clock cycle (regOut array signal).
