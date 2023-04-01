# parallelization_tests
To compare various data processing mechanisms such as using a looping logic vs using vector computations on gpu

# Test Setup
Objective is to process arund 1.2M rows. A simple mutiple of two values and summing total using below approaches
1. Looping logic where we split 1.2m rows processing into 2424 X 490 ( 490 rows processing sequentially using loop 2424 times )
2. Using tensorflow :
  2.a On CPU : process 1.2m rows as matrix multiplication in one iteration
  2.b On GPU " process 1.2m rows as matrix multiplication in one iternation 
