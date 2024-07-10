# T-cell_smFISH

The provided code assigns 3D subcellular localization (nucleus or cytoplasm) to individual RNA spots identified by smFISH. The code is a part of a more extensive analysis pipeline, employed in this specific use-case to cytokines TNF and IFN$\gamma$ in CD8<sup>+</sup> T-cells. 

For full details, please see our preprint: V. M. Lattanzio *et al.*: T cell smFISH.

In the repository, two scripts are provided:
1. `Filtering.Rmd` - An example script for filtering cells that would interfere with proper quantification: 1. cells with no detected nucleus, 2. incomplete cells located on the edges of images/coverslips, and 3. cells in division. The code compiles a list of such cells such that they can be excluded from downstream analyses.
2. `Spots_localization.ipynb` - For all non-filtered cells, a subcellular localization is assigned considering their 3D coordinates and 3D masks obtained from [Cellpose](https://github.com/MouseLand/cellpose).
