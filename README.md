# Scientific_Computing

Monte Carlo vs. Deterministic Volume Integration methods are compared for computing the volume of the hypersphere. We will be estimating the volume of a d-dimensional (hyper-)sphere of radius r=1 centered on the origin. So for d=1, the answer is 2;
for d=2, the answer is πr^2=π, and for d=3 the answer is 4πr^3/3, etc. There are analytical formulae for higher d as well
but we’re going to pretend we don’t know them (See the Wikipedia page on the volume of the n-ball).The implementation here is done using python.

Monte Carlo Integration:

In this method, I have surrounded the hypersphere with the smallest hypercube that can enclose it.
This hypercube is centered at the origin with sides of length 2 and has a volume of 2^d. I have then
selected N points at random inside the hypercube. I used Rejection algorithm to determine the count
of points that are inside the hypersphere. I do this by generating 2D matrix N*d size with random
numbers in range [-1,1] and checking if sum of the squares row wise is <=1. The volume of the hypersphere is then
(N-points inside / N-points in total) * 2^d.

Cube Based Integration:

In this method, I have divided each of the d dimensions into K segments, so that the side of
the smaller is of length 2/k. The volume of smaller hypercube is (2/k)^d.
