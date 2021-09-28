---
layout: default
title: "Chapter 12"
parent: Lecture
date: 2021-09-28
categories: lecture
author: Lars Pastewka
nav_order: 12
---


<h2 class='chapterHead'><span class='titlemark'>Chapter 12</span><br /><a id='x1-100012'></a>Brittle failure</h2>
<h3 class='sectionHead'><span class='titlemark'>12.1 </span> <a id='x1-200012.1'></a>Stress near a crack tip</h3>
<!-- l. 5 --><p class='noindent'><a class='url' href='https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=e30ac1a6-b801-465b-aedf-acb9015b0c7d'><span class='cmtt-12'>https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=e30ac1a6-b801-465b-aedf-acb9015b0c7d</span></a>
</p><!-- l. 7 --><p class='noindent'>
</p>
<h4 class='subsectionHead'><span class='titlemark'>12.1.1 </span> <a id='x1-300012.1.1'></a>Airy stress function</h4>
<!-- l. 10 --><p class='noindent'>First, we invoke Hooke’s law, Eq. \eqref{eqn:Isotropic˙elasticity˙inverse}.
Using Eq. \eqref{eqn:planestrain˙stressyy} Hooke’s law itself becomes \begin{align} \label{eqn:Planestrain_Hookes} \varepsilon _{xx} &amp;= \frac{1}{E} [(1+\nu )\sigma _{xx} - \nu (\sigma _{xx} + \sigma _{yy} + \sigma _{zz})] = \frac{1+\nu }{E} [(1-\nu )\sigma _{xx} - \nu \sigma _{yy}] \\ \varepsilon _{yy} &amp;= \frac{1+\nu }{E} [(1-\nu )\sigma _{yy} - \nu \sigma _{xx}] \\ \varepsilon _{xy} &amp;= \frac{1}{2G} \sigma _{xy} = \frac{1+\nu }{E} \sigma _{xy} \end{align}
</p><!-- l. 17 --><p class='indent'> under plane strain conditions. We have just eliminated reference to \(\sigma _{zz}\) and \(\varepsilon _{zz}\) from
the equations. Inserting Hooke’s law into the compatibility condition,
Eq. \eqref{eqn:Compatibility˙eqn}, yields \begin{equation} \label{eqn:Compatibility_stresses} (1-\nu ) \left [\frac{\partial ^2 \sigma _{xx}}{\partial y^2} + \frac{\partial ^2 \sigma _{yy}}{\partial x^2}\right ] - \nu \left [\frac{\partial ^2 \sigma _{xx}}{\partial x^2} + \frac{\partial ^2 \sigma _{yy}}{\partial y^2}\right ] = 2 \frac{\partial ^2 \sigma _{xy}}{\partial x \partial y}, \end{equation}
the compatibility condition for the stresses.
</p><!-- l. 24 --><p class='indent'> We now use a mathematical trick to solve the equations of elastic equilibrium.
We define the <span class='cmti-12'>Airy stress function</span> \(\phi (x,y)\), that gives the stresses (in Cartesian
coordinates) as \begin{align} \label{eqn:airyxx} \sigma _{xx} &amp;= \frac{\partial ^2 \phi }{\partial y^2} \equiv [\nabla (\nabla \phi )]_{yy}, \\ \label{eqn:airyzz} \sigma _{yy} &amp;= \frac{\partial ^2 \phi }{\partial x^2} \equiv [\nabla (\nabla \phi )]_{xx},\\ \label{eqn:airyxz} \sigma _{xy} &amp;= -\frac{\partial ^2 \phi }{\partial x \partial y} \equiv [\nabla (\nabla \phi )]_{xy} \end{align}
</p><!-- l. 34 --><p class='indent'> (Note that the first \(\nabla \) is the gradient of the vector field \(\nabla \phi \), not the
divergence! Hence \(\nabla (\nabla \phi )\) is a second order tensor with components \([\nabla (\nabla \phi )]_{ij}=\phi _{,ij}\)!)
Equation \eqref{eqn:planestrain˙elastic˙equixx} becomes \begin{equation} \label{eqn:elastic_equi_airy} \frac{\partial ^3 \phi }{\partial x \partial y^2} - \frac{\partial ^3 \phi }{\partial x \partial y^2} = 0 \end{equation}
and is automatically fulfilled! The same holds for Eq. \eqref{eqn:planestrain˙elastic˙equizz}
We can now insert Eqs. \eqref{eqn:airyxx} to \eqref{eqn:airyxz} into the
compatibility condition Eq. \eqref{eqn:Compatibility˙stresses} to give
\begin{equation} \label{eqn:compatibility_airy} (1-\nu )\left [\frac{\partial ^2 }{\partial y^2} \frac{\partial ^2 \phi }{\partial y^2} + \frac{\partial ^2 }{\partial x^2} \frac{\partial ^2 \phi }{\partial x^2}\right ] - \nu \left [\frac{\partial ^2 }{\partial x^2} \frac{\partial ^2 \phi }{\partial y^2} + \frac{\partial ^2}{\partial y^2} \frac{\partial ^2 \phi }{\partial x^2} \right ] + 2 \frac{\partial ^2}{\partial x \partial y} \frac{\partial ^2 \phi }{\partial x \partial y} = 0, \end{equation}
which can be rearranged to \begin{equation} \label{eqn:compatibility_airy_rearr} \frac{\partial ^4 \phi }{\partial x^4} + 2\frac{\partial ^4 \phi }{\partial x^2 \partial y^2} + \frac{\partial ^4 \phi }{\partial y^4} = \left (\frac{\partial ^2}{\partial x^2} + \frac{\partial ^2}{\partial y^2}\right )\left [\left (\frac{\partial ^2}{\partial x^2} + \frac{\partial ^2}{\partial y^2}\right ) \phi \right ] = \nabla ^4 \phi = 0 \end{equation}
Conditions \eqref{eqn:planestrain˙elastic˙equixx} to \eqref{eqn:Compatibility˙eqn}
are all simultaneously fulfilled if Eq. \eqref{eqn:compatibility˙airy˙rearr} is
fulfilled! Equation \eqref{eqn:compatibility˙airy˙rearr} is the compatibility
condition, but expressed for the Airy stress function.
</p><!-- l. 53 --><p class='indent'> The operator \(\nabla ^4\) is called the <span class='cmti-12'>biharmonic </span>operator and any function \(\phi \) satifying \(\nabla ^4 \phi =0\) is
called a biharmonic function. (Functions \(\phi \) that fulfill the Laplace equation \(\nabla ^2\phi =0\) are
called harmonic functions.) The derivation above tells us, that for isotropic
elasticity a biharmonic Airy stress \(\phi (x,y)\) automatically leads to a compatible strain
field. This means for <span class='cmti-12'>any </span>biharmonic function \(\phi (x,y)\), the stress field derived from
Eqs. \eqref{eqn:airyxx}-\eqref{eqn:airyxz} will describe a system in static
equilibrium. The only thing left to do is to find the function \(\phi (x,y)\) that fulfills a specific



boundary condition.
</p><!-- l. 55 --><p class='noindent'>
</p>
<h4 class='subsectionHead'><span class='titlemark'>12.1.2 </span> <a id='x1-400012.1.2'></a>Westergaard stress function</h4>
<!-- l. 58 --><p class='noindent'>The Westergaard stress function builds on top of the Airy function and eliminates
the need to even satisfy the biharmonic equation \(\nabla ^4\phi =0\). This means that for any choice
of the Westergaard stress function, the conditions for force and moment
equilibrium and the compatibility condition are fulfilled automatically. The
Westergaard stress function can then be chosen freely as to fulfill the boundary
conditions of the problem.
</p><!-- l. 60 --><p class='indent'> <a href='#XWestergaard:1933'>Westergaard</a> (<a href='#XWestergaard:1933'>1933</a>) introduced a function \(Z(z)\) that is now known as the
<span class='cmti-12'>Westergaard stress function</span>. Note that here \(z\) is a complex variable that contains
the \(x\) and \(y\)-position as its real and imaginary part, \(z=x+iy\), and <span class='cmti-12'>not </span>the \(z\)-coordinate.
Likewise, the function \(Z(z)\) is complex valued. Following common notation, we denote
its integrals by \begin{equation} \bar{\bar{Z}}_{,z} = \bar{Z} \quad \text{and}\quad \bar{Z}_{,z} = Z. \end{equation}
Westergaard defined the Airy stress function as \begin{equation} \label{eqn:Westergaard} \phi (x, y) = \Re \left \{\bar{\bar{Z}}(x+iy)\right \} + y \Im \left \{\bar{Z}(x+iy)\right \} \end{equation}
where \(\Re \) and \(\Im \) denote the real and imaginary part of a complex number,
respectively. This Airy stress function fulfills the biharmonic equation,
Eq. \eqref{eqn:compatibility˙airy˙rearr}, for any arbitrary function \(Z(z)\), as we will
show below.
</p><!-- l. 74 --><p class='indent'> We will now derive the expressions for the stresses. We first note that since \(Z(z)\) is
a function of a complex variable, it satisfies the Cauchy-Riemann conditions, \begin{align} \Re Z_{,z} &amp;= \left (\Re Z\right )_{,x} = \left (\Im Z\right )_{,y} \\ \Im Z_{,z} &amp;= \left (\Im Z\right )_{,x} = -\left (\Re Z\right )_{,y}, \end{align}
</p><!-- l. 79 --><p class='indent'> which implies that \begin{align} \label{eqn:laplaceRe} \nabla ^2 \left (\Re Z\right ) &amp;= \left (\Re Z\right )_{,xx} + \left (\Re Z\right )_{,yy} = 0 \\ \nabla ^2 \left (\Im Z\right ) &amp;= \left (\Im Z\right )_{,xx} + \left (\Im Z\right )_{,yy} = 0, \\ \end{align}
</p><!-- l. 97 --><p class='indent'> i.e. the real and imaginary parts of the complex function \(Z(z)\) fulfill the Laplace
equation.
</p>
<div id='shaded*-1' class='framedenv'>
<!-- l. 99 --><p class='noindent'><span class='underline'><span class='cmbx-12'>Note:</span> </span><span class='cmti-12'>Cauchy-Riemann equations – </span>The Cauchy-Riemann equations are a
cornerstone of complex analysis. They hold for any differential function of a
complex variable. Such functions are also called <span class='cmti-12'>holomorphic</span>. Given \(f(z)=u(z) + iv(z)\) (hence \(u=\Re f\) and \(v=\Im f\))
with \(z=x+iy\), we can formally write the derivative as \begin{equation} f'(z_0) = \lim \limits _{w\in \mathcal{C},w\to 0} \frac{f(z_0+w)-f(z_0)}{w} \end{equation}
as the limit of the difference quotient. For real numbers, we can approach \(z_0\)
from the left or the right and both limits must equal if the function is
differentiable. In the complex plane, we can approach from any direction in two
dimensions. For example, we can compute the derivative along the real (\(x\)-)axis, \(w=x\):



\begin{equation} f'(z_0) = \lim \limits _{x\in \mathcal{R},x\to 0} \frac{f(z_0+x)-f(z_0)}{x} = \frac{\partial u}{\partial x} + i\frac{\partial v}{\partial x} \end{equation}
We can equally well compute the derivative along the imaginary (\(y\)-)axis, \(w=iy\), which
gives \begin{equation} f'(z_0) = \lim \limits _{y\in \mathcal{R},y\to 0} \frac{f(z_0+iy)-f(z_0)}{iy} = -i\frac{\partial u}{\partial y} + \frac{\partial v}{\partial y}. \end{equation}
Since both expressions have to be equal, we find \begin{equation} \frac{\partial u}{\partial x}=\frac{\partial v}{\partial y} \quad \text{and}\quad \frac{\partial u}{\partial y}=-\frac{\partial v}{\partial x}, \end{equation}
the Cauchy-Riemann equations. </p></div>
<!-- l. 131 --><p class='indent'> Now we differentiate \(\phi \) with respect to \(x\) and \(y\). This yields \begin{align} \phi _{,x} &amp;= \left (\Re \bar{\bar{Z}}\right )_{,x} + y\left (\Im \bar{Z}\right )_{,x} = \Re \bar{\bar{Z}}_{,z} + y \Im \bar{Z}_{,z} = \Re \bar{Z} + y \Im Z \\ \phi _{,y} &amp;= \left (\Re \bar{\bar{Z}}\right )_{,y} + \left (y \Im \bar{Z}\right )_{,y} = -\Im \bar{\bar{Z}}_{,z} + \Im \bar{Z} + y \Re \bar{Z}_{,z} = y \Re Z \end{align}
</p><!-- l. 149 --><p class='indent'> for the first derivatives and \begin{align} \phi _{,xx} &amp;= \left (\Re \bar{Z}\right )_{,x} + y \left (\Im Z\right )_{,x} = \Re \bar{Z}_{,z} + y \Im Z_{,z} = \Re Z + y \Im Z_{,z} \\ \phi _{,yy} &amp;= \left (y\Re Z\right )_{,y} = \Re Z + y \left (\Re Z\right )_{,y} = \Re Z - y \Im Z_{,z} \\ \phi _{,xy} &amp;= \left (\Re \bar{Z}\right )_{,y} + \left (y \Im Z\right )_{,y} = -\Im \bar{Z}_{,z} + \Im Z + y \Re Z_{,z} = y \Re Z_{,z} \end{align}
</p><!-- l. 173 --><p class='indent'> for the second derivatives. In summary, we obtain \begin{align} \label{eqn:Westergaardstressxx} \sigma _{xx} &amp;= \phi _{,yy} = \Re Z - y \Im Z_{,z} \\ \label{eqn:Westergaardstressyy} \sigma _{yy} &amp;= \phi _{,xx} = \Re Z + y \Im Z_{,z} \\ \label{eqn:Westergaardstresszz} \sigma _{xy} &amp;= -\phi _{,xy} = -y \Re Z_{,z} \end{align}
</p><!-- l. 182 --><p class='indent'> for the components of the stress tensor. Note that the Ansatz
Eq. \eqref{eqn:Westergaard} fulfills the biharmonic equation. We know from summing
Eqs. \eqref{eqn:Westergaardstressxx} and \eqref{eqn:Westergaardstressyy} that
\begin{equation} \psi \equiv \left (\frac{\partial ^2}{\partial x^2} + \frac{\partial ^2}{\partial y^2}\right )\phi = 2\Re Z, \end{equation}
hence by virtue of Eq. \eqref{eqn:laplaceRe}, \(\nabla ^4\phi =\nabla ^2\psi =0\) is fulfilled for <span class='cmti-12'>any </span>function \(Z(x+iy)\).
The utility of the Westergaard function over the Airy stress function is
hence that we have eliminated the need to explicitly fulfill the biharmonic
equation.
</p><!-- l. 188 --><p class='noindent'>
</p>
<h4 class='subsectionHead'><span class='titlemark'>12.1.3 </span> <a id='x1-500012.1.3'></a>Stress field</h4>
<!-- l. 190 --><p class='noindent'>We here discuss only mode I fracture, i.e. crack opening displacement. Consider a
plane (strain or stress) situation in which we can derive the stress field from the
Westergaard stress function \(Z(x+iy)\), Sec. <a href='#x1-400012.1.2'>12.1.2<!-- tex4ht:ref: sec:Westergaard --></a>. <a href='#XWestergaard:1933'>Westergaard</a> (<a href='#XWestergaard:1933'>1933</a>) made the Ansatz
\begin{equation} Z(z) = \frac{\sigma _\infty }{\sqrt{1 - (a/z)^2}} \end{equation}
for the stress function of a central crack in a large sheet. Here \(2a\) is the length of the
crack and \(\sigma _\infty \) the stress at infinity. The derivative of the stress function is
\begin{equation} \label{eqn:Westergaard_derivative} Z_{,z} = \frac{\sigma _\infty }{\sqrt{z^2 - a^2}} \left [ 1 - \frac{1}{1-(a/z)^2} \right ] \end{equation}
and its integral is \begin{equation} \label{eqn:Westergaard_integral} \bar{Z} = \sigma _\infty \sqrt{z^2 - a^2}. \end{equation}
</p><!-- l. 222 --><p class='indent'> Let us first look in the plane of the crack where \(y=0\), \(z=x\) and hence \begin{equation} Z(x) = \frac{\sigma _\infty }{\sqrt{1 - (a/x)^2}}. \end{equation}
For \(|x|&lt;a\) (inside the crack) the function is imaginary but for \(|x|&gt;a\) (outside the crack) the
function is real. The stresses in the plane of the crack are given by \(\sigma _{xx}=\Re Z\), \(\sigma _{yy}=\Re Z\) and \(\tau _{xy}=0\). Hence
they vanish inside the crack. This is the condition for the crack faces which are
free surfaces and therefore tractionless. Note that \(\sigma _{xx}\) does not need to vanish from



this condition but does here.
</p><!-- l. 229 --><p class='indent'> Outside the crack (but in the plane of the crack, \(y=0\)), the stress is given by
\begin{equation} \sigma _{xx} = \sigma _{yy} = \frac{\sigma _\infty }{\sqrt{1 - (a/x)^2}}. \end{equation}
It diverges as \(x\to a\) from above and approaches the hydrostatic state \(\sigma _{xx}=\sigma _{yy}=\sigma _\infty \) as \(x\to \infty \).
</p><!-- l. 235 --><p class='indent'> We will now focus on the crack line and switch to the variable \(z^*=z-a\). The stress
function becomes \begin{equation} Z(z^*) = \frac{\sigma _\infty (z^*+a)}{\sqrt{(z^* + a)^2 - a^2}} = \frac{\sigma _\infty (z^*+a)}{\sqrt{(z^*)^2 + 2az^*}} \approx \sigma _\infty \sqrt{\frac{a}{2z^*}} \end{equation}
where the \(\approx \) sign is valid for small \(z^*\). We write this expression as \begin{equation} \label{eqn:stress_intensity} Z(z^*) = \frac{K_I}{\sqrt{2\pi z^*}} \quad \text{with}\quad K_I = \sigma _\infty \sqrt{\pi a}. \end{equation}
Note that we have absorbed both the stress at infinity \(\sigma _\infty \) and the crack length \(a\) into
a single constant, the <span class='cmti-12'>stress intensity factor </span>(for mode I fracture), \(K_I\). The stress
field near the crack tip depends only on \(K_I\), not on \(\sigma _\infty \) and \(a\) individually and hence the
loading condition and geometry, independently.
</p><!-- l. 255 --><p class='indent'> To derive the component of the stress tensor, we switch to cylindrical
coordinates and write \(z^*=r e^{i\theta }\), yielding \begin{equation} Z(r, \theta ) = \frac{K_I}{\sqrt{2\pi r}} e^{-i\theta /2}. \end{equation}
In order to obtain the full stress field, we also need the expression for the
derivative of the Westergaard stress function near the crack tip. From
Eq. \eqref{eqn:Westergaard˙derivative}, we find \begin{equation} Z_{,z} \approx \frac{\sigma _\infty }{\sqrt{2az^*}} \left [ 1-\frac{2az^* + a^2}{2az^*} \right ] = -\frac{\sigma _\infty a^2}{(2az^*)^{3/2}} = -\frac{K_I \pi }{(2\pi z^*)^{3/2}} = -\frac{K_I}{\sqrt{8\pi r}} e^{-3i\theta /2}. \end{equation}
We now obtain the individual components of the stress tensor from
Eq. \eqref{eqn:Westergaardstressxx}-\eqref{eqn:Westergaardstresszz}: \begin{align} \sigma _{xx} &amp;= \Re Z - y \Im Z_{,z} = \frac{K_I}{\sqrt{2\pi r}} \cos \frac{\theta }{2} \left (1 - \sin \frac{\theta }{2} \sin \frac{3\theta }{2}\right ) \\ \sigma _{yy} &amp;= \Re Z + y \Im Z_{,z} = \frac{K_I}{\sqrt{2\pi r}} \cos \frac{\theta }{2} \left (1 + \sin \frac{\theta }{2} \sin \frac{3\theta }{2}\right ) \\ \sigma _{xy} &amp;= -y \Re Z_{,z} = \frac{K_I}{\sqrt{2\pi r}} \cos \frac{\theta }{2} \sin \frac{\theta }{2} \cos \frac{3\theta }{2} \end{align}
</p><!-- l. 277 --><p class='indent'> Hence the stress field <span class='cmti-12'>near </span>the crack tip is entirely described by the stress
intensity factor \(K_I\). \(K_I\) is measured in (weird) units of Pa\(\sqrt{\text{m}}\). The \(I\) indicates that this is
the stress intensity factor for mode \(I\) fracture. \(K_{II}\) and \(K_{III}\) are related quatities for the
two other fracture modes.
</p><!-- l. 279 --><p class='indent'> Note that the stress intensity factor is the amplitude of the square-root
singularity of the stress field at the crack tip. It is often defined from the stress
field itself as the limit \begin{align} \label{eq:KI} K_I &amp;= \lim \limits _{r\to 0} \sqrt{2\pi r} \sigma _{yy}(r, 0) \\ \label{eq:KII} K_{II} &amp;= \lim \limits _{r\to 0} \sqrt{2\pi r} \sigma _{xy}(r, 0) \\ \label{eq:KIII} K_{III} &amp;= \lim \limits _{r\to 0} \sqrt{2\pi r} \sigma _{yz}(r, 0), \\ \end{align}
</p><!-- l. 288 --><p class='indent'> where the singularity has been removed by multiplying with \(\sqrt{2\pi r}\). Note that the
limit is taken at the angle \(\theta =0\), i.e. along \(y=0\) within the plane of the crack. From
Eqs. \eqref{eq:KI} to \eqref{eq:KIII} is also clear that only \(K_I\) is nonzero for the
crack geometry that is discussed in this chapter.
</p><!-- l. 290 --><p class='noindent'>
</p>
<h3 class='sectionHead'><span class='titlemark'>12.2 </span> <a id='x1-600012.2'></a>Fracture toughness</h3>
<!-- l. 292 --><p class='noindent'><a class='url' href='https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=993c55f0-a6d5-4df9-a1ff-acb9015f614e'><span class='cmtt-12'>https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=993c55f0-a6d5-4df9-a1ff-acb9015f614e</span></a>



</p><!-- l. 294 --><p class='noindent'>
</p>
<h4 class='subsectionHead'><span class='titlemark'>12.2.1 </span> <a id='x1-700012.2.1'></a>Displacement field at the crack tip</h4>
<!-- l. 296 --><p class='noindent'>In order to compute the displacement field near the crack, we first need the
strain field. As usual, we obtain this from Hooke’s law (in plain stress): \begin{align} \label{eqn:crackstrainxx} \varepsilon _{xx} &amp;\equiv u_{x,x} = \frac{1}{E}\left (\sigma _{xx} - \nu \sigma _{yy}\right ) = \frac{1}{E}\left [(1-\nu ) \Re Z - (1+\nu ) y \Im Z_{,z}\right ] \\ \label{eqn:crackstrainyy} \varepsilon _{yy} &amp;\equiv u_{y,y} = \frac{1}{E}\left (\sigma _{yy} - \nu \sigma _{xx}\right ) = \frac{1}{E}\left [(1-\nu ) \Re Z + (1+\nu ) y \Im Z_{,z}\right ] \\ \label{eqn:crackstrainxy} 2\varepsilon _{xy} &amp;\equiv u_{x,y}+u_{y,x} = 2\frac{1+\nu }{E} \sigma _{xy} = -2\frac{1+\nu }{E} y \Re Z_{,z} \end{align}
</p><!-- l. 305 --><p class='indent'> Now we use \(Z=\bar{Z}_{,z}\) to express \(\Re Z = \Re \bar{Z}_{,z} = (\Re \bar{Z})_{,x}\) and \(\Im Z_{,z}=(\Im Z)_{,x}\) in Eq. \eqref{eqn:crackstrainxx} to identify
\begin{equation} u_x = \frac{1}{E}\left [(1-\nu ) \Re \bar{Z} - (1+\nu ) y \Im Z\right ] =\frac{1}{2\mu }\left [\frac{1-\nu }{1+\nu } \Re \bar{Z} - y \Im Z\right ]. \end{equation}
The expression for \(u_y\) is more complicated because of the explicit \(y\) that shows up in
the expressions for the strains. It is given by \begin{equation} u_y = \frac{1}{2\mu }\left [\frac{2}{1+\nu } \Im \bar{Z} - y \Re Z\right ]. \end{equation}
It is straightforward to verify that from these two expressions we also recover the
expression for \(\varepsilon _{xy}\).
</p><!-- l. 316 --><p class='indent'> It is common to replace \(\nu \) with \(\kappa =(3-\nu )/(1+\nu )\). The displacements can then be written as \begin{align} u_x &amp;= \frac{1}{4\mu }\left [(\kappa -1) \Re \bar{Z} - 2y \Im Z\right ] \\ u_y &amp;= \frac{1}{4\mu }\left [(\kappa +1) \Im \bar{Z} - 2y \Re Z\right ]. \end{align}
</p><!-- l. 322 --><p class='indent'> Since the integral of the Westergaard function near the crack tip is
\begin{equation} \bar{Z}(z^*) \approx \sigma _\infty \sqrt{2 a z^*} = K_I \sqrt{\frac{2 z^*}{\pi }} = 2K_I \sqrt{\frac{r}{2\pi }} e^{i\theta /2}, \end{equation}
we can directly write the displacement field in cylindrical coordinates as \begin{align} u_x &amp;= \frac{K_I}{2\mu } \sqrt{\frac{r}{2\pi }} \left [ 2\frac{1-\nu }{1+\nu } \cos \frac{\theta }{2} + \sin ^2 \frac{\theta }{2} \right ]\\ u_y &amp;= \frac{K_I}{2\mu } \sqrt{\frac{r}{2\pi }} \left [ 2\frac{1-\nu }{1+\nu } \cos \frac{\theta }{2} + \sin ^2 \frac{\theta }{2} \right ]. \end{align}
</p><!-- l. 331 --><p class='indent'> Note that in the plane of the crack (\(y=0\), \(z^*=x\)), the displacement field is given by \begin{align} u_x &amp;= \begin{cases} \frac{K_I}{2\mu } (\kappa -1) \sqrt{\frac{x}{2\pi }} &amp; \text{if}\;x &gt; 0 \\ 0 &amp; \text{if}\;x \leq 0 \end{cases}\\ u_y^+ &amp;= \begin{cases} 0 &amp; \text{if}\;x \geq 0 \\ \frac{K_I}{2\mu } (\kappa +1) \sqrt{-\frac{x}{2\pi }} &amp; \text{if}\;x &lt; 0 \end{cases}. \label{eq:displyat0} \end{align}
</p><!-- l. 343 --><p class='indent'> The \(y\)-displacement here is denoted with a little \(+\), \(u_y^+\), to indicate that this is the
displacement of the top crack face at a position \(y=0^+\), i.e. slightly above \(y=0\). The
displacement \(u_y^-\) of the bottom crack face is the negative of this values, \(u_y^-=-u_y^+\), for
symmetry reasons. Mathematically, this property emerges because the square-root
has a <span class='cmti-12'>branch cut </span>along the negative real axis.
</p><!-- l. 345 --><p class='noindent'>
</p>
<h4 class='subsectionHead'><span class='titlemark'>12.2.2 </span> <a id='x1-800012.2.2'></a>Strain energy release rate</h4>
<!-- l. 347 --><p class='noindent'>In order to formulate a fracture criterion we will require an expression for the
elastic <span class='cmti-12'>energy </span>released during propagation of the crack. This will lead to the
concept of the <span class='cmti-12'>strain energy release rate</span>.
</p><!-- l. 349 --><p class='indent'> We have not yet talked about the concept of energy in this notes. Since
elasticity is fully reversible (an elastic object returns to its origin shape when
unloaded), the work carried out when deforming an elastic body is <span class='cmti-12'>conservative</span>.



This means we can define an elastic energy that is recoverable by unloading the
body. In order to define the energy release rate, we will here focus on the work \(W\)
done by a moving crack.
</p><!-- l. 351 --><p class='indent'> We first note that the crack faces do not contribute to the work because
the normal stress is zero by definition, since we are dealing with a free
surface. We therefore have to focus on the crack tip. The tip opens by the
distance given by Eq. \eqref{eq:displyat0} to both sides. This displacement
work against the stress \(\sigma _{yy}\) right at the crack tip. We now assume that the
crack moves by a distance \(\Delta a\) which we will later take to zero. We assume
that the stress before the crack has moved is taken to zero quasistatically
during the crack opening process. The crack faces have opened a distance
\begin{equation} u_y^+ - u_y^-=2\frac{K_I}{2\mu } (\kappa + 1) \sqrt{\frac{\Delta a - x^*}{2\pi }} \end{equation}
after the crack has moved by \(\Delta a\). The stress was \begin{equation} \sigma _{yy}=\frac{K_I}{\sqrt{2\pi x^*}} \end{equation}
before the movement of the crack. The work on the crack faces is then \(W=\int dx^* \sigma _{yy} (u_y^+-u_y^-)/2\). (The
factor \(1/2\) enters because we are taking the stress to zero as the crack faces are
displacing. Imagine a simple spring with force \(f=kx\) taken from \(x_0\) to \(x=0\). The work
is \(kx_0^2/2\), equal to the elastic energy of the string at extension \(x_0\).) This gives
\begin{equation} W(\Delta a) = \frac{K_I^2}{4\pi \mu } (\kappa + 1) \int \limits _0^{\Delta a} dx^* \sqrt{\frac{\Delta a - x^*}{x^*}} = \frac{K_I^2}{\mu } \frac{\kappa +1}{8} \Delta a = \frac{K_I^2}{E} \Delta a \end{equation}
where we have used \(\int _0^1 dx \sqrt{(1-x)/x}=\pi /2\). The energy released per crack length is then \begin{equation} G = \frac{W}{\Delta a} = \frac{K_I^2}{E}. \label{eq:energyreleaserate} \end{equation}
\(G\) is called the <span class='cmti-12'>strain energy release rate </span>and has units of energy per area. Note that
Eq. \eqref{eq:energyreleaserate} is valid for a state of plain strain, which
has entered through Hooke’s law in Eqs. \eqref{eqn:crackstrainxx} to
\eqref{eqn:crackstrainxy}.
</p><!-- l. 372 --><p class='noindent'>
</p>
<h3 class='sectionHead'><span class='titlemark'>12.3 </span> <a id='x1-900012.3'></a>Griffith’s fracture criterion</h3>
<!-- l. 374 --><p class='noindent'>The value of \(K_I\) uniquely defines the stress field near the crack tip and therefore
determines when the crack advances. We define a critical \(K_{Ic}\) beyond which the crack
becomes unstable and a new crack opens when \(K_I&gt;K_{Ic}\). \(K_{Ic}\) is called the <span class='cmti-12'>fracture toughness</span>.
Generally, \(K_I\) depends on crack geometry and loading condition. For the example
worked above, a straight crack of length \(a\) in an infinite isotropic medium we get
Eq. \eqref{eqn:stress˙intensity}. We see that the stress intensity factor \(K_I\) growth
with crack length \(a\); hence there is a critical length \(a_c\) beyond which the crack
becomes unstable.
</p><!-- l. 376 --><p class='indent'> As the crack advances it creates new surface area. An advance of the crack
from length \(a\) to length \(a+\Delta a\) requires the additional energy \(\Delta E_{\text{surf}}=2\gamma \Delta a\). Here, \(\gamma \) is the surface energy
of the pristine crack surface and the factor of \(2\) enters because a crack has two
faces. Since we are looking at a plane situation, \(\Delta E_{\text{surf}}\) is an energy per unit



length.
</p><!-- l. 378 --><p class='indent'> Griffith’s fracture criterion now states that the crack advances when
the energy released from the elastic field (described by the strain energy
release rate \(G\)) is larger than the energy needed to create a new surface,
\begin{equation} G&gt;G_c \end{equation}
where \(G_c\) is Griffith’s critical energy release rate. For an ideal brittle crack,
\begin{equation} G_c=2\gamma , \end{equation}
because we only need to “pay” for the new surface with elastic energy. This allows
us to define a fracture toughness, \(K_{Ic}=\sqrt{E G_c}\), from Griffith’s theory.



</p>
<h2 class='likechapterHead'><a id='x1-1000012.3'></a>Bibliography</h2>
<div class='thebibliography'>
<p class='bibitem'><span class='biblabel'>
<a id='XWestergaard:1933'></a><span class='bibsp'>   </span></span>H. M. Westergaard. Stresses at a crack, size of the crack, and the
bending of reinforced concrete. <span class='cmti-12'>Journal Proceedings</span>, 30(11), 1933. doi:
10.14359/8300.
</p>
</div>

