# PBLTELM
Fast Sparse Supervised Learning Framework with BLinex Loss Function

The code corresponds to the paper：Fast Sparse Supervised Learning Framework with BLinex Loss Function

If you are using our code, please give appropriate citations to the papers given above.

If you have any questions/errors in the code, please write to jiangtiantian0726@163.com.


%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
PBLTELM Code
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

%%The description of the PBLTELM Code is as follows:

1.PBLTELM.m：This file contains the functions of the iterative algorithm for solving PBLTELM. In PBLTELM.m, the input values and their meanings are as follows:
%Main Parameter Settings:
L = 200 represents the number of hidden layer nodes, corresponding to the quantity in the literature;
M = 10 denotes 10-fold cross-validation, aligning with the experimental setup in Section 4 of the paper; 
NN = 1 indicates the number of experimental repetitions.

%PBLTELM Core Parameters:
C1, C2, C3, C4 = 1 are regularization hyperparameters, corresponding to C₁, C₂, C₃, C₄ in Table 1 of the paper; 
p_val = 0.1 represents the p-value of the Lp-norm (0<p<1), corresponding to the Lₚ-norm sparsity constraint in Section 3; 
a = 1, b = 1, gamma_val = 1 are parameters of the Blinex loss function, corresponding to Formula (13) and Table 1 in the paper.

%Noise Settings:
noise_level = 0.30 indicates the noise level, corresponding to the noise experiments in Section 4.1.3 of the paper; 
noise_sigma = 0.30 represents the standard deviation of Gaussian noise, simulating the feature noise described in the literature.

%Adam Optimization Parameters:
alpha_adam = 0.001 is the learning rate, corresponding to the Adam algorithm in the paper;
beta1_adam = 0.9 and beta2_adam = 0.999 are the decay rates for the first and second moment estimates in the Adam algorithm; 
epsilon = 1e-8 is a constant for numerical stability.

%Iteration Parameters:
max_outer_iters = 10 indicates the number of outer iterations, corresponding to the dual-layer optimization strategy in Section 3.3 of the paper; 
max_inner_iters = 100 represents the number of inner iterations; 
tol = 1e-5 is the convergence tolerance.


%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
2.Artificial
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%% The Artificial Datasets code consists of artificial.m
%% file is described as follows:
%μ₁: mu1 = [0.5, -3]', the mean vector of the positive class samples, defining the center of the positive Gaussian distribution
%Σ₁: sigma1 = [0.2, 0; 0, 3], the covariance matrix of the positive class, which controls the shape and extent of the distribution of the positive class in the feature space
%μ₂: mu2 = [-0.5, 3]', the mean vector of the negative class samples, defines the center position of the negative class Gaussian distribution
%Σ₂: sigma2 = [0.2, 0; 0, 3], the covariance matrix of the negative class samples, which controls the distribution shape and range of the negative class samples in the feature space
%n_positive, the number of positive class samples, controls the number of positive class samples generated
%n_negative, the number of negative class samples, controls the number of negative class samples generated
%total_samples, the total number of samples, ensures that the total dataset size is fixed to 200 samples


%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
Loss Funcation, Real-World Datasets, Bar chart，CD_Figure
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%1. Loss Funcation code consists of the BLinex loss function Blinexf.m.
%%2.Bar chart, Violin plots, Line chart, CDya is the corresponding statistical chart.

To replicate the results obtained using PBLTELM, You should follow the paper "Fast Sparse Supervised Learning Framework with BLinex Loss Function".
