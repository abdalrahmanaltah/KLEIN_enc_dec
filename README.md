this is python code that simulate the process of the KLEIN CIPHER_ENC_DEC
Overview of KLEIN Cipher
Block Size: Typically, KLEIN operates on blocks of 64 bits.
Key Sizes: Supports key lengths of 64, 80, or 96 bits, depending on the level of security required.
Rounds: The number of rounds depends on the key size:
64-bit key: 12 rounds
80-bit key: 16 rounds
96-bit key: 20 rounds
Structure: KLEIN uses a Substitution-Permutation Network (SPN), which consists of multiple rounds of substitutions (non-linear transformations) and permutations (mixing operations).
Encryption (KLEIN_enc)
The encryption process of KLEIN involves:

Key Expansion: The original key is expanded into round keys.
Initial Key Addition: The plaintext block is XORed with the first round key.
Round Operations: Each round includes:
Substitution: Using an S-box to replace bytes.
Diffusion: Using matrix-based transformations to spread the influence of input bits.
Key Addition: XOR with the round key.
Final Output: After the last round, the resulting block is the ciphertext.
Decryption (KLEIN_dec)
The decryption process is the reverse of encryption:

Reverse Key Expansion: The same round keys are used but applied in reverse order.
Initial Key Addition: XOR the ciphertext with the last round key.
Reverse Round Operations:
Reverse Substitution: Using the inverse S-box.
Reverse Diffusion: Using the inverse matrix transformation.
Reverse Key Addition.
Final Output: The resulting block is the plaintext.
