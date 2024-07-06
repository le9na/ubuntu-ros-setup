## ✨ *Setting up Ubuntu 20.04, Installing ROS and Installing ROS 2 Foxy!* ✨

### *1. Setting Up Ubuntu 20.04:* 🌟

*Step 1: Installing VirtualBox* ✅

![1](https://github.com/le9na/ubuntu-ros-setup/assets/90223879/5d76b828-1309-439b-92f4-2b0dc02b550b)

*Step 2: Creating a new Virtual Machine, setting up the proper settings, then loading the Ubuntu ISO image!* ✅

![Screenshot_3](https://github.com/le9na/ubuntu-ros-setup/assets/90223879/4a24a9ac-7a12-4bd2-8123-8d810c4f0d1d)

*Step 3: Setting up Ubuntu!* ✅

![Screenshot_1](https://github.com/le9na/ubuntu-ros-setup/assets/90223879/4389d34a-a136-4ede-8bb3-edacd80034b3)

---------------------------------------------------------------------------------------------------------------

### *2. Installing ROS* 🌟

*To install ROS, first open up the terminal, then run these commands respectively:*

*1. Setting up sources.list and keys:*

```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

sudo apt install curl

curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
```


*2. Update apt and Install ROS:*

```
sudo apt update

sudo apt install ros-noetic-desktop-full
```

*3. To run ROS, we must set up the environment every time; using this command:*

```
source /opt/ros/noetic/setup.bash
```

*4. Installing dependencies:*

```
sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential

# to initialize rosdep:
sudo apt install python3-rosdep

sudo rosdep init

rosdep update
```

*5. Testing a ROS program, 'Hello World' talker & listener:*

*first we have to run ROS core:*

![4](https://github.com/le9na/ubuntu-ros-setup/assets/90223879/1905dffa-cc24-4e74-b187-e0febb4e20e2)

*then the talker:*

![5](https://github.com/le9na/ubuntu-ros-setup/assets/90223879/427cc614-f157-4655-b762-af1925f18e9d)

*then the listener:*

![6](https://github.com/le9na/ubuntu-ros-setup/assets/90223879/7aac3e7f-1718-4ecd-b70b-f031ad66073e)

--------------------------------------------------------------------------------------------------------

## *Installing ROS 2 Foxy!* 🌟

