# CSE425_Project
Neural Network

This project implements **unsupervised representation learning and clustering** on the MNIST handwritten digit dataset using two contrasting deep learning architectures: a deterministic standard autoencoder and a probabilistic variational autoencoder (VAE).
The **standard autoencoder** uses a deterministic encoder (784→512→128→32) and symmetric decoder (32→128→512→784) trained with MSE loss for 20 epochs using Adam optimizer (learning rate 1e-3) and batch size 256. 
The **Variational Autoencoder (VAE)** introduces stochastic latent representations through a probabilistic encoder that outputs mean (μ) and log-variance (log σ²) vectors, with a reparameterization trick (z = μ + ε·σ) enabling backpropagation through sampling.
VAE training optimizes a composite loss function combining **reconstruction loss (MSE)** and **KL divergence regularization** (−0.5 · Σ[1 + log σ² − μ² − σ²]) to balance data fidelity with latent space structure. 
Both models compress 28×28 grayscale images (normalized to [−1, 1]) into **32-dimensional latent embeddings** suitable for downstream clustering and visualization tasks.
**K-Means clustering** (10 clusters, 30 initializations) is applied to normalized latent embeddings, evaluated using silhouette score (cohesion), Davies-Bouldin index (separation), and Calinski-Harabasz index (compactness).
**t-SNE dimensionality reduction** visualizes 2,000 randomly sampled embeddings in 2D space colored by digit labels, revealing cluster quality and semantic structure in the learned latent representations. 
The VAE additionally generates **novel digit-like images** by sampling random 32-dimensional vectors from N(0,1) and decoding them, demonstrating its generative modeling capability beyond pure reconstruction. 
**Reconstruction quality assessment** displays side-by-side comparisons of 16 original and reconstructed images, quantifying how well each model captures input data structure after compression and decompression. 
The project is implemented in **PyTorch** with GPU acceleration support, utilizing torchvision for MNIST loading, scikit-learn for clustering/metrics, and matplotlib for comprehensive visualization of embeddings, generations, and reconstructions. 
