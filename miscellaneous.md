---
layout: default
title: Miscellaneous
permalink: /miscellaneous/
nav_order: 3
---

# Miscellaneous



<div style="display: flex; align-items: flex-start; gap: 20px; flex-wrap: wrap;">

  <!-- Text content -->
  <div style="flex: 1; min-width: 250px;">
  <p>
  Random projects, experiments, and notes that don’t fit neatly into modeling:
  <ul>
  <li><a href="#ElectricField">Electric Field from Moving Charge</a></li>
  <li><a href="#helicopterRope">Rope hanging from helicopter at constant speed</a></li>
  </ul>
  </p>
  </div>
</div>

---

<div id='ElectricField' style="display: flex; align-items: flex-start; gap: 20px; flex-wrap: wrap;">

  <!-- Text content -->
  <div style="flex: 1; min-width: 250px;">
    <p>
    <h2>Electric Field from Moving Charge</h2>
    </p>
    <p>
    <h3>(Feynman Volume II Derivation)</h3>
    </p>
    <p>
    On page 21-1 in Volume II of The Feynman Lectures on Physics, the equation for the electric field of an electron moving in an arbitrary direction (shown on right) is presented and some of the details about the equation are discussed.
    </p>
    <p>
    Further along (page 21-11) Feynman sort of challenges the reader in the footnote to fully derive the equation and I thought it would be useful to try to derive the equation and that it would be good practice
    </p>
    <p>Complete derivation with all details: <a href="/assets/miscellaneous//ElectricFieldFromArbitraryMovingCharge.pdf" target="_blank">Electric Field from Moving Charge Derivation</a></p>
  </div>

</div>

---

<div id='helicopterRope' style="display: flex; align-items: flex-start; gap: 20px; flex-wrap: wrap;">

  <!-- Text content -->
  <div style="flex: 1; min-width: 250px;">
    <p>
    <h2>Rope hanging from helicopter at constant speed</h2>
    </p>
    <p>
    I came across <a href="https://www.youtube.com/watch?v=q-_7y0WUnW4" target="_blank" rel="noopener noreferrer">this video</a> on youtube by Veritasium that shows a phsyics problem where a helicopter is moving at constant speed and asks if a rope is dangling from the helicopter, what shape is the rope making?
    </p>
    <p>
    The prompt makes it clear to not neglect air friction (drag). See the problem below. The question gives different options for the shape of the rope. 
    </p>
    
  </div>

</div>

<div style="display: flex; justify-content: center; align-items: center; gap: 20px; flex-wrap: wrap;">

  <!-- Figure -->
  <figure style="flex: 0 0 80%; min-width: 200px; align-self: center">
    <img src="/assets/miscellaneous/helicopterRope/HelicopterRopeProblem.png" alt="Helicopter Problem." style="width:100%; border-radius:5px;">
    <figcaption style="text-align:center;"><em>Helicopter Problem.</em></figcaption>
  </figure>

</div>

<div style="display: flex; align-items: flex-start; gap: 20px; flex-wrap: wrap;">

  <!-- Text content -->
  <div style="flex: 1; min-width: 250px;">
    <p>
    I think most people would select (B) or (C). Maybe you would pick (A) and say you assume a very heavy rope and a very low speed for the helicopter. 
    </p>
    <p>
    I thought it could be a cool exercise to see how I could find my answer analytically (if possible). To do this, I looked at a small (infitesimal) segment of robe and the force balance on that segment (free body diagram). This is shown below (note I draw the rope as a straight line but I could have drawn this with any arbitary shape - it's not important in the derivation). 
    </p>
    
  </div>

</div>

<div style="display: flex; justify-content: center; align-items: center; gap: 20px; flex-wrap: wrap;">

  <!-- Figure -->
  <figure style="flex: 0 0 80%; min-width: 200px; align-self: center">
    <img src="/assets/miscellaneous/helicopterRope/HelicopterRopeSchematic.png" alt="My Schematic." style="width:100%; border-radius:5px;">
    <figcaption style="text-align:center;"><em>My Helicopter-Rope Schematic.</em></figcaption>
  </figure>

</div>

<div style="display: flex; align-items: flex-start; gap: 20px; flex-wrap: wrap;">

  <!-- Text content -->
  <div style="flex: 1; min-width: 250px;">
    <p>
    In the above schematic, \(T\) is tension, \(F_g\) is the force of gravity, and \(F_D\) is the drag force (air friction).
    </p>
    <p>
    We assume the rope has length \(L\), the rope has uniform mass density \(\lambda\) (mass per unit length), and that the rope segment angle \(\theta\) can vary as a function of position on the rope. 
    </p>
    <p>
    We can first find the forces in the x direction (we assume the helicopter is moving in the negative \(x\) direction with speed \(u\)). We get:
    </p>
    $$ \sum F_x = -T_{x,y}cos(\theta) + T_{x+dx,y+dy}cos(\theta) + F_D $$
    <p>
    Expanding \(T_{x+dx,y+dy}\) using Taylor series gives:
    </p>
    $$ \sum F_x = -T_{x,y}cos(\theta) + T_{x,y}cos(\theta) + \frac{\partial T_{x,y}}{\partial x} cos(\theta) dx + \frac{\partial T_{x,y}}{\partial y} cos(\theta) dy + F_D $$
    $$ \sum F_x = \frac{\partial T}{\partial x} cos(\theta) dx + \frac{\partial T}{\partial y} cos(\theta) dy + \frac{1}{2} C_D \rho_{air} u^2 dy $$
    <p>
    We simplify the drag term by assuming that \(\frac{1}{2} C_D \rho_{air} u^2\) is the same for all rope segments. We also assume that we are at steady state so our force summation equals 0.
    </p> 
    $$ \frac{\partial T}{\partial x} cos(\theta) dx + \frac{\partial T}{\partial y} cos(\theta) dy + K_D dy = 0 $$
    <p>
    We do the same thing in the \(y\) direction and obtain:
    </p>
    $$ \sum F_y = -T_{x,y} sin(\theta) + T_{x+dx,y+dy} sin(\theta) + F_g $$
    <p>
    Expanding and simplifying, dropping subscripts for tension, substituting in for gravity, and equating to 0 gives:
    </p>
    $$ \frac{\partial T}{\partial x} sin(\theta) dx + \frac{\partial T}{\partial y} sin(\theta) dy + \lambda g ds = 0 $$
    <p>
    Note that for gravity, we have \(ds\) since gravity acts on the whole segment. We now have our two equations:
    </p>
    $$ \frac{\partial T}{\partial x} cos(\theta) dx + \frac{\partial T}{\partial y} cos(\theta) dy + K_D dy = 0 $$
    $$ \frac{\partial T}{\partial x} sin(\theta) dx + \frac{\partial T}{\partial y} sin(\theta) dy + \lambda g ds = 0 $$
    <p>
    From the geometry, we have \(\frac{dy}{dx} = tan(\theta)\) and that \(ds=\frac{dx}{cos(\theta)}=\frac{dy}{sin(\theta)}\). We can divide both equations by \(dx\) and substitute in for \(ds\) to get:
    </p>
    $$ \frac{\partial T}{\partial x} cos(\theta) + \frac{\partial T}{\partial y} cos(\theta) \frac{dy}{dx} + K_D \frac{dy}{dx} = 0 $$
    $$ \frac{\partial T}{\partial x} sin(\theta) + \frac{\partial T}{\partial y} sin(\theta) \frac{dy}{dx} + \lambda g \frac{1}{cos(\theta)} = 0 $$
    <p>
    We then use \(\frac{dy}{dx}=tan(\theta)\) to get:
    </p>
    $$ \frac{\partial T}{\partial x} cos(\theta) + \frac{\partial T}{\partial y} cos(\theta) tan(\theta) + K_D tan(\theta) = 0 $$
    $$ \frac{\partial T}{\partial x} sin(\theta) + \frac{\partial T}{\partial y} sin(\theta) tan(\theta) + \lambda g \frac{1}{cos(\theta)} = 0 $$
    <p>
    Solving the second equation for \(\frac{\partial T}{\partial y}\), we find:
    </p>
    $$ \frac{\partial T}{\partial y} = -\frac{\partial T}{\partial x} \frac{1}{tan(\theta)} - g \lambda \frac{1}{sin^2(\theta)} $$
    <p>
    Plugging this into the first equation gives:
    </p>
    $$ \frac{\partial T}{\partial x} cos(\theta) + ( -\frac{\partial T}{\partial x} \frac{1}{tan(\theta)} - g \lambda \frac{1}{sin^2(\theta)}) cos(\theta) tan(\theta) + K_D tan(\theta) = 0 $$
    <p>
    Expanding gives:
    </p>
    $$ \frac{\partial T}{\partial x} cos(\theta) -\frac{\partial T}{\partial x} cos(\theta) - g \lambda \frac{1}{sin(\theta)} + K_D tan(\theta) = 0 $$
    <p>
    We then get:
    </p>
    $$ g \lambda = K_D tan(\theta) sin(\theta) = K_D \frac{sin^2(\theta)}{cos(\theta)} = K_D \frac{1 - cos^2(\theta)}{cos(\theta)}$$
    <p>
    We then can divide both sides by \(K_D\) and say \(\alpha = \frac{g \lambda}{K_D}\) and obtain:
    </p>
    $$ cos^2(\theta) + \alpha \, cos(\theta) - 1 = 0 $$
    <p>
    We have a quadratic equation now and can solve for \(cos(\theta)\):
    </p>
    $$ cos(\theta) = \frac{-\alpha \pm \sqrt{\alpha^2 - 4}}{2} $$
    <p>
    We have found a solution for the angle that only depends on gravity, rope mass density, and drag. All of these are assumed constant and gives us a constant angle so we conclude we have the straight line which is answer (B). This is also what the youtube video above shows from Veritasium. 
    </p>
    <p>
    There is more we can do based on our findings. Below is a table for values of \(\alpha\) and \(\frac{-\alpha \pm \sqrt{\alpha^2 - 4}}{2}\). From \(\alpha\), we know that \(\alpha=0\) (or the limit as \(\alpha\) approaches 0) would correspond to a very, very light rope or a rope situation with very high drag. We know. that \(\alpha=\infty\) (or the limit as \(\alpha\) approaches \(\infty\)) would correspond to a scenario with a very low drag coefficient or a very, very heavy rope. Lets look at the results and what physics the results suggest
    </p>
    <table border="1" style="margin-left:auto; margin-right:auto; border-collapse: collapse; width: 90%; text-align: center;">
    <tr>
      <th>\(\alpha\)</th>
      <th>\(\frac{-\alpha + \sqrt{\alpha^2 - 4}}{2}\)</th>
      <th>\(\frac{-\alpha - \sqrt{\alpha^2 - 4}}{2}\)</th>
    </tr>
    <tr>
      <td>0</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>\(\infty\)</td>
      <td>0</td>
      <td>-\(\infty\)</td>
    </tr>
  </table>
  <p>
  From the table, we see that that \(\frac{-\alpha + \sqrt{\alpha^2 - 4}}{2}\) corresponds to our physical solution and while \(\frac{-\alpha - \sqrt{\alpha^2 - 4}}{2}\) is also a mathematical solution to the quadratic, it's not an actual physical solution since \(cos(\theta)\) is never \(-\infty\). Now we can check what values of \(\alpha\) correspond to what values of \(\theta\) and check our physical reasoning. We said above that when \(\alpha\) approaches 0, it represents a very light rope so we would expect \(\theta\) to also approach 0 meaning the rope is so light that any air resistance pushes the rope to be horizontal and be parallel with the ground. When \(\alpha\) approaches \(\infty\) we expect a very heavy rope with small air resistance so that the rope falls straight down giving us a \(\theta\) of 90 deg. In the table, below we calculate what values of \(\alpha\) give us what values of \(\theta\). 
  </p>
  <table border="1" style="margin-left:auto; margin-right:auto; border-collapse: collapse; width: 90%; text-align: center;">
    <tr>
      <th>\(\alpha\)</th>
      <th>\(cos(\theta)=\frac{-\alpha + \sqrt{\alpha^2 - 4}}{2}\)</th>
      <th>\(\theta (deg)\)</th>
    </tr>
    <tr>
      <td>0</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>\(\infty\)</td>
      <td>0</td>
      <td>90</td>
    </tr>
  </table>
  <p>
  We see that the \(\theta\) and \(\alpha\) values are consistent with our physical understanding. 
  </p>
  <p>
  The last thing we can look is checking the tension in the rope at different segments. We create a similar schematic to the one above (shown below):
  </p>

  </div>

</div>

<div style="display: flex; justify-content: center; align-items: center; gap: 20px; flex-wrap: wrap;">

  <!-- Figure -->
  <figure style="flex: 0 0 80%; min-width: 200px; align-self: center">
    <img src="/assets/miscellaneous/helicopterRope/HelicopterRopeSchematicS.png" alt="My Schematic." style="width:100%; border-radius:5px;">
    <figcaption style="text-align:center;"><em>My Helicopter-Rope Schematic.</em></figcaption>
  </figure>

</div>

<div style="display: flex; align-items: flex-start; gap: 20px; flex-wrap: wrap;">

  <!-- Text content -->
  <div style="flex: 1; min-width: 250px;">
    <p>
    We can again look at a small segment of the rope. We do the force balance in the \(s\) direction:
    </p>
    $$ \sum F_s = -T_s + T_{s+ds} + F_D cos(\theta) + F_g sin(\theta) $$
    $$ \frac{dT}{ds} ds + K_D cos(\theta) dy + \lambda g sin(\theta) ds = 0 $$
    $$ \frac{dT}{ds} ds + K_D cos(\theta) sin(\theta) ds + \lambda g sin(\theta) ds = 0 $$
    $$ \frac{dT}{ds} + K_D cos(\theta) sin(\theta) + \lambda g sin(\theta) = 0 $$
    $$ \frac{dT}{ds} = - K_D cos(\theta) sin(\theta) - \lambda g sin(\theta) = C_1 $$
    $$ T_s = C_1 s + C_2 $$
    <p>
    We now want to find \(C_2\). We know that the tension as we approach the end of the rope will be 0 since there will be no gravity or drag force, so no tension force:
    </p>
    $$ T(s=L) = C_1 L + C_2 = 0 $$
    $$ C_2 = - C_1 L $$
    $$ T_s = C_1 s - C_1 L = C_1 (s-L) $$
    $$ T_s = -[K_D cos(\theta) sin(\theta) + \lambda g sin(\theta)] (s-L) $$
    $$ T_s = [K_D cos(\theta) sin(\theta) + \lambda g sin(\theta)] (L-s) $$
    <p>
    There's a couple points to make here. First, tension is acting in the direction we assumed on our force balance (we know that \(0 \le \theta \le 90 \; deg.\) so that all parameters in the [] are positive). Any segment of rope that has it's end as the end of the rope will have gravity and air friction pulling in the \(s\) direction with tension pulling in the \(-s\) direction. We basically have tension in the rope due to gravity and air friction. We also note that tension is proportional to distance along the length of rope. 
    </p>
    <p>
    It's cool that such a simple problem can be very interesting.
    </p>

  </div>

</div>