EEG Loneliness — Subject-Independent K-Fold (PyTorch + Optuna)

This repository contains a subject-independent EEG binary classification pipeline (loneliness vs. not_loneliness) implemented in PyTorch with Optuna for hyperparameter optimization.

Note: No data is included. Users must generate their own FoldData.pkl file.

⸻

Features
	•	Subject-independent K-Fold cross-validation
	•	Hyperparameter tuning with Optuna (TPE sampler)
	•	Multiple activation functions: SELU, LeakyReLU, ReLU, ELU, Mish
	•	Early stopping with patience
	•	Reports accuracy, F1-scores, and confusion matrix

⸻

Project Structure
	•	data/ (user-provided, contains FoldData.pkl)
	•	outputs/ (stores results and best hyperparameters)
	•	scripts/ (helper scripts, e.g., make_folddata_template.py)
	•	src/models/ (model definitions)
	•	src/utils/ (data loaders)
	•	src/train_optuna.py (main training and optimization script)

⸻

Usage
	1.	Create a virtual environment and install dependencies from requirements.txt.
	2.	Prepare FoldData.pkl following the provided template.
	3.	Run training with:
python -m src.train_optuna --folddata data/FoldData.pkl --activation selu --n_trials 50
Replace selu with other activations if desired.

Outputs: results are printed to console and best hyperparameters are saved in outputs/.

⸻

License

MIT License

⸻

Acknowledgements

PyTorch, Optuna, and community EEG processing resources.
