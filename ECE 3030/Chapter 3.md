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

This feature of band gaps was discovered back in the 

### 3.2.2 Effective Mass
Electrons in a lattice structure are not considered completely free due to the complications the periodic potential brings to the wavefunctions. To use the regular electrodynamical equations on electrons within lattice structures, we must first find the *effective mass* of the electron, which depends on $E-k$ plot.

$$ 
    E = \frac{1}{2}mv^2 = \frac{1}{2} \frac{p^2}{m} = \frac{\hbar^2}{2m}k^2 \\
$$

From this equation, we can notice that the electron energy is parabolically related to the wavenumber k, or said another way, the electron mass is inverse parabolically related to the energy. If we differentiate with respect to our independent variable, k, we arrive at the effective mass equation:

$$
    E = \frac{\hbar^2}{2m}k^2 \\
    \space \\
    \frac{d^2E}{dk^2} = \frac{\hbar^2}{m} \\
    \space \\
    m^* = \frac{\hbar^2}{d^2E/dk^2} 
$$

An E-K graph is given below, showing how the curvature (2nd derivative) changes the effective mass.

![Simple E-K Graph](Chapter&#32;3/E-K&#32;Graph.png)

The graph below shows the E-K graphs for GaAs and AlAs and their lowest energy bands. GaAs is a direct band gap material and AlAs is an indirect band gap material. Using the effective mass equation we found earlier, we can discern that the effective mass at the $X$ node is higher than that at the $\Gamma$ node for both materials. $\Gamma$ has a higher $\frac{dE^2}{dk^2}$ than $X$ does, which relates to a $\Gamma$ having a higher effective mass.
