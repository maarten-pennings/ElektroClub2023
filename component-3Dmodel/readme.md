# Model

Modeling a PCB including one's own components.


## Introduction

Most EDA tools - including [easyeda](easyeda.com) - can render a PCB in 3D.
This render includes the components that are on the PCB, provided that each component has an associated 3D model.
If a component doesn't have one, you may model one yourself, for example in Fusion 360, and add it to the EDA tool.


## Steps

 - Draw the component in some tool, e.g. Fusion 360, using real colors for its parts (plastic housing, copper wires).
 - Export the modeled component as .obj file (this is a text file).
 - Create a file describing the colors - an .mtl file.
    - Create an empty text file with the same name as the .obj file but with extension .mtl.
    - In the .obj file find all lines that define a color, they start with `usemtl`.
      For example `usemtl ABS_(White)`.
    - For each distinct color, create a section in the .mtl file, with `newmtl` and the same color name.
      For example `newmtl ABS_(White)`.
    - Add a line `Kd` with three values denoting the RGB values as fraction.
      For example `Kd 0.90 0.90 0.90`.
    - I suggest to append a white line at the end of the section (as third line).
    - Both the .obj and the .mtl file maye have comments: lines starting with `#`
 - Create a zip with the .obj and the .mtl file, suggested to give it the same base name.


## Example

The (abridged) `example.obj` file exported by design tool (Fusion 360).

```text
# WaveFront *.obj file (exported)
...

usemtl ABS_(White)
f 1/1/1 2/2/2 4/3/3
f 4/3/3 2/2/2 3/4/4
f 5/5/5 1/6/6 6/7/7
...

usemtl Nylon_12_(with_Formlabs_Fuse_1_3D_Printer)
f 130/385/385 131/386/386 129/387/387
f 129/387/387 131/386/386 134/388/388
f 134/388/388 131/386/386 133/389/389
...

usemtl ABS_(White)
f 141/421/421 142/422/422 144/423/423
f 144/423/423 142/422/422 143/424/424
f 145/425/425 141/426/426 146/427/427
...
```

The handcrafted `example.mtl` file.

```text
# .mtl file handcrafted by Maarten Pennings

newmtl ABS_(White)
Kd 0.90 0.90 0.90

newmtl Nylon_12_(with_Formlabs_Fuse_1_3D_Printer)
Kd 0.15 0.15 0.15
```

The `example.zip` contains `example.obj` and `example.mtl`.


## Real

Check out the micro USB plug model
 - [MicroUSB-2pin-poweronly-TH.obj](MicroUSB-2pin-poweronly-TH.obj)
 - [MicroUSB-2pin-poweronly-TH.mtl](MicroUSB-2pin-poweronly-TH.mtl)
 - [MicroUSB-2pin-poweronly-TH.zip](MicroUSB-2pin-poweronly-TH.zip)


(end)


