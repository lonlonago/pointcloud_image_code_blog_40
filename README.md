#  I. Overview of algorithms 

    Given the minimum and maximum values of the cube coordinates, extract points located within and outside the cube. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574444370
  ```  
#  III. Display of results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574444370
  ```  
 ![avatar]( 05f511a50cf74c9eb9e05de56817c232.png) 



--------------------------------------------------------------------------------

#  I. Overview 

 ![avatar]( eeb3612f672a4458aa6c875db0255841.png) 

   As the title, based on the elevation of the point cloud to make heat map rendering color point cloud. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574458526
  ```  
#  III. Display of results 

 ![avatar]( b6e88e04da9440ada3c6cc72e529f768.png) 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##  1. Overview of the principle 

   This paper presents a simple and fast operator, the "hidden" point removal operator, which determines the visible point in a point cloud from a given viewpoint. Visibility is determined without reconstructing the surface or estimating the normal. The results show that extracting the point located on the convex hull of the transformed point cloud is equivalent to determining the visible point. The operator is generic - it can be applied to point clouds in various dimensions, point clouds on point clouds, and viewpoints inside and outside point clouds. The results show that the operator is useful in point cloud visualization, viewpoint-dependent reconstruction, and shadow casting. 

##  2. References 

>  [1] Katz, Sagi, Tal, Ayellet, Basri, & Ronen. (2007). Direct visibility of point sets. Tog. 

##  3. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574432812
  ```  
#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574432812
  ```  
#  III. Display of results 

 ![avatar]( 20201120153918150.png) 



--------------------------------------------------------------------------------

#  Image processing 

##  1. Overview 

   It integrates some basic functions of image processing, such as image flipping, filtering, pyramid, and so on. 

##  2. Main functions 

###  2.1 Image flipping 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957441989
  ```  
   flip_horizontal realize the function of flipping the image horizontally from left to right. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957441989
  ```  
   flip_vertical realize the function of flipping the image vertically from top to bottom. 

###  2.2 Image filtering 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957441989
  ```  
   The source code of the algorithm is C++, and image processing is not done, so it is not studied in depth. 

#  Code implementation 

##  1. Image flipping 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957441989
  ```  
###  1.1 The original image 

 ![avatar]( c2fac0e2417e45e0a0e9039478acb818.png) 

###  1.2 Flip left and right 

 ![avatar]( 8a879169b38b488aae84ceca02b3ecdd.png) 

###  1.3 Flip up and down 

 ![avatar]( 5036f6b187884427a011a573006c5f76.png) 

##  2. Image filtering 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957441989
  ```  
###  2.1 The original image 

 ![avatar]( d180c9f81b8c4c10bc304c8f15bd488f.png) 

###  2.2 Processing results 

 ![avatar]( 8a020cf2a96f4332b64fe607ec683752.png) 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##  1. Implementation process 

 ![avatar]( 572e0c06bcb54451ac192ce6da16e5c5.png) 

 1. Grid diagram 2. Calculate the number of grid rows and columns  

 ![avatar]( 8f2cb9b5bfc24a5384cb05ee7c01f4e4.png) 

   The special symbol in the formula is round up, which is the length of the grid side. 3. Calculate the row and column number where any point is located.  

 4. Calculate the grid number of any point. 

 ![avatar]( bf04de34f1f240cfa2fc1a2806722d3b.png) 

  5. Slope filtering  

    The slope value is the ratio of the elevation difference to the distance between the two points. The slope value of the ground object point is obviously larger than the slope value of the ground point, and the slope value is positively correlated with the elevation difference of the ground point. Therefore, if you find the exact ground point and calculate the slope based on it, you can filter the ground point. In the point cloud data, the slope value of any point in any grid and the lowest point in the grid are calculated and analyzed using the formula (4). The point where the slope and elevation difference are less than a certain threshold is the ground point.  

##  2. References 

>  [1] LI Xiaoli, LIU Rufei, TANG Yubing, Ren Hongwei, Chai Yongning. Three-dimensional automatic modeling method of pavement using high-precision vector data [J]. Bulletin of Surveying and Mapping, 2021 (07): 70-73. [2] LIU Shuo, LIU Rufei, Chai Yongning. A road marking line classification method based on structural feature matching [J]. Geospatial Information, 2021, 19 (03): 14-17 + 6. [3] WANG Fei, LIU Rufei, Ren Hongwei, Chai Yongning. Multi-phase vehicle laser point cloud registration using road target features [J]. Journal of Surveying and Mapping Science and Technology, 2020, 37 (05): 496-502. [4] Ding Shaopeng, Liu Rufei, Cai Yongning, Wang Peng. An adaptive slope filtering method for point clouds considering terrain [J]. Remote Sensing Information, 2019, 34 (04): 108-113. [5] Ma Xinjiang, Liu Rufei, Cai Yongning, Wang Peng. A method for extracting road boundaries from point clouds based on curb features [J]. Remote Sensing Information, 2019, 34 (02): 80-85. [6] Liu Rufei, Wang Peng. Nonuniform compression method for vehicle laser point clouds preserving road surface features [J]. Remote Sensing Information, 2017, 32 (01): 100-103. [7] Liu Rufei, Lu Xiushan, Yue Guowei, Tian Maoyi. An automatic road extraction method from vehicle laser point cloud data [J]. Journal of Wuhan University (Information Science Edition), 2017, 42 (02): 250-256. [8] Liu Rufei, Tian Maoyi, Xu Junyi. Highway road point filtering in vehicle laser scanning data [J]. Journal of Wuhan University (Information Science Edition), 2015, 40 (06): 751-755. [9] Lu Xiushan, Liu Rufei, Tian Maoyi, Liu Bing. Ground filtering of vehicle laser point cloud using improved mathematical morphology [J]. Journal of Wuhan University (Information Science Edition), 2014, 39 (05): 514-519. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957445701
  ```  
#  III. Display of results 

 、

 There is no visual code written in the code, after all, the algorithm is not focused on visualization. 

 ![avatar]( 587746ed4fb2452b8990cbbf8ed168b3.png) 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##   1. Process overview 

 1) Use the point cloud filtering algorithm or point cloud processing software to filter out outliers; 2) Invert the lidar point cloud; 3) Set the simulated fabric, set the mesh resolution of the fabric, and determine the number of simulated particles. The position of the fabric is set above the highest point of the point cloud; 4) Project the fabric simulation point and radar point to the horizontal plane, find the height value of the most adjacent laser point for each fabric simulation point, and set the height value to; 5) The fabric example is set to be movable, and the fabric particles are first affected by gravity. When the particle height is less than that, the particle height is set to; the particle is set to be immovable; 6) Calculate the internal force action between the fabric particles, and adjust the relative position between the fabric particles according to the set fabric rigidity parameters; 7) Repeat 5) and 6) calculations, and the number of iterations reaches the set maximum number of iterations; 8) Calculate the distance between the lidar point and the corresponding fabric simulation point. The distance is less than the threshold value and is marked as the ground point. The distance is greater than the threshold value Marked as a non-ground point. 

>  Introduction to "Cloth" Filtering Algorithm of Point Cloud Ground Point Filter (CSF) 

##   2. Detailed process 

 I'm too lazy to type it by hand, so I'll paste it directly. Let's improve it when uploading the PCL version code!!!! 

 ![avatar]( 1ff89325340b474bb57cf990821d4553.png) 

 ![avatar]( 19c674a57d3241c7944d0472706b8966.png) 

##   3. References 

>  Wang Chuanbo. Research on filtering and compression method based on point cloud data [D]. Heilongjiang University, 2021. 

#  Second, environmental installation 

 ![avatar]( 25824760800c4c01a0e4ab8257b1bb85.png) 

 1. Source code acquisition: https://github.com/jianboqi/CSF 2. Source code compilation. In the python folder, bring up the cmd black box,  

 Enter in the black box: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957448133
  ```  
 Press the Enter key, wait until the run is complete, and then enter: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957448133
  ```  
 Press the Enter key and the run is complete! Since my environment has been successfully installed, no screenshots will be displayed. 

#  III. Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957448133
  ```  
#  IV. Display of results 

 Green are ground points, and red are non-ground points. 

 ![avatar]( 5f147bebee8846aa94874c48fd49a939.png) 

  comparison result  

#  CloudCompare 

   The algorithm is also implemented in CloudCompare software, and the specific operation process is as follows: 

 ![avatar]( 20200906191318615.png) 

 ![avatar]( 20200906191823577.png) 

 ![avatar]( 20200906192140334.png) 

 ![avatar]( 20200906192559437.png) 

 1. Load the point cloud data and click on the CSF Filter function in Plugins 2. The following window pops up: In the figure: Cloth resolution: refers to the mesh size of the cloth used to cover the terrain (in the same units as the point cloud). The larger the cloth resolution you set, the rougher the DTM you get; Max iterations: refers to the maximum number of iterations of the terrain simulation. 500 is enough for most scenarios. Classification threshold: refers to the threshold that divides the point cloud into ground and non-ground parts based on the distance between the point and the simulated terrain. 0.5 is suitable for most scenes. The minimum mesh resolution and distance threshold here can only be set to 10cm. The range of 10cm on the ground is the ground point by default, and the precision is not as high as in your own code implementation. 3. The final result: It can be seen that the curbs cannot be extracted from non-ground points. 



--------------------------------------------------------------------------------

##  First, the main function 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574491963
  ```  
 select_by_index () in Open3D uses a binary mask to output only selected or unselected points. 

##  Code example 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574491963
  ```  


--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

 ![avatar]( 20210307124845583.png) 

   Internal Shape Descriptor (ISS) is a method to represent solid geometry. The algorithm contains rich geometric feature information and can complete high-quality point cloud registration. Set a point in the point cloud, and the specific process of extracting key points is as follows: 1. Establish a local coordinate system for each point in the point cloud and set a search radius for all points;  

 2. Determine that each point in the point cloud is centered and is all points within the radius area, and calculate the weights of these points, the expression of which is: 3. Calculate the covariance matrix for each point: 4. Calculate the eigenvalues {} of the covariance matrix for each point and arrange them in order from largest to smallest; 5. Select the key points according to the following rules. The significance feature is the smallest eigenvalue: The value of usually does not exceed 1. The basic principle is to avoid detecting key points at points where similar diffusion occurs along the main direction. Since a repeatable standard reference frame cannot be established, it is difficult for the subsequent description stage to produce an effect. In the remaining points, the significance depends on the size of the smallest eigenvalue. Non-maximum suppression () is performed on the significant features within the set radius, and the points with large changes in the main direction are reserved as key points. 

 References 

>  [1] Zhong Y. Intrinsic shape signatures: A shape descriptor for 3D object recognition [C]//IEEE International Conference on Computer Vision Workshops. IEEE, 2010. [2] Li Renzhong, Yang Man, Tian Yu, Liu Yangyang, Zhang Yanluan. Point cloud registration algorithm based on ISS feature points combined with improved ICP [J]. Advances in Laser and Optoelectronics, 2017, 54 (11): 312-319. [3] Ge Baozhen, Zhou Tianyu, Chen Lei, Tian Qingguo. Point cloud splicing method based on improved ISS feature points and artificial bee colony algorithm [J]. Journal of Tianjin University (Natural Science and Engineering Technology Edition), 2016, 49 (12): 1296-1302. [4] Li Yuxiang, Guo Jiming, Pan Shangyi, Lu Lili, Lu Zhuxing, Zhang Di. A point cloud registration algorithm based on IS-SHOT features [J]. Bulletin of Surveying and Mapping, 2020 (04): 21-26. 

#  Second, the main function 

 1, o3d.geometry.keypoint.compute_iss_keypoints function realizes the extraction of ISS key points 2, custom function: keypoints_to_spheres realizes the visualization of key points 

#  III. Complete code 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574420587
  ```  
#  IV. Display of results 

 ![avatar]( 20201202090629496.png) 

#  Visualization contains mesh 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574420587
  ```  
 ![avatar]( 20201202223831700.png) 

#  VI. Related Links 

 [1] 基于ISS方法得到点云的特征点（Python代码） 



--------------------------------------------------------------------------------

#  I. Overview 

   The previous article python - KITTI dataset .bin to .pcd/.txt and visualization has carried out a brief code implementation for Open3D to read .bin files. This article gives another implementation method and batch conversion method for reading .bin files using Open3D. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574437668
  ```  
#  III. Display of results 

 ![avatar]( 816bb22301b54b0b983a8f0c7e34a78b.png) 

#  IV. Batch conversion 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574437668
  ```  


--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##  1. Algorithm overview 

   The kmeans clustering algorithm is also known as the mean clustering algorithm. It is relatively mature in clustering algorithms, characterized by simplicity and classics, and takes distance as the entry point. The k-means clustering algorithm belongs to the cluster analysis algorithm, and its operation method is mainly iterative solution. Specifically, the algorithm uses distance as the evaluation parameter benchmark of similarity, that is, it considers that the distance between two targets is proportional to the similarity. This algorithm regards the cluster as a part of multiple distance objects, so compact and independent clusters can be used as the final research goal. 

##  2. The implementation process 

 The implementation steps of the kmeans clustering algorithm are as follows: (1) The premise of the operation is to specify the value k as the limit of the final number of clusters; (2) k clustering centers need to be randomly selected from all data sets; (3) When the clustering center is determined, whenever a sample is assigned to the clustering center, the clustering center will perform a new round of operations according to the existing allocated object data, calculate the distance between each object and the k clustering centers and obtain the data. Each object is close to which cluster center, and is divided into the set to which the cluster center belongs; (4) After all the data is grouped into sets, there are k sets in total. Then recalculate the cluster center of each set; (5) When the distance between the final calculated cluster center and the original randomly selected cluster center is less than the original set threshold, it means that the cluster center obtained by the system recalculation is very close to the initial cluster center, and the data system is relatively stable or converges to meet the desired effect. At this time, the algorithm terminates operation, and the final result error obtained by this operation process is relatively minimal; (6) If the distance between the newly calculated cluster center and the initial cluster center exceeds the original set threshold, then (3)~ (5) iterate. 

##  3. Algorithm characteristics 

   The advantages and disadvantages of the kmeans algorithm are as follows: (1) The principle is relatively simple, the implementation is also very easy, and the convergence speed is fast; (2) When the result cluster is dense, and the difference between clusters is obvious, its effect is better; (3) The main parameter that needs to be tuned is only the number of clusters k. The disadvantages are: (1) the k value needs to be given in advance, and in many cases the estimation of the k value is very difficult; (2) the kmeans algorithm can keenly detect the subtle differences between the centroid points initially selected by the system. When there are differences between random seed points, the clustering results obtained by the operation will also vary, which has a great impact on the results; (3) it is sensitive to noise and outlier comparison, so it can be used to detect outliers; (4) using an iterative method, it may only be possible to obtain a local optimal solution, but not a global optimal solution. 

##  4. References 

>  [1] He Han. Research on 3D point cloud semantic segmentation technology [D]. University of Electronic Science and Technology of China, 2020.p27-28 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574458552
  ```  
#  III. Display of results 

 ![avatar]( 20210613195927800.png) 

#  IV. Reference link 

 [1] K-means 方法实现3D点云的聚类算法 [2] 点云学习【3.1】k-means聚类算法 [3] 调用机器学习的库实现 

#  V. Save the classification results 

 Python - point cloud Kmean clustering and save the clustering results 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

 This paper implements the least squares fitting plane based on principal component analysis.

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574417142
  ```  
#  III. Display of results 

##  1. Point cloud 

 ![avatar]( 29b5c2a2deb04b89b0b656ad9e2bd3c7.png) 

##  2. Fitting results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574417142
  ```  
 ![avatar]( 959dd463b8e2480e9938ae7309234a0f.png) 



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##  1. Fitting the ball 

 ![avatar]( 0d275637d6de4a9ab313376b3b642745.png) 

   The spherical equation can be expressed as: in the formula, the coordinates of the target point; the spherical center coordinates; the radius of the sphere. As shown in Figure 1, the radius and spherical center coordinates are regarded as unknown parameters, and the square sum of the distance from the point to the fitted spherical surface is the minimum criterion. After linearizing the spherical equation, the spherical center coordinates are solved according to the least squares principle.  

##  2. References 

>  Li Zongchun, Lu Zhiyong, Guo Yinggang, Zhang Guanyu, He Hua, Feng Qiqiang, Chen Shaoqing, Wang Junwei. Antenna rotation center measurement method based on pitch axis intersection and ball fitting [J]. Journal of Wuhan University (Information Science Edition), 2019, 44 (10): 1449-1456. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574455004
  ```  
#  III. Display of results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574455004
  ```  
 ![avatar]( 82c27964e44641c5abab68367b40ad33.png) 



--------------------------------------------------------------------------------

#  Overview of the principle 

##  1. Space straight line 

 ![avatar]( 92b36424e61e4bce8fadcf0aaffb88ed.png) 

##  2. Least square fitting 

 ![avatar]( 1e110ed91f814e818784ca79171e701f.png) 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574455969
  ```  
#  III. Display of results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574455969
  ```  
 ![avatar]( fc654964a1b7442caef4aa28cf24c068.png) 

#  IV. Reference link 

 [1] PCL 最小二乘拟合空间直线 [2] 3D Line Fitting in 5 Easy Steps with SVD 

#  Test data 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574455969
  ```  


--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

   See: Open3D Least Squares Fitting 2D Circles (Python Detailed Procedure Edition) 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574455311
  ```  
#  III. Display of results 

 ![avatar]( 9ad5f396688049599720108a9647b9e3.png) 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##  1. Overview 

   The principle of the least squares method is to determine the best function match for a set of data based on minimizing the sum of squares of errors. The principle of its specific fitting circle is as follows. Assuming that the circle equation is known: Equation (1) can be written as: Rewrite equation (2) into the form of the right equal to 0, and convert the formula: Therefore, the values of the three parameters of the above binary quadratic equation can be determined, so as to calculate the radius of the fitting circle and give the coordinates of the center of the circle. The distance from the point in the sample set to the center of the circle: In order to obtain the most accurate fitting of the actual parameters of the circle, use the distance from the sample point to the center of the circle to square the difference with the radius, and find the value that minimizes the sum of squares, that is, the final solution, so as to determine the parameters of the circle and draw the circle. 

##  2. References 

>  Cheng Yabin, Zhang Hongwei, Guo Zilu. Research on riveting hole detection technology of mine car carriage based on least square fitting circle [J]. Coal Mine Machinery, 2021, 42 (12): 168-171. DOI: 10.13436/j.mkjx.202112055. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574413050
  ```  
#  III. Display of results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574413050
  ```  
 ![avatar]( 874808d9696c4931979493a493fb95e0.png) 

#  IV. Test data 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574413050
  ```  


--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

   The polynomial curve is expressed as: the polynomial coefficient is:, and the linear least squares can solve the coefficient. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574449442
  ```  
#  III. Display of results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574449442
  ```  
 ![avatar]( b97218e8f3e74b9aa263fafde92113c0.png) 



--------------------------------------------------------------------------------

#  First, the code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574413232
  ```  
#  III. Display of results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574413232
  ```  
 ![avatar]( e4772f4ba4534057826272b6ca7d2863.png) 

#  IV. Test data 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574413232
  ```  


--------------------------------------------------------------------------------

#  I. Overview 

   The VisualizerWithEditing class in Open3d provides graphical user interaction. The draw_geometries_with_editing ([pcd]) function provides vertex selection and clipping. 

#  1. Main function 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574482758
  ```  
#  2. Basic operation 

 ![avatar]( 374b59dd757247568742e1d95f60c65c.png) 

   After the geometry is displayed, pressing Y twice aligns the geometry with the negative half axis of the Y axis, and pressing X or Z twice aligns the X or Z axis. After adjusting the viewing angle, press K to lock the view and switch to selection mode.  

>  Tip: In the actual operation of the selected area, the orthographic projection model is generally used to align the geometry with any axis. This technique avoids the problem of occlusion due to the perspective projection strip, making the selection easier. 

 ![avatar]( bfa99e99bd3a4fa89febb4fc2b7b2322.png) 

   When selecting an area, you can drag with the mouse (rectangular area) or ctrl + left mouse button click (select polygon area). Mouse drag box selection  

 ![avatar]( 4a0d7877e6da454fa18fada0c3d63f92.png) 

 Polygon region selection  

 ![avatar]( d5a18673692d45c89a971b6d9db6fd5b.png) 

   The selected area is dark shaded. If you want to save the selected area and discard the rest, press C. A dialog box will pop up to select the file path to save the crop. The result of the crop is saved after it is displayed.  

>  In practice, only saving in .ply format is supported. 

 ![avatar]( d8b38dbb0c094498ad323c3690e19498.png) 

 ![avatar]( 4cee860cde854c90855e13fed0cbafcf.png) 

   Press F to end selection mode and enter free browsing mode.  

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574482758
  ```  
#  III. Display of results 

 ![avatar]( 4c5d5eceaa9f4bb6a66abba239c99a6e.gif) 

#  IV. Relevant links 

 [1] Open3D 裁剪点云 [2] Open3D 裁剪任意指定区域的点 [3] Open3D 获取指定立方体区域的点 (python详细过程版) [4] Open3D 可视化(6) ——交互式可视化 



--------------------------------------------------------------------------------

#  First, XYZ coordinate data merging 

   Merge XYZ coordinate data in two point clouds. 

##  1. Main function 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 20240203095744850
  ```  
 Complete the splicing of multiple arrays at once. Where a1, a2,... are the parameters of the array type. Axis = 0: represents splicing by column, the default value is: axis = 0. Therefore, if the axis parameter is not written, the default is splicing by column. Axis = 1: represents splicing by row. 

##  2. Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 20240203095744850
  ```  
##  3. Display of results 

 ![avatar]( 26e6c95d012140e1a2ce46bc17a0d503.png) 

##  4. Reference link 

 [1] numpy.concatenate()函数 [2] Open3D 使用numpy 

#  Merge all fields 

 PointCloud has a handy operator + that merges two point clouds into one. 

##  1. Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 20240203095744850
  ```  
##  2. Results display 

 ![avatar]( af7852e5925d4f99b6849f078586aca0.png) 



--------------------------------------------------------------------------------

