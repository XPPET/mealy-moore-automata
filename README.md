# Cryptographic Sequence Transformation using Mealy and Moore Machines (DFST)

<img width="1893" height="841" alt="moore_decoder jff" src="https://github.com/user-attachments/assets/a863b4ba-eeca-41bc-b7df-19bc1faf384c" />

This repository contains the implementation of **Deterministic Finite-State Transducers (DFST)** designed to execute a specific 3-bit sliding window encryption and decryption algorithm. The projects were developed using the **JFLAP** software framework based on the **DFST.pdf** assignment requirements for the *Theory of Computation* course taught by **Professor Yiannis Refanidis** at the University of Macedonia (PAMAK).

## 📋 Project Overview
The system processes a binary sequence and computes an output bit based on the sum of the last three inputs. If the sum is `01` or `11` in binary, the output is `1`; otherwise, if the sum is `00` or `10`, the output is `0`. Decryption is processed inversely from the end to the beginning of the sequence.

## 📂 Repository Contents
* **Mealy Machines:**
  * `mealy_encoder.jff` - The Mealy transducer that computes output sequences directly on state transitions.
  * `mealy_decoder.jff` - The inverse Mealy transducer configured to decode encrypted text.
* **Moore Machines:**
  * `moore_encoder.jff` - The Moore transducer where output signals are tied explicitly to the internal states.
  * `moore_decoder.jff` - The inverse Moore transducer modified for decryption.
* **Documentation:**
  * `Report.pdf` - The technical report containing functional descriptions, state diagrams, and simulation traces.

## 🚀 How to Run
1. Download and run **JFLAP** (requires Java JRE/JDK installed on your system).
2. Open JFLAP and select `File -> Open`.
3. Load any of the `.jff` files.
4. Go to `Input -> Fast Run` or `Input -> Multiple Run` to test the machine with custom binary inputs.
