triangulate-polyline
====================
Triangulates a polygon with holes encoded as a list of loops.

# Example

```javascript
var triangulate = require("triangulate-polyline")


```

# Install

```
npm install triangulate-polyline
```

# API

#### `require("triangulate-polyline")(loops, positions)`
Triangulates a complex polygon

* `loops` is a list of vertices of the polygon, where each vertex is represented as an index into `positions`
* `positions` is a list of vertex positions encoded, each represented by a length 2 array

**Returns** A list of triangles represented by triples of indices of position indices.

**Note** This library is built on top of poly2tri, which is not robust.  Points which are close together or near the boundary of other loops may be incorrectly classified and could result in broken triangulations.

# Credits
(c) 2014 Mikola Lysenko. MIT License