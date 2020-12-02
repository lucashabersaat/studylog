---
description: The project for the course phsyically based simulation in computer graphics
---

# solar system simulation

`studies` `c++`

## resources

* [Brittle Fracture](http://graphics.berkeley.edu/papers/Obrien-GMA-1999-08/Obrien-GMA-1999-08.pdf)
* Fast Multipole
  * Wikipedia
  * [Javascript Implementation](https://github.com/davidson16807/fast-multipole-method/blob/master/fast-multipole-method-optimized.js)

{% embed url="https://gitlab.ethz.ch/halucas/pbs20\_solarsystem" caption="Repository" %}



## time tracking

<table>
  <thead>
    <tr>
      <th style="text-align:left">Date</th>
      <th style="text-align:left">Hours worked</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">27.10.2020</td>
      <td style="text-align:left">8</td>
      <td style="text-align:left">
        <p>Project started,</p>
        <p>first meeting,</p>
        <p>Scenes added,</p>
        <p>naive gravitational force</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">28.10.2020</td>
      <td style="text-align:left">2.5</td>
      <td style="text-align:left">cleanup Scenes,
        <br />add ThreeBodyScene,
        <br />fix Scene change</td>
    </tr>
    <tr>
      <td style="text-align:left">31.10.2020</td>
      <td style="text-align:left">2.5</td>
      <td style="text-align:left">
        <p>Fasten Narrow Phase Collision Detection Loop,</p>
        <p>Put BoundarySphere into RigidObject</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">2.11.2020</td>
      <td style="text-align:left">0.5</td>
      <td style="text-align:left">Review Tati&apos;s Broad Phase Collision Detection</td>
    </tr>
    <tr>
      <td style="text-align:left">3.11.2020</td>
      <td style="text-align:left">6</td>
      <td style="text-align:left">
        <p>AsteroidScene,</p>
        <p>Debug Fixd Grid Space Partitioning</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">5.11.2020</td>
      <td style="text-align:left">2</td>
      <td style="text-align:left">First Test Rendering in blender</td>
    </tr>
    <tr>
      <td style="text-align:left">10.11.2020</td>
      <td style="text-align:left">4.5</td>
      <td style="text-align:left">
        <p>Looked into Fracture,</p>
        <p>started Collision Scene</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">12.11.2020</td>
      <td style="text-align:left">0.75</td>
      <td style="text-align:left">Fracture Paper lese</td>
    </tr>
    <tr>
      <td style="text-align:left">17.11.2020</td>
      <td style="text-align:left">4</td>
      <td style="text-align:left">Created scenes for milestone presentation</td>
    </tr>
    <tr>
      <td style="text-align:left">18.11.2020</td>
      <td style="text-align:left">2</td>
      <td style="text-align:left">Milestones Presentation</td>
    </tr>
    <tr>
      <td style="text-align:left">21.11.2020</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Rendering scenes</td>
    </tr>
    <tr>
      <td style="text-align:left">23.11.2020</td>
      <td style="text-align:left">2</td>
      <td style="text-align:left">Fracture math</td>
    </tr>
    <tr>
      <td style="text-align:left">24.11.2020</td>
      <td style="text-align:left">3</td>
      <td style="text-align:left">Fracture structure and math</td>
    </tr>
    <tr>
      <td style="text-align:left">29.11.2020</td>
      <td style="text-align:left">3</td>
      <td style="text-align:left">Fast Multipole continued</td>
    </tr>
    <tr>
      <td style="text-align:left">1.12.2020</td>
      <td style="text-align:left">5</td>
      <td style="text-align:left">
        <p>Debug Fast Multipole,</p>
        <p>export in framework/import in blender</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">2.12.2020</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Debug Fast Multipole</td>
    </tr>
  </tbody>
</table>

## log

* 27.10.2020: project started, worked till 22:00, Tamara can be very critical, that's nice
* 2.12.2020: after milestone presentation we dropped fracture, as it is too much and instead implement a faster gravitational loop, to be able to simulate thousands of objects for some nice n-body simulations.

