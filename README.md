## Project description
This project implements an end-to-end pipeline for zero-shot 3D object segmentation and extraction from RGB-D data. It combines Segment Anything Model (SAM) for class-agnostic 2D mask generation with CLIP for language-guided semantic matching, enabling the system to extract precise 3D point clouds from arbitrary natural language prompts. By linking open-vocabulary text understanding with spatial perception, the framework bridges high-level semantic concepts and low-level geometric information for object-centric scene understanding in unstructured 3D environments.

The algorithm is implemented on ROS.
## Environment preparation:
Follow the install instructions of [Segment Anything](https://github.com/facebookresearch/segment-anything) and [CLIP](https://github.com/openai/CLIP)

build the ROS package.

Package based on Tiago robot from Pal. Change the corresponding camera topic etc. before using.

RUN
```
rosrun sam_fp samros.py “beer”
rosrun sam_fp pcd_processing_node
```
where "beer" is the item that you want the CLIP to choose. If no args input, it will segment all the items.
