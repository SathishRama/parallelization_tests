# parallelization_tests
To compare various data processing mechanisms such as using a looping logic vs using vector computations on gpu

# Test Setup
Objective is to process around 1.2M rows. A simple mutiple of two values and summing total using below approaches
1. Looping logic where we split 1.2m rows processing into 2424 X 490 ( 490 rows processing sequentially using loop 2424 times )
2. Using tensorflow :
  2.a On CPU : process 1.2m rows as matrix multiplication in one iteration
  2.b On GPU " process 1.2m rows as matrix multiplication in one iternation 

# Observations
The results may vary for each experiment but on average 2-5x improvement observed using GPU vs looping for basic multiplication of two numbers & summing total

Number of cpu's:1 gpu's:1 in the runtime.
Time with Loop logic: 0.009 for 2424 iterations with 490 rows in each iteration. Rows processed 1187760
GPU time: 0.0029357990006246837 for 1187760 rows
Using Looping code vs TF CPU : 0.284 x improvement for 1187760 rows processed
Using Looping code vs TF GPU : 3.066 x improvement for 1187760 rows processed
