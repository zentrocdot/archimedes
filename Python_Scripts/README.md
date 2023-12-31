# Introductory Words

This section contains Python scripts that can be used to calculate the circle number Pi. Once completed, one will find here a bunch of Python scripts that are based directly on Archimedes' ideas.

It should be noted that Python works with a limited number of decimal places by default. This is also valid for square roots from the standard module 'math'. To avoid this problem, the standard Python module 'decimal' can be used. Take also a look at the docstrings in the Python scripts with respect to the aforementioned comment.

Standard Python is not suitable for performing calculations with a sufficient number of decimal places. Nevertheless, I first create the algorithms in standard Python in order to convert them into a form in which the Python module decimal is used in a second step. 

Based on Archimedes' approach, further algorithms were developed to calculate both the lower limit and the upper limit as well as Pi as the mean value of the lower and upper limits.

As soon as I have a little more time, I will explain in more detail how the corresponding equations can be derived from the geometric relationships. 

# The Archimedes' algorithm

Not knowing that Pi is a transcendental number, Archimedes stated that it is possible to find a right-handed triangle that has the the same area as a circle. This is a similar problem like squaring the circle.     

<p align="center">
<img src="\images/archimedes_figure1.png" alt="Figure 3"><br/>
Figure 1: Archimedes, Measurement of a Circle, circle and right-handed triangle
</p>
<br/>

In Proposition II he is using the last statement for the introduction of an upper and a lower bound for the base of such a right-handed triangle.

<p align="center">
<img src="\images/archimedes_figure3.png" alt="Figure 3"><br/>
Figure 3: Archimedes, Measurement of a Circle, geometrical model for one edge of the outer regular polygon
</p>
<br/>

<p align="center">
<img src="\images/archimedes_figure4.png" alt="Figure 3"><br/>
Figure 4: Archimedes, Measurement of a Circle, geometrical model for one edge of the inner regular polygon
</p>
<br/>

Aryabhatta as well as Al Kashi apparently knew the relationship to the iterative calculation of the side lengths of a regular polygon using recurrence.

<p align="center">
$s_{2n} = \sqrt{2 - \sqrt{ 4 - s_{n}^2}}$
</p>

This equation for the inner polygon in conjunction with a relationship to the outer polygon in form of an iterative formula can be found in the known sources under the name Archimedes algorithm.

<p align="center">
$s_{2n} = \sqrt{2 - \sqrt{ 4 - s_{n}^2}}$
</p>

<p align="center">
$S_{2n} = \frac{\huge{s_{2n}}}{
  \large{\sqrt{1- \left( \frac{\huge{s_{_{2n}}}}{2} \right)^2}}}$
</p>

If one looks at the geometric explanations of Archimedes and Huygens in particular, these equations are easy to find.

The also so-called Archimedes algorithm, which can be found in a lot of resources, is called Archimedean iterative algorithm, Archimedean mean iteration, Pfaff-Borchardt-Schwab algorithm, Archimedes–Borchardt algorithm as well as Archimedes recurrence formula. First appearance around 1800 at Pfaff reinvented by Borchardt.

<p align="center">
$S_{2n} = \frac{\huge{2 S_{n} s_{n}}}{\huge{S_{n}+ s_{n}}}$ 
</p>

<p align="center">
$s_{2n} = \sqrt{S_{2n} s_{n}}$
</p>

The latter method is similar to the Gauss-Legendre algorithm. In this method two numbers are repeatedly replaced by their arithmetic and geometric mean in order to approximate their arithmetic-geometric mean.

Taking a look at Figure 3 and Figure 4 shows, that it is in principle not possible, to derive a recurrence relationship from two different geometrical approaches.

In the context of the Archimedes algorithm or Archimedes method a distinction must be made between recursive and recurrence or iterative algorithm. The wording recurrence or iterative is correct and recursive is not. It becomes recursive if we use symbolic math and when we do not use numbers for the calculation. 
