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

