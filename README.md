### Device schema
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
