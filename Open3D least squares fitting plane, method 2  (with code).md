#  First, the principle of the algorithm 

 This paper implements the least squares fitting plane of matrix singular value decomposition method. The principle is as follows: 

   For the obtained point cloud data, let the fitted plane equation be: the constraint condition is: the plane parameters can be obtained. At this time, to make the obtained fitted plane optimal, that is, to minimize the sum of squares of the distances from the adjacent points to the plane,

 In fact, some points are outside the plane, and the purpose of fitting is to minimize the sum of the distances from all points on the plane. 

  If singular value decomposition can be done: then: where: is a column matrix, and: because the diagonal element of is a singular value, assuming that the last diagonal element is the smallest singular value, then if and only if:, formula (10) can obtain the minimum value, that is, formula (7) holds. At this time: the optimal solution of the objective function (7) under the constraint condition (8) is: Therefore, the minimum value of is the minimum eigenvalue of the matrix, and the corresponding eigenvector is a plane parameter, which can be obtained by using the centroid. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574457910
  ```  
#  III. Display of results 

##  1. Point cloud 

 ![avatar]( 29b5c2a2deb04b89b0b656ad9e2bd3c7.png) 

##  2. Fitting results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574457910
  ```  
 ![avatar]( 8b4eda694e9140b4bd1d2a8def6fe132.png) 

