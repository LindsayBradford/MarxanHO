# Marxan with Heuristic Ordering C source code

This is the C source code for 'Marxan with Heuristic Ordering' (MarxanHO), a modification of the static Marxan 2.4.4 source repository, from which this project was forked.

Compiled 32-bit and 64-bit Windows binaries of this project can be requested directly from [Lindsay](mailto:lindsay.w.bradford@gmail.com). 

This  software is intended to be compiled with GCC (the GNU Compiler Collection) and to be platform independant between Linux, OSX, Windows. 

This repository includes C source code to generate compiled binary executables for the Command Line Interface (CLI) application that is Marxan itself, and some related CLI applications.

## Licence:
As per Marxan copyright licencing requirements, this repository operates under the [GNU AFFERO GENERAL PUBLIC LICENSE](http://www.gnu.org/licenses/agpl-3.0.html). 

## Usage:

The input.dat file for Marxan now recognies the following new directive:
  `SAVEHEURISTICORDER [1-3]`

As per typical Marxan "SAVE" directives, a value of "1" outputs the heuristic ordering filer as per the original Marxan format, "2" for an ArcView compatible format, and "3" for a general-purpose CSV file format.

In scenarios where Marxan has been configured to run heuristics with the above directive, new output file(s) will be generated that report the order in which planning units are reserved via the heuristic chosen. 

These output files are stored in same output directory as all other Marxan output files, and follow convention by taking the general file format of `output_ho<rRunNumber>.[dat|txt|csv]`

If the SAVEBEST directive is active, there will also be an `output_hobest.[dat|txt|csv]` 
present for the best run identified in a number of replicates. 
  
