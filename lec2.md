# Ubuntu 20.04 설치
- ubuntu desktop 과 ubuntu server로 나뉘어져있다.
- 다른 작업과 하기에는 ubuntu desktop이 더 편리하다.
- Virtual Box 이용하여 실행
- Ubuntu 내의 네트워크 설정 및 추가 설정 필요 

# Ubuntu 내의 환경 설정
- 한글로 실행하는 경우 오류가 있음 ( 영어로 실행 )
- 시스템에서 프로세서 수 2개 이상으로 설정
- windows 와 virtualbox를 연결하기 위해 게스트 모드 cd삽입

# alias
- 축약어로 긴 리눅스의 명령어의 앞글자를 따서 사용
- source /opt/ros/foxy/setup.bash && source ~/gcamp_ros2_ws/install/local_setup.bash를 rosfoxy로 축약

- terminal 키고 바로 rosfoxy 입력
- cd ~/gcamp_ros2_ws/src로 workspace 들어가기
- alias eb='gedit ~/.bashrc'
- alias sb='source ~/.bashrc'
- alias cba='colcon build --symlink-install'
- alias cbp='colcon build --symlink-install --packages-select'
- alias killg='killall -9 gzserver && killall -9 gzclient && killall -9 rosmaster'
- alias rosfoxy='source /opt/ros/foxy/setup.bash && source ~/gcamp_ros2_ws/install/local_setup.bash'
- source /usr/share/colcon_cd/function/colcon_cd.sh
- export _colcon_cd_root=~/gcamp_ros2_ws
