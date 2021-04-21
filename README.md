# Meet-in-the-middle Attacks Revisited

## A Quick Revision
A revised version of the paper is provided at (https://github.com/mitm-revisited/submission-150/blob/main/paper-revised.pdf). In this revision:
- We identify the first preimage attack on 10-round hashing mode with AES-256 by employing the new representation of the AES key schedule due to Leurent and Pernot (EUROCRYPT 2021).
- We discuss the difficulties in building bit-oriented models, and refer the reader to [1,2] as a starting point for bit-level MITM attacks.
- We revise the attack on Saturnin, where the time complexity is improved significantly.

[1] Thomas Fuhr, Brice Minaud: Match Box Meet-in-the-Middle Attack Against KATAN. FSE 2014.
[2] Yu Sasaki: Integer Linear Programming for Three-Subset Meet-in-the-Middle Attacks: Application to GIFT. IWSEC 2018


## Additional details

> How X_13[8] and Z_12[4,8] are computed?

Z_12[4] = Y_12[7] by SR^-1, and Y_12[7] = X_12[7] + STK_12[7]. X_12[7]=Z_11[3] due to MC (Equation 4). Z_12[8] = Y_12[10] by SR^-1, and Y_12[10] = X_12[10]. X_12[10] = Z_11[6] + Z_11[10] due to MC. All the cells needed to compute Z_12[4] and Z_12[8] are blue or gray which are independent to the red cells. Similarly, we can compute X_13[8] which only depends on the red and gray cells.

> Very little time is spent explaining what the attack actually does.

We have added a dedicated section (see Appendix A of the [paper](https://github.com/mitm-revisited/submission-150/blob/main/paper-revised.pdf)) to explain the actual attack.
