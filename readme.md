jme-position-plotters
===

A library to position objects such as vegetation or buildings onto a mesh.

#### CirclePlotter

The CirclePlotter creates positions that do not overlap over a given dimension.
A collection of positions are calculated by defining an amount, minimum and maximum radius, and minimum space in-between each position.
You may add as many different points as you wish, for example, one for trees, one for bushes and one for flowers.
None of the positions will overlap, as shown in the image below. 

The method is tileable and repeatable as shown in the test class.

``` java

int seed = 123;
Vector2f dimensions = new Vector2f(sizeX, sizeY)

CirclePlotter circlePlotter = new CirclePlotter(seed, dimensions);

List<Circle> bigTrees = circlePlotter.addPoints(
        20,             // amount
        10,             // min radius
        30,             // max radius
        15,             // min space between
        1000,           // max attempts
        ColorRGBA.Red   // optional : color

List<Circle> bushes = circlePlotter.addPoints(bushCount, 5, 6, 8, 1000, ColorRGBA.Green);
List<Circle> flowers = circlePlotter.addPoints(flowerCount, 1, 2, 3, 1000, ColorRGBA.Yellow);



);

```

![Cirle Plotter](https://i.ibb.co/7pVbxVy/image.png)

#### MeshPlotter

To be updated.


The mesh plotter defines valid points in a mesh based defined rules.
See the test class for a working explanation and demo of these rules.

![Mesh Plotter](https://i.ibb.co/kGLhRTN/image.png)