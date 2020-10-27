# meeting 20.10.2020

## houdini implementation

* for visualization only
* npc \(or npy? npyc?\) for terrain, exported from python, import in houdini

## optimization

* regularizer? currently 0
* loss function? currently: nn.MSELoss\(reduction='mean'\)
* not convex, yes? local minima
* efficiency
* make sense to just try out a range for say max\_iter/step size or number of epochs?
* isolated test: **n**
  * only working for range \[0.7, 1.1\]
  * not working when skipping hillslope
  * due to n/m = 2?



* Tensorboard: good for loss, curves
* optimizer of jingwei
* after 1 iteration, did value change?

## presentation

* first slide: timeline
  * working hours/ expected hours
  * points where should start writing
  * visual timeline
* last meeting, progress, what has been done
* roadmap for next week and meeting
* show equations

## gradients

* should never fail
* try smallest/most isolated examples and build up
* careful with discontinuities
* depression filling alg might cause problem
  * discard cases with depressions
* numerical accuracy, play with tolerance
* find buggy terrain and run gradcheck on it
* plot objective function with scalar parameter in local surrouding, to check if local minimum, and how much terrain changes

houdini

