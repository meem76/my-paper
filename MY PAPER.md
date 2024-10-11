Resource 
--paper : https://www.nature.com/articles/s41597-024-03117-2
 paper code: https://github.com/masih4/NuInsSeg

NuInsSeg dataset:
--dataset of H&E-stained histological images with fully annotated nuclei and ambiguous area masks.
Purpose: To support the development and evaluation of supervised deep learning models for nuclei instance segmentation in computational pathology.

Unique feature: Includes ambiguous area masks, which can help improve model robustness and accuracy


Challenges of manual segmentation: Tedious, complex, and prone to inter- and interobserver variability due to artifacts and the complex nature of histological samples.

Advent of automated methods: Semi- and fully-automatic computer-based methods using classical image processing and machine learning techniques have been proposed.

deep learning: Supervised deep learning methods
                         --Mask R-CNN and its variants




Semi-automatically generated datasets: like PanNuke, Lizard, and Hou et al

**Limitations of semi-automatically generated datasets: Training on these datasets may introduce a bias towards the reference model and not accurately capture human expert style.


Tissue preparation: Formaldehyde-fixed and embedded in celloidin or paraffin.
Scanning: WSIs generated using a TissueFAXS scanning system.
Dataset creation: 665 raw image patches extracted from representative FOVs of the WSIs.

Ground truth segmentation masks: Created using ImageJ with manual delineation of nuclei borders.

Auxiliary segmentation masks: Border-removed binary masks, elucidation distance maps, and weighted binary masks are included.

Ambiguous area segmentation masks: Annotated for the first time in this dataset, indicating regions where accurate manual annotation is impossible.

Annotation process: Performed by multiple students with quality control by a senior cell biologist.


        ****Baseline Segmentation Benchmark:

        Dataset split into 5 folds with equal images per fold (133 images each).
       Five-fold cross-validation was used to evaluate model performance.
    
Evaluation Metrics:
        Dice score, Aggregate Jaccard Index (AJI), and Panoptic Quality (PQ) scores used for evaluation.

 Baseline Models and Performance:
        Shallow U-Net and Deep U-Net models with dropout layers implemented .
        Other models evaluated include Attention U-Net, Residual Attention U-Net, Two-stage U-Net, and Dual Decoder U-Net (architectures in respective articles).
        Residual Attention U-Net achieves best Dice score.
        Dual Decoder U-Net achieves the best average AJI and PQ scores (also achieved the best PQ score in the MoNuSAC challenge).
    
Dataset Accessibility:

        NuInsSeg dataset available on Zenodo and Kaggle.
        Step-by-step instructions and code for manual annotations and segmentation mask generation on GitHub.
        Three Kaggle kernels for EDA, shallow U-Net, and deep U-Net models.
    Python Packages:
        Pandas, Matplotlib, Tensorflow, Keras, Scikit-learn, Scikit-image, and Albumentation used .
    Computational Resources:
        Kaggle platform provides limited free computational resources for direct analysis.
     
   


