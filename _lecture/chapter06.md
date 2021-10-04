---
layout: default
title: "Chapter 06"
parent: Lecture
date: 2021-10-04
categories: lecture
author: Lars Pastewka
nav_order: 6
---


<h2 class='chapterHead'><span class='titlemark'>Chapter 6</span><br /><a id='x1-10006'></a>Strain and displacement</h2>
<h3 class='sectionHead'><span class='titlemark'>6.1 </span> <a id='x1-20006.1'></a>Strain</h3>
<!-- l. 5 --><p class='noindent'><a class='url' href='https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=1a7ba6e0-1cdb-4422-b7a5-ac9100b5586c'><span class='cmtt-12'>https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=1a7ba6e0-1cdb-4422-b7a5-ac9100b5586c</span></a>
</p><!-- l. 7 --><p class='noindent'>
</p>
<h3 class='sectionHead'><span class='titlemark'>6.2 </span> <a id='x1-30006.2'></a>Displacement</h3>
<!-- l. 9 --><p class='noindent'>The displacement field \(\v{u}(\v{r})\) describes how a point on our solid body moves during
deformation. For a rigid body \(\v{u}\equiv 0\), but for a deformable body we obtain finite
displacements during deformation. The point \(\v{r}\) then moves to the point \(\v{r}^\prime (\v{r}) = \v{r} + \v{u}(\v{r})\). The
displacement field \(\v{u}(\v{r})=\v{r} - \v{r}^\prime (\v{r})\) is hence the difference of the deformed (“displaced”) point to
its reference position \(\v{r}\). Note that the displacement field itself is defined as a
function of this reference position \(\v{r}\).
</p><!-- l. 11 --><p class='noindent'>
</p>
<h3 class='sectionHead'><span class='titlemark'>6.3 </span> <a id='x1-40006.3'></a>Strain</h3>
<!-- l. 13 --><p class='noindent'>The strain field in the small strain approximation is given by the symmetrized
gradient of \(\v{u}(\v{r})\), \begin{equation} \label{eqn:Strain_gradient} \t{\varepsilon }(\v{r}) = \frac{1}{2} \left (\nabla \v{u} + (\nabla \v{u})^T\right ). \end{equation}
The left hand side of Eq. \eqref{eqn:Strain˙gradient} contains the gradient of a
vector field, \(\nabla \v{u}\), which is a second rank tensor, \begin{equation} \nabla \v{u} = \begin{pmatrix} \frac{\partial u_x}{\partial x} &amp; \frac{\partial u_x}{\partial y} &amp; \frac{\partial u_x}{\partial z} \\ \frac{\partial u_y}{\partial x} &amp; \frac{\partial u_y}{\partial y} &amp; \frac{\partial u_y}{\partial z} \\ \frac{\partial u_z}{\partial x} &amp; \frac{\partial u_z}{\partial y} &amp; \frac{\partial u_z}{\partial z} \end{pmatrix}, \end{equation}
whose components are given by \([\nabla \v{u}]_{ij}=\partial u_i/\partial r_j = u_{i,j}\). It is <span class='cmti-12'>not </span>the divergence, \(\nabla \cdot \v{u}\) which would give a
scalar. This potential source of confusion can be avoided by writing the equation
in the component-wise notation, \begin{equation} \label{eqn:Strain_gradient_comp} \varepsilon _{ij} = \frac{1}{2} (\partial _i u_j + \partial _j u_i) = \frac{1}{2} (u_{j,i} + u_{i,j}). \end{equation}
(Note that these expression do not contain a sum since there is no repeated
index.)
</p><!-- l. 35 --><p class='indent'> The geometric interpretation of the strain is that is converts a vector \(\v{r}\) that
has a direction and length into the change this vector undergoes under
deformation: \(\v{u}=\t{\varepsilon }\cdot \v{r}\) with the new (transformed) vector \(\v{r}'=\v{r}+\v{u}=(1+\t{\varepsilon })\cdot \v{r}\). In terms of thinking
about tensors as a representation of a linear transformation, the strain
tensor transforms a position into a displacement. The strain tensor is
dimensionless.



</p>
<h2 class='likechapterHead'><a id='x1-50006.3'></a>Bibliography</h2>

