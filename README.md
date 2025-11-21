# UTS-Lokalisasi-dan-Pemetaan
Ratna Dwi Lestari
4222201029


# Turtlebo4 Navigation dari Point A ke Point B
Project ini merupakan tugas ATS mata kuliah Lokalisasi dan Pemetaan RE702, tujuannya adalah menjalankan turtlebot bergerak ke titik A, menyalakan buzzer satu kali, kemudian robot berjalan menuju titik B dan menyalakan buzzer dua kali.

# CARA KERJA
## Buat Folder Workspace
```bash
mkdir -p Winner/src
cd Winner/src
```
## Instal package dan dependencies
```bash
cd ../ && rosdep install --from-paths src --ignore-src -r -y
```

## Build Package
```bash
colcon build
```

## Sambungkan pc dan turtlebot (Via Ethernet)
```bash
ssh ubuntu@192.168.185.3
```

## Melakukan Mapping
```bash
ros2 launch turtlebot4_navigation slam.launch.py
ros2 launch turtlebot4_viz view_robot.launch.py
```

# Menjalankan Nav2
## Menjalankan Lokalization
```bash
source install/setup.bash
ros2 launch winner1 localization.launch.py
```

## Menjalankan Navigation
```bash
source install/setup.bash
ros2 launch winner1 uts_nav.launch.py
```

## Menjalankan Rvis
```bash
ros2 launch turtlebot4_viz view_robot.launch.py
```

## Menjalankan program goal point ke point
```bash
source install/setup.bash
ros2 run winner1 winner1
```
