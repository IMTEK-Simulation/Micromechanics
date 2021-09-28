---
layout: default
title: "Chapter 04"
parent: Lecture
date: 2021-09-28
categories: lecture
author: Lars Pastewka
nav_order: 4
---


<h2 class='chapterHead'><span class='titlemark'>Chapter 4</span><br /><a id='x1-10004'></a>Elastostatic equilibrium</h2>
<h3 class='sectionHead'><span class='titlemark'>4.1 </span> <a id='x1-20004.1'></a>Stress and static equilibrium</h3>
<!-- l. 5 --><p class='noindent'><a class='url' href='https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=c3d56bf8-3178-43ac-8c58-ac720115ef26'><span class='cmtt-12'>https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=c3d56bf8-3178-43ac-8c58-ac720115ef26</span></a>
</p><!-- l. 7 --><p class='noindent'>
</p>
<h4 class='subsectionHead'><span class='titlemark'>4.1.1 </span> <a id='x1-30004.1.1'></a>Small strain theory</h4>
<!-- l. 9 --><p class='noindent'>We will treat elasticity exclusively in the limit of small or infinitesimal strains
where all equations are linear. The generalization of this “small strain” theory is
“finite strain” elasticity. Note that linear elasticity is a classical <span class='cmti-12'>field theory</span>, this
means all quantities typically depend continuously on positions \(\v{r}\). Those quantities
are called <span class='cmti-12'>fields</span>.
</p><!-- l. 11 --><p class='indent'> The central quantities of small strain elasticity are the (Cauchy) stress field \(\t{\sigma }(\v{r})\)
and the displacement field \(\v{u}(\v{r})\). Given a material point has moved from position \(\v{r}\) to \(\v{r}^\prime \),
the displacement field is \(\v{u}(\v{r})=\v{r}^\prime -\v{r}\). The stress \(\t{\sigma }\) is a tensor that transforms an area (vector) \(\v{A}\)
into a force vector \(\v{F}\), \(\v{F}=\t{\sigma }\cdot \v{A}\). Note that the direction of the area vector points outwards on
that area.
</p><!-- l. 13 --><p class='noindent'>
</p>
<h5 class='subsubsectionHead'><a id='x1-40004.1.1'></a>Force equilibrium</h5>
<!-- l. 15 --><p class='noindent'>We will now consider the equilibrium of forces inside a solid body. Specifically, we
regard a small volume element inside this body. For simplicity, we remain
in a two-dimensional picture but generalization to three dimensions is
straightforward.
</p><!-- l. 17 --><p class='indent'> Figure <a href='#x1-4001r1'>4.1<!-- tex4ht:ref: fig:force_equilibrium --></a>a shows a sketch of some body with the (in two-dimensional areal)
volume element highlighted in red. If the size of the element \(\Delta x\times \Delta y \times \Delta z\) is small
enough, then the forces on opposite sites of the elements must balance.
We here denote the forces on the faces perpendicular to the \(x\)-direction
by \(\v{X}\), the forces on the \(y\)-faces by \(\v{Y}\) and the forces on the \(z\)-faces by \(\v{Z}\) (see
Fig. <a href='#x1-4001r1'>4.1<!-- tex4ht:ref: fig:force_equilibrium --></a>b, \(z\)-direction not shown). If we know the areas, we can get the
forces from the stress tensor \(\t{\sigma }\) (that converts areas into forces), specifically \begin{align} \label{eqn:forceX} \v{X} &amp;= \begin{pmatrix} \sigma _{xx} \Delta y \Delta z \\ \sigma _{yx} \Delta y \Delta z \\ \sigma _{zx} \Delta y \Delta z \\ \end{pmatrix} \\ \label{eqn:forceY} \v{Y} &amp;= \begin{pmatrix} \sigma _{xy} \Delta x \Delta z \\ \sigma _{yy} \Delta x \Delta z \\ \sigma _{zy} \Delta x \Delta z \\ \end{pmatrix} \\ \label{eqn:forceZ} \v{Z} &amp;= \begin{pmatrix} \sigma _{xz} \Delta x \Delta y \\ \sigma _{yz} \Delta x \Delta y \\ \sigma _{zz} \Delta x \Delta y \\ \end{pmatrix}. \end{align}
</p><!-- l. 46 --><p class='indent'> Note that \(\v{X}\), \(\v{Y}\), \(\v{Z}\) and \(\t{\sigma }\) are field; they explicitly depend on position \(\v{r}\) within the
body.
</p>



<figure class='figure'>







<!-- l. 50 --><p class='noindent'> <img alt='PIC' width='390' height='274' src='figures/Figure_Stress_Equilibrium-.png' /> <a id='x1-4001r1'></a>
<a id='x1-4002'></a>
</p>
<figcaption class='caption'><span class='id'>Figure 4.1:: </span><span class='content'>Force equilibrium in a small volume element inside a solid body.</span></figcaption><!-- tex4ht:label?: x1-4001r4.1 -->



</figure>
<!-- l. 55 --><p class='indent'> For a volume element located at position \(\v{r}=(x,y,z)\), force equilibrium inside the element
can be expressed as \begin{equation} \label{eqn:forceeq} \begin{split} \v{X}(x+\Delta x, y, z) - \v{X}(x, y, z) &amp;+ \v{Y}(x, y+\Delta y, z) - \v{Y}(x, y, z) \\ &amp;+ \v{Z}(x, y, z+\Delta z) - \v{Z}(x, y, z) = \v{F}(x,y,z) \end{split} \end{equation}
where \(\v{F}(x,y,z)\) is an external force, often called the <span class='cmti-12'>body force</span>, acting on the volume
element. We can insert Eqs. \eqref{eqn:forceX}, \eqref{eqn:forceY} and
\eqref{eqn:forceZ} and divide by the volume of the element \(\Delta x \Delta y \Delta z\) to obtain
\begin{equation} \begin{split} \frac{\sigma _{xx}(x+\Delta x,y,z)-\sigma _{xx}(x, y, z)}{\Delta x} &amp;+ \frac{\sigma _{xy}(x,y+\Delta y,z)-\sigma _{xy}(x, y, z)}{\Delta y} \\ &amp;+\frac{\sigma _{xz}(x,y,z+\Delta z)-\sigma _{xz}(x, y, z)}{\Delta z} = f_x(x,y,z) \end{split} \end{equation}
for the \(x\)-component of Eq. \eqref{eqn:forceeq}. Here \(f_x=F_x/\Delta x \Delta y \Delta z\) is a volume force. In the
limit \(\Delta x\to 0\) and \(\Delta y\to 0\) this becomes \begin{equation} \frac{\partial \sigma _{xx}}{\partial x} + \frac{\partial \sigma _{xy}}{\partial y} + \frac{\partial \sigma _{xz}}{\partial z} = f_x. \end{equation}
From the \(y\) and \(z\)-component of Eq. \eqref{eqn:forceeq} we get two more
differential equations, \begin{align} \frac{\partial \sigma _{yx}}{\partial x} + \frac{\partial \sigma _{yy}}{\partial y} + \frac{\partial \sigma _{yz}}{\partial z} &amp;= f_y \\ \frac{\partial \sigma _{zx}}{\partial x} + \frac{\partial \sigma _{zy}}{\partial y} + \frac{\partial \sigma _{zz}}{\partial z} &amp;= f_z. \end{align}
</p><!-- l. 107 --><p class='indent'> These can be summarized to the compact notation \begin{equation} \label{eqn:Equi_condition} \nabla \cdot \t{\sigma }=\v{f}. \end{equation}
Equation \eqref{eqn:Equi˙condition} is the central expression of elastostatics that
describes force balance within a solid body.
</p><!-- l. 114 --><p class='indent'> An alternative derivation of force balance invokes Gauss’ theorem. We can
integrate Eq. \eqref{eqn:Equi˙condition} over a volume element inside this body
of volume \(V\) and surface area \(S(V)\). Using Gauss’ theorem (sometimes also called the
divergence theorem), we obtain \begin{equation} \label{eqn:sum_of_forces_in_V} \int _V d^3 r \ \nabla \cdot \t{\sigma } = \int _{S(V)} d^2 r \ \t{\sigma } \cdot \v{e}_S = \int _{S(V)} d^2 r \ d\v{F} = \int _V d^3 r \ \v{f} \end{equation}
where \(\v{e}_S\) is the normal vector pointing outwards on \(S(V)\). The infinitesimal area vector \(\v{e}_S d^2 r\)
is hence transformed into an (infinitesimal) force vector \(d \v{F} = \t{\sigma } \cdot \v{e}_S \ d^2 r\) and integrated over.
Eq. \eqref{eqn:sum˙of˙forces˙in˙V} hence contains a sum over all forces acting on
the surface of the volume element \(V\), and these forces must sum to the body force.
It is nothing else than a statement of force balance for any volume element within
the solid body.
</p>
<div class='framedenv' id='shaded*-1'>
<!-- l. 122 --><p class='noindent'><span class='underline'><span class='cmbx-12'>Note:</span> </span><span class='cmti-12'>Notation – </span>Note that \(\nabla \cdot \t{\sigma } \equiv \text{div} \ \t{\sigma }\). Sometimes it is useful to make use of Einstein
summation, i.e. implicit summation over repeated indices within the same
quantity of in products. Examples are: \(\nabla \cdot \t{\sigma } = \partial _{i} \sigma _{ij} = \sum _i \partial _{i} \sigma _{ij}, 3\,\sigma _h = \sigma _{kk} = \sum _k \sigma _{kk} = tr \,\t{\sigma }\), where \(\sigma _h\) is the hydrostatic stress. In the
solid mechanics literature, derivatives are often expressed as indices following a
comma. For example, the derivative of the function \(f(x,y,z)\) with respect to \(x\) would be
written as \(f_{,x}\). In this notation, Eq. \eqref{eqn:Equi˙condition} becomes \(\nabla \cdot \t{\sigma } = \partial _{i} \sigma _{ij} = \sigma _{ij,i}=0\). By virtue
of the Einstein summation convention we need to sum over the repeated index \(i\) in
the right hand side expression. Vector/tensor and component notation with
Einstein summation will be used intermixed throughout these notes. </p></div>



<h5 class='subsubsectionHead'><a id='x1-50004.1.1'></a>Moment equilibrium</h5>
<!-- l. 128 --><p class='noindent'>Besides equilibrium of forces, we also need to fulfills the equilibrium of moments
acting on the volume element. The moment around the \(z\)-axis is given by
\begin{equation} Y_x \Delta y + X_y \Delta x = 0 \end{equation}
which immediately implies \(\sigma _{yx}=\sigma _{xy}\). The moment equilibrium around the \(x\)- and \(y\)-axes
leads to conditions on the other off-diagonal components of \(\t{\sigma }\), \(\sigma _{zx}=\sigma _{xz}\) and \(\sigma _{zy}=\sigma _{yz}\). By
virtue of moment balance, the stress tensor is a <span class='cmti-12'>symmetric </span>tensor, \(\sigma _{ij}=\sigma _{ji}\) or
\(\t{\sigma }=\t{\sigma }^T\).
</p><!-- l. 135 --><p class='noindent'>
</p>
<h3 class='sectionHead'><span class='titlemark'>4.2 </span> <a id='x1-60004.2'></a>Force equilibria in three dimensions</h3>
<!-- l. 137 --><p class='noindent'><a class='url' href='https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=e5d1512d-7a80-4e79-8ea1-ac82015e82df'><span class='cmtt-12'>https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=e5d1512d-7a80-4e79-8ea1-ac82015e82df</span></a>



</p>
<h2 class='likechapterHead'><a id='x1-70004.2'></a>Bibliography</h2>
