Download Link: https://assignmentchef.com/product/solved-m232-homework-7-numerical-solution-of-differential-equations-ii
<br>
<ol>

 <li>Consider the following method for solving the heat equation <em>u<sub>t </sub></em>= <em>u<sub>xx</sub></em>:</li>

</ol>

<ul>

 <li>Determine the order of accuracy of this method (in both space and time).</li>

 <li>Suppose we take <em>k </em>= <em>αh</em><sup>2 </sup>for some fixed <em>α &gt; </em>0 and refine the grid. For what values of <em>α </em>(if any) will this method be Lax-Richtmyer stable and hence convergent?</li>

</ul>

<strong>Hint: </strong>Consider the MOL interpretation and the stability region of the time-discretization being used.

<ul>

 <li>Is this a useful method?</li>

</ul>

<ol start="2">

 <li>The m-file m solves the heat equation <em>u<sub>t </sub></em>= <em>κu<sub>xx </sub></em>using the Crank-Nicolson method. Run this code, and by changing the number of grid points, confirm that it is second-order accurate. (Observe how the error at some fixed time such as <em>T </em>= 1 behaves as <em>k </em>and <em>h </em>go to zero with a fixed relation between <em>k </em>and <em>h</em>, such as <em>k </em>= 4<em>h</em>.)</li>

</ol>

You might want to use the function error_table.m to print out this table and estimate the order of accuracy, and error_loglog.m to produce a log-log plot of the error vs. <em>h</em>. See bvp_2.m for an example of how these are used.

<ol start="3">

 <li>Modify m to produce a new m-file heat_trbdf2.m that implements the TR-BDF2 method on the same problem. Test it to confirm that it is also second order accurate. Explain how you determined the proper boundary conditions in each stage of this Runge-Kutta method.</li>

 <li>Modify m to produce a new m-file heat_FE.m that implements the forward Euler explicit method on the same problem. Test it to confirm that it is <em>O</em>(<em>h</em><sup>2</sup>) accurate as <em>h </em>→ 0</li>

</ol>

provided when <em>k </em>= 24<em>h</em><sup>2 </sup>is used, which is within the stability limit for <em>κ </em>= 0<em>.</em>02. Note how many more time steps are required than with Crank-Nicolson or TR-BDF2, especially on finer grids.

<ol start="5">

 <li>Modify m to solve the heat equation for −1 <em>&lt; x &lt; </em>1 with step function initial data</li>

</ol>

<table width="0">

 <tbody>

  <tr>

   <td width="96">1<em>u</em>(<em>x,</em>0) =0</td>

   <td width="52">if <em>x &lt; </em>0<em>, </em>if <em>x </em>≥ 0<em>.</em></td>

  </tr>

 </tbody>

</table>

With appropriate Dirichlet boundary conditions, the exact solution is

where erfc is the complementary error function

erfc(

<ul>

 <li>Test this routine <em>m </em>= 39 and <em>k </em>= 4<em>h</em>. Note that there is an initial rapid transient decay of the high wave numbers that is not captured well with this size time step.</li>

 <li>How small do you need to take the time step to get reasonable results? For a suitablysmall time step, explain why you get much better results by using <em>m </em>= 38 than <em>m </em>= 39. What is the observed order of accuracy as <em>k </em>→ 0 when <em>k </em>= <em>αh </em>with <em>α </em>suitably small and <em>m </em>even?</li>

</ul>