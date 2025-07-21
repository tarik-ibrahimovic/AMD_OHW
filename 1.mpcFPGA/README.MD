# MPC on FPGA implementation
## Flow
After formulating the QP with CasADi, we export it to embedded-friendly C code using SPLIT. An ADMM solver is selected as the FPGA-based QP optimization method, following its widespread adoption in the past decade. Programmable Logic is used to accelerate matrix-vector multiplications (MVM), integrated directly into the SPLIT-generated C code. The complete system runs on FreeRTOS, targeting the R5 cores.
## References
> [1] I. McInerney, G. A. Constantinides, and E. C. Kerrigan, “A survey of the implementation of linear model predictive control on FPGAs,” in Proc. IFAC Conf. Nonlinear Model Predictive Control (NMPC), Madison, WI, USA, vol. 51, no. 20, pp. 381–387, Aug. 2018, doi: 10.1016/j.ifacol.2018.11.063.