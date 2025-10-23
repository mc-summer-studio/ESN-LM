# ESN-LM
ESN-LM made by summer-studio

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/gist/Summer110622/2c06bc9ccaf5c8b608bc613cbfba2507/summer-studio.ipynb)

## ESN-LM Summer Studio Mechanism
- Overview
- ESN-LM applies Echo State Networks (reservoirs) for efficient language modeling, leveraging fixed random recurrent layers for representation.
## Key Components
	•	Input Encoding: Token embeddings fed into reservoir.
	•	Reservoir Layer: Sparse, fixed-weight RNN (echo state property ensures fading memory).
	•	Readout Layer: Linear regression on reservoir states to predict next token probabilities.
## Workflow
	1	Initialize random reservoir weights (spectral radius <1 for stability).
	2	Project input sequence through reservoir to collect states.
	3	Train output weights via ridge regression on states vs. targets.
	4	Inference: Forward pass, sample from readout softmax.
