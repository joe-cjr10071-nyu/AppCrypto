# Many-Time Pad — Project 2

**Status:** starter workspace ready; assignment ciphertexts and analysis pending.

## Files

| File or folder | Purpose |
| --- | --- |
| [P2_Many_Time_Pad_Analysis.ipynb](P2_Many_Time_Pad_Analysis.ipynb) | Starter notebook: validate hex inputs, inspect lengths, and compare ciphertexts by XOR |
| [data/](data/) | Instructions for adding the official ciphertext dataset |
| [analysis_notes.md](analysis_notes.md) | Source information, assumptions, hypotheses, and results |
| [encode-encrypt-decrypt-decode_hints.yml](encode-encrypt-decrypt-decode_hints.yml) | Existing preliminary hints, preserved unchanged; plain-text notes despite the YAML extension |

## Get started

1. Read the professor's Many-Time Pad instructions and record the required deliverables in `analysis_notes.md`.
2. Add `data/ciphertexts.txt`: one complete hexadecimal ciphertext per nonempty line, in the original order. Follow [data/README.md](data/README.md).
3. Open `P2_Many_Time_Pad_Analysis.ipynb` in JupyterLab and run the cells in order. Use Python 3.9 or newer; the analysis code uses only the standard library.
4. Run from the repository root or this folder. Set the notebook kernel's working directory accordingly.
5. Inspect the inventory and selected-pair XOR output. Record hypotheses with message labels and zero-based byte offsets.

The notebook runs without a dataset and displays readiness messages. It does not generate dummy assignment ciphertexts, recover plaintext automatically, or write over input files.

## Analysis plan

When the same pad is reused at matching offsets, `C_i XOR C_j = M_i XOR M_j`. Compare overlapping bytes only when lengths differ. Pairwise XOR output is not a decrypted message.

Confirm the exercise's character set and key alignment before adding space-pattern scoring or crib testing. Treat character-pattern hints as hypotheses and cross-check proposed key bytes against the other messages.

Keep original source data and document any formatting changes. Add HTML/PDF exports after meaningful analysis results are available.
