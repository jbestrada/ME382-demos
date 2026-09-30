# ME382-demos
Demonstration webpages for ME382, Mechanical Behavior of Materials

## Crystal planes demo

The standalone page is [`index.html`](index.html). It displays simple-cubic, BCC, FCC, HCP, and diamond-cubic structures as hard spheres sized to touch their nearest neighbors. Select a plane to highlight the circular cross-sections through those spheres. A camera-tracking coordinate triad identifies Cartesian `x`, `y`, and `z`; for cubic structures these directions correspond to the `h`, `k`, and `l` plane indices. Hexagonal indices use the reciprocal hexagonal basis instead, as explained above the viewer. The equations above the viewer state the fractional-coordinate plane equation, the representative plane through the cell center, and the interplanar spacing. Each elemental structure includes a 2D contact sketch and a step-by-step radius derivation in formal math, followed by the packing-fraction derivation. An optional “Show hidden edges faintly through atoms” control adds translucent unit-cell edges over the space-filling spheres; by default, sphere surfaces occlude hidden edges to preserve depth cues.

Binary-compound examples include rock-salt NaCl/MgO/LiF/KCl, B2 CsCl/CsBr/CsI, zincblende ZnS/ZnSe/GaAs, and wurtzite ZnO/AlN/GaN/ZnS. Preset ionic radii use Shannon's effective ionic radii for the coordination number of each prototype: VI for rock salt, VIII for B2, and IV for zincblende and wurtzite. GaAs is covalent, so its preset uses neutral-atom single-bond covalent radii (Ga 1.22 Å, As 1.19 Å) from Cordero et al., not formal Ga³⁺/As³⁻ ionic radii. The applet displays the radius convention and source for each selection. You can still adjust radii, masses, and colors. The lattice parameter is derived from ideal unlike-neighbor contact; packing fraction and density are estimates from that radius-sum model, not measured material data.

Radius references:

- R. D. Shannon, “Revised effective ionic radii and systematic studies of interatomic distances in halides and chalcogenides,” *Acta Crystallographica Section A* 32 (1976), 751–767. [doi:10.1107/S0567739476001551](https://doi.org/10.1107/S0567739476001551).
- B. Cordero et al., “Covalent radii revisited,” *Dalton Transactions* (2008), 2832–2838. [doi:10.1039/B801115J](https://doi.org/10.1039/B801115J).

Each binary prototype's default mixed-species plane is checked against both sublattices, and the page reports the number of A/B atom centers on the selected plane. Such a mixed-species plane is not always the densest plane: for example, the close-packed FCC `{111}` layers in rock salt and zincblende contain one species at a time.

To preview it on your computer, open the repository in a terminal and run:

```sh
python3 -m http.server 8000
```

Then visit <http://localhost:8000> in a browser. Serving it this way is recommended because the page loads Three.js as a JavaScript module.

To publish it with GitHub Pages, push this branch to GitHub, merge it into `main`, then open the repository's **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/(root)`, and save. GitHub will provide the published site URL on that settings page.
