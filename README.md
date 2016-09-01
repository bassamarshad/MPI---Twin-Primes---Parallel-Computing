# MPI---Twin-Primes---Parallel-Computing
Using MPI library to find the next largest Twin Prime Pair
#
1)	I have written the two functions prime(long int n) and twin(long int n), by using the same logic as provided . The long int takes a number upto 2,147,483,647. They return the nearest prime value q (q>n) to n and the nearest twin prime pair near to n, respectively. Enter the number from command line.
#
2)	prime (long int n) and twin(long int n), are called on 4 process (0,1,2,3) separately. And utilize MPI_Send() , to send the results to process 4 
#
3)	On process 4, we get 4 results (utilize MPI_Recv() )and then we get the nearest (smallest) result. This is done using the MPI_Reduce() , function.
#
4)	I run the program from the command line and specify the creation of 5 processes, also passing the number as argument . Using below :
#

From directory of program exe file:

#mpiexec –n 5 PrimeNumberMPI.exe 10

