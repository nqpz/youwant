# You Want

A computer game idea in progress!


## Idea

You Want is an idea for a game of setting goals for a 2D top-down system
and its inhabitants, similar in style to other construction and
management simulation games, but with a focus on the deep customization
of goal-setting for the simulation, and then potentially letting it run
on its own.

The main gameplay loop is to specify goals, watch as solutions to those
goals are attempted, and then change the goals again. There is no win
condition. Maybe it makes sense to also be able to pause the simulation
and change some things manually to see how it adapts to such changes.

It must be fairly easy to create easy goals, but it's okay if it's
complicated to create complicated goals. All of the goals will have to
be defined within the constrains of this 2D world. Maybe it will make
sense to extend that if this first approach turns out to generate
something meaningful.

My hope is that it will be possible to derive some basic storybuilding
from the concrete things happening in the simulation, which might work
if the goal-setting player associates meaning with the objects that the
goals are defined in relation to.


### Food-eating example

We can try to describe a world where animals eat food:

  - You define a purple block to mean "food".
  - You define a light-purple block to mean "food smell".
  - You define a green block to mean "animal".
  - You state that the system should optimize for a green block
    (animals) being on the same position as a purple block (food).
  - You state that a purple block disappears when it occupies the same
    position as a green block (food is eaten).
  - You state that each light-purple block (food smell) always spreads
    in all directions for each simulation tick.
  - You give each green block four smell sensors: one for north, east,
    south, and west.

You then hope that the animal will be able to learn that following the
smell will cause it to find food.  The alternatives are (1) not moving
or (2) moving away from the smell.  Alternative (1) will always be a
wrong choice, since food is static in this simulation.  Alternative (2)
might work in some cases where the food smell hasn't spread enough yet,
and might provide the same result as following the smell in worlds that
are overpopulated with animals and very little food.

Future example: Allow the animals to build roads, which will make travel
faster.  Refine the goal to not be just the highest amount of
instantaneous food, but the highest amount of food over a long period.
Also allow food to "grow" by letting it spawn occasionally, and let each
position have a "fertility" value.  Next up from that is something like
farming.


### House-building example

We can try to focus on building nice and square-like housing,
transforming the randomness of the auto-generated world into neat living
quarters.
