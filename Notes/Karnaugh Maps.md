---
tags:
  - DigitalCircuits
---
Subjects: [[Digital Circuits]]
Links: [[Logic Gates]], [[Boolean Equations for Digital Circuits]], [[Boolean Algebra]]

After working throught several minimizations of Boolean equations using Boolean algebra, you will realize that, if you are not careful you sometimes end up with completely different equations instead of a simplified equations. 

*Karnaugh maps* or $K$-maps are graphical method of simplifying Boolean equations. $K$-maps work well for problems with up to four variables. More important, they give insight into manipulating Boolean equations.

$K$-maps provide an easy visual way to minimise logic. Simply circle all the rectangular blocks of $1$'s in the map, using the fewest possible number of circles. Each circle should be as large as possible. Then read off the implicants that were circled. 

More formally, recall that a Boolean equation is minimised when ti is written as a sum of the fewest number of prime implicants. Each circle on the $K$-map represents an implicant. The largest possible circles are prime implicants. Rules for finding a minimised equation from a $K$-map are as follows:
- Use the fewest circles necessary to cover all the $1$'s.
- All the squares in each circle must contain $1$'s.
- Each circle must span a rectangular block that is a power of $2$ squares in each direction.
- Each circle should be as large as possible.
- A circle may wrap around the edges of the $K$-map
- A $1$ in a $K$-map may be circles multiple times if doing so allows fewer circles to be used. 