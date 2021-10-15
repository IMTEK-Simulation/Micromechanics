---
layout: default
title: "Chapter 10 [Jan. 10-16 (2022)]"
parent: Lecture
date: 2021-10-15
categories: lecture
author: Lars Pastewka
nav_order: 10
---


<h2 class='chapterHead'><span class='titlemark'>Chapter 10</span><br /><a id='x1-100010'></a>Plates</h2>
<!-- l. 3 --><p class='noindent'><a href='https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=567d8212-1aeb-4360-90e4-acb901506868' class='url'><span class='cmtt-12'>https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=567d8212-1aeb-4360-90e4-acb901506868</span></a>
</p>
<h3 class='sectionHead'><span class='titlemark'>10.1 </span> <a id='x1-200010.1'></a>Stress</h3>
<!-- l. 7 --><p class='noindent'>Kirchhoff plate theory is the straightforward generalization of Euler-Bernoulli
beam theory to plates. We abandon the plane situation in which all derivatives in
\(y\)-direction vanish. The weak boundary conditions then become \begin{align} \label{eq:beamweakforcex} Q_x(x,y) &amp;= \int _h \dif z\, \tau _{xz}(x, y, z) \\ \label{eq:beamweakforcey} Q_y(x,y) &amp;= \int _h \dif z\, \tau _{yz}(x, y, z) \\ \label{eq:beamweakmomentxx} M_{xx}(x, y) &amp;= \int _h \dif z\, z \sigma _{xx}(x, y, z) \\ \label{eq:beamweakmomentyy} M_{yy}(x, y) &amp;= \int _h \dif z\, z \sigma _{yy}(x, y, z) \\ \label{eq:beamweakmomentxy} M_{xy}(x, y) &amp;= \int _h \dif z\, z \tau _{xy}(x, y, z), \end{align}
</p><!-- l. 20 --><p class='indent'> where the integral is over the height \(h\) of the plate. \(Q_x\) and \(Q_y\) are called shear forces,
\(M_{xx}\) and \(M_{yy}\) are bending moments and \(M_{xy}\) is the torsional moment.
</p><!-- l. 22 --><p class='indent'> Note that employing static equilibrium \(\sigma _{ij,j}=0\) we obtain \begin{equation} Q_{x,x} + Q_{y,y} = \int _{-h/2}^{h/2} \dif z\, \left ( \tau _{zx,x} + \tau _{zy,y} \right ) = -\int _{-h/2}^{h/2} \dif z\, \tau _{zz,z} \end{equation}
but \begin{equation} \int _{-h/2}^{h/2} \dif z\, \tau _{zz,z} = \tau _{zz}(x, y, h/2) - \tau _{zz}(x, y, -h/2) \equiv p(x,y) \end{equation}
where \(p(x,y)\) is the pressure on the plate (cf. also the corresponding equation
Eq. \eqref{eq:beambczz} for the beam). Similarly \begin{equation} M_{xx,x} + M_{xy,y} = \int _{-h/2}^{h/2} \dif z\, z\left ( \tau _{xx,x} + \tau _{xy,y} \right ) = -\int _{-h/2}^{h/2} \dif z\, z\tau _{xz,z} \end{equation}
and \begin{equation} \int _{-h/2}^{h/2} \dif z\, z\tau _{xz,z} = \left [z\tau _{xz}\right ]_{-h/2}^{h/2} - \int _{-h/2}^{h/2} \dif z\, \tau _{xz} = -Q_x. \end{equation}
where the last equality holds because \(\tau _{xz}(x,y,h/2)=-\tau _{xz}(x,y,-h/2)\). The condition for static equilibrium \(\sigma _{ij,j}=0\)
therefore becomes \begin{align} \label{eq:plateeq1} Q_{x,x} + Q_{y,y} &amp;=-p(x,y) \\ \label{eq:plateeq2} M_{xx,x} + M_{xy,y}&amp;=Q_x(x,y) \\ \label{eq:plateeq3} M_{xy,x} + M_{yy,y}&amp;=Q_y(x,y) \end{align}
</p><!-- l. 48 --><p class='indent'> in the weak form. Note that this can be written in the compact form \(Q_{i,i}=-p\) and
\(M_{ij,j}=Q_i\).
</p><!-- l. 50 --><p class='indent'> As in the Euler-Bernoulli case, we assume that the components \(\sigma _{xx}\), \(\sigma _{yy}\) and \(\tau _{xy}\) vary
linearly with \(z\). We can write \begin{align} \sigma _{xx}(x, y, z) &amp;= \frac{M_{xx}(x, y)}{I} z \\ \sigma _{yy}(x, y, z) &amp;= \frac{M_{yy}(x, y)}{I} z \\ \tau _{xy}(x, y, z) &amp;= \frac{M_{xy}(x, y)}{I} z \end{align}
</p><!-- l. 56 --><p class='indent'> with \(I=\int dz\, z^2=h^3/12\). The remaining components of the stress tensor are obtained from static
equilibrium. Static equilibrium yields \begin{equation} \tau _{xz,z} = -\frac{z}{I} Q_x \quad \text{and}\quad \tau _{yz,z} = -\frac{z}{I} Q_y \end{equation}
which can be integrated under the condition \(\tau _{xz}(x, y, h/2)=\tau _{xz}(x, y, -h/2)=0\) to \begin{equation} \tau _{xz}(x, y, z) = \frac{Q_x}{2I} \left (\frac{h^2}{4}-z^2\right ) \quad \text{and}\quad \tau _{yz}(x, y, z) = \frac{Q_y}{2I} \left (\frac{h^2}{4}-z^2\right ). \end{equation}
This is analogous to Eq. \eqref{eq:beamstressxz} for the beam.
</p><!-- l. 70 --><p class='indent'> We are finally left with finding an expression for \(\sigma _{zz}\). Again we use static
equilibrium to obtain \begin{equation} \sigma _{zz,z} = -\tau _{xz,x}-\tau _{yz,y} = \frac{p(x,y)}{2I} \left (\frac{h^2}{4}-z^2\right ). \end{equation}
Integration under the condition that the loads on top and bottom surface of the
plate balance, \(\sigma _{zz}(x,h/2)=-\sigma _{zz}(x,-h/2)\), gives \begin{equation} \label{eq:platestresszz} \sigma _{zz}(x, y, z) = \frac{p(x, y)}{2I} \left (\frac{h^2}{4} - \frac{z^2}{3}\right ) z. \end{equation}
At the top and bottom of the plate we find \(\sigma _{zz}(x,h/2)=-\sigma _{zz}(x,-h/2)=p(x,y)/2\).
</p><!-- l. 83 --><p class='noindent'>
</p>
<h3 class='sectionHead'><span class='titlemark'>10.2 </span> <a id='x1-300010.2'></a>Displacements</h3>
<!-- l. 85 --><p class='noindent'>Now that we know the stress inside the plate, we can again compute the



displacements from Hooke’s law. In the full three-dimensional case, Hooke’s law, \begin{align} \label{eq:platehooke1} \varepsilon _{xx} \equiv u_{x,x} &amp;= (\sigma _{xx} - \nu \sigma _{yy} - \nu \sigma _{zz})/E \\ \label{eq:platehooke2} \varepsilon _{yy} \equiv u_{y,y} &amp;= (\sigma _{yy} - \nu \sigma _{xx} - \nu \sigma _{zz})/E \\ \label{eq:platehooke3} 2\varepsilon _{xz} \equiv u_{x,z} + u_{z,x} &amp;= 2(1+\nu )\tau _{xz}/E \\ \label{eq:platehooke4} 2\varepsilon _{yz} \equiv u_{y,z} + u_{z,y} &amp;= 2(1+\nu )\tau _{yz}/E \\ \label{eq:platehooke5} 2\varepsilon _{xy} \equiv u_{x,y} + u_{y,x} &amp;= 2(1+\nu )\tau _{xy}/E, \end{align}
</p><!-- l. 98 --><p class='indent'> and taking the derivative of Eq. \eqref{eq:platehooke3} with respect to \(x\) and
of Eq. \eqref{eq:platehooke4} with respect to \(y\), we obtain \begin{align} \label{eq:ux1} u_{x,xz} + u_{z,xx} &amp;= 2(1+\nu )\tau _{xz,x}/E \\ \label{eq:uy1} u_{y,yz} + u_{z,yy} &amp;= 2(1+\nu )\tau _{yz,y}/E \end{align}
</p><!-- l. 105 --><p class='indent'> and \begin{align} \label{eq:ux2} u_{x,xz} + u_{z,xx}=\partial _z( u_{x,x}) + u_{z,xx}&amp;=u_{z,xx} + (\sigma _{xx,z} - \nu \sigma _{yy,z} - \nu \sigma _{zz,z})/E \\ \label{eq:uy2} u_{y,yz} + u_{z,yy}=\partial _z( u_{y,y}) + u_{z,yy}&amp;=u_{z,yy} + (\sigma _{yy,z} - \nu \sigma _{xx,z} - \nu \sigma _{zz,z})/E. \end{align}
</p><!-- l. 112 --><p class='indent'> Combining Eqs. \eqref{eq:ux1}, \eqref{eq:ux2} and Eqs. \eqref{eq:uy1},
\eqref{eq:uy2} and noting that \(\sigma _{zz,z}=-\tau _{xz,x}-\tau _{xz,y}\) yields \begin{align} u_{z,xx} &amp;= \left [(2+\nu )\tau _{xz,x} - \nu \tau _{yz,y} - \sigma _{xx,z} + \nu \sigma _{yy,z} \right ]/E \\ u_{z,yy} &amp;= \left [(2+\nu )\tau _{yz,y} - \nu \tau _{xz,x} - \sigma _{yy,z} + \nu \sigma _{xx,z}\right ]/E. \end{align}
</p><!-- l. 117 --><p class='indent'> We now create linear combination of these expressions such that \(\sigma _{xx,z}=M_{xx}/I\) or \(\sigma _{yy,z}=M_{yy}/I\) drop out,
\begin{align} u_{z,xx} + \nu u_{z,yy} &amp;= \left [(2+\nu -\nu ^2)\tau _{xz,x} - \nu (1+\nu )\tau _{yz,y} - (1-\nu ^2)M_{xx}/I \right ]/E \\ u_{z,yy} + \nu u_{z,xx} &amp;= \left [(2+\nu -\nu ^2)\tau _{yz,y} - \nu (1+\nu )\tau _{xz,x} - (1-\nu ^2)M_{yy}/I \right ]/E. \end{align}
</p><!-- l. 122 --><p class='indent'> We now only consider the displacement at the surface, \(w(x,y)\equiv u_z(x,y,h/2)\). Since the surfaces are
traction free, all terms involving \(\tau _{xz}\) and \(\tau _{yz}\) vanish. Hence \begin{align} \label{eq:plateMxx} M_{xx} &amp;= -K (w_{,xx} + \nu w_{,yy}) \\ \label{eq:plateMyy} M_{yy} &amp;= -K (w_{,yy} + \nu w_{,xx}) \end{align}
</p><!-- l. 129 --><p class='indent'> with the <span class='cmti-12'>flexural rigidity</span> \(K=EI/(1-\nu ^2)=Eh^3/[12(1-\nu ^2)]\).
</p><!-- l. 131 --><p class='indent'> Finally, we are looking for an expression for \(M_{xy}=I\tau _{xy,z}\). We have from
Eqs. \eqref{eq:platehooke3}-\eqref{eq:platehooke5}\begin{equation} \frac{2(1+\nu )}{EI} M_{xy} = u_{x,yz} + u_{y,xz} = \frac{2(1+\nu )}{E} (\tau _{xz,y} + \tau _{yz,x}) - 2u_{z,xy}, \end{equation}
which yields \begin{equation} \label{eq:plateMxy} M_{xy} = -K(1-\nu ) w_{,xy}, \end{equation}
the desired expression.
</p><!-- l. 142 --><p class='indent'> We now plug Eqs. \eqref{eq:plateMxx}, \eqref{eq:plateMyy} and
\eqref{eq:plateMxy} into the equilibrium conditions Eqs. \eqref{eq:plateeq2} and
\eqref{eq:plateeq3}. This yields \begin{align} -K(w_{,xxx} + w_{,xyy}) &amp;= Q_x(x, y) \\ -K(w_{,yyy} + w_{,xxy}) &amp;= Q_y(x, y) \\ -K(w_{,xxxx} + 2w_{,xxyy} + w_{,yyyy}) &amp;= -p(x, y). \end{align}
</p><!-- l. 148 --><p class='indent'> The last expression is Kirchhoff’s equation, \begin{equation} w_{,xxxx} + 2w_{,xxyy} + w_{,yyyy} = \nabla ^2 \nabla ^2 w = \nabla ^4 w = \frac{p}{K}, \end{equation}
that governs the deformation of plates.



</p>
<h2 class='likechapterHead'><a id='x1-400010.2'></a>Bibliography</h2>

