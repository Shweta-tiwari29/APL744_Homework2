This project implements a Latent Diffusion Operator (LDO) — a generative surrogate model that learns to predict PDE solutions from initial/boundary conditions. It combines:

FNO encoders to compress input and target fields into a low-dimensional latent space
Conditional DDPM to model the distribution of target latent codes given the input
FNO decoders to reconstruct full-resolution output fields from sampled latent codes

At inference time, the model draws an ensemble of K=16 samples to produce both a point prediction and an uncertainty estimate.
