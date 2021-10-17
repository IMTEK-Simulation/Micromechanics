---
layout: default
title: "Chapter 01 [Okt. 18-22 (2021)]"
parent: Lecture
date: 2021-10-17
categories: lecture
author: Lars Pastewka
nav_order: 1
---


<h2 class='chapterHead'><span class='titlemark'>Chapter 1</span><br /><a id='x1-10001'></a>Force and moment equilibria</h2>
<h3 class='sectionHead'><span class='titlemark'>1.1 </span> <a id='x1-20001.1'></a>Statics, rigid bodies and force systems</h3>
<!-- l. 5 --><p class='noindent'><a class='url' href='https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=f4af2ded-cd2b-4e10-adf4-ac720118d222'><span class='cmtt-12'>https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=f4af2ded-cd2b-4e10-adf4-ac720118d222</span></a>
</p><!-- l. 7 --><p class='indent'> Statics is the subdivision of mechanics concerned with the <span class='cmbx-12'>forces </span>that
act on <span class='cmbx-12'>solid bodies </span>at rest under <span class='cmbx-12'>equilibrium conditions</span>. The solid
body can be thought of as a collection of matter within an identifiable
boundary, and it is important to distinguish notions of <span class='cmti-12'>rigid </span>and <span class='cmti-12'>deformable</span>
bodies.
</p>
<figure class='figure'>







<!-- l. 14 --><p class='noindent'> <img src='newFigures/ch1_RigidvsDeformable-.png' width='585' alt='PIC' height='412' /> <a id='x1-2001r1'></a>
<a id='x1-2002'></a>
</p>
<figcaption class='caption'><span class='id'>Figure 1.1:: </span><span class='content'>The rigid body (a) can translate and rotate, while the deformable
body (b) can also change its shape. </span></figcaption><!-- tex4ht:label?: x1-2001r1.1 -->



</figure>
<div class='flushleft'>
<!-- l. 20 --><p class='noindent'>
<!-- tex4ht:inline --></p><div class='tabular'> <table class='tabular' id='TBL-1'><colgroup id='TBL-1-1g'><col id='TBL-1-1' /></colgroup><tr style='vertical-align:baseline;' id='TBL-1-1-'><td class='td11' id='TBL-1-1-1' style='white-space:nowrap; text-align:left;'><span class='cmbx-12'>Rigid body </span>(Chapters 1-3) </td>
</tr><tr class='hline'><td><hr /></td></tr><tr style='vertical-align:baseline;' id='TBL-1-2-'><td class='td11' id='TBL-1-2-1' style='white-space:nowrap; text-align:left;'>Do not change its shape under internal or external forces </td>
</tr><tr style='vertical-align:baseline;' id='TBL-1-3-'><td class='td11' id='TBL-1-3-1' style='white-space:nowrap; text-align:left;'>Forces and moments can be plotted as a function of a position</td>
</tr><tr style='vertical-align:baseline;' id='TBL-1-4-'><td class='td11' id='TBL-1-4-1' style='white-space:nowrap; text-align:left;'>”Nothing” happens within material </td>
</tr></table></div></div>
<div class='flushleft'>
<!-- l. 30 --><p class='noindent'>
<!-- tex4ht:inline --></p><div class='tabular'> <table class='tabular' id='TBL-2'><colgroup id='TBL-2-1g'><col id='TBL-2-1' /></colgroup><tr style='vertical-align:baseline;' id='TBL-2-1-'><td class='td11' id='TBL-2-1-1' style='white-space:nowrap; text-align:left;'><span class='cmbx-12'>Deformable body </span>(Chapters 4-12) </td>
</tr><tr class='hline'><td><hr /></td></tr><tr style='vertical-align:baseline;' id='TBL-2-2-'><td class='td11' id='TBL-2-2-1' style='white-space:nowrap; text-align:left;'>Can change its shape under internal or external forces </td>
</tr><tr style='vertical-align:baseline;' id='TBL-2-3-'><td class='td11' id='TBL-2-3-1' style='white-space:nowrap; text-align:left;'>Inherent material properties must be accounted to find deformation</td>
</tr></table></div></div>
<div class='wrapfig-r'> <img src='newFigures/ch1_Force3-.png' width='97' alt='PIC' height='68' /> <a id='x1-2003r2'></a>
<a id='x1-2004'></a>
<figcaption class='caption'><span class='id'>Figure 1.2::
</span><span class='content'>The force \(F\) is fully
determined by
magnitude \(|F|\), line of
action (dashed
line), direction and
contact point A. </span></figcaption><!-- tex4ht:label?: x1-2003r1.1 --></div>
<!-- l. 50 --><p class='indent'> Mechanics heavily relies on the notion of <span class='cmti-12'>force</span>. We all intuitively understand
this concept, and in physics, force usually represents internal or external action on
the body. From a practical point of view, any force can be represented as a vector
\(\v{F}\), and it is fully determined by its magnitude \(|F|\), line of action, direction and contact
point (Fig. <a href='#x1-2003r2'>1.2<!-- tex4ht:ref: fig:forcevector --></a>).
</p><!-- l. 52 --><p class='indent'> Fig. <a href='#x1-2015r3'>1.3<!-- tex4ht:ref: fig:resultant --></a>a shows a rigid body subjected to multiple forces. In engineering
mechanics, every combination of forces acting on the rigid body is called a <span class='cmti-12'>force
</span><span class='cmti-12'>system</span>. Graphical representation of force vectors enables the replacement of
multiple forces acting on the body by a single equivalent force called the <span class='cmti-12'>resultant
</span><span class='cmti-12'>of the system</span>. Besides one important exception that will be discussed later,
every force system can be reduced to resultant via a simple step-by-step
procedure:
</p><ol class='enumerate1'>
<li class='enumerate' id='x1-2006x1'>Pick two forces acting on the body;
</li>
<li class='enumerate' id='x1-2008x2'>Shift both forces along their corresponding acting line to the point of
intersection;



</li>
<li class='enumerate' id='x1-2010x3'>Replace these forces by their resultant (vector sum of the initial forces);
</li>
<li class='enumerate' id='x1-2012x4'>Start all-over, until only one force is left;
</li>
<li class='enumerate' id='x1-2014x5'>The remaining force is the resultant of the initial force system.</li></ol>
<figure class='figure'>







<!-- l. 69 --><p class='noindent'> <img src='newFigures/ch1_ResultantEvolution-.png' width='585' alt='PIC' height='412' /> <a id='x1-2015r3'></a>
<a id='x1-2016'></a>
</p>
<figcaption class='caption'><span class='id'>Figure 1.3:: </span><span class='content'>Reduction of the force system to the single resultant. </span></figcaption><!-- tex4ht:label?: x1-2015r1.1 -->



</figure>
<!-- l. 75 --><p class='indent'> Fig. <a href='#x1-2015r3'>1.3<!-- tex4ht:ref: fig:resultant --></a> illustrates this procedure for arbitrarily selected force system. First,
blue forces \(F_4\) cancel each other since they share the line of action, have the same
magnitude and opposite directions (Fig. <a href='#x1-2015r3'>1.3<!-- tex4ht:ref: fig:resultant --></a>a). Then, by sliding the forces \(F_1\) and \(F_2\)
to the intersection point of their corresponding action lines, we can get the
resultant of \(F_1\) and \(F_2\) (red vector in Fig. <a href='#x1-2015r3'>1.3<!-- tex4ht:ref: fig:resultant --></a>b). Then, the same procedure for this new
resultant and initial force \(F_3\) gives us the resultant of the whole system (green vector
in Fig. <a href='#x1-2015r3'>1.3<!-- tex4ht:ref: fig:resultant --></a>c).
</p>
<h3 class='sectionHead'><span class='titlemark'>1.2 </span> <a id='x1-30001.2'></a>Force couples and moments</h3>
<!-- l. 78 --><p class='noindent'><a class='url' href='https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=01a89ffb-ca4e-434d-8368-ac72011bb5bb'><span class='cmtt-12'>https://uni-freiburg.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=01a89ffb-ca4e-434d-8368-ac72011bb5bb</span></a>
</p><!-- l. 81 --><p class='indent'> Two forces (Fig. <a href='#x1-3001r4'>1.4<!-- tex4ht:ref: fig:forcecouple --></a>a) cannot be reduced to a single resultant if they have
</p>
<ul class='itemize1'>
<li class='itemize'>Same magnitude
</li>
<li class='itemize'>Parallel lines of action
</li>
<li class='itemize'>Opposite directions</li></ul>
<figure class='figure'>







<!-- l. 94 --><p class='noindent'> <img src='newFigures/ch1_ForceCouple-.png' width='585' alt='PIC' height='412' /> <a id='x1-3001r4'></a>
<a id='x1-3002'></a>
</p>
<figcaption class='caption'><span class='id'>Figure 1.4:: </span><span class='content'>(a) Two forces forming force couple. (b) Moment of the force
couple. </span></figcaption><!-- tex4ht:label?: x1-3001r1.2 -->



</figure>
<!-- l. 100 --><p class='indent'> Such a force system is called a <span class='cmti-12'>force couple </span>or <span class='cmti-12'>pure moment</span>. If a resultant
represents the translation movement of the rigid body, a pure moment
corresponds to rotation. The moment of force couple is defined by direction of
rotation, magnitude and distance between corresponding lines of action
(Fig. <a href='#x1-3001r4'>1.4<!-- tex4ht:ref: fig:forcecouple --></a>b). Note that force moment is not fixed at any certain contact point
and can be moved freely over the whole body as long as the direction
of rotation and magnitude of the moment are conserved. In a general
3D system, we can define the moment as cross product of two vectors
\begin{equation} \v{M}=\v{a}\times{\v{F_1}}, \end{equation}
where \(\v{a}\) is a vector connecting the contact points of two vectors in force couple, and
\(\v{F_1}\) is one of these vectors as shown in Fig. <a href='#x1-3001r4'>1.4<!-- tex4ht:ref: fig:forcecouple --></a>b. The vector representation of
moment enables us to define <span class='cmti-12'>moment area</span> \(|\v{M}|\) as \begin{equation} |\v{M}|=|\v{a}\times{\v{F_1}}|=|\v{a}||\v{F_1}|\sin{\alpha }, \end{equation}
where \(\alpha \) is the angle enclosed by \(\v{a}\) and \(\v{F_1}\). Note that by definition, the moment area is
always positive, however a specific sign can be assigned to the moment depending
on its direction.
</p>
<div class='wrapfig-r'> <img src='newFigures/ch1_SingleForceMoment-.png' width='312' alt='PIC' height='219' /> <a id='x1-3003r5'></a>
<a id='x1-3004'></a>
<figcaption class='caption'><span class='id'>Figure 1.5:: </span><span class='content'>Force \(F\)
exerts moment at a
point B. </span></figcaption><!-- tex4ht:label?: x1-3003r1.2 --></div>
<!-- l. 125 --><p class='indent'> A single force will exert a moment at a certain point B <span class='cmbx-12'>outside from its line
</span><span class='cmbx-12'>of action </span>(Fig. <a href='#x1-3003r5'>1.5<!-- tex4ht:ref: fig:singleforcemoment --></a>). This <span class='cmti-12'>moment of single force </span>is defined as a product of the
force magnitude \(|F|\) and the perpendicular distance \(a\) between point B and the line of
action (\(M=a|F|\)). Note that the contact point of \(F\) and action point B cannot coincide. The
moment of a single force is sometimes called a <span class='cmti-12'>torque</span>. <span class='cmbx-12'>It is important not
</span><span class='cmbx-12'>to mix up moments generated by force couple and by a single
</span><span class='cmbx-12'>force</span>.
</p>
<div class='flushleft'>
<!-- l. 128 --><p class='noindent'>
<!-- tex4ht:inline --></p><div class='tabular'> <table class='tabular' id='TBL-3'><colgroup id='TBL-3-1g'><col id='TBL-3-1' /></colgroup><tr style='vertical-align:baseline;' id='TBL-3-1-'><td class='td11' id='TBL-3-1-1' style='white-space:nowrap; text-align:left;'><span class='cmbx-12'>The force couple </span></td>
</tr><tr class='hline'><td><hr /></td></tr><tr style='vertical-align:baseline;' id='TBL-3-2-'><td class='td11' id='TBL-3-2-1' style='white-space:nowrap; text-align:left;'>May induce a pure rotation of a body</td>
</tr><tr style='vertical-align:baseline;' id='TBL-3-3-'><td class='td11' id='TBL-3-3-1' style='white-space:nowrap; text-align:left;'>Does not have a reference point </td>
</tr></table></div></div>
<div class='flushleft'>
<!-- l. 137 --><p class='noindent'>
<!-- tex4ht:inline --></p><div class='tabular'> <table class='tabular' id='TBL-4'><colgroup id='TBL-4-1g'><col id='TBL-4-1' /></colgroup><tr style='vertical-align:baseline;' id='TBL-4-1-'><td class='td11' id='TBL-4-1-1' style='white-space:nowrap; text-align:left;'><span class='cmbx-12'>The single force </span></td>
</tr><tr class='hline'><td><hr /></td></tr><tr style='vertical-align:baseline;' id='TBL-4-2-'><td class='td11' id='TBL-4-2-1' style='white-space:nowrap; text-align:left;'>May induce a translation of the body </td>
</tr><tr style='vertical-align:baseline;' id='TBL-4-3-'><td class='td11' id='TBL-4-3-1' style='white-space:nowrap; text-align:left;'>Exert a moment in a reference point outside its line of action</td>
</tr></table></div></div>



<!-- l. 146 --><p class='indent'> Now we understand how to work with forces and moments, and it is time to
define the last word in the definition given at the beginning of this chapter –
<span class='cmti-12'>equilibrium</span>. </p><div class='framedenv' id='shaded*-1'>
<!-- l. 148 --><p class='noindent'> A 2D force system is in equilibrium if the sum of all forces \(F_i\) and the sum of all
moments \(M_i\) equal zero. \begin{equation} \sum _{i}{F_i}=0 \quad \text{and}\quad \sum _{i}{M_i}=0 \end{equation}
</p></div>



<h2 class='likechapterHead'><a id='x1-40001.2'></a>Bibliography</h2>

