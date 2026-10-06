# Project 2 — Requirements and Review Checklist

Source: `project2-MTP-problems-v2026B.docx(1).pdf`, supplied by Joe. This checklist summarizes the assignment; the original PDF controls if there is a discrepancy.

## Problems and rubric

| Problem | Required work | Maximum points | Current workspace status |
| --- | --- | --- | --- |
| 1: Understanding OTP | Define the OTP, explain its conditions and operational principles | 1 | Written explanation remains to be prepared or linked |
| 2: Alice and Bob | Alice prompts for plaintext and saves ciphertext/key in separate hex files; Bob reads those files and displays plaintext | 2 | Existing `../OTP/` notebooks and exports |
| 3: Many-Time Pad simulation | Encrypt ten predefined messages using one sufficiently long shared key; save plaintexts, key, and ciphertexts, all in hex, into one file; explore patterns | 2 | `P3_Many_Time_Pad_Encrypt.ipynb`; editable example messages and `data/simulation.json` output |
| 4: Cryptanalysis | Design a feasible attack, implement it in a Python Jupyter notebook, decrypt the target, and discuss iterations/results | 5 | Official inputs loaded; interactive attack tools prepared; target recovery pending |

Problem 4 allocates 1 point to strategy, 2 to working code (human intervention allowed), and 2 to correct target decryption. Incomplete recovery can also affect strategy credit.

## Problem 3

- Exactly ten predefined messages chosen by the team.
- One shared key, long enough for the longest message.
- All messages use the same key from the beginning.
- A file containing plaintexts, shared key, and ciphertexts as hexadecimal values.
- Experiments changing messages or the key, with observations explaining patterns.

The starter's ten messages are editable examples. Their known plaintexts/key are confined to the simulation and do not supply the key for the official cryptanalysis dataset.

## Problem 4

- The source supplies ten numbered ciphertexts and a separately labeled target.
- Preserve the numbered inputs in `data/ciphertexts.txt` and the explicit target in `data/target.txt`.
- English plaintext; listed punctuation is space, comma, period, and question mark.
- Key reuse is given. The notebook compares shared starting offsets.
- Use the XOR and ASCII hints; include crib dragging per Hint J.
- Iterate: adjust parameters and guesses, cross-check, and rerun.
- Discuss successful and unsuccessful approaches, partial results, and adjustments.
- Recover the explicitly labeled target correctly for full recovery credit.

### Source ambiguities to keep visible

1. The prose refers to the “last message,” but the target printed after ciphertext 10 is different. The workspace uses the explicitly labeled target and does not replace C10.
2. Hint I discusses numeric characters. The initial candidate filter therefore includes digits alongside letters and the named punctuation; tighten it if the instructor clarifies that digits are excluded.
3. Submission refers back to Project 1 rather than spelling out packaging here. Verify that course guidance before the final submission.

## Deliverables and team review

- Written report explaining all four problems, implementation details, attack strategy, outcomes, and security implications.
- Jupyter notebooks for OTP encryption/decryption, many-time pad encryption, and cryptanalysis.
- Notebook and PDF submission, following Project 1's procedure.
- All team members review and sign off on all problems, support each other, and cross-check results.

No deadline is specified in this PDF. Final report, final PDFs, and team sign-off remain pending.

