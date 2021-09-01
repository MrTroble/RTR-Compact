# Light and Color

This is currently a run down of ***Realtime Rendering 4th Edition*** Chapter 8 ***Light and Color***. It will be expanded upon with various other resource when time comes.

## Radiometry

| Name              | Symbol   | Units           | Explanation                                     | Equation                          |
| ----------------- | -------- | --------------- | ----------------------------------------------- | --------------------------------- |
| solid angle       | $\omega$ | steradians (sr) | surface area of a $\dfrac{1}{4\pi}$ unit sphere | $\omega = \dfrac{A_{patch}}{r^2}$ |
| radiant flux      | $\Phi$   | watt (W)        | power -> flow of radiant energy per time        | measured?                         |
| irradiance        | E        | $W / m^2$       | density of radiant flux per area                | $\dfrac{d\Phi}{dA}$               |
| radiant intensity | I        | W/sr            | density of radiant flux per steradian           | $\dfrac{d\Phi}{d\omega}$          |

Solid angle further reading: [https://mathworld.wolfram.com/SolidAngle.html](https://mathworld.wolfram.com/SolidAngle.html)

[Back](./)
