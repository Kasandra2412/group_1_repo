
Section 1:
The authors are addressing the prediction of three-dimensional protein structures from a protein's amino acid sequence. And this problem has been an essential open research problem for over fifty years. There were two development pathways of computational methods to predict three-dimensional (3D) protein structures from the protein sequence, physical interaction programme and evolutionary programme. However, in the majority of cases, if a close homologue has not been solved experimentally, the prediction accuracy of both methods is less than ideal. In this article, the authors developed the first computational approach that can predict protein structures with near experimental accuracy in most situations.

Section 2: Highly accurate protein structure prediction with AlphaFold: The computational approach the authors are proposing to use.

The authors are proposing a new computational method, AlphaFold2, which achieves near-experimental accuracy prediction of protein structures by incorporating novel neural network architectures and training procedures based on protein structure constraints. AlphaFold2 particularly predicts 3D coordinates of all heavy atoms for a given protein using the primary amino acid sequence and aligned sequences of homologues as inputs. The architecture is set in two stages, Evoformer, which processes the inputs through repeated layers of a novel neural network block into a processed MSA and residue pairs representations, and the structure module, which introduces an explicit 3D structure in the form of a rotation and translation for  each protein, rapidly developing and refining a highly accurate protein structure with precise atomic details.

<<<<<<< Updated upstream
Section3: The AlphaFold paper in Nature grounds its advances on several streams of prior work. It builds on decades of experimental structure determination through crystallography, cryo-EM, and NMR that underpin the Protein Data Bank as the essential training resource. From theory, the study relies on classic formulations of the protein folding problem developed by Anfinsen, Dill, and colleagues that defined sequence-to-structure principles. Computationally, it draws from earlier comparative modeling methods by Šali and Blundell as well as Zhang’s I-TASSER, and from co-evolutionary analyses that first linked correlated mutations to structural contacts, such as the work of Altschuh, Marks, Jones, and Weigt. Deep learning–based contact prediction models, including those by Senior and colleagues, Wang and colleagues, and Zheng and colleagues, provided immediate precedents for machine learning approaches to folding. The critical CASP benchmarks established by Moult and collaborators created the rigorous testing framework in which AlphaFold’s performance is assessed. Together, these experimental, theoretical, and computational foundations created the conditions for DeepMind’s integration of physical principles with advanced neural networks to achieve near-atomic accuracy.






=======
Section 4: Even though DeepMind put out a GitHub repo with the code nd models, it's not possible for us to fully redo the AlphaFold study. The main reason is the amount of computing power it needs - they used tons of GPU's/TPUs and trained the system for a long time, which we dont have access to. It also depend on really big databases like UniRef and PDB that take a lot of stoage and setup. On top of that, a lot of their exact preprocessing steps, optimization, and fine-tuned weights can't easily be recreated without their retup. So, the GitHub repo lets us run predictions with the pre-trained models, but we can't retrain in ourselves or get the same results they did.
>>>>>>> Stashed changes
