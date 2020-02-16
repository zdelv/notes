% Chapter 3

### 3.2.3 Energy Bands

The repetitive nature of the lattice structure in semiconductors changes how the wavefunction for a free particle acts, giving rise to a band structure throughout the medium. This band structure can be thought of as a continuous "band" of $N$ electron states that are formed from each addtional atom added to the lattice. Continually adding more of these atoms 

This structure can be found by looking at how the electrons in a quantum well are confined to specfic energy states $n$, based on the following eqauation:

$$
    E_n = \hbar \omega_n = \frac{\hbar^2 n^2 \pi^2}{2mL}
$$

As $n \rightarrow \infty$, a continuous *band* is created, where the $n$ value can vary greatly, allowing many electrons to exist simultaneously in a close area.

![Si Energy Band Graph](Chapter&#32;3/Si_Energy_Band_Graph.png)

The above graph shows how these bands are formed. The $x$ axis is the atomic spacing, $a$, and the $y$ axis is the energy an electron could have given that atomic spacing. As the spacing increases, we approach discrete energy levels, which are represented by the single lines coming from the right axis. As the spacing is decreased, the effect described above begins to occur, and the possible energy levels increase quickly. This causes the discrete energy level to spint into *bands*, where an electron could have any energy level within that band. At the actual spacing, which is marked in the diagram, we can see the appearence of the *conduction* band, *valence* band and their respective energy band gap, $E_g$.

### 3.3.3 Metals, Semiconductors, and Insulators
The three materials when it comes to the topics of bonds and conductivity are metals, semiconductors, and insulators.

Metals are characterised by their metallic bonding and their "sea of electrons" where excess electrons not used between bonding exist. The band structure of a metal will either have the valence and conduction bands partially overlapping or the conduction band will be partially filled. This causes the electrons to easily flow in an applied electric field and is why metals commonly are great conductors.

Semiconductors on the other hand, have distinctly split valence and conduction bands, with all electrons existing in the valence band at 0K. At higher temperatures, (like room temperature, 293K) electrons have enough kinetic energy to move out of the valence band and into the conduction band. The amount of electrons that are able to jump bands is based on the band gap, $E_g$ of the semiconductor. This characteristic is why semiconductors are commonly used for very precise electronics, like microprocessors. We can tune the conductivity of the material given doping and other thermal or optical operating conditions.

Insulators are related to semiconductors in that they also have distinctly split valence and conduction bands, but their difference exists from the size of the band gap. For insulators, the band gap is much larger, which greatly increases the amount of energy needed for electrons to jump bands. With very few electrons in the conduction band and very few holes in the valence band, current does not flow easily through an insulator.

The image below demonstrates concepts mentioned above.

![Metal Band Comparison](Chapter&#32;3/Insulators_Semiconductors_Metals_Band_Comparison.png)

### 3.1.4 Direct and Indirect Semiconductors
Continuing with our discussion on energy bands within semiconductors, we arrive at an important concept about direct and indirect semiconductors.

Below is a simplified graph of the band structure for GaAs and AlAs. The upside-down parabola at the bottom of the picture is the valence band, while the three bands above are all apart of the conduction band, but just at different minimums across the entire band.

![E-K Graph](Chapter&#32;3/GaAs-AlAs_E-K_Graph.png)

For an electron to move from the valence band in GaAs, we notice that there is a *direct* path for it to move in, with a relatively low band gap energy, compared to AlAs. A direct semiconductor has this vertical characteristic and in general has lower band gaps. 

The lowest conduction band energy for AlAs is shown to the +$k$ direction from the highest point of the valence band. This causes electrons to have an *indirect* path between the conduction band and the valence band, and thus, a higher band gap energy. An indirect semiconductor does not have a direct movement from the conduction band to valence band which increases the energy band gap. There needs to be other structure or helping mechanisms to move electrons from the conduction band to the valence band or vice versa.

*Side Note:*
The mathematics for this phenomenon is the following. Given the form for a wavevector in a lattice:
$$
    \Psi_\mathbf{k}(x) = U(\mathbf{k}_x, x)e^{j\mathbf{k}_xx} \\
    \space \\
    \mathbf{k}_x = \mathbf{k} \cdot \mathbf{r}
$$
where $\mathbf{k}_x$ is the wavevector for the wave, describing the direction and speed of the wave in multi-dimensional space. $U(\mathbf{k}_x, x)$ is the periodicity function of the material, which modulates the function based on the wavevector and positon within the lattice.


Common Semiconductor Types

| Direct | Indirect |
|---|---|
| GaAs | Si, AlAs|  


### 3.1.5 Variations of Energy Bands with Alloy Composition
As semiconductors are varied in their composition, their band structures change. An example of this is with GaAs and AlAs, where GaAs is a direct semiconductor and AlAs is a indirect semiconductor. If we transition a sample of GaAs into AlAs and measure the band gap energy as the compositon changes, we end up with the graph below.

![Band Gap Graph](Chapter&#32;3/GaAs_AlAs_BandGap_Graph.png)

As we can tell, the GaAs sample has its conduction band minimum at $\Gamma$, which increases in its energy level as the Al concentration increases. If we continue adding Al, we eventually notice that the conduction band minimum switches to $X$, as $\Gamma$ continues at a much larger slope than $X$ does. This switch in minimum causes the change from a direct semiconductor to indirect semiconductor.

This feature of band gaps was discovered back in the early days of semiconductors. Scientists were testing different doping compositions and discovered that at some point the band gap energy changed very abrutly. This was due to the conduction band minimum moving from a direct location, to another indirect location.

## 3.2 Charge Carries in Semiconductors

### 3.2.1 Electrons and Holes
At 0K, all of the electrons in a semiconductor exist in the valence band, which leads to an empty conduction band. As thermal energy is added, electrons are excited from the valence band and moved into the conduction band, leaving holes in the valence band. Each pair of excited-electron and valence-hole are called *electron hole pairs* (EHPs).

An excited electron in the conduction band is relatively free to move around, as the number of energy states is much larger than the number of electrons. For example, with silicon at room temperature, there are around $10^{10}$ $\text{EHP}/cm^3$ in the conduction, while the density of Si is around $10^{22}$ $\text{atoms}/cm^3$. The multiple orders of difference allows electrons to move freely and highlights the conductivity of semiconductors, in the view of the conduction band.

When looking at the current flow due to the holes, we have to change our view to look at the current density in the valence band. At 0K, when the valence band is full, the following equation describes the current density:

(4)
$$
    J = (-q)\sum^N_i{v_i} = 0
$$

This equation essentially says for every electron that is moving in a specific direction, there *must* be another electron moving the in the opposite direction. This is due to every energy state in the valence band being filled, and for the electron to move, it must occupy another, already filled energy state. The electron in this already filled state must then be ejected into another state, which then finds another filled state, leading to a chain reaction, or said in other words, leads to *zero net current flow*. The $E-K$ graph below shows some of this, as in the valence band, there will always be two electrons with opposite momentum at the same given energy level.

![EHP Momentum Pairs](Chapter&#32;3/EHP_Momentum_EK.png)

If the semiconductor is brought above 0K, EHPs are created, leaving holes in the valence band. Equation 4 above transforms into the following, given that the $j^{th}$ electron is now missing:

(5)
$$
    J = (-q)\sum^N_i{(v_i)} - (-q)v_j
$$

If we rememeber that the summation is the same as equation 4, (5) changes to just the following equation:

(6)
$$
    J = -(-q)v_j = qv_j
$$

Rememebering that this describes the net current flow, we realize that equation 6 is actually saying that the holes have a *net positive current flow!* Now of course, this doesn't mean that the holes are actually moving current or have a positive charge, but actually what is happening is that an electron is filling the gap and "moving" the hole in the opposite direction. It remains to say though, that the general way of describing holes is that they have a positive charge and positive mass.

#### TODO: Write section for pg 76-78



### 3.2.2 Effective Mass
Electrons in a lattice structure are not considered completely free due to the complications the periodic potential brings to the wavefunctions. To use the regular electrodynamical equations on electrons within lattice structures, we must first find the *effective mass* of the electron, which depends on $E-k$ plot. We start by finding how the energy of en electron relates to its momentum, which also what spawns the shape an $E-K$ graph:

$$ 
    E = \frac{1}{2}mv^2 = \frac{1}{2} \frac{p^2}{m} = \frac{\hbar^2}{2m}k^2 \\
$$

From this equation, we can notice that the electron energy is parabolically related to the wavevector $k$, or said another way, the electron mass is inverse parabolically related to the energy. If we differentiate with respect to our independent variable, $k$, we arrive at the effective mass equation:

$$
    E = \frac{\hbar^2}{2m}k^2 \\
    \space \\
    \frac{d^2E}{dk^2} = \frac{\hbar^2}{m} \\
    \space \\
    m^* = \frac{\hbar^2}{d^2E/dk^2} 
$$

The equation shows us that the 2nd derivative, or the curvature of the band edge determies the effective mass. The graph below shows the E-K graphs for GaAs and AlAs and their lowest energy bands.

![Complicated E-K Graph](Chapter&#32;3/GaAs-AlAs_E-K_Graph.png)

GaAs is a direct band gap material and AlAs is an indirect band gap material. Using the effective mass equation we found earlier, we can discern that the effective mass at the $X$ node is higher than that at the $\Gamma$ node for both materials. $\Gamma$ has a higher $\frac{d^2E}{dk^2}$ than $X$ does, which relates to a $\Gamma$ having a lower effective mass.

Looking further at this graph, we notice that if we calculate the effective mass for the valence band maximum (for electrons), that it is actually a *negative value!* Negative mass makes no sense, but if we remember that this is *effective* mass, it makes much more sense. Just viewing valence band electrons, this means that negative mass and negative charge electrons move in the same directon as positive mass and positive charge holes.

###### Why calculate effective mass?
Effective mass is a somewhat abstract concept and doesn't seem all that useful especially given the fact that it causes some complications, like negative mass. The reason why we find this value comes from Newton's Second Law:

$$
    \frac{dp}{dt} = \frac{d(mv)}{dt} = F
$$

The above equation for an electron in a periodic crystal structure combines the internal and external forces; $F_{int} + F_{ext}$, where $F_{int}$ is the forces due to the period crystal structure and $F_{ext}$ is due to an external applied force. This problem is very difficult to solve for most semiconductors due to their completely different compositions from each other. It would be a waste of time to redo most of the same work to achieve different conclusions for each material. To work around this, we find the the band structure, $E-k$, for each material and relate what the *effective mass* of the particle would be for a given momentum. This simplification makes it easier to make general conclusions about semiconductors but also brings with it some issues where things like $\hbar k$ being a quasi-momentum or that effective mass needs to be treated differently in equations (summation, average, etc). Regardless of the issues, it comes to a net reduction of burden for calculation, so scientists stuck with it.

### 3.2.3 Intrinsic Materials

An intrinsic material is a material with no defects or external additions (eg. not doped or contaminated). At 0K, an intrinsic material has zero electrons in the conduction band (zero EHPs) and a completely filled valence band. At higher temperatures, EHPs are generated and become the only charge carries in the material. The previous section 3.2.1 assumed an intrinsic material.

EHPs only are generated in pairs, therefore there must be an equal number of electrons in the conduction band and holes in valence band. This relationship is shown succinctly below:

$$
    n = p = n_i
$$ 

where $n$ is the number of *negative* electrons, $p$ is the number of *positive* holes, and $n_i$ is the *intrinsic* carrier concentration.

As the temperature varies, the EHP concentration must also vary. If we keep the carrier concentration the same, we realize that for every EHP *generated* we must have another EHP go through a *recombination*. These two rates, $g_i$ and $r_i$, for generation and recombination, respectively, can be related through the following equation:

$$ 
    g_t = r_t
$$

Given a specific carrier concentration, the rate at which EHPs are created must equal the rate at which EHPs are destroyed. This relation makes sense; if we created more EHPs then we destroyed, then we would no longer have $n = p$ and would no longer have an intrinsic material. We also realize that for an intrinsic material, this must hold true for all temperature (although the rates can vary) and we reach the following conclusion:

$$
    r_t = \alpha_rn_0p_0 = \alpha_rn_i^2 = g_t
$$

where $\alpha_r$ is a recombination factor that is determined by the mechanism that used to recombine the EHP. This relation tells us that the number of holes and electrons is directly proportional to the recombination and generation rates.

### 3.2.4 Extrinsic Materials

Through specific processes, we can change the carrier concentrations in ways other than just temperature dependence. One of these ways is called *doping*, where other elements are added to the lattice structure. These new elements have different numbers of electrons then the main material of the lattice, which results in either extra electrons (n-type) or extra holes (p-type). When materials are doped such that $n_0$ or $p_0$ are different from $n_i$, the intrinsic carrier concentration, we call the material *extrinsic*.

###### n-type Dopants

For n-type dopants, like those from column V (P, As, Sb), the extra atoms introduce a *donor* energy level, which resides just below the conduction band. This donor level is completely filled at 0K, but due to its proximity to the conduction band, electrons do not need much energy to move into the conduction band. Thus, at low temperatures, the donor level will be completely empty, and all of its electrons will exist in the conduction band. This causes $n_0$ to larger than $p_0$ as EHPs are still created with the temperature variance and the extra donor level does not contribute to the number of holes in the valence band. This donor band is shown in the image below.

![n-type Material](Chapter&#32;3/n-type_material.png)

At 0K, all of the electrons in the donor level reside within the its energy level, but at low temperatures, like 50K, we see that electrons move into the conduction band. This means that $n_0 > p_0, n_i$.

###### p-type Dopants

For p-type dopants, like those from column III (B, Al, Ga, In), the extra atoms introduce an *acceptor* energy level, existing just above the valence band. This energy level is normally empty, as the column III elements are misisng an electron when compared to the column IV main element. At 0K this band remains completely empty, just above the filled valence band. At low temperatures, the small energy difference between it and the valence band allows for electrons in the valence band to move into the acceptor level. This creates an extra amount of holes in the valence band. The image below shows the effect a p-type dopant has.

![p-type Material](Chapter&#32;3/p-type_material.png)

At 0K, no electrons exist in the acceptor level, but at 50K, we notice many electrons leave the valence band to join the acceptor level. This causes the concentration to change, where $p_0 > n_0, n_i$.

###### Doping Examples

Doping Si with a column III element would be a p-type dopant, while a column IV element would be a n-type dopant. A combined III-V base semiconductor, like GaAs, gets donors from column VI, so S, Sc, and Te would be examples of substitutes for As. An acceptor for GaAs would reside in column II, so Be, Zn, and Cd would substitute for Ga. 

A more odd example would be that of doping a III-V material with a column IV material, like Si or Ge. These column IV materials can act as donors or acceptors based on which atom location they reside in. For example, in GaAs, when Si resides in a Ga location, it acts as a donor, while on an As location, it acts an acceptor. These types of dopants are called *amphoteric*.

Doping a material will cause changes in the electronic properties, which will be discussed later, but on a simple level, the following example demononstrates how powerful the process is. For Si, the intrinsic carrier concentration, $n_i$ is around $10^{10} \space\text{cm}^{-3}$ at room temperature. If Si is doped with As at a density of $10^{15} \space\text{atoms/cm}^3$, the resistivity drops from $2\times10^{5} \space\Omega\text{-cm}$ to $5 \space\Omega\text{-cm}$.

When a semiconductor is doped, either electrons or holes will be much greater than the other. In either p-type or n-type, we describe the greater of the two as the *majority carrier* and the lesser the *minority carrier*. For example, in n-type the electrons are the majority carrier and the holes are the minority carrier. In p-type, the opposite is true.

###### Citation

All images are sourced from *Solid State Electronic Devices*, 7th Editon, by Ben Streetman and Sanjay Banerjee