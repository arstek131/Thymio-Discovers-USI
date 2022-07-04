# Thymio-Discover-USI
Final project for Robotics course @ USI 21/22.

## Usage

This project requires [Pytorch](https://pytorch.org/) to run.
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
