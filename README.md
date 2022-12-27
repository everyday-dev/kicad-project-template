# 2-Layer KiCAD Template
![3d photo of the atmega32u4 breakout board](img/3d.png)
## Intro
Template for 2-Layer KiCAD projects. Stackup follows the PCBWay standard stackup and the design rules are setup to be the smallest and most accomodating without going into the "Advanced" process thus greatly increasing the price of board fabrication. There are really two major rules that drive board complexity:
- Min Track/Spacing: 5mil
- Min Hole Size: 0.25mm

## Updating Project Name
To update the project name, you must rename all three of the base files - the schematic, PCB and the project file. The folder in which these files reside can be named whatever you'd like.
```shell
mv kicad-2-layer-template.kicad_pro NEW_PROJECT_NAME.kicad_pro
mv kicad-2-layer-template.kicad_sch NEW_PROJECT_NAME.kicad_sch
mv kicad-2-layer-template.kicad_pcb NEW_PROJECT_NAME.kicad_pcb
```

## 3D Models
In some cases you will use a component that does not have a 3D model built-in to KiCAD. You can place these ```.step``` or ```.wrl``` files in the ```models/``` folder.
To reference them you can use the KiCAD Project variable (```KIPROJMOD```) to set a relative path to these models when updating the pcb component properties. Ex:
```
${KIPRJMOD}/../models/EXAMPLE_MODEL.step
```

## Schematic Variables
Several variables are already set such as a company name, license type, revision etc. Be sure to update these with your variables as needed. These settings are accessible by opening a ```.kicad_sch``` file and then navigating to ```File > Page Settings```