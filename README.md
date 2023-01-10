# Discrete-Distribution

iscreteDistribution.java that takes an integer command-line argument m, followed by a sequence of positive integer command-line arguments a1,a2,…,an, 
and prints m random indices (separated by whitespace), choosing each index i with probability proportional to ai.

To generate a random index i with probability proportional to ai:

  - Define the cumulative sums Si=a1+a2+…+ai, with S0=0.

  - Pick a random integer r uniformly between 0 and Sn−1.

  - Find the unique index i between 1 and n such that Si−1≤r<Si.

Geometrically, this subdivides the interval [0,Sn) into n subintervals [Si−1,Si), with the length of subinterval i proportional to ai. For example, 
if the discrete distribution is defined by

(a1,a2,a3,a4,a5,a6)=(10,10,10,10,10,50),

then the cumulative sums are

(S1,S2,S3,S4,S5,S6)=(10,20,30,40,50,100)

and the following diagram illustrates the 6 subintervals:

![image](https://user-images.githubusercontent.com/100317918/211557670-974a7f04-5fad-4981-b893-9c272560e36a.png)


In probability theory, this is known as sampling from a discrete distribution.
