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
- The network is trained using a combination of objectives, including a simplified objective and a variational lower bound (VLB)
- A neural network learns to reverse the noising process by predicting the original data from the noisy data.
- The learned variances and hybrid objective allow the model to achieve high-quality samples with fewer steps, reducing the computational cost of sampling.

Variational Lower Bound (VLB) and Hybrid Objective:

The Variational Lower Bound (VLB) is a crucial component in training Denoising Diffusion Probabilistic Models (DDPMs). It ensures that the model learns to approximate the true data distribution accurately. 

***The VLB is designed to ensure the model learns an accurate approximation of the true data distribution by minimizing the KL divergence between the true and learned reverse processes.*** The hybrid objective, which combines the VLB with a simplified noise prediction objective, provides stable gradients and better performance. This combination helps the model achieve high-quality samples and good log-likelihoods, making the training process more efficient and effective.

Cosine Noise Schedule in DDPMs:

- The cosine noise schedule is an innovative approach introduced to improve the efficiency and quality of Denoising Diffusion Probabilistic Models (DDPMs).
- Purpose of the Noise Schedule: It determines the amount of noise added to the data at each step in the forward process of diffusion models. Proper scheduling is crucial as it influences how well the model can learn to denoise the data during the reverse process.

Estimate Loss Contributions: Track and update the loss contributions for each timestep during training.
Calculate Sampling Probabilities: Compute the sampling probabilities based on the estimated loss contributions.
Sample Timesteps: During each training iteration, sample timesteps according to the computed probabilities instead of uniformly.
By focusing on more critical timesteps, the model can learn more effectively and reduce the overall training time.

***Training the model***
Step 1: Define the Forward Diffusion Process
- Set the total number of timesteps T.
- Define noise schedule, linear or cosine. Cosine is often used for improved performance.
- The forward process that adds Gausian noise to the data.
  
Step 2: Formulate the Reverse Process
- Parameterize the Reverse Process by a neural network, predicting mean and variance.
- Predict noise.

Step 3: Define the Loss Functions
- Simplified objective: directly minimizes the difference between the true noise and the predicted noise.
- Variational Lower Bound (VLB): ensures that the learned reverse process approximates the true reverse process
- Hybrid objective: combines the simplified objective with the VLB to balance stability and accuracy.

Step 4: Importance Sampling
- Estimate the contribution of each timestep 𝑡 to the overall loss and adjust the sampling probabilities accordingly.
- Maintain a running history of loss values to dynamically update the sampling probabilities.
- During each training iteration, sample timesteps dynamically according to the computed probabilities

Step 5: Train the Model
- Initialize the neural network with parameters 𝜃.
- Choose an optimizer (e.g., Adam) and set the learning rate.
- Training loop: For each training iteration, Sample Data, Forward Process, Compute Loss, Backpropagation
- Monitor training progress using metrics like the log-likelihood, sample quality (e.g., FID), and gradient noise scales.
- Adjust hyperparameters if necessary to stabilize and improve training.
- After training, evaluate the model’s performance using a reduced number of sampling steps.
- Assess the quality of generated samples using metrics such as FID and precision-recall.
- Fine-tune the noise schedule and sampling strategy if needed to balance speed and quality.

### Diffusion-based Time Series Imputation and Forecasting with Structured State Space Models

**Link:** https://arxiv.org/pdf/2208.09399

**Description:**
Various datasets (ECG, MuJoCo, Electricity) under different missingness scenarios.

Time series data often suffer from missing values due to various reasons like sensor failures or data entry errors. Accurate imputation of these missing values is crucial for effective downstream analysis. The paper introduces (Structured State Space Diffusion) SSSD, which integrates diffusion models and structured state space models, providing a robust solution for time series imputation and forecasting.

- Imputation targets are specified using binary masks indicating missing values. (1 - Observed value, 0 - missing value)
- Various missingness scenarios include Random Missing (RM), Random Block Missing (RBM), Blackout Missing (BM), and Time Series Forecasting (TF).
- Diffusion Model: Forward Process, Reverse Process, Objective function --> minimizes the difference between added noise and predicted noise.
- The diffusion process is applied only to the portions of the sequence to be imputed.
- The training objective combines a reconstruction loss for observed values and an imputation loss for missing values.
- The loss function minimizes the difference between the actual noise and the predicted noise
- Conditional Information for Imputation: To handle missing data, the reverse process is conditioned on the observed parts of the data and the imputation mask.
- To generate imputations, the model starts from the noisy data 𝑥𝑇 and iteratively applies the reverse process to recover the original data with imputed values.
- During this process, the neural network uses the conditioning information to ensure that the reconstructed data aligns with the observed values.
- This conditioned sampling process ensures that the imputed values are consistent with the observed data and the learned dependencies.
- The final imputed values are obtained after the reverse diffusion process reaches 𝑥0, original data.
- The imputed values are those that best fit the learned distribution conditioned on the observed data.

Forecasting: the task is to predict future values given past observed values.
- Similar to the imputation process, the forward process adds noise to the past observed values, and the reverse process denoises it to predict future values.
- The model conditions the reverse process on the past observed values.
- The model uses the learned reverse process to generate forecasts by starting from noisy predictions and iteratively denoising them.

Evaluation Metrics:

- Mean Absolute Error (MAE), Root Mean Square Error (RMSE), and Mean Relative Error (MRE) were used to evaluate imputation accuracy.
- Forecasting accuracy was assessed using MAE and Mean Square Error (MSE).

The SSSD model effectively imputes missing values by leveraging the forward diffusion process to add noise and the reverse diffusion process to iteratively denoise the data. By conditioning the reverse process on observed data and imputation masks, the model ensures that the imputed values are consistent with the known parts of the data, resulting in high-quality imputations and forecasts.
