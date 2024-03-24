# AC/DC Converter Example

Created with [Scilab/Xcos 20024.0.0](https://www.scilab.org/download/2024.0.0/scilab-2024.0.0.bin.x86_64-linux-gnu.tar.xz) on Ubuntu 23.04.


## Scope

This example demonstrates how to model a AC/DC converter without load at a German 230V/50Hz
mains voltage supply.

One scope shows one period of the mains sine wave AC voltage.

Another scope shows the resulting DC voltage. 

![Rectifier Example](./images/ac-dc-example_1.png)

## Creation Steps

Create the rectifier the same way as done in the [Rectifier Example](../rectifier-example/README.md).

Add a transformer and a capacitor as shown above using the ***Ideal Transformer*** and the ***Capacitor*** block from ***Electrical*** with
an additional voltage measurement - use CMSCOPE instead of CSCOPE - with ***Ymin*** ***0*** Volt and ***Ymax*** ***25*** Volt.

The transformer needs a ***Turn Ratio*** of ***13.55***:

![Rectifier Example](./images/ac-dc-example_2.png)

The capacitor needs a ***C(F)*** of ***0.000001*** Farad (Microfarad):

![Rectifier Example](./images/ac-dc-example_3.png)

Link everything as shown above.

Run the simulation with the same ***Final integration time*** of 20 Millisconds.

