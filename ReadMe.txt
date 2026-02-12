# Project: Comparing Unsupervised Neural Network Models

This project was completed in a single Google Colab notebook (`https://colab.research.google.com/drive/1o8wYp7SaLu5cSm4ohBA9UhO4JfUByPMJ?usp=sharing` file), which contains the code for two different models, run one after the other.

The two parts of the notebook are:
1.  **Code 1: Standard Autoencoder:** This is the baseline deterministic model.
2.  **Code 2: Variational Autoencoder (VAE):** This is the proposed non-deterministic model.

---

### Required Resources

*   **Software:** A web browser to access Google Colab.
*   **Hardware:** A GPU is recommended for faster training (this can be enabled for free in Google Colab).
*   **Python Libraries:**
    *   `torch` and `torchvision`
    *   `scikit-learn`
    *   `matplotlib`
    *   `numpy`

All required libraries are installed automatically by running the `!pip install` commands at the top of the notebook.

---

### Instructions for Running the Code

To see the results exactly as they were generated for the report, please follow these steps:

1.  **Open the `https://colab.research.google.com/drive/1o8wYp7SaLu5cSm4ohBA9UhO4JfUByPMJ?usp=sharing` file** in Google Colab.
2.  **Enable the GPU:** In the menu at the top, go to **Runtime** → **Change runtime type** and select **GPU** from the dropdown menu. Then click **Save**.
3.  **Run All Cells:** In the menu, go to **Runtime** → **Run all**. This will execute the code for the Autoencoder first, followed by the code for the Variational Autoencoder.

You can then scroll through the notebook to see the outputs for each part, including the training progress, final metrics, and all the plots.
