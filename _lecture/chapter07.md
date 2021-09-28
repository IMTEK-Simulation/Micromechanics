---
layout: default
title: "Chapter 07"
parent: Lecture
date: 2021-09-28
categories: lecture
author: Lars Pastewka
nav_order: 7
---


<h2 class='chapterHead'><span class='titlemark'>Chapter 7</span><br /><a id='x1-10007'></a>Hooke’s law</h2>
<!-- l. 3 --><p class='noindent'><a href='https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=6580c65e-93a2-4e11-9a50-ac9100b55895' class='url'><span class='cmtt-12'>https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=6580c65e-93a2-4e11-9a50-ac9100b55895</span></a>
</p><!-- l. 5 --><p class='indent'> Finally, we need a constitutive relation (material law) to close
Eqs. \eqref{eqn:Equi˙condition} and \eqref{eqn:Strain˙gradient}. Since we
will be working in linear elasticity, the constitutive equation is a linear
relationship between \(\t{\sigma }\) and \(\t{\varepsilon }\). The most general form of this linear relationship is
\begin{equation} \label{eqn:Hookeslaw} \t{\sigma } = \t{\t{C}} : \t{\varepsilon }, \text{or using Einstein summation} \ \sigma _{ij} = C_{ijkl} \varepsilon _{kl}. \end{equation}
It is called <span class='cmti-12'>Hooke’s law</span>. The quantity \(\t{\t{C}}\) is a fourth order symmetric tensor of elastic
constants that contains at most 21 independent elastic moduli. To see
that there are only \(21\) independent coefficients, it is useful to remove the
symmetric entries from \(\t{\sigma }\) and \(\t{\varepsilon }\) and express them as 6-vectors in Voigt notation,
\begin{equation} \label{eqn:sig_eps_Voigt} \v{\sigma } = (\sigma _{xx},\sigma _{yy},\sigma _{zz},\sigma _{yz},\sigma _{xz},\sigma _{xy}) \ \text{and} \ \v{\varepsilon } = (\varepsilon _{xx},\varepsilon _{yy},\varepsilon _{zz},2\varepsilon _{yz},2\varepsilon _{xz},2\varepsilon _{xy}). \end{equation}
Then \(\sigma =\t{C} \cdot \v{\varepsilon }\) where \(\t{C}\) is a \(6\times 6\) symmetric matrix called the <span class='cmti-12'>stiffness matrix </span>containing the
above-mentioned 21 independent elastic constants. (There are \(6\cdot 6=36\) components, but
the matrix is symmetric.)
</p><!-- l. 18 --><p class='indent'> Note that the off-diagonal components of \(\t{\sigma }\) are often denoted by \(\tau _{xy} \equiv \sigma _{xy}, \tau _{xz} \equiv \sigma _{xz}\ \text{and}\ \tau _{yz} \equiv \sigma _{yz}\). The
off-diagonal components of \(\t{\varepsilon }\) are often denoted by \(\gamma _{xy} \equiv 2\varepsilon _{xy}, \gamma _{xz} \equiv 2\varepsilon _{xz}\ \text{and}\ \gamma _{yz} \equiv 2\varepsilon _{yz}\) and absorb the factor of 2 that
occurs in Eq. \eqref{eqn:sig˙eps˙Voigt}. Voigt notation then becomes \begin{equation} \label{eqn:sig_eps_Voigt_gamma} \v{\sigma } = (\sigma _{xx},\sigma _{yy},\sigma _{zz},\tau _{yz},\tau _{xz},\tau _{xy}) \ \text{and} \ \v{\varepsilon } = (\varepsilon _{xx},\varepsilon _{yy},\varepsilon _{zz},\gamma _{yz},\gamma _{xz},\gamma _{xy}) \end{equation}
</p>
<div class='framedenv' id='shaded*-1'>
<!-- l. 24 --><p class='noindent'><span class='underline'><span class='cmbx-12'>Note:</span></span> It is important to keep in mind that the \(\gamma \)’s contain a factor 2 but the \(\tau \)’s do
not. The factor of 2 ensures that \(\v{\sigma }=\t{C} \cdot \v{\varepsilon }\) and \(\t{\sigma } = \t{\t{C}} : \t{\varepsilon }\) are the same constitutive law. </p></div>
<!-- l. 28 --><p class='indent'> For isotropic elasticity, the total 21 independent elastic constants reduce to
two. The constitutive equation for isotropic elasticity is \begin{equation} \label{eqn:Isotropic_elasticity} \sigma _{ij} = \lambda \delta _{ij} \varepsilon _{kk} + 2\mu \varepsilon _{ij} \end{equation}
or its inverse \begin{equation} \label{eqn:Isotropic_elasticity_inverse} \varepsilon _{ij} = \frac{1}{2G} \sigma _{ij} - \frac{\nu }{E} \delta _{ij} \delta _{kk} = \frac{1}{E} [(1+\nu )\sigma _{ij} - \nu \delta _{ij} \sigma _{kk}], \end{equation}
where \(\delta _{ij}\) is the Kronecker-Delta. These expressions have been conveniently
written in their most simple form. The constants that show up in
Eqs. \eqref{eqn:Isotropic˙elasticity} and \eqref{eqn:Isotropic˙elasticity˙inverse}
are the shear modulus \(\mu \), Lamé’s first constant \(\lambda \), Young’s modulus \(E\) and Poisson
number \(\nu \). Both \(\lambda \) and \(\nu \) are often called Lamé’s constants. Note that \(\sigma _{kk} = 3\sigma _h\) (Einstein
summation!) where \(3\sigma _h\) is the hydrostatic stress.
</p><!-- l. 41 --><p class='indent'> The four moduli are not independent (only two are), and the following
expressions relate the pairs \(\lambda \), \(\mu \) and \(E\), \(\nu \) to each other: \begin{align} \label{eqn:Relation_Lame} \lambda &amp;= \frac{E\nu }{(1+\nu )(1-2\nu )} \\ \mu &amp;= \frac{E}{2(1+\nu )} \\ \lambda + \mu &amp;= \frac{E}{2(1+\nu )(1-2\nu )} \\ E &amp;= \frac{\mu (3\lambda + 2\mu )}{\lambda + \mu } \\ \nu &amp;= \frac{\lambda }{2(\lambda + \mu )} \end{align}
</p><!-- l. 51 --><p class='indent'> Note that the volumetric strain \(\varepsilon _h = \frac{1}{3}\:{\rm tr} \ \t{\varepsilon } = \frac{1}{E} [(1 + \nu )\sigma _h - 3\, \nu \sigma _h] = \frac{1}{E} (1-2\nu )\sigma _h\) vanishes at \(\nu = 1/2\). In this case, \(\sigma _{ij} = 2\sigma _h \varepsilon _{ij}\) because the \(\varepsilon _h = \varepsilon _{kk}\) must
vanish. Note that another common symbol for the shear modulus \(\mu \) is the Latin



letter \(G\).
</p><!-- l. 53 --><p class='indent'> We can also write down a free energy functional (often also called a
hyperelastic energy density), which is quadratic in the strain \(\t{\varepsilon }\), \begin{equation} \label{eqn:Free_energy} W = \frac{1}{2} \lambda \varepsilon _{ii}^2 + \mu \varepsilon _{ij}^2 \end{equation}
Using \(\sigma _{ij} = \partial W / \partial \varepsilon _{ij}\) recovers the above constitutive expression Eq. \eqref{eqn:Isotropic˙elasticity}.
From the free energy functional we see that any isotropic material must have \(\lambda &gt; 0\) and
\(\mu &gt; 0\), otherwise the energy could be made arbitrarily small by increasing the
deformation of the solid. This limits the Poisson number to the range \( -1 &lt; \nu &lt; 1/2 \). Note that \(\nu &lt;0\)
is typically only achieved for architectured materials such as foams or
metamaterials.
</p><!-- l. 60 --><p class='indent'> <a href='https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=61fa9204-ff9c-4874-b217-acaa0109e189' class='url'><span class='cmtt-12'>https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=61fa9204-ff9c-4874-b217-acaa0109e189</span></a>
</p><!-- l. 62 --><p class='indent'> <a href='https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=2f5be83c-cd57-41c8-aa7a-acaa0109e1f0' class='url'><span class='cmtt-12'>https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=2f5be83c-cd57-41c8-aa7a-acaa0109e1f0</span></a>



</p>
<h2 class='likechapterHead'><a id='x1-20007'></a>Bibliography</h2>

