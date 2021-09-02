# Light and Color

This is currently a run down of ***Realtime Rendering 4th Edition*** Chapter 8 ***Light and Color***. It will be expanded upon with various other resource when time comes.

## Radiometry and Photometry

| Name              | Symbol   | Units           | Explanation                                          | Equation                          |
| ----------------- | -------- | --------------- | ---------------------------------------------------- | --------------------------------- |
| solid angle       | $\omega$ | steradians (sr) | surface area of a $\dfrac{1}{4\pi}$ unit sphere      | $\omega = \dfrac{A_{patch}}{r^2}$ |
| radiant flux      | $\Phi$   | watt (W)        | power -> flow of radiant energy per time             | measured?                         |
| irradiance        | E        | $W / m^2$       | density of radiant flux per area                     | $\dfrac{d\Phi}{dA}$               |
| radiant intensity | I        | W/sr            | density of radiant flux per steradian                | $\dfrac{d\Phi}{d\omega}$          |
| radiance          | L        | $W/(m^2 sr)$    | density of radiant flux per ray (area and steradian) | $\dfrac{d^2\Phi}{dA d\omega}$     |

Solid angle further reading: [https://mathworld.wolfram.com/SolidAngle.html](https://mathworld.wolfram.com/SolidAngle.html)

***Radiance*** is what is to measured by sensors such as cameras. The value of L along the given ray is equivalent to the shaded surface color at the given surface point. Therefore a ***radiance distribution*** function can be defined as $L_i(x, d)$ where **x** is the 3D position and **d** is the direction (Which is 2D for some reason? TODO: Look into this.). ***Radiance*** is not effected by distance, environmental effects (I think this is intuitive? In case check the equation).

### Spectral power distributions (SPDs)

SPDs are used to visualize the lights's energy of mixed wavelength and break it down into the according wavelengths. Every radiometric quantity can be broken down into different wavelengths and can hence be visualized by a SPD. However in rendering practice SPDs are not used because of performance and practicality. See section for Colorimetry.

Further reading SPDs [https://www.sciencedirect.com/topics/agricultural-and-biological-sciences/spectral-power-distribution](https://www.sciencedirect.com/topics/agricultural-and-biological-sciences/spectral-power-distribution) and [http://hyperphysics.phy-astr.gsu.edu/hbase/vision/spd.html](http://hyperphysics.phy-astr.gsu.edu/hbase/vision/spd.html)

[Back](./)
