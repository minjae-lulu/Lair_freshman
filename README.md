# How to install ros

[참고 링크](http://wiki.ros.org/melodic/Installation/Ubuntu) <- 우분투에 ros melodic 설치방법

1. sources.list 설정

`sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'`

<br/><br/>

2. keys 설정

`sudo apt install curl # if you haven't already installed curl
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -`

<br/><br/>

3. 설치전 apt 업데이트

`sudo apt update`

<br/><br/>

4. Desktop full 설치 (권장) -> ROS, rqt,rviz,robot-generic libraries, 2D/3D simulators and 2D/3D perception

`sudo apt install ros-melodic-desktop-full`

<br/><br/>

5. 환경 세팅
  * 로스 환경변수 자동 추가해주는 세팅 (새로운 쉘 실행될때마다)
  
  `echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
  source ~/.bashrc`
  
  * 현재쉘에서 환경변수 수정 원하면 
  
  `source /opt/ros/melodic/setup.bash`
  
  * bash 대신 zsh사용하기 원하면
  
  `echo "source /opt/ros/melodic/setup.zsh" >> ~/.zshrc
   source ~/.zshrc`
   
<br/><br/>
   
 6. 패키지 빌딩을 위한 의존성
   * too 또는 다른 로스패키지 빌딩 dependencies 설치하려면
   
   `sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential`
   
   * ROS사용전 초기화 해줘야함
   
   `sudo apt install python-rosdep`
   
   `sudo rosdep init
   rosdep update`
   
