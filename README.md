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

### *Installing ROS 2 Foxy!* 🌟

*The process is very similar to installing ROS! Following these commands respectively:*

*1. Setting up the sources and adding the keys:*

```
sudo apt install software-properties-common
sudo add-apt-repository universe

sudo apt update && sudo apt install curl -y
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg

echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(. /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null
```

*2. Update & upgrade apt!*

```
sudo apt update

sudo apt upgrade
```

*3. Install ROS 2 packages:*

```
sudo apt install ros-foxy-desktop python3-argcomplete
```

*4. Setup the environments:*

```
source /opt/ros/foxy/setup.bash
```

*Note: Because we downloaded ROS before, we might need to be carefull with setup.bash.* ✨

*5. We can run a program to test our installation~*

*Trying the talker program on ROS 2!* 🎃

![7](https://github.com/le9na/ubuntu-ros-setup/assets/90223879/564f9554-69cb-4937-ba37-c7379fa70b8a)


*That's it!* 💫
