### Improved Denoising Diffusion Probabilistic Models

**Citation:** @InProceedings{pmlr-v139-nichol21a,
  title = 	 {Improved Denoising Diffusion Probabilistic Models},
  author =       {Nichol, Alexander Quinn and Dhariwal, Prafulla},
  booktitle = 	 {Proceedings of the 38th International Conference on Machine Learning},
  pages = 	 {8162--8171},
  year = 	 {2021},
  editor = 	 {Meila, Marina and Zhang, Tong},
  volume = 	 {139},
  series = 	 {Proceedings of Machine Learning Research},
  month = 	 {18--24 Jul},
  publisher =    {PMLR},
  pdf = 	 {http://proceedings.mlr.press/v139/nichol21a/nichol21a.pdf},
  url = 	 {https://proceedings.mlr.press/v139/nichol21a.html},

**Description:**
code and pre-trained models at https://github.com/openai/improved-diffusion 

Detailed Mechanics of the Approach

Forward and Reverse Processes:

- In the forward process, Gaussian noise is added to the data at each step, gradually destroying the data structure until it becomes nearly isotropic Gaussian noise.
- The reverse process attempts to recover the original data from the noisy version by learning a parameterized distribution for each step. This process is modeled by a neural network that predicts the mean and variance of the reverse distribution.


### Diffusion-based Time Series Imputation and Forecasting with Structured State Space Models

**Link:** https://arxiv.org/pdf/2208.09399

**Description:**
