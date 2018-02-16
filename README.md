# Automatic super and public properties

Current

```javascript

class Point2D {
    constructor(x, y) {
        this.x = x
        this.y = y
    }
}

class Point3D extends Point2D {
    constructor(x, y, z) {
        super(x, y)
        this.z = z
    }
}

```

Proposed

```javascript

class Point2D {
    constructor(x, y)
}

class Point3D extends Point2D {
    constructor(super x, super y, z)
}

```

Notice:
1. super keyword qualifying x and y params.
2. no body for constructor results in z being public member of Point3D
3. no body for constructor results in x and y being public member of Point2D
