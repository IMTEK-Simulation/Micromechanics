---
layout: default
title: "Chapter 05"
parent: Lecture
date: 2021-10-06
categories: lecture
author: Lars Pastewka
nav_order: 5
---


<h2 class='chapterHead'><span class='titlemark'>Chapter 5</span><br /><a id='x1-10005'></a>Stress</h2>
<div id='shaded*-1' class='framedenv'>
<!-- l. 3 --><p class='noindent'><span class='underline'><span class='cmbx-12'>Note:</span></span> We have encountered vectors in the first chapters on statics of rigid bodies
and have intuitively worked with them. To recap, a vector is an object that
represents a direction and a magnitude. Geometrically, they are often represented
as arrows. In a Cartesian coordinate system (or basis), a vector can be represented
by a set of numbers. For example in two dimensions, we denote the components of
the vector \(\v{v}\) as the \(x\) and \(y\) components and typically write the vector in the
column-form \begin{equation} \label{eq:cartvec} \v{v} = v_x \hat{x} + v_y \hat{y} \equiv \begin{pmatrix} v_x \\ v_y \end{pmatrix} \end{equation}
where \(v_x\) and \(v_y\) are real numbers that are called the <span class='cmti-12'>components </span>of the vector \(\v{v}\). \(\hat{x}\) and \(\hat{y}\)
are vectors of unit length that point along the \(x\)- and \(y\)-directions of the coordinates.
The length of the vector is given by the 2-norm \(|\v{v}|\equiv \lVert \v{v}\rVert _2=(v_x^2 + v_y^2)^{1/2}\).
</p><!-- l. 11 --><p class='indent'> It is important to emphasize that this is a <span class='cmti-12'>representation </span>of the vector and the
components \(v_i\in \mathbb{R}\) depend on the specific basis \(\hat{x}\) and \(\hat{y}\). This representation is called a
<span class='cmti-12'>tensor of order</span> \(1\). The order of a tensor is sometimes also called degree or rank.
Any component-wise representation, such as the one on the right hand side of
Eq. \eqref{eq:cartvec}, implies a basis. The basis is written explicitly as \(\hat{x}\) and \(\hat{y}\) in
the middle expression of Eq. \eqref{eq:cartvec}. Note that in component
notation, the basis vectors are \begin{equation} \hat{x} = \begin{pmatrix} 1 \\ 0 \end{pmatrix} \quad \text{and}\quad \hat{y} = \begin{pmatrix} 0 \\ 1 \end{pmatrix}. \end{equation}
Note that we will restrict the discussion here to orthogonal bases where \(\hat{x}\cdot \hat{y}=0\). The
discussion here will use two-dimensional examples, but a generalization to more
that two dimensions is straightforward
</p><!-- l. 19 --><p class='indent'> Formally, a vector is an element of a <span class='cmti-12'>vector space</span>. A vector space \(V\) (often also
called a <span class='cmti-12'>linear space</span>) is a set of objects (for example the set containing our basis
vectors \(\hat{x}\) and \(\hat{y}\) and linear combinations thereof) along with two operations:
Addition (of two vectors) and multiplication (of a vector) with a scalar. These
operations again yield a vector, i.e. an element of \(V\). This can be expressed as
</p>
<ul class='itemize1'>
<li class='itemize'>\(\v{u},\;\v{v}\in V\), then \(\v{u}+\v{v}\in V\)
</li>
<li class='itemize'>\(a\in \mathbb{R}\) and \(\v{u}\in V\), then \(a\cdot \v{u}\in V\)</li></ul>
<!-- l. 25 --><p class='noindent'>and hence Eq. \eqref{eq:cartvec} yields a vector. In general, we may multiply the
vectors by an element of a <span class='cmti-12'>algebraic number field</span> \(\mathbb{F}\) rather than \(\mathbb{R}\). Then we say \(V\) is a
vector space over the field \(\mathbb{F}\). In this notes (and our lectures) we will always deal
with either real (\(\mathbb{F}=\mathbb{R}\)) or complex (\(\mathbb{F}=\mathbb{C}\)) numbers.
</p><!-- l. 28 --><p class='indent'> Recall the concept of an algebraic number field in mathematics. A field is an
algebraic structure that is a set along with two operations “\(+\)” and “\(\cdot \)” associating
an element with two elements of the set. The operations are required to satisfy the
field axioms: </p>



<ul class='itemize1'>
<li class='itemize'>Associativity of addition and multiplication: \(a+(b+c)=(a+b)+c\) and \(a\cdot (b\cdot c)=(a\cdot b)\cdot c\).
</li>
<li class='itemize'>Commutativity of addition and multiplication: \(a+b=b+a\) and \(a\cdot b=b\cdot a\).
</li>
<li class='itemize'>Additive and multiplicative identity: \(0\in \mathbb{F}\) with \(a+0=a\) and \(1\in \mathbb{F}\) with \(1\cdot a=a\).
</li>
<li class='itemize'>Additive inverses: \(\forall a\in \mathbb{F}\) we have an inverse element \(i=-a\) with \(a+i=a+(-a)=0\)
</li>
<li class='itemize'>Multiplicative inverses: \(\forall a\ne 0\) we have an element \(a^{-1}\) with \(a\cdot a^{-1}=1\).
</li>
<li class='itemize'>Distributivity of multiplication over addition: \(a\cdot (b+c)=a\cdot b+a\cdot c\)</li></ul>
<!-- l. 37 --><p class='noindent'>Note that in physics a <span class='cmti-12'>field </span>is typically a quantity that depends on position and not
an algebraic number field. A scalar field \(\phi (\v{r})\) would be scalar quantity \(\phi \in \mathbb{R}\) that depends
on a vector (the position) \(\v{r}\in V\). While these two meanings of the term <span class='cmti-12'>field </span>exist, we
will always refer to this latter physical meaning in the following. Additionally, we
have here used the dot \(\cdot \) to indicate a scalar multiplication, but we will reserve this
dot in the rest of these notes for contractions, i.e. operations that implicitly
include a sum.
</p><!-- l. 39 --><p class='indent'> The simplest (and also most important) operation on a vector is a linear
transformation. The simplest linear transformation is the multiplication with a
scalar \(a\in \mathbb{R}\). In terms of the geometric interpretation of a vector, this multiplication
would change the length of the vector by \(a\) but not its direction.
</p><!-- l. 41 --><p class='indent'> A general linear transformation can in addition change the direction of the
vector and therefore represent for example rotations. Given a vector \(\v{u}\)
and a scalar \(\alpha \), a linear transformation \(\mathcal{L}\) to a vector \(\v{u}'=\mathcal{L}\v{u}\) has the properties: \begin{align} \label{eq:linscalar} \mathcal{L}(\alpha \v{u})&amp;=\alpha \mathcal{L}\v{u} \\ \label{eq:linsum} \mathcal{L}(\v{u} + \v{v})&amp;=\mathcal{L}\v{u} + \mathcal{L}\v{v} \end{align}
</p><!-- l. 51 --><p class='indent'> We will only deal with linear operations that map between the same vector
space \(V\), \(\mathcal{L}: V\mapsto V\). (It may map between quantities with different physical units.) Given a
component-wise (Cartesian) representation of a vector, Eq. \eqref{eq:cartvec}, a
linear transformation can be expressed as a multiplication by a matrix. This is
easily by applying Eqs. \eqref{eq:linscalar} and \eqref{eq:linsum} to
\begin{equation} \label{eq:linvec} \v{w} = \mathcal{L}\v{v} = \mathcal{L}(v_x \hat{x} + v_y \hat{y}) = v_x \mathcal{L} \hat{x} + v_y \mathcal{L} \hat{y}. \end{equation}
We can express any element of our vector space as a linear combination of the
basis vectors, hence also \begin{align} \label{eq:linbasis} \mathcal{L}\hat{x} &amp;= L_{xx} \hat{x} + L_{yx} \hat{y} \\ \mathcal{L}\hat{y} &amp;= L_{xy} \hat{x} + L_{yy} \hat{y}. \end{align}



</p><!-- l. 63 --><p class='indent'> Application of the linear operation to an arbitrary vector, Eq. \eqref{eq:linvec},
can therefore be expressed as \begin{equation} \label{eq:linmat} \v{w} = \mathcal{L}\v{v} = (L_{xx} v_x + L_{xy} v_y) \hat{x} + (L_{yx} v_x + L_{yy} v_y) \hat{y} \equiv \t{L}\cdot \v{v} \end{equation}
where \(\t{L}\cdot \v{v}\) is the multiplication of the matrix \(\t{L}\) with the vector \(\v{v}\). A matrix is therefore
a <span class='cmti-12'>representation </span>of a linear operation. Note that from Eq. \eqref{eq:linbasis} it is
straightforward to see that formally we obtain the components of the matrix from
\begin{equation} \label{eq:matcomp} L_{ij}=\hat{i}\cdot \mathcal{L}\hat{j}. \end{equation}
Here the \(\cdot \) indicates the inner product or contraction of two vectors.
</p><!-- l. 79 --><p class='indent'> In component-wise notation we can express Eq. \eqref{eq:linmat} as
\begin{equation} w_i = \sum _{j=x,y} L_{ij} v_j \equiv L_{ij} v_j \end{equation}
where the last term on the right-hand side uses the <span class='cmti-12'>Einstein summation</span>
convention. In this convention, a summation over repeated indices within the
same quantity or in products is implicit. This summation is also often called a
<span class='cmti-12'>contraction </span>and in dyadic notation it is indicated by a centered dot, e.g.
\(\v{w}=\t{L}\cdot \v{v}\).
</p><!-- l. 85 --><p class='indent'> It is straighforward to “convert” from dyadic notation to component-wise or
<span class='cmti-12'>index notation</span>. Imagine the \(i,j\) component of the resultant matrix of the product
\begin{equation} \left [ \t{A}\cdot \t{B}\cdot \t{C} \right ]_{ij} = A_{ik} B_{kl} C_{lj}. \end{equation}
Converting from the dyadic notation to index notation involves identifying the
indices of the resultant (first index of the first matrix in the product \(i\) and last
index of the last matrix in the product \(j\)) and introducing repeated indices for the
summation. These indices, \(k\) and \(l\) in the example, always sit next to each
other and are the indices that are <span class='cmti-12'>contracted</span>. The advantage of the index
notation is that it is unambiguous, but it may hide the physical structure
of the underlying operations. In these notes, we will therefore intermix
“dyadic” notation as in Eq. \eqref{eq:linmat} and index notation as
appropriate.
</p><!-- l. 91 --><p class='indent'> Note that there is also a double contraction, for example \begin{equation} \sigma _{ij} = C_{ijkl}\varepsilon _{kl}, \end{equation}
that in dyadic notation we would indicate with two dots: \(\t{\sigma }=\tt{C}:\t{\varepsilon }\). Each dot therefore
represents a sum over some (hidden) index.
</p>
</div>
<h3 class='sectionHead'><span class='titlemark'>5.1 </span> <a id='x1-20005.1'></a>Rotating the stress tensor</h3>
<!-- l. 101 --><p class='noindent'><a href='https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=7103f19f-f4b0-4d11-9030-ac82015e8337' class='url'><span class='cmtt-12'>https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=7103f19f-f4b0-4d11-9030-ac82015e8337</span></a>
</p><!-- l. 103 --><p class='noindent'>
</p>



<h4 class='subsectionHead'><span class='titlemark'>5.1.1 </span> <a id='x1-30005.1.1'></a>Rotating vectors</h4>
<!-- l. 105 --><p class='noindent'>A rotation \(\mathcal{R}\) is a linear operation that does not affect the length (or norm) of the
vector, \(|\mathcal{R}\v{x}|=|\v{x}|\). Note that if \(\mathcal{R}\) is represented by a matrix \(\t{R}\), then \begin{equation} |\t{R}\cdot \v{x}| = ( R_{ij} x_j R_{ik} x_k )^{1/2} = ( x_j R^T_{ji} R_{ik} x_k )^{1/2} = \left ( \v{x}\cdot \t{R}^T\cdot \t{R}\cdot \v{x} \right )^{1/2} \end{equation}
which is is equal to \(|\v{x}|\) only if \(\t{R}^T\cdot \t{R}=\t{1}\), i.e. if \(\t{R}\) is an orthogonal matrix. Here the superscript \(^T\)
indicates the transpose operation, \(R^T_{ij}=R_{ji}\), and \(\t{1}\) is the unit matrix. Note that this
relationship implies \(\t{R}^{-1}=\t{R}^T\), i.e. the inverse of an orthogonal matrix is simply its
transpose.
</p><!-- l. 111 --><p class='indent'> Let us assume we want to rotate from a coordinate system (basis
vectors) \(\hat{x}\) and \(\hat{y}\) to the primed coordinate system \(\hat{x}'\) and \(\hat{y}'\). Then the rotation
should transform the basis vectors of the unprimed into the primed system,
\begin{equation} \mathcal{R}\hat{x} = \hat{x}' \quad \text{and}\quad \mathcal{R}\hat{y} = \hat{y}'. \end{equation}
From Eq. \eqref{eq:matcomp} we obtain the components of the rotation matrix
as \begin{equation} \t{R} = \begin{pmatrix} R_{xx} &amp; R_{xy} \\ R_{yx} &amp; R_{yy} \end{pmatrix} = \begin{pmatrix} \hat{x}\cdot \mathcal{R}\hat{x} &amp; \hat{x}\cdot \mathcal{R}\hat{y} \\ \hat{y}\cdot \mathcal{R}\hat{x} &amp; \hat{y}\cdot \mathcal{R}\hat{y} \end{pmatrix} = \begin{pmatrix} \hat{x}\cdot \hat{x}' &amp; \hat{x}\cdot \hat{y}' \\ \hat{y}\cdot \hat{x}' &amp; \hat{y}\cdot \hat{y}' \end{pmatrix}. \end{equation}
If all vectors are expressed in the coordinate system \(\hat{x}\) and \(\hat{y}\), then those vectors have
the simple representation given by Eq. \eqref{eq:cartvec} and the rotation matrix
can be written as \begin{equation} \t{R} = (\hat{x}', \hat{y}'), \end{equation}
i.e. we just stack the basis vectors as columns together to obtain \(\t{R}\). This is a simple
prescription to construct the rotation matrix given the basis vectors of the
rotated coordinate system (in terms of the original coordinate system). It is
straightforward to see that \(\t{R}\) is an orthogonal matrix, \begin{equation} \t{R}^T\cdot \t{R} = \begin{pmatrix} \hat{x}'\cdot \hat{x}' &amp; \hat{x}'\cdot \hat{y}' \\ \hat{y}'\cdot \hat{x}' &amp; \hat{y}'\cdot \hat{y}' \end{pmatrix} = \t{1}, \end{equation}
if \(\hat{x}'\) and \(\hat{y}'\) are orthogonal vectors of unit length.
</p><!-- l. 153 --><p class='indent'> The basis vectors of a coordinate system rotated counterclockwise by an angle \(\theta \)
are given by \begin{equation} \hat{x}' = \begin{pmatrix} \cos \theta \\ \sin \theta \end{pmatrix} \quad \text{and}\quad \hat{y}' = \begin{pmatrix} -\sin \theta \\ \cos \theta \end{pmatrix} \end{equation}
and hence the rotation matrix is \begin{equation} \label{eq:rotmat} \t{R} = \begin{pmatrix} \cos \theta &amp; -\sin \theta \\ \sin \theta &amp; \cos \theta \end{pmatrix}. \end{equation}
It is straightforward to verify that indeed \(\t{R}^T\cdot \t{R}=\t{1}\).
</p><!-- l. 171 --><p class='noindent'>
</p>
<h4 class='subsectionHead'><span class='titlemark'>5.1.2 </span> <a id='x1-40005.1.2'></a>Rotating tensors</h4>
<!-- l. 173 --><p class='noindent'>A tensor is a representation of a linear transformation: A tensor of order 2 (a
matrix) transforms a tensor of order 1 (a vector) into another tensor of order 1.
We have already encountered the Cauchy stress tensor \(\t{\sigma }\) of solid mechanics. It
transforms an area vector \(\v{A}\) into a force vector \(\v{F}\), \begin{equation} \label{eq:tensex} \v{F} = \t{\sigma }\cdot \v{A} \quad \text{or in index notation}\quad F_i = \sigma _{ij} A_j. \end{equation}
We describe \(\v{F}\), \(\v{A}\) and \(\t{\sigma }\) in terms of their components, i.e. we describe a realization of
the linear transformation (and the area and force vectors).
</p><!-- l. 182 --><p class='indent'> A rotation does not affect the effect of the linear transformation. Hence, if we
change the coordinate system from \(\hat{x}\), \(\hat{y}\) to \(\hat{x}'\), \(\hat{y}'\), then the component of our vector \(\v{F}\)
change to \begin{align} F_x' &amp;= \v{F}\cdot \hat{x}' = F_x \hat{x}\cdot \hat{x}' + F_y \hat{y}\cdot \hat{x}' \\ F_y' &amp;= \v{F}\cdot \hat{y}' = F_y \hat{x}\cdot \hat{y}' + F_y \hat{y}\cdot \hat{y}'. \end{align}



</p><!-- l. 187 --><p class='indent'> Comparing with Eq. \eqref{eq:rotmat} yields the compact notation
\begin{equation} \label{eq:vecrot} \v{F}'=\t{R}^T\cdot \v{F} \quad \text{or in index notation}\quad F'_i = F_j R_{ji}. \end{equation}
Note that the transpose shows up because \(\t{R}\) describes the rotation of the basis and
we are here rotating a vector expressed within this basis, which is the inverse
operation.
</p><!-- l. 195 --><p class='indent'> Since we now understand how to rotate vectors, we can ask the question of
how to rotate a tensor of order 2. Starting from Eq. \eqref{eq:tensex} and using
the inverse of Eq. \eqref{eq:vecrot}, we write \begin{equation} \t{R}\cdot \v{F}' = \t{\sigma }\cdot \left (\t{R}\cdot \v{A}'\right ), \end{equation}
and multiply by \(\t{R}^T\) from the left to yield \begin{equation} \v{F}' = \left (\t{R}^T\cdot \t{\sigma }\cdot \t{R}\right )\cdot \v{A}'. \end{equation}
In the rotated coordinate system, the tensor attains the representation
\begin{equation} \label{eq:tens2rot} \t{\sigma }'=\t{R}^T\cdot \t{\sigma }\cdot \t{R} \quad \text{or in index notation}\quad \sigma _{ij}' = \sigma _{kl}R_{ki}R_{lj} \end{equation}
since this leave the expression for the linear transformation \begin{equation} \v{F}' = \t{\sigma }'\cdot \v{A}'. \end{equation}
invariant. The trace and determinant of the rotated tensor are \begin{align} \tr \t{\sigma }' &amp;= \tr \left (\t{R}^T\cdot \t{\sigma }\cdot \t{R}\right ) = \tr \left (\t{R}\cdot \t{R}^T\cdot \t{\sigma }\right ) = \tr \t{\sigma } \\ \det \t{\sigma }' &amp;= \det \left (\t{R}^T\cdot \t{\sigma }\cdot \t{R}\right ) = \det \left (\t{R}\cdot \t{R}^T\cdot \t{\sigma }\right ) = \det \t{\sigma } \end{align}
</p><!-- l. 219 --><p class='indent'> and hence invariant under rotation. Note that in general for an \(n\times n\) tensor, there
are \(n\) invariants; more on this will be discussed below when talking about
eigenvalues.
</p><!-- l. 221 --><p class='indent'> Since we now understand how to rotate tensors of order 2, we can ask the
question how to rotate a tensor of order 4. As an example, we use the stiffness
tensor \(\tt{C}\), that we will encounter in the next chapter. This tensor transforms a
strain tensor \(\t{\varepsilon }\) into a stress tensor \(\t{\sigma }\), \begin{equation} \t{\sigma } = \tt{C}:\t{\varepsilon } \quad \text{or in index notation}\quad \sigma _{ij} = C_{ijkl} \varepsilon _{kl}. \end{equation}
We can rewrite this using the inverse of Eq. \eqref{eq:tens2rot} as \begin{equation} \t{R}\cdot \t{\sigma }'\cdot \t{R}^T = \tt{C}:\left (\t{R}\cdot \t{\varepsilon }'\cdot \t{R}^T\right ) \quad \text{or}\quad R_{ik}R_{jl}\sigma '_{kl} = C_{ijkl} R_{km}R_{ln} \varepsilon '_{mn}, \end{equation}
which we now multiply from the left with \(\t{R}^T\) and from the right with \(\t{R}\). This gives
\begin{equation} \sigma '_{ij} = C_{mnop} R_{mi}R_{nj}R_{ok}R_{pl} \varepsilon '_{kl}, \end{equation}
and hence the transformation rule \begin{equation} \label{eq:tens4rot} C_{ijkl}' = C_{mnop} R_{mi}R_{nj}R_{ok}R_{pl}. \end{equation}
Quantities that transform as Eqs. \eqref{eq:vecrot}, \eqref{eq:tens2rot} and
\eqref{eq:tens4rot} are called <span class='cmti-12'>tensors</span>.
</p><!-- l. 244 --><p class='noindent'>
</p>
<h3 class='sectionHead'><span class='titlemark'>5.2 </span> <a id='x1-50005.2'></a>Principal stresses</h3>
<!-- l. 246 --><p class='noindent'><a href='https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=5cdff30a-9f6b-47cb-bc25-ac82015e830b' class='url'><span class='cmtt-12'>https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=5cdff30a-9f6b-47cb-bc25-ac82015e830b</span></a>
</p><!-- l. 248 --><p class='indent'> Let us discuss in more detail what happens if we rotate a symmetric tensor of
order 2, i.e. a tensor that fulfills \(\t{\sigma }^T = \t{\sigma }\). From Eq. \eqref{eq:tens2rot} it is
straightforward to see, that \(\t{\sigma }'^T=\t{\sigma }'\), i.e. the transformed tensor is also symmetric.
</p><!-- l. 250 --><p class='indent'> We now explicitly write the rotation for the tensor \begin{equation} \t{\sigma } = \begin{pmatrix} \sigma _{xx} &amp; \sigma _{xy} \\ \sigma _{xy} &amp; \sigma _{yy} \end{pmatrix}, \end{equation}
using the rotation matrix Eq. \eqref{eq:rotmat}. This gives symmetric \(\t{\sigma }'=\t{R}^T\cdot \t{\sigma }\cdot \t{R}\) with the
components \begin{align} \sigma '_{xx} &amp;= \frac{1}{2}(\sigma _{xx} + \sigma _{yy}) + \frac{1}{2}(\sigma _{xx} - \sigma _{yy}) \cos 2\theta + \sigma _{xy} \sin 2\theta \\ \sigma '_{yy} &amp;= \frac{1}{2}(\sigma _{xx} + \sigma _{yy}) - \frac{1}{2}(\sigma _{xx} - \sigma _{yy}) \cos 2\theta - \sigma _{xy} \sin 2\theta \\ \sigma '_{xy} &amp;= - \frac{1}{2}(\sigma _{xx} - \sigma _{yy}) \sin 2\theta + \sigma _{xy} \cos 2\theta . \end{align}



</p><!-- l. 276 --><p class='indent'> There is a specific rotation angle \(\theta _0\) where the diagonal elements \(\sigma '_{xx}\) and \(\sigma '_{yy}\) become
extremal. It is determined from \(\sigma '_{xx,\theta }=\sigma '_{yy,\theta }=0\), \begin{equation} \tan 2\theta _0 = \frac{2\sigma _{xy}}{\sigma _{xx}-\sigma _{yy}}. \end{equation}
At this rotation angle we find that the off-diagonal components vanish, \(\sigma '_{xy}(\theta _0)=0\), and the
rotated matrix is diagonal, \begin{equation} \label{eq:diag} \t{\sigma } = \begin{pmatrix} \sigma _1 &amp; 0 \\ 0\textbf{} &amp; \sigma _2 \end{pmatrix}, \end{equation}
with diagonal elements \begin{align} \sigma _1 &amp;= \frac{\sigma _{xx} + \sigma _{yy}}{2} + \left [\left (\frac{\sigma _{xx} - \sigma _{yy}}{2}\right )^2+\sigma _{xy}^2\right ]^{1/2} \\ \sigma _2 &amp;= \frac{\sigma _{xx} + \sigma _{yy}}{2} - \left [\left (\frac{\sigma _{xx} - \sigma _{yy}}{2}\right )^2+\sigma _{xy}^2\right ]^{1/2}. \end{align}
</p><!-- l. 295 --><p class='indent'> This is the simplest example of the diagonalization of a matrix. The elements
of the diagonalized Cauchy stress tensor, \(\sigma _1\) and \(\sigma _2\), are called the <span class='cmti-12'>principal
</span><span class='cmti-12'>stresses</span>.
</p><!-- l. 297 --><p class='indent'> The diagonalization of a symmetric matrix always corresponds to the
rotation into a new coordinate system. We have explictly shown this for the
two-dimensional case here and will now show it in more generality for the
three-dimensional case. In this process, we will encounter the concept of a stress
invariant.
</p><!-- l. 299 --><p class='noindent'>
</p>
<h3 class='sectionHead'><span class='titlemark'>5.3 </span> <a id='x1-60005.3'></a>Stress invariants</h3>
<!-- l. 301 --><p class='noindent'><a href='https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=11d2e291-bdf5-4f2b-8134-ac8300604f90' class='url'><span class='cmtt-12'>https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=11d2e291-bdf5-4f2b-8134-ac8300604f90</span></a>
</p><!-- l. 303 --><p class='indent'> Equation \eqref{eq:diag} fulfills the eigenvalue equations \(\t{\sigma }\cdot \hat{x}=\sigma _1\hat{x}\) and \(\t{\sigma }\cdot \hat{y}=\sigma _2\hat{y}\). Rather
than explicitly computing a rotation, we can ask the question whether
we can find a scalar \(\lambda \) and a vector \(\v{v}\) that fulfills the eigenvalue equation
\begin{equation} \t{\sigma }\cdot \v{v} = \lambda \v{v}. \end{equation}
This equation of course has the trivial solution \(\v{v}=0\). It can only have a nontrivial
solution if \begin{equation} \label{eq:ev} \det \left (\t{\sigma }-\lambda \t{1}\right )=0. \end{equation}
For a \(n\times n\) matrix, Eq. \eqref{eq:ev} leads to a polynomial of order \(n\) in \(\lambda \) with \(n\)
(possibly complex valued) solutions.
</p><!-- l. 314 --><p class='indent'> For the case of a symmetric \(3\times 3\) matrix, we can write this down explicitly as
\begin{equation} \det \begin{pmatrix} \sigma _{xx} - \lambda &amp; \sigma _{xy} &amp; \sigma _{xz} \\ \sigma _{xy} &amp; \sigma _{yy} - \lambda &amp; \sigma _{yz} \\ \sigma _{xz} &amp; \sigma _{yz} &amp; \sigma _{zz} - \lambda \end{pmatrix} = -\lambda ^3 + I_1 \lambda ^2 - I_2 \lambda + I_3 =0 \end{equation}
with \begin{align} \label{eq:genI1} I_1 &amp;= \tr \t{\sigma } = \sigma _{xx} + \sigma _{yy} + \sigma _{zz} \\ \label{eq:genI2} I_2 &amp;= \sigma _{yy}\sigma _{zz} + \sigma _{xx}\sigma _{zz} + \sigma _{xx}\sigma _{yy} - \sigma _{yz}^2 - \sigma _{xz}^2 - \sigma _{xy}^2 \\ \label{eq:genI3} I_3 &amp;= \det \t{\sigma } \end{align}
</p><!-- l. 335 --><p class='indent'> The quantities \(I_1\) to \(I_3\) are called <span class='cmti-12'>invariants</span>. We have shown above explicitly that
the trace and the determinat is invariant under rotation. The same holds
true for all coefficients of the characteristic polynomial. This is because
\begin{equation} \det \left (\t{R}^T\cdot \t{\sigma }\cdot \t{R}-\lambda \t{1}\right ) = \det \left [\t{R}^T\cdot \left (\t{\sigma }-\lambda \t{1}\right ) \cdot \t{R}\right ] = \det \left (\t{\sigma }-\lambda \t{1}\right ). \end{equation}
The 3-dimensional tensor therefore has three invariants. These invariants have
important physical interpretation. For the stress tensor, \(I_1\) is related to the
hydrostatic stress and \(I_2\) to the shear stress.
</p><!-- l. 345 --><p class='indent'> Note that for a diagonal matrix, \begin{equation} \t{\sigma }' = \begin{pmatrix} \sigma _{1} &amp; 0 &amp; 0 \\ 0 &amp; \sigma _{2} &amp; 0 \\ 0 &amp; 0 &amp; \sigma _{3} \end{pmatrix}, \end{equation}



the invariants are \begin{align} \label{eq:diagI1} I_1 &amp;= \sigma _1 + \sigma _2 + \sigma _3 \\ \label{eq:diagI2} I_2 &amp;= \sigma _1\sigma _2 + \sigma _1\sigma _3 + \sigma _2\sigma _3 \\ \label{eq:diagI3} I_3 &amp;= \sigma _1\sigma _2\sigma _3 \end{align}
</p><!-- l. 364 --><p class='indent'> By equating Eqs. \eqref{eq:genI1} to \eqref{eq:genI3} with
Eqs. \eqref{eq:diagI1} to \eqref{eq:diagI3} we can calculate the eigenvalues \(\sigma _1\), \(\sigma _2\)
and \(\sigma _3\).
</p><!-- l. 366 --><p class='indent'> Once we have computed the eigenvalues, we can obtain the corresponding
eigenvectors by solving \begin{equation} \label{eq:eigenvectors} \t{\sigma }\v{v}_1 = \sigma _1 \v{v}_1, \quad \t{\sigma }\v{v}_2 = \sigma _2 \v{v}_2, \quad \text{and}\quad \t{\sigma }\v{v}_3 = \sigma _3 \v{v}_3. \end{equation}
Note that the expressions only determine the direction of \(\v{v}_i\), not its length, and
we are free to require \(|\v{v}_i|=1\). Furthermore, let us regard scalar product \(\v{v}_1\cdot \v{v}_2\), then
\begin{equation} \sigma _1 \v{v}_1\cdot \v{v}_2 = (\t{\sigma }\cdot \v{v}_1)\cdot \v{v}_2 = \v{v}_1\cdot (\t{\sigma }^T\cdot \v{v}_2) = \v{v}_1\cdot (\t{\sigma }\cdot \v{v}_2) = \sigma _2\v{v}_1\cdot \v{v}_2 \end{equation}
and if \(\sigma _1\not =\sigma _2\) we must have \(\v{v}_1\cdot \v{v}_2=0\). Hence the eigenvectors of a symmetric matrix
are orthonormal, or in other words, they form the basis of a coordinate
system.
</p><!-- l. 389 --><p class='indent'> We can write Eq. \eqref{eq:eigenvectors} in the more compact notation
\begin{equation} \t{\sigma } \cdot \t{R} = \begin{pmatrix} \sigma _{1} &amp; 0 &amp; 0 \\ 0 &amp; \sigma _{2} &amp; 0 \\ 0 &amp; 0 &amp; \sigma _{3} \end{pmatrix} \cdot \t{R} \end{equation}
with \(\t{R}=(\v{v}_1, \v{v}_2, \v{v}_3)\). Multiplying from the left with \(\t{R}^{-1}=\t{R}^T\) (this holds because the eigenvectors are
orthonormal) we get \begin{equation} \t{R}^T \cdot \t{\sigma } \cdot \t{R} = \begin{pmatrix} \sigma _{1} &amp; 0 &amp; 0 \\ 0 &amp; \sigma _{2} &amp; 0 \\ 0 &amp; 0 &amp; \sigma _{3} \end{pmatrix}. \end{equation}
This is nothing else than a coordinate transformation (rotation) of the tensor \(\t{\sigma }\).
Since the diagonalization of a symmetric matrix leads to orthonormal
eigenvectors, the diagonalization is a rotation of the coordinate system.
</p><!-- l. 419 --><p class='noindent'>
</p>
<h3 class='sectionHead'><span class='titlemark'>5.4 </span> <a id='x1-70005.4'></a>Hydrostatic and deviatoric stress</h3>
<!-- l. 421 --><p class='noindent'>We call \(\sigma _h = \tr \t{\sigma }/3 = I_1/3\) the <span class='cmti-12'>hydrostatic stress</span>. It is the stress measure that tells us about
volume expansion and contraction. The pressure is the negative of the
hydrostatic stress, \(p=-\sigma _h\). Our sign convention is such that positive stresses
(negative pressures) mean tension and negative stresses (positive pressures)
compression.
</p><!-- l. 423 --><p class='indent'> Using the hydrostatic stress, we can construct yet another stress tensor that
quantifies the <span class='cmti-12'>deviation </span>from a pure hydrostatic condition with stress \(\sigma _h \t{1}\). We define
\begin{equation} \t{s} = \t{\sigma } - \sigma _h \t{1}, \end{equation}
the <span class='cmti-12'>deviatoric stress</span>. Note that this tensor is constructed such that \(\tr \t{s}=0\).
</p><!-- l. 429 --><p class='indent'> The invariants of the deviatoric stress are commonly denoted by the symbol \(J\).
We already know that \(J_1=0\) by construction. The second invariant is given by
\begin{equation} \begin{split} J_2 &amp;= \frac{1}{6}\left [ (\sigma _1 - \sigma _2)^2 + (\sigma _2 - \sigma _3)^2 + (\sigma _1 - \sigma _3)^2 \right ] \\ &amp;= \frac{1}{6}\left [ (\sigma _{xx} - \sigma _{yy})^2 + (\sigma _{yy} - \sigma _{zz})^2 + (\sigma _{xx} - \sigma _{zz})^2 + 6(\sigma _{xy}^2 + \sigma _{yz}^2 + \sigma _{xz}^2) \right ]. \end{split} \end{equation}
From this invariant we can derive the <span class='cmti-12'>von-Mises stress</span> \(\sigma _{vM}=\sqrt{3 J_2}\). The von-Mises stress
characterizes the pure shear contribution to the stress. The second invariant of the
deviatoric stress plays an important role in plasticity models, where it is often



assumed that a material flows when the von-Moses stress exceeds a certain
threshold.



</p>
<h2 class='likechapterHead'><a id='x1-80005.4'></a>Bibliography</h2>

