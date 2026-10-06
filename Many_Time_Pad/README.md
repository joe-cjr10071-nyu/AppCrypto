# Many-Time Pad — Problems 3 and 4

The workspace now follows the supplied Project 2 PDF. See [assignment_requirements.md](assignment_requirements.md) for requirements, rubric, and submission/review items.

## Start with Problem 3

Open [P3_Many_Time_Pad_Encrypt.ipynb](P3_Many_Time_Pad_Encrypt.ipynb). It encrypts ten editable example messages with one shared key, validates round trips, and writes plaintexts, key, and ciphertexts in hexadecimal to [data/simulation.json](data/simulation.json).

Run the experiments at the end and explain your observations. The example messages can be replaced by the team's chosen messages.

## Then work on Problem 4

Open [P2_Many_Time_Pad_Analysis.ipynb](P2_Many_Time_Pad_Analysis.ipynb). Its retained filename identifies the overall Project 2 workspace; it implements the Problem 4 analysis workflow.

The notebook loads the ten official ciphertexts and the separately labeled target, checks source integrity, and provides:

- Length inventory and pairwise XOR inspection.
- Space-candidate scores with character-filter checks.
- Crib dragging across a selected pair.
- Cross-checking a plaintext guess against all messages.
- Explicitly accepted cribs, conflict detection, and partial target display.

No cribs are accepted initially. Scoring and readable candidate fragments do not establish verified recovery. Record iterations in [analysis_notes.md](analysis_notes.md).

**Source ambiguity:** the PDF calls the target the “last message” but supplies a separate target after C10. This workspace uses that explicitly labeled target; it is 59 bytes long.

## Run the notebooks

Use Python 3.9 or newer with a Jupyter Python kernel. The notebook code requires only the standard library. Run from this folder or the repository root, setting the kernel working directory accordingly.

The simulation notebook writes `data/simulation.json`. The analysis notebook reads the official inputs without modifying them.

## Supporting files

| File | Purpose |
| --- | --- |
| [data/](data/) | Official inputs, transcription provenance, and separate simulation output |
| [analysis_notes.md](analysis_notes.md) | Assumptions, hypothesis/evidence log, and report preparation |
| [assignment_requirements.md](assignment_requirements.md) | All four problems, rubric, deliverables, and team review |
| [encode-encrypt-decrypt-decode_hints.yml](encode-encrypt-decrypt-decode_hints.yml) | Earlier preliminary notes, preserved unchanged; plain text despite the extension |

The original PDF is the authoritative source. Final plaintext recovery, written report, PDF exports, and all-member review/sign-off remain pending.

