# ME382-demos
Demonstration webpages for ME382, Mechanical Behavior of Materials

## Crystal planes demo

The standalone page is [`index.html`](index.html). It displays simple-cubic, BCC, FCC, HCP, and diamond-cubic structures as hard spheres sized to touch their nearest neighbors. Select a plane to highlight the circular cross-sections through those spheres. Each elemental structure shows its radius derivation and hard-sphere packing fraction. Cubic cells use signed Miller indices `(hkl)`; negative signs are shown as overbars. Hexagonal structures use Miller-Bravais indices `(hkil)` with an `i` slider constrained by `h + k + i = 0`, and an ideal `c/a` ratio.

Binary-compound examples include rock-salt NaCl/MgO/LiF/KCl, B2 CsCl/CsBr/CsI, zincblende ZnS/ZnSe/GaAs, and wurtzite ZnO/AlN/GaN/ZnS. Select a compound from the structure-specific dropdown, then adjust its radii, masses, and colors if desired. The applet derives the lattice parameter from unlike-neighbor contact and estimates packing fraction and density; these are ideal hard-sphere calculations, not measured material data. The initial ionic radii are illustrative coordination-dependent values and can be changed. Each binary prototype's default mixed-species plane is checked against both sublattices, and the page reports the number of A/B atom centers on the selected plane. Such a mixed-species plane is not always the densest plane: for example, the close-packed FCC `{111}` layers in rock salt and zincblende contain one species at a time.

To preview it on your computer, open the repository in a terminal and run:

```sh
python3 -m http.server 8000
```

Then visit <http://localhost:8000> in a browser. Serving it this way is recommended because the page loads Three.js as a JavaScript module.

To publish it with GitHub Pages, push this branch to GitHub, merge it into `main`, then open the repository's **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/(root)`, and save. GitHub will provide the published site URL on that settings page.
