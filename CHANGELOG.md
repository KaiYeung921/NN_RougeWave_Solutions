# Changelog



#### [0.2.0] 
#### Added
- Changed the wieght CoEf of L5 from 10 -> 25 to highlight importance of this loss more
  ```
    c1, c2, c3, c4, c5 = 1, 1, 1, 1, 25
   ```

- Gave `A_Raw` & `B_Raw` paramters their own learning rate as they have much more gradient steps need to optimize them
  ```
  # Optimize network weights AND the ODE parameters together
  params    = list(u_NN.parameters()) + [A_raw, B_raw]
  optimizer = torch.optim.Adam([
      {'params': u_NN.parameters(), 'lr': 1e-4},
      {'params': [A_raw, B_raw],    'lr': 1e-3},  
  ])
  mse       = nn.MSELoss()
  ```
- Decreased # of Epochs from 500,000 -> 200,000
  ```
  n_epochs      = 2 * 10**5
  ```


#### Results
- Now loss =  7.106696e-06
- Learned  A = 12.4207
  Learned  B = 24.8446
  Expected A/B ratio ≈ 0.4999  (true = 0.5 for unit-peak sech)







#### [0.1.0] 
#### Added
- ```
  u_withAB  = np.sqrt(2 * A_val / B_val) / np.cosh(np.sqrt(A_val) * x_test)
  ```


#### Changed
- ```
  u_withAB  = np.sqrt(2 * A_val / B_val) / np.cosh(np.sqrt(B_val) * x_test)
  ```

#### Results
- Simple bug in modeling the solution using the learned A & B values to align solution graphs.




