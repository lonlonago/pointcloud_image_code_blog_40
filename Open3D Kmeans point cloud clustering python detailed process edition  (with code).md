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

