##  metacontrol_move_base_configurations 

This repository contains files autogenerated by the [ROS tooling](https://github.com/ipa320/ros-model/)

Technical Maintainer: [**ipa-nhg**](https://github.com/ipa-nhg/) (**Nadia Hammoudeh Garcia**, **Fraunhofer IPA**) - **nadia.hammoudeh.garcia@ipa.fraunhofer.de**

The repository [metacontrol_models_experiment](https://github.com/rosin-project/rosin-experiments/tree/master/metacontrol_models_experiment) holds the script and the base models used to auto-create the ROS packages of this repository. To re-generate them we strongly recommend the use of the following instructions:

```
cd 
mkdir rosin-experiment
cd rosin-experiment
git clone https://github.com/rosin-project/rosin-experiments/
git clone https://github.com/rosin-project/metacontrol_move_base_configurations
cd rosin-experiments/metacontrol_models_experiment/MoveBaseConfigurations
./create_config_combination_move_base.sh
```
The last command will create a folder that includes a rossystem file for each configuration under `rosin-experiments/metacontrol_models_experiment/src-gen` .

Open the ROS tooling (latest release version from May 20th) , press the ["import common ROS objects" button ](https://github.com/seronet-project/SeRoNet-examples/blob/master/SeRoNet-Tooling-ROS-Mixed-Port/ROS-MixedPort-Examples/ROSMixedPortTutorials_WSsetup.md#ros-workspace-setup) and import the project: rosin-experiments/metacontrol_models_experiment/.

Automatically the ROS deployable artifacts for all your rossystem configuration will be created, that for the current version of the ROS tooling this means a rospackage that includes a launch file.

```
cd rosin-experiments/metacontrol_models_experiment/src-gen
cp f*_v*_r* ../../../metacontrol_move_base_configurations -rf
cd ../../../metacontrol_move_base_configurations
git checkout -b NewConfigs
git commit -am "new auto-genarted rossystem and launch files"
git push origin NewConfigs
```
-> OPEN a PR to https://github.com/rosin-project/metacontrol_move_base_configurations :wink:
