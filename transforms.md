# Transforms

Matrix transform are the basics of all vector transforms. The MVP matrix is the final matrix which whom the vertex points are being multiplied with. The MVP matrix consists of (in multiplication order) the projection (P) matrix, the view (V) matrix and the model (M) matrix.

$MVP = projection \cdot view \cdot model$

## Model matrix

The model matrix defines the transforms of the givin model within it's world space. This usually can be calculated with a TSR or TSRS multiplication. Starting mit the translation (T) matrix following the scale (S)matrix ending with the rotation (R) matrix. Additionally an other post rotation scale can be added in order to scale after the rotation was applied.

$model = translation \cdot scale \cdot rotation (\cdot \text{second-scale})$

Depending if the matrices are column or row based one might need to use the inverse of what is shown here. The following examples are row based matrices.

translation = {

```text
    1, 0, 0, x
    0, 1, 0, y
    0, 0, 1, z
    0, 0, 0, 1
```

}

| Library  | Function                     |
| -------- | ---------------------------- |
| SDL2/GLM | `glm::translation(vec3 pos)` |
| OGL 3    | `glTranslated(x, y, z)`      |

scale = {

```text
    x, 0, 0, 0
    0, y, 0, 0
    0, 0, z, 0
    0, 0, 0, 1
```

}

| Library  | Function               |
| -------- | ---------------------- |
| SDL2/GLM | `glm::scale(vec3 pos)` |
| OGL 3    | `glScaled(x, y, z)`    |

rotation_x = {

```text
    1,      0,       0, 0
    0, cos(x), -sin(x), 0
    0, sin(x), cos(y), 0
    0,       0,      0, 1
```

}

rotation_y = {

```text
    cos(a),  0,  sin(a), 0
    0,       1,       0, 0
    -sin(a), 0,  cos(a), 0
    0,       0,       0, 1
```

}

rotation_z = {

```text
    cos(a), -sin(a), 0, 0
    sin(a),  cos(a), 0, 0
         0,       0, 1, 0
         0,       0, 0, 1
```

}

| Library  | Function                          |
| -------- | --------------------------------- |
| SDL2/GLM | `glm::rotate(angle, vec3 offset)` |
| OGL 3    | `glRotated(angle, x, y, z)`       |

### Quaternion representation



[Back](./)
