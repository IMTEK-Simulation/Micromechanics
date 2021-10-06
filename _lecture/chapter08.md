---
layout: default
title: "Chapter 08 [Dez. 6-12]"
parent: Lecture
date: 2021-10-06
categories: lecture
author: Lars Pastewka
nav_order: 8
---


<h2 class='chapterHead'><span class='titlemark'>Chapter 8</span><br /><a id='x1-10008'></a>Plane problems</h2>
<!-- l. 3 --><p class='noindent'><a href='https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=7ebb9e3e-c8c8-4640-ab4b-acaa0109e1b4' class='url'><span class='cmtt-12'>https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=7ebb9e3e-c8c8-4640-ab4b-acaa0109e1b4</span></a>
</p><!-- l. 5 --><p class='indent'> Plane problems are problems where the system has a symmetry in a certain
direction. We will here use the \(y\)-direction as the direction in which the plane
conditions hold. This symmetry implies that the relevant quantities do not
vary in \(y\)-direction. Note that throughout this text, we will switch this
direction.
</p>
<h3 class='sectionHead'><span class='titlemark'>8.1 </span> <a id='x1-20008.1'></a>Plane strain</h3>
<!-- l. 9 --><p class='noindent'>For a plane strain situation, the system cannot elongate or shrink in that direction
and hence \(\varepsilon _{yy} = 0\). From Hooke’s law for isotropic elasticity, \begin{equation} \varepsilon _{ij} = \frac{1}{E} [(1+\nu )\sigma _{ij} - \nu \delta _{ij} \sigma _{kk}], \end{equation}
we see that \begin{equation} \label{eqn:planestrainzz} \varepsilon _{yy} = \frac{1+\nu }{E} \sigma _{yy} - \frac{\nu }{E} (\sigma _{xx} + \sigma _{yy} + \sigma _{zz}) = 0 \end{equation}
and hence \begin{equation} \label{eq:planestrainstressyy} \sigma _{yy} = \nu (\sigma _{xx} + \sigma _{zz}). \end{equation}
With the two relations for \(\varepsilon _{yy}\) and \(\sigma _{yy}\) we can express Hooke’s law as \begin{align} \label{eq:planestrainHooksxx} \varepsilon _{xx} &amp;= \frac{1-\nu ^2}{E} \sigma _{xx} - \frac{\nu (1+\nu )}{E} \sigma _{zz} \\ \label{eqn:planestrain_Hooksyy} \varepsilon _{zz} &amp;= -\frac{\nu (1+\nu )}{E} \sigma _{xx} + \frac{1-\nu ^2}{E} \sigma _{zz} \end{align}
</p><!-- l. 30 --><p class='indent'> and its inverse \begin{align} \label{eq:planestrainHooksinversexx} \sigma _{xx} &amp;= (\lambda + 2\nu ) \varepsilon _{xx} + \lambda \varepsilon _{zz} \\ \label{eqn:planestrain_Hooksinverseyy} \sigma _{zz} &amp;= \lambda \varepsilon _{xx} + (\lambda + 2\mu ) \varepsilon _{zz} \end{align}
</p><!-- l. 37 --><p class='indent'> Note that the condition for elastic equilibrium becomes (in Cartesian
coordinates) \begin{align} \label{eqn:planestrainelasticequixx} \frac{\partial \sigma _{xx}}{\partial x} + \frac{\partial \sigma _{xz}}{\partial z} &amp;= 0 \\ \label{eqn:planestrainelasticequizz} \frac{\partial \sigma _{zz}}{\partial z} + \frac{\partial \sigma _{xz}}{\partial x} &amp;= 0. \end{align}
</p><!-- l. 45 --><p class='noindent'>
</p>
<h3 class='sectionHead'><span class='titlemark'>8.2 </span> <a id='x1-30008.2'></a>Plane stress conditions</h3>
<!-- l. 48 --><p class='noindent'>For plane stress we consider a situation with \(\sigma _{yy} = 0\), i.e. there is no stress in the
\(y\)-direction. This is a good approximation for example for a thin plate. In this limit,
Hooke’s law becomes \begin{align} \label{eqn:planestresse1} \varepsilon _{xx} &amp;= \frac{1}{E} (\sigma _{xx} - \nu \sigma _{zz}) \\ \label{eqn:planestresse2} \varepsilon _{zz} &amp;= \frac{}{E} (-\nu \sigma _{xx} + \sigma _{zz}) \end{align}
</p><!-- l. 55 --><p class='indent'> and its inverse \begin{align} \label{eqn:planestresss1} \sigma _{xx} &amp;= \frac{E}{1-\nu ^2} (\varepsilon _{xx} + \nu \varepsilon _{zz}) \\ \label{eqn:planestresss2} \sigma _{zz} &amp;= \frac{E}{1-\nu ^2} (\nu \varepsilon _{xx} + \varepsilon _{zz}). \end{align}
</p><!-- l. 63 --><p class='indent'> Note that plane strain and plane stress are described by the same set of
differential equations but with different elastic moduli. We can convert the plane
stress Eqs. \eqref{eqn:planestresse1}-\eqref{eqn:planestresss2} to the
corresponding plane strain equation by substituting the elastic constants,
\begin{equation} E \to \frac{E}{1-\nu ^2}\quad \text{and}\quad \nu \to \frac{\nu }{1-\nu }. \end{equation}
Hence any plane stress solution can be converted into a plane strain solution using
this substitution. In the following, we will continue to work with the plane stress



expression (because they are simpler), but all results carry over to plane strain
with this substitution.
</p><!-- l. 69 --><p class='noindent'>
</p>
<h3 class='sectionHead'><span class='titlemark'>8.3 </span> <a id='x1-40008.3'></a>Compatibility condition</h3>
<!-- l. 71 --><p class='noindent'>Another condition to be fulfilled is the <span class='cmti-12'>compatibility condition</span>. For plane
problems, the compatibility conditions is the single equation: \begin{equation} \label{eqn:Compatibility_eqn} \frac{\partial ^2 \varepsilon _{xx}}{\partial z^2} + \frac{\partial ^2 \varepsilon _{zz}}{\partial x^2} = 2\ \frac{\partial ^2 \varepsilon _{xz}}{\partial x \partial z} \end{equation}
That it must hold is easily seen by expressing the strain in terms of the
displacements \(\v{u}\). It is therefore a consequence of the fact that the strain field is the
gradient of the displacement field. It is similar to the well-known condition that
the curl of a gradient has to disappear.
</p><!-- l. 78 --><p class='indent'> The compatibility condition has a simple geometric explanation. Imaging a
jigsaw puzzle that you deform in its assembled state. Even in the deformed state,
all pieces still have to fit together. They deformation of neighboring pieces can
therefore not be independent of each other.



</p>
<h2 class='likechapterHead'><a id='x1-50008.3'></a>Bibliography</h2>

