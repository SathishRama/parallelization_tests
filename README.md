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

![image](https://user-images.githubusercontent.com/26101449/229294329-26eec17e-8082-4ca0-be42-bb005ac269ba.png)

