# 사소한 지식들



1. scan line수 변경

aloam 에서 벨로다인과 키티데이터셋 에서 변경해줘야 할것있음!(레고 로암등등도 마찬가지이며, include에 유틸리티에서 16 32 64등 변경가능)


scanRegistration.cpp 파일의 215번째줄에서 에러가 나는데 이는 KITTI dataset은 64line이고, 우리실험실의 velodyne은 16line이여서 위의 if 문에서 64,16을 상황에 맞게 변형시켜줘야함


2. 실시간 vs 저장된 데이터셋 시간 설정

런치파일을 보면 **param name="/use_sim_time" value="false"** 이 있는데 이는 실시간 데이터로 할것인지, 저장된 데이터셋의 시간을 따를것인지를 설정하는 것이다. value값이 false이면 실시간으로 측정하겠다는 의미, true이면 데이터셋 저장된것을 불러서 사용하겠다는 의미이다. 



3. 데이터셋 경로설정 봐줘야 한다. segdata같은 경우는 segmentation_ros.cpp의 9번째 줄에 있다.