# Node
- 로봇을 구성하는 센서들을 판단하고 동작하는 시스템
- TOPIC, SERVICE, ACTION, PARAMETER를 통해 데이터 주고 받을 수 있음

# 로봇의 인식
- 로봇이 사물을 인식할 때 일어나는 일련의 과정들에서 노드간의 데이터를 주고 받는 구조 형성

# Node 실행
- $ ros2 run --
![image](https://user-images.githubusercontent.com/88695655/180922309-abd54a7c-c43d-4285-9b4d-03f7d822342f.png)
- gazebo  실행시 ros graph를 통한 노드의 데이터 구조 모습 확인
- 노드간의 화살표가 존재해야 데이터 전송되고 있는 것 (debug 할 때 사용)
 
# 문법
- generate_launch_discription : ros2 launch 커멘드를 통해 launch file을 실행시키면, 이 이름을 가진 함수를 찾아들어갑니다. 그래서 모든 launch file에는 빠지지 않고 제일 먼   저 등장하는 함수
- LaunchDiscription :이 부분에서는 말 그대로, 어떤 Node들을 실행시킬지 기술해둔 Description을 작성. 다만 특정한 규칙으로 실행시킨 Node에 대한 옵션을 지정해주어야 하며,
  여러 Node들의 실행이 필요할 수 있기에, 기본적으로 list의 구조를 가짐을 파악 가능
- ExecuteProcess : 프로세스 하나를 실행시킨다는 구분의 개념
 - cmd : 앞에서 살펴본 바와 같이 터미널에서 입력하는 커멘드를 그대로 실행하고자 할 시에 사용.  입력은 list 형태로 주어지며, space를 기점으로 나누어 주기.
 - output : Error log 등의 output이 출력되는 수단을 입력.

# Node 방식
- 각각의 터미널에서 실행되는 launch files들을 하나의 terminal에서 실행 가능
 - $ cd ~/gcamp_ros2_ws/src/gcamp_ros2_basic/gcamp_gazebo/launch
   $ touch second_launch.launch.py
   $ gedit second_launch.launch.py
   $ cd ~/gcamp_ros2_ws
   $ cbp gcamp_gazebo
   $ ros2 launch gcamp_gazebo second_launch.launch.py
   
# 문법
- Node : Node 하나를 실행시킬  수 있는 옵션.
 - package : 실행시킬 Node가 포함된 package를 선택. 
 - executable : c++ Node의 경우, colcon build를 하면 실행 가능한 프로그램이 생성. python의 경우도 추가 작업이 필요하여, 우선 지금은 기존 커멘드의 마지막 인자.
 - parameters : 실행시킬 Node의 추가 매개변수가 있다면 여기 추가됨.
 
 # 환경 변수, 제어변수
 - https://github.com/rnanosaur/nanosaur_robot/blob/6aaf41d00c2f95d393d942d22e35c0a3c60fdf66/nanosaur_camera/param/camera.yml 
 - param 폴더 : parameter 게시

# ExecuteProcess , Node
- 둘 다 필요한 경우 있으므로 source에서 무엇을 의미하는지 정도 알아
