---
layout: default
title: "Chapter 09 [Dez. 13-19]"
parent: Lecture
date: 2021-10-15
categories: lecture
author: Lars Pastewka
nav_order: 9
---


<h2 class='chapterHead'><span class='titlemark'>Chapter 9</span><br /><a id='x1-10009'></a>Beams</h2>
<h3 class='sectionHead'><span class='titlemark'>9.1 </span> <a id='x1-20009.1'></a>Stresses</h3>
<!-- l. 5 --><p class='noindent'><a href='https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=4555e4d3-94b0-450d-92f7-acac00e98b5f' class='url'><span class='cmtt-12'>https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=4555e4d3-94b0-450d-92f7-acac00e98b5f</span></a>
</p><!-- l. 7 --><p class='indent'> Assume a rectangular beam in plane stress or plane strain subject to bending.
(The “plane” direction is the \(y\)-direction.) The surface normal of the beam is
oriented in \(z\)-direction and \(z=0\) is in the middle of the beam. Bending will give rise to
internal stresses inside of the beam. We will require that these stresses comply
with the external shear force \(Q(x)\) and bending moment \(M(x)\) in the <span class='cmti-12'>weak </span>or integral sense, \begin{align} \label{eq:beamweakforce} Q(x) &amp;= \int _A \dif y \dif z\, \tau _{xz}(x, z) \\ \label{eq:beamweakmoment} M(x) &amp;= \int _A \dif y \dif z\, z\sigma _{xx}(x, z). \end{align}
</p><!-- l. 14 --><p class='indent'> Because of the plane state, integration in \(y\)-direction will only yield a constant
factor, the width \(t\) of the beam.
</p><!-- l. 16 --><p class='indent'> We can derive a condition equivalent to static equilibrium, \(\sigma _{ij,j}=0\), for
the weak quantities defined in Eqs. \eqref{eq:beamweakforce} and
\eqref{eq:beamweakmoment}. Taking the derivative of \(Q(x)\) yields \begin{equation} Q_{,x} = \int _A \dif y \dif z\, \tau _{xz,x} = -\int _A \dif y \dif z\, \sigma _{zz,z} = -t \left [\sigma _{zz}(x, h/2) - \sigma _{zz}(x, -h/2)\right ]. \end{equation}
We call the quantity \(q(x)\equiv t \left [\sigma _{zz}(x, h/2) - \sigma _{zz}(x, -h/2)\right ]\) the line load of the beam. Next, we take the derivative of \(M(x)\),
\begin{equation} M_{,x} = \int _A \dif y \dif z\, z\sigma _{xx,x} = -\int _A \dif y \dif z\, z\tau _{xz,z} =-t\left [z\tau _{xz}\right ]_{-h/2}^{h/2} + \int _A \dif y \dif z\, z\tau _{xz}. \end{equation}
The first term on the right hand side vanishes because the surfaces are traction
free, \(\tau _{xz}=0\) at \(z=h/2\) and \(z=-h/2\). This yields \begin{align} Q_{,x} &amp;= -q(x) \\ M_{,x} &amp;= Q(x) \end{align}
</p><!-- l. 34 --><p class='indent'> for the weak form of the equilibrium conditions.
</p>
<div class='framedenv' id='shaded*-1'>
<!-- l. 36 --><p class='noindent'><span class='underline'><span class='cmbx-12'>Note:</span></span> We have not yet talked about free surfaces, but of course every physical
object will be bounded by surfaces. The surface can be loaded, i.e. there can a
force acting on it. This force, normalized by area, is called a <span class='cmti-12'>tractions</span>. (We have
already encountered a type of traction in form of the <span class='cmti-12'>line load </span>in the first
chapters.) The traction is a vector field (defined over the surface of our object)
with components \(t_x\), \(t_y\) and \(t_z\). Note that in the literature these are often denoted by \(P\)
for the normal component, and \(Q_x\), \(Q_y\) for the components perpendicular to the surface.
(Attention: Do not confuse this with the \(Q\) that we call the shear force
here!)
</p><!-- l. 39 --><p class='indent'> These traction enter our equations as boundary condition. They fix three
components of the stress tensor at the surface. For a surface with a normal in
\(z\)-direction, \begin{equation} \sigma _{zz} = -t_z, \quad \sigma _{xz} = t_x \quad \text{and}\quad \sigma _{yz} = t_y. \end{equation}
For a traction-free surface, \begin{equation} \sigma _{zz} = \sigma _{xz} = \sigma _{yz} = 0 \end{equation}
at the surface. Since the stress-tensor is a tensor field that varies throughout the
body, these components will of course deviate from the surface tractions when we
regard points in the interior of our (deformed) body. </p></div>



<!-- l. 50 --><p class='indent'> We now <span class='cmti-12'>assume </span>that the stress is a linear function of the position \(z\)
perpendicular to the beam axis, \begin{equation} \label{eq:beamstress1} \sigma _{xx}(x,z) = C(x) z. \end{equation}
In what follow we show that this is a good assumption, i.e. we can fulfill force and
moment equilibrium and the resulting strains fulfill the compatibility
conditions.
</p>
<div class='framedenv' id='shaded*-1'>
<!-- l. 57 --><p class='noindent'><span class='underline'><span class='cmbx-12'>Note:</span></span> The theory derived in this chapter is commonly referred to as the
<span class='cmti-12'>Euler-Bernoulli beam theory</span>. The starting point of this theory is typically not
Eq. \eqref{eq:beamstress1}, but the assumption that each cross section will
remain plane and undergo small rotations during deformation. These are
sometimes called the <span class='cmti-12'>Bernoulli assumptions</span>. They imply that the strain \(\varepsilon _{xx}\propto z\) rather
than the stress. It is often argued that \(\sigma _{xx}=E \varepsilon _{xx}\) but this of course ignores the other
components of the strain tensor. As will be seen below, the Bernoulli
assumptions are actually wrong but assuming a linear stress profile leads
to the correct small strain expression for the deformation of a beam. </p></div>
<!-- l. 61 --><p class='indent'> It is straightforward to compute the bending moment, \begin{equation} \label{eq:beammoment} M(x) = \int _A \dif y \dif z\, \sigma _{xx}(x, z) z = C(x) \int _A \dif y \dif z\, z^2 = C(x) I_y, \end{equation}
where \(A\) is the cross-section of the beam and \begin{equation} I_y = \int _A \dif y \dif z\, z^2 \end{equation}
is the <span class='cmti-12'>axial moment of inertia</span>. For a rectangular beam of height \(h\) and width \(t\), \(I_y=h^3 t/12\).
The moment of inertia is a geometric factor and depends on the shape of the
cross-section of the beam.
</p><!-- l. 72 --><p class='indent'> We can rewrite Eq. \eqref{eq:beamstress1} as \begin{equation} \label{eq:beamstressxx} \sigma _{xx}(x,z) = \frac{M(x)}{I_y} z. \end{equation}
Note that an additional longitudinal force \(L\) will simple be an additive contribution
to Eq. \eqref{eq:beamstressxx}, \(\sigma _{xx}(x,z) = M(x)/I_y z + L/A\).
</p><!-- l. 79 --><p class='indent'> We can now use the condition for static equilibrium to compute the full stress
tensor \(\t{\sigma }\). From \(\sigma _{xx,x} + \tau _{xz,z}=0\) we obtain \begin{equation} \tau _{xz,z} = - \frac{z}{I_y} M_{,x} = - \frac{z}{I_y} Q(x). \end{equation}
We can integrate this across the height \(h\) of the beam, keeping in mind that \(\tau _{xz}=0\) at a
traction-free surface, to yield \begin{equation} \label{eq:beamstressxz} \tau _{xz}(x, z) = \frac{Q(x)}{2I_y} \left (\frac{h^2}{4} - z^2\right ). \end{equation}
Next, we use \(\sigma _{zz,z}+\tau _{xz,x}=0\) to obtain \begin{equation} \sigma _{zz,z} = - \frac{1}{2I_y} Q_{,x} \left (\frac{h^2}{4} - z^2\right ) = \frac{q(x)}{2I_y} \left (\frac{h^2}{4} - z^2\right ). \end{equation}
We need to integrate this equation again, but now \(\sigma _{zz}\not =0\) at the surface since
the beam is subject to a line load \(q(x)\). Rather, we need the condition that
the loads on top and bottom surface of the beam balance, \(\sigma _{zz}(x,h/2)=-\sigma _{zz}(x,-h/2)\). This gives
\begin{equation} \label{eq:beamstresszz} \sigma _{zz}(x, z) = \frac{q(x)}{2I_y} \left (\frac{h^2}{4} - \frac{z^2}{3}\right ) z \end{equation}
with \begin{equation} \label{eq:beambczz} \sigma _{zz}(x,h/2)=\frac{q(x)h^3}{24I_y}=\frac{q(x)}{2t} \end{equation}
where \(t\) is the width of the beam.
</p><!-- l. 116 --><p class='indent'> Note that in this derivation, we have required that the stress gives rise to a



certain bending moment through Eq. \eqref{eq:beammoment}. Since we do not
prescribe the specific stress state \(\sigma _{xx}(x, z)\) but only its integral, this is a <span class='cmti-12'>weak </span>condition.
Similarly, integration of Eq. \eqref{eq:beamstressxz} in accordance with
Eq. \eqref{eq:beamweakforce} gives \begin{equation} \int _{-t/2}^{t/2} \dif y \int _{-h/2}^{h/2} \dif z\, \tau _{xz}(x, z) = Q(x), \end{equation}
i.e. the force acting on the cross-section at position \(x\) along the beam. Again, this
condition is fulfilled in the integral, i.e. in the weak sense.
</p><!-- l. 124 --><p class='noindent'>
</p>
<h3 class='sectionHead'><span class='titlemark'>9.2 </span> <a id='x1-30009.2'></a>Displacements</h3>
<!-- l. 126 --><p class='noindent'><a href='https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=8e0b3bab-8abc-4c2a-87cc-acac00e98b92' class='url'><span class='cmtt-12'>https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=8e0b3bab-8abc-4c2a-87cc-acac00e98b92</span></a>
</p><!-- l. 128 --><p class='indent'> Now that we know the stress inside the beam, we can compute the
displacement and thereby the deformation of the beam from Hooke’s law. Starting
from Hooke’s law (in plain stress, i.e. for \(\sigma _{yy}=0\)), \begin{align} \label{eq:beamhooke1} \varepsilon _{xx} \equiv u_{x,x} &amp;= \sigma _{xx}/E - \nu \sigma _{zz}/E \\ \label{eq:beamhooke2} 2\varepsilon _{xz} \equiv u_{x,z} + u_{z,x} &amp;= 2(1+\nu )\tau _{xz}/E, \end{align}
</p><!-- l. 135 --><p class='indent'> and taking the derivative of Eq. \eqref{eq:beamhooke2} with respect to \(x\), we
obtain \begin{equation} u_{x,xz} + u_{z,xx}=2(1+\nu )\tau _{xz,x}/E \end{equation}
and \begin{equation} u_{x,xz} + u_{z,xx}=\partial _z( u_{x,x}) + u_{z,xx}=u_{z,xx} + (\sigma _{xx,z} - \nu \sigma _{zz,z})/E. \end{equation}
Combining these two equations yields \begin{equation} u_{z,xx} = \left [2(1+\nu )\tau _{xz,x} - \sigma _{xx,z} + \nu \sigma _{zz,z}\right ]/E, \end{equation}
where we now insert Eqs. \eqref{eq:beamstressxx}, \eqref{eq:beamstressxz} and
\eqref{eq:beamstresszz}. This gives \begin{equation} u_{z,xx} = \frac{1}{E I_y} \left [-\left (1+\frac{\nu }{2}\right ) \left (\frac{h^2}{4} - z^2\right )q(x) - M(x)\right ], \end{equation}
which at the surface of the beam \(w(x)=u_z(x,h/2)\) becomes \begin{equation} E I_y w_{,xx} = - M(x). \end{equation}
This equation is called the <span class='cmti-12'>Euler-Bernoulli beam equation</span>. By using \(M_{xx}=-q(x)\) we can write
this as \begin{equation} (E I_y w_{,xx})_{,xx} = q(x), \end{equation}
in terms of the line load \(q(x)\), or \begin{equation} E I_y w_{,xxxx} = q(x), \end{equation}
if \(E I_y\) does not depend on position \(x\).
</p><!-- l. 166 --><p class='noindent'>
</p>
<h3 class='sectionHead'><span class='titlemark'>9.3 </span> <a id='x1-40009.3'></a>Buckling</h3>
<!-- l. 168 --><p class='noindent'><a href='https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=95ca7b6a-0bf7-441e-9ca0-acb901506883' class='url'><span class='cmtt-12'>https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=95ca7b6a-0bf7-441e-9ca0-acb901506883</span></a>



</p>
<h2 class='likechapterHead'><a id='x1-50009.3'></a>Bibliography</h2>

