# CDCMX Challenge Task 7

Objective: Explain the process of purification of a protein and how is the protein's structure determined by the cryo-EM technique including an overview of the obstacles in this process.

Based on the Article "SARS-CoV-2 and bat RaTG13 spike glycoprotein structures inform on virus evolution and furin-cleavage effects" published on Nature structural and molecular biology by Antoni G. Wrobel, Donald J. Benton, Pengqi Xu, Chloe Roustan, Stephen R. Martin, Peter B. Rosenthal, et. al

## Purification of proteins

![protein](https://upload.wikimedia.org/wikipedia/commons/e/e3/6VSB_spike_protein_SARS-CoV-2_homotrimer.png)
>*Image of SARS-CoV-2 Spike protein homotrimer structure*

#### 1. Proteins need to be expressed in a cell culture to produce them in large quantities for specific subjects of study. 

Spike glycoproteins in the comparative study of SARS-CoV-2 and RaTG13 were expressed in Expi293 cells - a human cell lineage for culture which have higher protein expresison levels and rapid cell growth compared to other cell lineages - at 37°C and 125 r.p.m. These cells were cultured in a FreeStyle 293 Expression Medium - a free protein medium that enhances cell transfection - and transfected (or delivered with external nucleic acids) with DNA and ExpiFectamine 293 - a transfection reagent that boosts protein expression and folding. The supernatants were collected during the 3rd or 4th day and 6th or 7th day after culture and were clarified, filtered and incubated with affinity resin.

![expression](https://www.leinco.com/wp-content/uploads/2019/08/ExpressionOfRecombinantProtein-01-2-1024x362.jpg)
>*Diagram of the protein expression process*

#### 2. Protein purification is important to avoid pollutants in our subjects of study and get more reliable results.

Spike proteins were bound to TALON cobalt leads (a purification resin which delivers his-tagged proteins of the highest purity), washed and eluted (reverse process of binding to the resin) with imidazol. ACE2 was bounded to Strep-Tactin XT resin (part of a purification system for recombined proteins). The protein was eluted with Strep-Tactin Elution Buffer BXT. Next, all proteins were flash-frozen (froze proteins in a short amount of time due to exposition to cryogenic temperatures in liquid nitrogen)or gel-filtration (process of separation of molecules based on their ability to enter the pores of the gel-filtration medium) a Superdex 200 Increase column which delivers higher resolution purification in a short time.

![purification](https://ruo.mbl.co.jp/bio/e/product/tag/images/purification/tagged_protein_purification_kit_procedure_summary.png)
>*Diagram of the protein purification process*

#### 3. Furin is important for SARS-CoV-2 S glycoprotein to bind to ACE2

A furin treatment was applied to SARS-CoV-2 S glycoprotein. Recombinant furin (furin cloned in an expression system) was used to cleave SARS-CoV-2 S glycoprotein. SDS-PAGE (Sodium dodecyl sulfate Polyacrylamide Gel Electrophoresis is used to separate components of a protein mixture based on their size) was used to track the reaction. 

![furin](https://www.researchgate.net/publication/309070939/figure/fig1/AS:560653511008256@1510681621348/Structure-of-the-furinRVKR-CMKNb14-complex-Human-furin-is-shown-as-surface.png)
>*Image of human furin protein*

## Determining the structure of proteins by cryo-EM

#### Preparing SARS-CoV-2 S

The furin-uncleavable SARS-CoV-2 S was frozen.

#### Preparing RaTG13 S

RaTG13 S need to be prepared for cryo-EM by buffer optimization and cross-linking (binding two or more protein molecules to facilitate scientific probes on protein-protein interactions). The protein was treated with BS^3 - a crosslinker (chemical agent used to cross-link)- and double cross-linking was achieved using the Grafix Protocol (method to purify and stabilize macromolecular complexes for single particle cryo-EM). Fractions containing RaTG13 S indentified with SDS-PAGE were concetrated and gel-filtered.

The resulting RaTG13 S and furin-treated SARS-CoV-2 S were frozen at mesh grids with a thin layer carbon. The grids were glow discharged prior to freezing. Glow discharge negatively charges a carbon layer in order to make aqueous solutions spread easier over the carbon surface. 

#### Preparing the Samples

To prepare the samples, 4 microliters of sample was added to a grid and the was plunge freezing (rapidly submerging it in a cryogen) into liquid ethane - cryogen.

#### Devices and software used for collecting data

- EPU Software
- Thermo Scientific Titan Krios microscope
- Falcon 3 (furin-uncleavable SARS-CoV-2 S micrographs)
- Gatan K2 (furin-treated SARS-CoV-2 S and RaTG13 S micrographs)

### Obstacles in determining the structure of proteins by cryo-EM

Processing cryo-EM data to reveal heterogeneity in the protein structure and to refine 3D maps to high resolution requires expert intervention, prior structural knowledge, and weeks of calculations on expensive computer clusters.

![cryoem](https://www.researchgate.net/profile/EV_Orlova/publication/318102798/figure/fig13/AS:668721475489807@1536447032967/Cryo-EM-sample-preparation-a-3-mm-copper-mesh-grid-covered-with-a-film-of-holey.png)

## Data processing

Movie frameswere aligned using MotionCor2 (corrects beam-induced sample motion recorded on dose fractionated movie stacks) and Contrast Transfer Function (multiplies the Fourier transform by an oscillating function that depends on defocus and the spherical aberration coefficient of the objective lens). Furin-uncleavable SARS-CoV-2 S micrographs were manually picked using crYOLO (fast and accurate particle picking procedure, based on convolutional neural networks and utilizes You Only Look Once object detection system). Particles on the carbon support were picked using RELION (open-source computer program for the refinement of macromolecular structures by single-particle analysis) auto-picking. Using RELION, classes with a clear secondary structure were retained and then classifing using RELION with models in cryoSPARC (scientific software platform for cryo-EM). Final refinements were made with cryoSPARC, except for intermediate conformation whose refinements were made by RELION. Local resolution was estimated in cryoSPARC. Maps were filtered and sharpened in cryoSPARC.

## Model Building

Uncleavable SARS-CoV-2 S in closed conformation was first based on the already published structure, it was fitted to density and added extra regions. This model was used for building RaTG13 S structure, in which some residues were changed. PHENIX refined and validated this models.
Intermediate and open structures were generated by fitting uncleavable SARS-CoV-2 S to density and elect the Receptor-Binding Domain manually in the open structure. These proteins' structure were refined by Namdinator and normalized geometrically by PHOENIX.

## Advantages of cry-EM technique

Cryo-EM technique especializes in the analizes of large proteins, like homotrimers in the case of SARS-CoV-2 S and RaTG13 S, and specifically in those obtained form viruses. 

The process to prepare the sample is really easy, fast and efficient compared to the processes of other techniques. This is due to the fact that only 1 microgram per milliliter is needed, while in other techniques this quantity multiplies up to 10 times.

There is no need in cristallizing the proteins thus the protein can be present in different conformations and the different flexible structures can be observed such as the close, the intermediate and the open conformations in SARS-CoV-2 S and RaTG13 S.

## References

1. Thermo Fisher Scientific. (2020). Expi293F™ Cells. Retrieved August 14, 2020, from https://www.thermofisher.com/order/catalog/product/A14527#/A14527
2. Polyplus-transfection. (2020, August 03). What is transfection? Retrieved August 15, 2020, from https://www.polyplus-transfection.com/about-us/what-is-transfection/
3. Thermo Fisher Scientific. (2020). FreeStyle™ 293 Expression Medium. Retrieved August 15, 2020, from https://www.thermofisher.com/order/catalog/product/12338018
4. Fisher Scientific. (2020). Gibco™&nbsp;ExpiFectamine™ 293 Transfection Kit - Inicio. Retrieved August 15, 2020, from https://www.fishersci.es/shop/products/expifectamine-293-transfection-kit-3/p-7075867
5. Takara. (2020). TALON Metal Affinity Resin: Batch or gravity flow purification of his-tagged proteins. Retrieved August 15, 2020, from https://www.takarabio.com/products/protein-research/purification-products/his-tagged-protein-purification/bulk-resins-and-gravity-columns/cobalt-resin
6. Urh, M., &amp; Zhao, K. (2009). Elution. Retrieved August 15, 2020, from https://www.sciencedirect.com/topics/biochemistry-genetics-and-molecular-biology/elution
7. Iba. (2019). Recombinant Protein Purification using Strep-Tactin®XT. Retrieved August 15, 2020, from https://www.iba-lifesciences.com/strep-tactin-xt-system-technology.html
8. Sharpe, T. (2013, May 14). Freezing and Storing Protein Solutions. Retrieved August 14, 2020, from https://www.biozentrum.unibas.ch/fileadmin/redaktion/05_Facilities/01_Technology_Platforms/BF/Protocols/Freezing_and_Storing_Protein.pdf
9. S.G. Prapulla, N.G. Karanth. (2014). Gel Filtration. Retrieved August 15, 2020, from https://www.sciencedirect.com/topics/immunology-and-microbiology/gel-filtration
10. Cytiva. (2020). Superdex 200 Increase small-scale SEC columns. Retrieved August 15, 2020, from https://www.cytivalifesciences.com/en/us/shop/chromatography/prepacked-columns/size-exclusion/superdex-200-increase-small-scale-size-exclusion-chromatography-columns-p-06190
11. Dobro, M., Melanson, L., Jensen, G., &amp; McDowall, A. (2010, September 29). Chapter Three - Plunge Freezing for Electron Cryomicroscopy. Retrieved August 15, 2020, from https://www.sciencedirect.com/science/article/pii/S0076687910810031
12. Stark, H. (2010). GraFix: Stabilization of Fragile Macromolecular Complexes for Single Particle Cryo-EM. Retrieved August 15, 2020, from http://cryoem.life.tsinghua.edu.cn/wp-content/uploads/2013/05/GraFix_method.pdf
13. G Biosciences. (2012, October 12). What is Protein Cross-Linking and Which Reagents are Used in it? Retrieved August 16, 2020, from https://info.gbiosciences.com/blog/bid/160707/what-is-protein-cross-linking-and-which-reagents-are-used-in-it
13. TED PELLA, INC. (2020). PELCO easiGlow™ Glow Discharge Cleaning System. Retrieved August 16, 2020, from https://www.tedpella.com/easiGlow_html/Glow-Discharge-Cleaning-System.htm
14. Aryal, S. (2020, January 14). Polyacrylamide Gel Electrophoresis (PAGE): Instrumentation. Retrieved August 16, 2020, from https://microbenotes.com/polyacrylamide-gel-electrophoresis-page/
