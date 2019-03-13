# Scientific_Computing

Monte Carlo vs. Deterministic Volume Integration methods are compared for computing the volume of the hypersphere. I will be estimating the volume of a d-dimensional (hyper-)sphere of radius r=1 centered on the origin. The implementation is done using python.

Monte Carlo Integration:

In this method, I have surrounded the hypersphere with the smallest hypercube that can enclose it.
This hypercube is centered at the origin with sides of length 2 and has a volume of 2d
. I have then
selected N points at random inside the hypercube. I used Rejection algorithm to determine the count
of points that are inside the hypersphere. I do this by generating 2D matrix N*d size with random
numbers in range [-1,1] and checking if sum of the squares row wise is <=1.

Cube Based Integration:

In this method, I have divided each of the d dimensions into K segments, so that the side of
the smaller is of length 2/k. The volume of smaller hypercube is (2/k)d.
