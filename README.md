# Decision Certificates for Cross-World Utilities in Finite-Horizon Policies

Reproducibility materials for the paper by Shenggang Li, Bilian Song, Yunfeng Qi, and Joseph Li.

## Code and data

Download and extract `Conterfact_GitHub_Release.zip`.

The archive contains:

- Python code for experiments E1–E9.
- Synthetic replicate-level data and numerical summaries.
- 78 experiment checkpoints for E7–E9.
- Scripts for mathematical checks, result verification, and figure generation.
- Documentation of experimental assumptions and limitations.

## Reproduction

Requires Python 3.10+ with NumPy, SciPy, and Matplotlib.

From the extracted archive, run:

1. `pip install -r requirements.txt`
2. `python -m unittest discover -s experiment_code -p "test_*.py" -v`
3. `python experiment_code/run_e7_e9.py --verify-only`
4. `python experiment_code/audit_output.py`

For the original experiments E1–E6, enter `historical_source` and run `python reproduce.py --verify`.

## Scope

All experiments use synthetic models. The reported guarantees depend on the specified structural and calibration assumptions. The archive provides no evidence of deployed-policy effects or real-world proxy calibration.
