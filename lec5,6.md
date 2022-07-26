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
- generate_launch_discription : ros2 launch 커멘드를 통해 launch file을 실행시키면, 이 이름을 가진 함수를 찾아들어갑니다. 그래서 모든 launch file에는 빠지지 않고 제일 먼저   등장하는 함수입니다.
- LaunchDiscription :이 부분에서는 말 그대로, 어떤 Node들을 실행시킬지 기술해둔 Description을 작성합니다. 다만 특정한 규칙으로 실행시킨 Node에 대한 옵션을 지정해주어야 하며,   여러 Node들의 실행이 필요할 수 있기에, 기본적으로 list의 구조를 가짐을 파악할 수 있습니다.
- ExecuteProcess : 프로세스 하나를 실행시킨다는 구분의 개념으로 생각하시면 좋습니다.
 - cmd : 앞에서 살펴본 바와 같이 터미널에서 입력하는 커멘드를 그대로 실행하고자 할 시에 사용 됩니다.  입력은 list 형태로 주어지며, space를 기점으로 나누어 주면 됩니다.
 - output : Error log 등의 output이 출력되는 수단을 입력합니다.
