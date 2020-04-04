# Comparing spatial smoothing methods in AFNI
This repo contains a Jupyter Notebook comparing several methods for spatial smoothing in AFNI ([Cox, 1996](https://doi.org/10.1006/cbmr.1996.0014), [2012](https://doi.org/10.1016/j.neuroimage.2011.08.056)). This notebook provides a simple walkthrough of the methods and is not intended to be an authoritative comparison. We use an example dataset from the Narratives collection of story-listening fMRI experiments (OpenNeuro [ds002345](https://openneuro.org/datasets/ds002345); [Nastase et al., 2019](https://doi.org/10.18112/openneuro.ds002345.v1.0.1)). We use AFNI's [`3dmerge`](https://afni.nimh.nih.gov/pub/dist/doc/program_help/3dmerge.html) and [`3dBlurInMask`](https://afni.nimh.nih.gov/pub/dist/doc/program_help/3dBlurInMask.html) to smooth the data, then evaluate the resulting smoothness using [`3dFWHMx`](https://afni.nimh.nih.gov/pub/dist/doc/program_help/3dFWHMx.html) ([Forman et al., 1995](https://doi.org/10.1002/mrm.1910330508)). We then compare this to [`3dBlurToFWHM`](https://afni.nimh.nih.gov/pub/dist/doc/program_help/3dBlurToFWHM.html) which iteratively smooths the data until a desired smoothness is reached. We perform a similar comparison on the cortical surface using SUMA's [`SurfSmooth`](https://afni.nimh.nih.gov/pub/dist/doc/program_help/SurfSmooth.html) and [`SurfFWHM`](https://afni.nimh.nih.gov/pub/dist/doc/program_help/SurfFWHM.html) ([Saad et al., 2004](https://doi.org/10.1109/ISBI.2004.1398837), [2012](https://doi.org/10.1016/j.neuroimage.2011.09.016)), which implement heat kernel smoothing ([Chung et al., 2005](https://doi.org/10.1016/j.neuroimage.2004.12.052), [Hagler et al., 2006](https://doi.org/10.1016/j.neuroimage.2006.07.036)). Standardizing spatial smoothness across datasets and relating this to smoothing methods used previously in the literature is an important element of data harmonization ([Friedman et al., 2006](https://doi.org/10.1016/j.neuroimage.2006.03.062)).

![Alt text](./docs/source/images/smoothing_figure.png?raw=true&s=100 "Comparison of smoothing methods")

#### References
* Chung, M. K., Robbins, S. M., Dalton, K. M., Davidson, R. J., Alexander, A. L., & Evans, A. C. (2005). Cortical thickness analysis in autism with heat kernel smoothing. *NeuroImage*, *25*(4), 1256-1265. https://doi.org/10.1016/j.neuroimage.2004.12.052

* Cox, R. W. (1996). AFNI: software for analysis and visualization of functional magnetic resonance neuroimages. *Computers and Biomedical Research*, *29*(3), 162-173. https://doi.org/10.1006/cbmr.1996.0014

* Cox, R. W. (2012). AFNI: what a long strange trip it's been. *NeuroImage*, *62*(2), 743-747. https://doi.org/10.1016/j.neuroimage.2011.08.056

* Forman, S. D., Cohen, J. D., Fitzgerald, M., Eddy, W. F., Mintun, M. A., & Noll, D. C. (1995). Improved assessment of significant activation in functional magnetic resonance imaging (fMRI): use of a cluster‐size threshold. *Magnetic Resonance in Medicine*, *33*(5), 636-647. https://doi.org/10.1002/mrm.1910330508

* Friedman, L., Glover, G. H., Krenz, D., Magnotta, V., & The FIRST BIRN (2006). Reducing inter-scanner variability of activation in a multicenter fMRI study: role of smoothness equalization. *NeuroImage*, *32*(4), 1656-1668. https://doi.org/10.1016/j.neuroimage.2006.03.062

* Hagler Jr, D. J., Saygin, A. P., & Sereno, M. I. (2006). Smoothing and cluster thresholding for cortical surface-based group analysis of fMRI data. *NeuroImage*, *33*(4), 1093-1103. https://doi.org/10.1016/j.neuroimage.2006.07.036

* Nastase, S. A., Liu, Y.-F., Hillman, H., Zadbood, A., Hasenfratz, L., Keshavarzian, N., Chen, J., Honey, C. J., Yeshurun, Y., Regev, M., Nguyen, M., Chang, C. H. C., Baldassano, C. B., Lositsky, O., Simony, E., Chow, M. A., Leong, Y. C., Brooks, P. P., Micciche, E., Choe, G., Goldstein, A., Halchenko, Y. O., Norman, K. A., & Hasson, U. (2019). Narratives: fMRI data for evaluating models of naturalistic language comprehension. *OpenNeuro*, ds002345. https://doi.org/10.18112/openneuro.ds002345.v1.0.1

* Saad, Z. S., & Reynolds, R. C. (2012). SUMA. *NeuroImage*, *62*(2), 768-773. https://doi.org/10.1016/j.neuroimage.2011.09.016

* Saad, Z. S., Reynolds, R. C., Argall, B., Japee, S., & Cox, R. W. (2004). SUMA: an interface for surface-based intra-and inter-subject analysis with AFNI. In *2nd IEEE International Symposium on Biomedical Imaging: Nano to Macro* (pp. 1510-1513). IEEE. https://doi.org/10.1109/ISBI.2004.1398837
