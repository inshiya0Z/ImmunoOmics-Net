# ImmunoOmics-Net
A Multi-Omics Late Fusion Neural Network built in PyTorch to integrate high-dimensional RNA-Seq and Proteomic data tracks for predicting immune cell response phenotypes. Includes a high-signal biological pathway simulation.
# ImmunoOmics-Net

A PyTorch deep learning project built on Google Colab to predict immune cell responses by integrating high-dimensional RNA-Seq data and Proteomics data.

##  Run it Instantly
Click the badge below to open the code directly in Google Colab and run the network:

[![Open In Colab]
https://colab.research.google.com/drive/19BpsLdAcgAs1-chtX5Ijzp0GuDXLgBzk#scrollTo=YqddEfettLRD

##  How it Works
Instead of mixing the data types at the start, this project uses a **Late Fusion** neural network architecture to prevent modality imbalance:
1. **RNA Branch:** Processes 500 gene expression features independently using Batch Normalization.
2. **Protein Branch:** Parallel branch processing 100 protein abundance features.
3. **Fusion Classifier:** Concatenates the learned latent features to predict if the immune response will succeed (1) or fail (0).

---

##  Features & Results
- **Framework:** 100% PyTorch (`torch.nn`)
- **Accuracy:** Achieves **77.33% accuracy** on unseen test data using dynamic optimization techniques.
- **Optimization:** Built with a learning rate step-down scheduler (`StepLR`) and Dropout layers to handle experimental data noise.
- **Environment:** Designed to run with zero setup directly on a free Google Colab notebook.
- 
