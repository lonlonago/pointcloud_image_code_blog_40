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

