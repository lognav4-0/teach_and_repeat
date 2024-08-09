# Teach and Repeat

This package uses the *teach and repeat* technique to teach a certain path while the operator teleoperating the robot and then repeats the path autonomously. See below how you can test the package.

## Dependencies
- Ubuntu;
- [ROS Humble](https://docs.ros.org/en/humble/Installation.html)

## Preparing the package

Create your workspace:
```
mkdir -p ~/colcon_ws/src
```

Access the folder:
```
cd ~/colcon_ws/src
```

Clone this package:
```
git clone https://github.com/jardeldyonisio/teach_and_repeat
```

Compile the package:
```
colcon build
```

## Steps to test

To teach the path use the following command:
```
ros2 run freedom_vehicle teach_path_coords.py
```

To repeat the path using the dot-to-dot method:
```
ros2 run freedom_vehicle repeat_path_coords.py
```

To repeat the path using the Bézier curve-based method:
```
ros2 run freedom_vehicle repeat_bezier_path.py
```

## TODO

- Launch
- Parâmetro para definir o tipo de robô
- Parâmetros de configuração (distância entre rodas e etc)
- Definir se é frame map ou odom (se vai considerar ou não o mapa)
