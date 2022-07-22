aloam 에서 벨로다인과 키티데이터셋 에서 변경해줘야 할것있음!


scanRegistration.cpp 파일의 215번째줄에서 에러가 나는데 이는 KITTI dataset은 64line이고, 우리실험실의 velodyne은 16line이여서 위의 if 문에서 64,16을 상황에 맞게 변형시켜줘야함