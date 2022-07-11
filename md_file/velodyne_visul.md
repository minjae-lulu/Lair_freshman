참고 주소
- https://youtu.be/QtChxWFEVlk
-http://wiki.ros.org/velodyne/Tutorials/Getting%20Started%20with%20the%20Velodyne%20VLP16
-http://www.lumisol.co.kr/sub/reference/lidar.asp?mode=view&bid=4&s_type=&s_keyword=&s_cate=&idx=212&page=1
0. pconfig 써야하는데 없으면 (sudo apt-get install net-tools) 로 설치해준다
1.
sudo apt-get install ros-melodic-velodyne -> 멜로딕, 키네틱, 등등 상황에 맞게해야함
2. mkdir로 폴더 catkin_ws/src 만들어주고, src에서 git clone https://github.com/ros-drivers/velodyne.git 으로 다운해준다.
3. 그후 src가 아닌 catkin_ws 에서 빌드해준다 (명령어는 catkin_make)
4. 그후 이더넷과 로컬 랜선 해제하고 벨로다인이랑 로컬이랑 랜선으로 연결해준다.
5. sudo ifconfig enp5s0 192.168.1.201 (를 입력한다. enp5s0은 라이더마다 가진 고유의 이름으로 랜선 연결후 sudo ipconfig로 이름을 확인할수 있다.)(이작업은 벨로다인과, 로컬이 잘 연결되었나 확인하는 것이다)
(연결확인전에 로컬에서 통신위한 ip를 설정해줘야 하는데, 네트워크 설정 들어가서 ipv4들어가고 수동으로 설정해서 입력할수 있게한다. 주소 192.168.1 까지는 동일하게 그뒤는 동일하지 않게 해준다. 네트마스크는 255.255.255.0 로 게이트웨이는 0.0.0.0으로 해준다 이유는 모름 ㅋ )
하지만 그냥 브라우져 열어서 192.168.1.201을 입력하면 연결이 되었으면,
이런 화면이 뜨고, 값들 변경할수 있다 (시간날때 변경 해보셈)
6. 그후 새로운 터미널을 열고 catkin_ws/src에 들어가 loslaunch를 한다
- roslaunch velodyne_pointcloud VLP16_points.launch (띄워쓰기 주의 points.launch임)
7. 새터미널을 띄워서 rosrun rviz rviz -f velodyne 명령어를 입력하는데 안되면 (만약 안될경우 다른 터미널 열어서 roscore 또는 roslaunch 실 해준다음 명령어 치면 된다 (이는 roslaunch랑 차이가 있는데행 코어 프로세스 뭐시기 뭐시기 때 문이라고 한다 나중에 공부하고 이해해보자))
7. 새터미널에서 (rosrun rviz rviz -f velodyne) 를 통해 시각화하는 gui를 열고 관찰한다

