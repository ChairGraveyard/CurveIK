# CurveIK

CurveIK is an IK library for Unreal Engine 4. It provides a simple, single bone chain (no branches) solver that uses bezier curves to model the path of the bone chain.

This repo contains the initial release of the project - use in commercial projects should be done cautiously.


[Demo](#demo)

[Animation Blueprints](#animation-blueprints)

[Solver](#solver)

[Debug](#debug)

## Demo

![Image not found, I wonder why](https://raw.githubusercontent.com/dharness/CurveIK/master/Docs/All_3_vs.gif)

## Animation Blueprints

CurveIK provides a single animation blueprint node:

![Image not found, I wonder why](https://raw.githubusercontent.com/dharness/CurveIK/master/Docs/AnimationBlueprintNode.png)

## Paramaters

#### Solver

| Property        | Usage           |
| ------------- |:-------------|
| Curve Type      | Which type of curve the bones align with |
| Tip Bone      | The last bone in the chain to be affected      |
| Root Bone | The first bone in the chain to be affected      |
| Max Iterations | Increasing this value can increase accuracy but may affect performance if set too high|
| Curve Detail | The number of subdivisions the curve is partitioned into. Increasing this value should make the curve smoother, but may affect performance |
| Curve Fit Tolerance | The acceptable amount of error between bone positions and the calculated curve position |
| Stretch | The degree to which the bones should stretch to fit the curve more precisely. High values will create short bones in areas of the curve with more bends, and longer bones in straight areas. |
| Handle Angle | The angle of offset (in degrees) for the bezier handles. The owning component's up vector is defined to be 0-degrees |


#### Debug

To Debug your IK setup, enable debug draw in the details panel.

![Image not found, I wonder why](https://raw.githubusercontent.com/dharness/CurveIK/master/Docs/debug.gif=250x250)


##### Show Normals
![Image not found, I wonder why](https://raw.githubusercontent.com/dharness/CurveIK/master/Docs/ShowNormals.png=250x250)
##### Show Tangents
![Image not found, I wonder why](https://raw.githubusercontent.com/dharness/CurveIK/master/Docs/ShowTangents.png=250x250)
##### Show Bone Direction
![Image not found, I wonder why](https://raw.githubusercontent.com/dharness/CurveIK/master/Docs/ShowBoneDirection.png=250x250)
##### Show Links
![Image not found, I wonder why](https://raw.githubusercontent.com/dharness/CurveIK/master/Docs/ShowLinks.png=250x250)