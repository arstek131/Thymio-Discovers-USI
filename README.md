# Thymio-Discover-USI
Final project for Robotics course @ USI 21/22.

**Final Score:** 85,50/100

Final report can be found [here](https://github.com/arstek131/Thymio-Discover-USI/blob/main/Ali_Robotics_Project.pdf)

## Details

The main idea is to reproduce an environment as much as similar as [USI](https://www.usi.ch/it) west and east campus in a simulated world, where the Thymio navigate through it without crashing and in the meanwhile recognize objects using a real time object detection algorithm

## Usage

This project requires [Pytorch](https://pytorch.org/).
In order to run it follow these steps in a terminal:

```sh
unzip thymio_discover_USI.zip
cd thymio_discover_USI
pip install -r requirements.txt
```

Move to CoppeliaSim folder and launch it
```sh
./coppeliaSim.sh
```

In CoppeliaSim load the scene:
- File>Open Scene...>thymio_discover_USI>main_scene.ttt

And start the simulation in real time mode.
Meanwhile in another terminal launch the ROS-Thymio bridge
```sh
ros2 launch thymioid main.launch device:="tcp:host=localhost;port=33333" simulation:=True name:=thymio0
```

And finally launch the node
```sh
cd thymio_discover_USI/scripts
python3 thymio_random.py
```
