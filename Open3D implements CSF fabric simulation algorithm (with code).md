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

