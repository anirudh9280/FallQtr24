**Lecture 21**
- triangular matrices diagonal entries are the eigenvalues
- two nxn matrices are similar if there exists an invertible nxn matrix such that A = PBP^-1
- similar matrices have the same eigenvalues
- if two matrices have the same eigenvalues, they do not have to be similar
- if one of the entries on a diagonal matrix is a zero, it is not invertible
- If there is a matrix A, a matrix P, and a matrix D and we know that A=PDP^-1, A^K = PD^kP^-1.
- ![[Screenshot 2024-03-12 at 11.19.38 PM.png]]
- a matrix A is diagonalizable if A = PDP^-1
- in general, [a 1; 0 a] is not diagonalizable
![[Screenshot 2024-03-12 at 11.26.32 PM.png]]
**Lecture 22**
- ![[Screenshot 2024-03-13 at 12.29.39 AM.png]]
- in general, the multiplicity of lambda is always greater than or equal to the dimension of the eigenspace 
- matrices with distinct eigen values are diaganolizable
- ![[Screenshot 2024-03-13 at 12.50.16 AM.png]]
- values are diagnolized 
**Lecture 23**
- a nxn matrix is diagonalizable if it has n distinct eigen values
- the normalization of a vector is if you divide it by the magnitude of said vector
- the distance between two vectors is the magnitude of the first vector minus the second vector
- cos theta = u . v / ||u||||v|| 
- |u . v| = |cos theta| . ||u|| . ||v|| <= ||u||.||v||
- two vectors are orthogonal if their dot product is 0 
- ||u-v||^2 = ||u||^2 + ||v||^2
- ![[Screenshot 2024-03-13 at 3.49.00 PM.png]]
**Lecture 24**
- determine if a set is orthogonal by checking if the dot products equal to 0
- ![[Screenshot 2024-03-14 at 4.29.48 AM.png]]
 - to see if a set is orthonormal (orthogonal vectors that are also normalized) you check if ui * ui = 1 and all ui * uj is 0 
 - ![[Screenshot 2024-03-14 at 3.48.13 PM.png]]
  - you know if a set of vectors is orthonormal if you multiply the transpose of that matrix with the original matrix and if you get an identity matrix, then the vectors are orthonormal
  - suppose you have an mxn matrix U, where the columns are sets of vectors that are orthonormal
	  - for any vector x, y in Rn, |Ux| = |x|. 
	  - (U.x)*(U.y) = x.y 
	  - (U.x)*(U.y) = 0 if x.y = 0
	  - therefore, this matrix preserves lengths and angles 
  - if U is a orthonormal matrix that is also square, the inverse of U = U transpose. So if you are given to find an inverse of an orthonormal matrix, just put it on its tranpose. 
**Lecture 25**
- an orthogonal set can have the zero vector in it, but an orthogonal set that does not have the zero vector in it is linearly independent
- in that vein, not every linearly independent set is orthogonal but every orthogonal set minus the zero vector is linearly independent
- projection of y onto L is ( (y.u1)/u1.u1 ) * u1  
- using this, the vector y = proj of y onto W + vector z
- proj y onto W is equal to c1u1+..+cpup such that ci is (y.ui)/(ui.ui)
- ![[Screenshot 2024-03-14 at 5.55.41 PM.png]]
- the distance of vector y to w is the length of the vector z in the equation, vector y = proj of y onto W + vector z
- if there is a subspace W with an orthonormal set of bases, U x U^T . vector y is the proj of y onto W
- to find the standard matrix given a basis, first normalize the basis and make sure it is orthogonal. then, do U (columns) of the orthonormal bases and multiply it with matrix U^T
- W perp of is an eigenspace of W the subspace of eigenvalue 0
- when given bases that are not orthonormal, you can build an orthonormal basis
**Lecture 26**
- when bases of a subspace are orthogonal, it helps to project vectors which has many applications
- however, there are many times when matrices do not have orthogonal bases 
- to make the bases orthogonal, you can use the gran-schmidt process
- ![[Screenshot 2024-03-14 at 7.05.46 PM.png]]
- QR factorization of matrices is when you have a matrix A, you find Q which is the orthonormal column space of A, then you multiply the transpose of Q with A, which yields matrix R
- R is almost always a triangular matrix which has eigen values that we want
- ![[Screenshot 2024-03-14 at 7.07.23 PM.png]]