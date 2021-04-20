# Meet-in-the-middle Attacks Revisited



## Additional details

> How X_13[8] and Z_12[4,8] are computed?

Z_12[4] = Y_12[7] by SR^-1, and Y_12[7] = X_12[7] + STK_12[7]. X_12[7]=Z_11[3] due to MC (Equation 4). Z_12[8] = Y_12[10] by SR^-1, and Y_12[10] = X_12[10]. X_12[10] = Z_11[6] + Z_11[10] due to MC. All the cells needed to compute Z_12[4] and Z_12[8] are blue or gray which are independent to the red cells. Similarly, we can compute X_13[8] which only depends on the red and gray cells.
