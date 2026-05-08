# S-DES Data Security Project

This repository contains a university-level **data security project** built around **S-DES (Simplified Data Encryption Standard)**. It combines a manual Python implementation of the algorithm with an interactive Streamlit interface, validation scripts, and supporting project artifacts such as the report, presentation, and UML material.

The project is designed to make core cryptography ideas visible rather than hidden behind black-box libraries. It focuses on how a simplified block cipher works internally, how round-based encryption is constructed, and why small key spaces are insecure.

## Why This Project Stands Out

Instead of only presenting theory, this repository turns a classroom cryptography topic into a practical and inspectable implementation.

It demonstrates:

- manual bit-level implementation of S-DES
- key generation and subkey scheduling
- encryption and decryption logic
- block cipher modes
- brute-force analysis on a small key space
- introductory differential cryptanalysis support
- an interactive interface for demonstration and learning

## Repository Structure

The repository is organized into three main parts:

- `kod/`
  Source code for the S-DES implementation, the Streamlit interface, and validation scripts.

- `rapor/`
  Project documentation and UML material.

- `sunum/`
  Presentation assets prepared for the course project.

## Core Features

- manual implementation of the S-DES algorithm
- S-DES permutation and transformation tables
- subkey generation for `K1` and `K2`
- single-block encryption and decryption
- support for `ECB`, `CBC`, and `OFB` modes
- validation checks for binary keys, blocks, and IV values
- brute-force known-plaintext search utilities
- differential cryptanalysis helper functions
- Streamlit interface with step-by-step explanation flow

## Technical Stack

- `Python` for the algorithm implementation
- `Streamlit` for the interactive web interface
- `pandas` for tabular displays in the app

The cryptographic core is implemented manually for educational transparency and does not depend on a ready-made S-DES package.

## Main Source Files

Inside `kod/` the most important files are:

- `sdes_core.py`
  Core S-DES logic, helper functions, cipher modes, and analysis utilities.

- `gui_app.py`
  Streamlit-based interface for encryption, decryption, and interactive demonstration.

- `test_sdes_core.py`
  Validation and demonstration tests for checking correctness.

- `README_TR.md`
  Turkish-language documentation for the code folder.

## What You Can Do with the App

The Streamlit interface is structured for demonstration and explanation.

Main usage areas:

- encrypt or decrypt a single 8-bit block
- inspect generated subkeys and intermediate round values
- experiment with `ECB`, `CBC`, and `OFB`
- try known-plaintext brute-force key search
- explore differential cryptanalysis helpers
- view reference permutation and S-box tables

This makes the repository useful both as a course submission and as a portfolio example of implementation-heavy security coursework.

## Quick Start

Install the required packages:

```bash
pip install streamlit pandas
```

Move into the code directory:

```bash
cd kod
```

Run the Streamlit application:

```bash
streamlit run gui_app.py
```

Run the validation script:

```bash
python test_sdes_core.py
```

## Example Test Vector

The implementation includes validation-friendly sample values such as:

```text
Key:        1010000010
Plaintext:  11010111
K1:         10100100
K2:         01000011
Ciphertext: 10101000
```

These values are used to verify that encryption and subkey generation behave as expected.

## Educational Value

This repository is especially useful for showing:

- understanding of Feistel-style cipher structure
- comfort with low-level binary transformations
- ability to turn theory into a working tool
- awareness of key-space weakness and brute-force feasibility
- interest in analytical security concepts beyond simple encryption/decryption

## Notes and Limitations

- S-DES is an educational algorithm and is not secure for real-world protection
- the repository is intended for learning, experimentation, and presentation
- the analysis components are simplified for academic use
- the focus is clarity and interpretability rather than production performance

## License

For academic and educational use.
