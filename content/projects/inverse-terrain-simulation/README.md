---
description: Bachelor's Thesis and semster project.
---

# inverse terrain simulation

`studies` `bachelor's thesis` `semester project` `python` `simulation`

## outline

The project currently consists of roughly three phases. 

1. fixing the gradients
2. finish optimization
3. ~~neural network~~

## references

* [Optimization & LBFGS](http://apmonitor.com/me575/index.php/Main/BookChapters)

## optimization

### history graph

An issue arose when calling `backward()` the second time. Some tensor's history contained computations of earlier iterations, but of which the graph was already freed. Make sure all involved tensors have a clean history on each iteration.

### tensorboard

To start tensorboard: `tensorboard --logdir [path/to/runs]`

## time tracking

<table>
  <thead>
    <tr>
      <th style="text-align:left">Date</th>
      <th style="text-align:left">Hours worked</th>
      <th style="text-align:left">Comment</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">28.10.2020</td>
      <td style="text-align:left">9h</td>
      <td style="text-align:left">Fix gradients, checking W&apos;, implementing A (without tilde)</td>
    </tr>
    <tr>
      <td style="text-align:left">2.11.2020</td>
      <td style="text-align:left">8.5h</td>
      <td style="text-align:left">Implement backward of A (note: not &#xC3;)</td>
    </tr>
    <tr>
      <td style="text-align:left">4.11.2020</td>
      <td style="text-align:left">5h</td>
      <td style="text-align:left">Debug dA/dz, found bug</td>
    </tr>
    <tr>
      <td style="text-align:left">9.11.2020</td>
      <td style="text-align:left">8h</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">11.11.2020</td>
      <td style="text-align:left">8.5h</td>
      <td style="text-align:left">
        <p>Add tests for mdr, excluding some cases, adding more example terrains,</p>
        <p>-&gt; Clue: must be something when boundary is receiver.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">16.11.2020</td>
      <td style="text-align:left">8h</td>
      <td style="text-align:left">Found out, that double not precise enough</td>
    </tr>
    <tr>
      <td style="text-align:left">18.11.2020</td>
      <td style="text-align:left">4.25h</td>
      <td style="text-align:left">
        <p>Fixing gradients for z(..)</p>
        <p>grads wrt. k and z don&apos;t work yet</p>
        <p>might be epsilon?</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">23.11.2020</td>
      <td style="text-align:left">7</td>
      <td style="text-align:left">
        <p>Fixing gradient for z, k stlil buggy,</p>
        <p>started optimization</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">30.11.2020</td>
      <td style="text-align:left">7</td>
      <td style="text-align:left">Fixing dz/dk, not much more</td>
    </tr>
    <tr>
      <td style="text-align:left">16.12.2020</td>
      <td style="text-align:left">6</td>
      <td style="text-align:left">Fix optimization</td>
    </tr>
    <tr>
      <td style="text-align:left">?</td>
      <td style="text-align:left">?</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">27.12.2020</td>
      <td style="text-align:left">5</td>
      <td style="text-align:left">
        <p>Read Optimization book,</p>
        <p>debugging lake issue</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">1.1.2021</td>
      <td style="text-align:left">3.5</td>
      <td style="text-align:left">
        <p>Read Optimization book,</p>
        <p>debug</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">4.1.2021</td>
      <td style="text-align:left">6</td>
      <td style="text-align:left">Isolated Optimization</td>
    </tr>
    <tr>
      <td style="text-align:left">5.1.2021</td>
      <td style="text-align:left">6.5</td>
      <td style="text-align:left">
        <p>Fix forward,</p>
        <p>Isolated k map</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">6.1.2021</td>
      <td style="text-align:left">3</td>
      <td style="text-align:left">Isolated Parameters</td>
    </tr>
    <tr>
      <td style="text-align:left">7.1.2021</td>
      <td style="text-align:left">3</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">12.1.2021</td>
      <td style="text-align:left">6</td>
      <td style="text-align:left">Fix isolated uplift</td>
    </tr>
  </tbody>
</table>



