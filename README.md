# REU_wrapup


## This repository contains files, links, and information about the following:

1. Additional datasets and LaneNet training for right and left turns at intersections
2. Updates to Owen Ma's v-e2e-rl-ad repository
3. 3D Modeling with RoadRunner and the CARLA version of Unreal Engine

## LaneNet Training for Intersections

## Updates to v-e2e-rl-ad

## 3D Modeling with RoadRunner and CARLA Unreal Engine
The Minicity 3D models I have created are located here in this repo:
1. RoadRunner model: one folder for the .fbx, .xodr, .geojson, and .xml files, and one folder for the textures. Place all individual files in one folder if importing to CARLA.
2. Unreal Engine model:

A guide for creating custom maps for CARLA simulator is located [here](https://docs.google.com/document/d/1nGkW9r-JUrX9DzVkiATIxvYBm__sEEYetNbHLP2ewoU/edit#heading=h.j5jq9pdnhxqd), including information and instructions about exporting 3D models from RoadRunner and importing to CARLA.

### Custom Map Creation and Import/Export Guide
This guide contains links and documentation updates for 3D modeling with CARLA and RoadRunner. Although it is possible to import custom maps using a [packaged installation of CARLA](https://carla.readthedocs.io/en/latest/tuto_M_add_map_package/), you must use Docker to do so and it will require 600-700 GB of space to initially build the image. The documentation for importing custom maps using the CARLA source build is [here](https://carla.readthedocs.io/en/latest/tuto_M_add_map_source/), and this guide is intended for the source build version of CARLA.

There is additional documentation [here](https://carla.readthedocs.io/en/0.9.4/how_to_make_a_new_map/) and [here](https://www.mathworks.com/help/roadrunner/ug/export-to-carla.html) for exporting from RoadRunner and importing with the CARLA source build, but some of the instructions are incorrect or unclear. As such, the following guide provides more accurate instructions.

### Start Modeling with RoadRunner
It is recommended to create the road structure in RoadRunner before importing your map into CARLA. CARLA provides better tools for traffic lights, props, foliage, etc. than RoadRunner, so you might want to model the road structure and road markings in RoadRunner and then add additional things once the model is imported into CARLA. Note that you will need a license to use the RoadRunner application, but [WashU should be able to provide it](https://www.mathworks.com/content/dam/mathworks/mathworks-dot-com/images/responsive/supporting/solutions/automated-driving/roadrunner-tutorial/access-roadrunner-cwl.pdf).

### RoadRunner Tips
The documentation is [here](https://www.mathworks.com/help/roadrunner/fundamentals.html) for modeling in RoadRunner. [This guide](https://www.mathworks.com/help/roadrunner/ug/choose-a-roadrunner-tool.html) also contains quick information about how to use the modeling tools. Please note that RoadRunner crashes quite often. This usually happens if you drag or move something too fast or if you connect roads in an unexpected way. It is recommended to save often. Additionally, if you have added road markings (crosswalks, stencils, etc.) on a road section and then connect another road to it, your markings can disappear. After connecting roads, verify that the road markings are as you intend, or go to a previous save file if needed.

### Exporting a Custom Map in RoadRunner
Once you have completed your model in RoadRunner, you can export your model files. Keep in mind that all exported files should be placed in the same folder during the import step.

In RoadRunner, select “File”, then “Export”.

Select “CARLA Filmbox”, and a menu will pop up:



