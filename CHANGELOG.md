# Changelog

## [0.1.0] - Mar 26th
### Added
- ```
  u_withAB  = np.sqrt(2 * A_val / B_val) / np.cosh(np.sqrt(A_val) * x_test)
  ```


### Changed
- ```
  u_withAB  = np.sqrt(2 * A_val / B_val) / np.cosh(np.sqrt(B_val) * x_test)
  ```

### Results
- Simple bug in modeling the solution using the learned A & B values to align solution graphs.
