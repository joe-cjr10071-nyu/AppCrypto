# Many-Time Pad — Analysis Notes

## Assignment and source

- Project instructions: supplied PDF; see assignment_requirements.md.
- Source of ciphertexts: project2-MTP-problems-v2026B.docx(1).pdf, pages 2–3; transcription details/hashes in data/provenance.json.
- Required deliverables: written explanation of all four problems, Jupyter notebooks, and PDFs following Project 1 submission guidance.
- Permitted plaintext characters: English; named punctuation is space, comma, period, and question mark. Initial candidate filter includes ASCII letters and digits (Hint I); clarify digit use if needed.
- Number and ordering of ciphertexts: ten numbered inputs retained as C01–C10; one separately labeled TARGET.
- Designated target message: explicit Target Message block, 59 bytes; different from the 52-byte C10.
- Shared key and starting-offset assumptions: shared key given by Problem 4; comparisons assume each message starts at key byte zero.
- Input formatting changes: joined wrapped hex fragments; removed numbering and excluded page footnotes; preserved digits and message order.

## Input validation

All ten numbered ciphertexts and the target parse as hexadecimal byte strings. Lengths: C01 78, C02 113, C03 90, C04 90, C05 103, C06 98, C07 110, C08 46, C09 123, C10 52; TARGET 59. Integrity checks compare the inputs with the recorded source fragments and hashes.

## Hypotheses and evidence

Use notebook labels C01, C02, etc. and **zero-based byte offsets**.

| Message | Byte offset or range | Hypothesis | Supporting evidence | Contradictions | Status |
| --- | --- | --- | --- | --- | --- |
| — | — | No hypotheses recorded | — | — | Pending |

Distinguish an untested guess, a supported candidate, and a verified result. A printable character or letter/space pattern alone does not establish correctness.

## Candidate key bytes

| Byte offset | Candidate key byte (hex) | Derivation | Cross-checks against other messages | Status |
| --- | --- | --- | --- | --- |
| — | — | No candidate bytes recorded | — | Pending |

## Recovered text and unknown positions

No recovery performed. Keep unknown positions explicit rather than silently filling them.

## Findings and open questions

The source's separate target differs from C10 despite its prose referring to the last message. Both are preserved. Space scores and crib tools are available, but no cribs or recovered key bytes have been accepted.

## Review and submission

- Compare final results with the professor's required outputs.
- Note unresolved positions and the evidence for any claimed recovery.
- Regenerate notebook exports after the final analysis.

