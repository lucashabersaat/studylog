---
description: The project for the course phsyically based simulation in computer graphics
---

# solar system simulation

`studies` `c++` `computer graphics` `simulation`

## overview

For the master course Physically based Simulation in Computer Graphics, a group project is done with a topic of free choosing. Together with _Tamara Gini_ and _Tatiana Gerth_, we chose to to a rigid body simulation with gravitational forces and later implement fracture. After feedback of the assistants, we dropped fracture, as it's not feasible for the time given, and did a **Fast N-Body Simulation** instead.

Using the **Fast Multipole** method, we reduced complexity of the force computation between each pair of bodies from `O(n²)` to `O(nlogn)` and setup some scenes with high number of bodies up until 100k that run in reasonable time periods.

### result

_todo_

## references

* [Repository](https://gitlab.ethz.ch/halucas/pbs20_solarsystem)
* [Brittle Fracture](http://graphics.berkeley.edu/papers/Obrien-GMA-1999-08/Obrien-GMA-1999-08.pdf)
* Fast Multipole
  * Wikipedia
  * [Javascript Implementation](https://github.com/davidson16807/fast-multipole-method/blob/master/fast-multipole-method-optimized.js)

## features

### fast multipole

_todo_

### threading

Using the [concurrent\_unordered\_map ](https://docs.microsoft.com/en-us/cpp/parallel/concrt/parallel-containers-and-objects?view=msvc-160#unordered_map)from c++ in the FMM class instead of the `unordered_map`, the particles can be added in parellel.

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
      <td style="text-align:left">?</td>
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
      <td style="text-align:left">?</td>
      <td style="text-align:left">Debug Fast Multipole</td>
    </tr>
    <tr>
      <td style="text-align:left">8.12.2020</td>
      <td style="text-align:left">9</td>
      <td style="text-align:left">Normal Fast Multipole</td>
    </tr>
    <tr>
      <td style="text-align:left">9.12.2020</td>
      <td style="text-align:left">9</td>
      <td style="text-align:left">Particle System</td>
    </tr>
    <tr>
      <td style="text-align:left">12.12.2020</td>
      <td style="text-align:left">7.5</td>
      <td style="text-align:left">Vicinity Methods, Scene Setup</td>
    </tr>
    <tr>
      <td style="text-align:left">13.12.2020</td>
      <td style="text-align:left">9</td>
      <td style="text-align:left">Threading, Presentation, New Scenes</td>
    </tr>
    <tr>
      <td style="text-align:left">14.12.2020</td>
      <td style="text-align:left">7</td>
      <td style="text-align:left">Finish Presentation, Debug Grid, More Scenes</td>
    </tr>
    <tr>
      <td style="text-align:left">15.12.2020</td>
      <td style="text-align:left">4</td>
      <td style="text-align:left">Presentation</td>
    </tr>
    <tr>
      <td style="text-align:left">Total</td>
      <td style="text-align:left">~90h</td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>



