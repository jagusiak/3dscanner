## Device schema
![Scanner Top View Schema](https://user-images.githubusercontent.com/9595719/82748024-e88a6900-9d9e-11ea-82f0-ffd32c83a73a.png)

**(1) Bed Table**

Scanned object are placed on bed table.

Properties:

- can rotate 360 degrees,
- its current angle rotation is precise and known.

**(2) Camera**

Camera allows to determine surface point in 3d space using laser marker on image (See (3)).

Properites:

- it is always placed in constant distance from **Bed Table** center (constant radius laength),
- can rotate 180 degrees,
- lens is always aimed at the center of **Bed Table**,
- its current angle rotation is precise and known.

**(3) Vertical Laser**

Laser puts vertical laser light on object.

Properites:

- it is in fixed position (angle 0),
- laser is poiting to the **Bed Table** center.


## Rotation mechanism

![Rotation](https://user-images.githubusercontent.com/9595719/82751618-bb4ab480-9db8-11ea-87eb-33d6e573618e.png)

**(1) Main wheel**

This part is rotated. Contains cogs on the edge with radius _R_.

**(2) Metal bearing**

This part is responsible for fluent **Main Wheel** roataion and reducing friction.

**(3) Step motor with cogs**

Step motor with cogs of radius _r_ and _S_ steps per rotation.

**(4) Tensioner**

Adds extra force on **Belt** to avoid sliding.

**(5) Belt**

Transfers **Step motor** rotation to **Main wheel**.

### Calculations

_R_ ~= 0.149 _L_ - 0.532 _r_ 

_Precision_ ~= 360 / ( _S_ (0.149 _L_ / _r_ - 0.532))

Example:

Belt _L_ = 800mm, Motor steps _S_ = 64, Motor radius _r_ = 5mm

Produces:

_R_ ~= 119mm

_Precision_ ~= 0.25 degree 
