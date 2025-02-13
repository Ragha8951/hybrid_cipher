# Cracking the Code: Design and Analysis of a Hybrid Cipher  

This repository contains the implementation of a **hybrid cipher** that combines **substitution** (using a modified **Hill Cipher**) and **transposition techniques** to achieve **robust encryption** with at least **128-bit security strength**.  
The hybrid approach ensures resistance against classical cryptanalysis methods such as **frequency analysis** and **linear algebra attacks**. 
---
<br>

## **Table of Contents**  
- [Live Test](#live-test)  
- [Overview](#overview)  
- [Features](#features)  
- [How It Works](#how-it-works)  
- [Installation](#installation)  
- [Usage](#usage)  
- [Example](#example)  
- [Security Justification](#security-justification)  
- [Contributing](#contributing)  
- [Acknowledgments](#acknowledgments)  
- [Contact](#contact)  

---

## **Live Test**  

Try the **Hybrid Cipher** in **Google Colab**:  

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1LzGcHLn47gnmc_h-4ccZFbAARYSOuH2E?usp=sharing)  

---

## **Overview**  

The hybrid cipher integrates two classical cryptographic techniques:

- **Substitution Layer**: A modified **Hill Cipher** encrypts plaintext blocks using **matrix multiplication over a finite field**.  
- **Transposition Layer**: A **pseudorandom permutation** rearranges the encrypted blocks to disrupt patterns.  

This combination ensures both **confusion (substitution)** and **diffusion (transposition)**, making the cipher **more secure** than either technique alone.  

---

## **Features**  

- **128-bit encryption strength** for enhanced security.  
- **Combines** substitution (Hill Cipher) and transposition for stronger encryption.  
- **Modular design** for scalability (e.g., increasing block size).  
- **Deterministic yet unpredictable** behavior using a seeded **pseudorandom number generator (PRNG)**.  

---

## **⚙️ How It Works**  

### 🔹 **Substitution Layer**  
1. Converts plaintext into **numerical blocks**.  
2. Encrypts each block using a **randomly generated invertible matrix** (Hill Cipher).  

### 🔹 **Transposition Layer**  
1. **Shuffles** the encrypted blocks using a **PRNG seeded with a secret key**.  

### 🔹 **Decryption**  
1. Reverses the **transposition and substitution layers** to recover the original plaintext.  

---

## **Installation**  

### **Prerequisites**  
You need the following **Python libraries** to run the hybrid cipher:

- `numpy`: For matrix operations.  
- `sympy`: For modular matrix inversion.  

### **Steps to Install Dependencies**  
1. **Clone the repository**:

   First, clone the repository to your local machine using the following command:

   ```sh
   git clone https://github.com/Ragha8951/hybridcipher.git
2. **Install the required libraries using pip:**:
   ```sh
   pip install num py
   pip install numpy sympy

---
# Hybrid Cipher - Usage Guide

Once the dependencies are installed, follow these steps to run the **Hybrid Cipher**:

---

## **Usage**

1. **Save the `hyb.py` file** in your working directory.

2. **Run the script** using Python:

   ```sh
   python hyb.py
---
## **Customizing Parameters**
**block_size: Set the size of each plaintext block (default is 4) for the Hill Cipher encryption.**<br>

**substitution_key: Modify the randomly generated key matrix for the Hill Cipher (it is automatically generated).**<br>

**transposition_key: Provide a custom secret key for shuffling the blocks during the transposition phase (entered by the user).**<br>

---
## **Example**
### INPUT
   Enter SECRETKEY: gobimn
   Enter Plain text: good morningG

###OUTPUT
   Ciphertext Blocks: [[109, 138, 179, 95], [173, 217, 85, 138], [114, 177, 138, 4], [231, 77, 97, 89]]**

   Decrypted Text: good morningG

---

##**Security Justification**

  *Confusion: The Hill Cipher obscures relationships between plaintext and ciphertext by replacing plaintext blocks with seemingly unrelated ciphertext blocks.*
  
  *Diffusion: The transposition layer spreads the influence of each plaintext character across multiple ciphertext blocks, disrupting patterns and ensuring that partial information about the ciphertext is 
    insufficient for decryption.*
    
*128-bit Strength: By operating on large matrices and using modular arithmetic, the cipher achieves computational complexity comparable to modern encryption standards, ensuring brute-force attacks are computationally prohibitive.*
---

##**Acknowledgments**

**The design of this hybrid cipher is inspired by classical cryptographic techniques and modern encryption principles. Special thanks to the open-source community for tools like numpy and sympy, which made this implementation possible.**

---
##***Contact**
 **For questions or feedback, feel free to reach out:**

    **GitHub: @Ragha8951**
    **Email: ragha8951@gmail.com**
---




