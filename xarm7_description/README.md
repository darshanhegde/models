# xARM Meshes 

All mesh files were converted from original versions in xARM ROS package, which is avaialabel at:

* https://github.com/xArm-Developer/xarm_ros/tree/master/xarm_description/meshes/xarm7/visual
* https://github.com/xArm-Developer/xarm_ros/tree/master/xarm_gripper/meshes


The licence for all these are BSD 3-Clause "Revised". Please see [`LICENSE`](./LICENCE) for more information.

The conversion from `STL` to `.obj` and `.mtl` used open3D with the following sample code:
```
import open3d as o3d
import glob

for stl_file in glob.glob("*.STL"):
  mesh = o3d.io.read_triangle_mesh(stl_file)
  o3d.io.write_triangle_mesh(stl_file.replace(".STL", ".obj"), mesh)


```


