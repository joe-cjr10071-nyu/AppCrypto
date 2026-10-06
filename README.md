# AppCrypto — Project 2: Applied Cryptography

Working repository for Project 2 in NYU Tandon's CS-GY 6903 Applied Cryptography course, taught by Prof. Zhixiong Chen.

This repository brings together Jupyter notebooks, exercise inputs, and rendered outputs for team review. It will expand as the remaining project components are developed.

## Project status

| Component | Status | Contents |
| --- | --- | --- |
| One-Time Pad (OTP): Alice | Implemented; notebook includes example output | ASCII encoding, key generation, XOR encryption, hexadecimal file output |
| One-Time Pad (OTP): Bob | Implemented; notebook includes example output | Hexadecimal file input, XOR decryption, ASCII decoding |
| Problem 3: Many-Time Pad simulation | Implemented with editable example messages | Shared-key encryption of ten messages; one file of plaintext/key/ciphertext hex values |
| Problem 4: Many-Time Pad cryptanalysis | Official data loaded; recovery pending | XOR inspection, space scoring, crib dragging, and hypothesis cross-checks |
| Written report and team review | Pending | Explanation of all four problems, analysis, PDFs, and all-member sign-off |

The repository is a working project workspace. Inclusion of a file does not establish a final submission or team approval.

## Repository layout

| Location | Purpose |
| --- | --- |
| `README.md` | Project overview, status, and usage |
| `LICENSE` | Repository license |
| [`OTP/`](OTP/) | Alice and Bob notebooks, HTML/PDF exports, and sample input files |
| [`Many_Time_Pad/`](Many_Time_Pad/) | Starter notebook, ciphertext input folder, preliminary hints, and analysis notes |

### One-Time Pad files

| File | Purpose |
| --- | --- |
| [`P2_Alice_OTP_Encrypt.ipynb`](OTP/P2_Alice_OTP_Encrypt.ipynb) | Alice's editable encryption notebook |
| [`P2_Bob_OTP_Decrypt.ipynb`](OTP/P2_Bob_OTP_Decrypt.ipynb) | Bob's editable decryption notebook |
| [`P2_Alice_OTP_Encrypt.html`](OTP/P2_Alice_OTP_Encrypt.html) / [PDF](OTP/P2_Alice_OTP_Encrypt.pdf) | Alice's saved notebook exports |
| [`P2_Bob_OTP_Decrypt.html`](OTP/P2_Bob_OTP_Decrypt.html) / [PDF](OTP/P2_Bob_OTP_Decrypt.pdf) | Bob's saved notebook exports |
| [`ciphertext.txt`](OTP/ciphertext.txt) | Sample ciphertext, stored as hexadecimal text |
| [`key.txt`](OTP/key.txt) | Matching sample key, stored as hexadecimal text |

## Reviewing the work

- Open the `.ipynb` files on GitHub to inspect the code and saved outputs.
- Use the PDFs for static review.
- Download the HTML exports and open them in a browser to review locally.
- Use JupyterLab to edit or rerun the notebooks.

HTML and PDF exports capture a particular run; they do not update automatically when a notebook changes.

## Running the OTP notebooks

**Requirements:** Python 3 and JupyterLab with a Python kernel. The notebook code uses Python's standard library (`pathlib` and `secrets`).

1. Download or clone the repository.
2. Start JupyterLab from the `OTP/` directory, with the notebook kernel's working directory set to that folder.
3. To decrypt the included sample, open `P2_Bob_OTP_Decrypt.ipynb` and run its cells in order.
4. To create a new example, run `P2_Alice_OTP_Encrypt.ipynb` in order and enter an ASCII message when prompted. Alice generates a key with `secrets.token_bytes(len(plaintext_bytes))` and writes `ciphertext.txt` and `key.txt`.
5. Run Bob's notebook again to recover the new message.

**Running Alice overwrites the two sample text files in the kernel's working directory.** Keep the matching ciphertext and key together when exchanging exercise files.

The notebooks use relative filenames, so both notebooks and the two text files belong in the same working directory. Inputs are encoded or decoded as ASCII; ciphertext and key bytes are represented as hexadecimal text.

The included sample decrypts to:

> My, oh my what a fine day.

These are classroom demonstration artifacts: the sample key and plaintext are intentionally visible. A real OTP requires a uniformly random secret key as long as the message, used only once; this exercise uses Python's cryptographically secure random-byte generator.

## Many-Time Pad: Problems 3 and 4

Start with [P3_Many_Time_Pad_Encrypt.ipynb](Many_Time_Pad/P3_Many_Time_Pad_Encrypt.ipynb) to simulate ten messages encrypted with one shared key. It writes all required byte values in hex to `Many_Time_Pad/data/simulation.json`.

Then use [P2_Many_Time_Pad_Analysis.ipynb](Many_Time_Pad/P2_Many_Time_Pad_Analysis.ipynb) for Problem 4. The supplied ten ciphertexts and separate target are loaded and checked. Interactive tools support space hypotheses, crib dragging, and cross-checking candidate key fragments.

The explicit target is preserved separately from C10 because the source prints a distinct Target Message block. See the [folder README](Many_Time_Pad/README.md), [requirements checklist](Many_Time_Pad/assignment_requirements.md), and [analysis notes](Many_Time_Pad/analysis_notes.md).

Target recovery, the written report, final PDF exports, and all-member review/sign-off remain pending.

## Team workflow

All team members must review and sign off on every problem, as required by the project instructions. Keep each component's notebooks, inputs, and exports together. Use descriptive filenames and commit messages. When a notebook changes, regenerate any exports intended to reflect that version.

Share the [repository link](https://github.com/joe-cjr10071-nyu/AppCrypto) in Slack as the common entry point, and link individual files when requesting specific feedback.

## License

See [LICENSE](LICENSE) for the repository's GNU Affero General Public License, version 3.

