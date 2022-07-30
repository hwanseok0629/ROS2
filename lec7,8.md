# ROS2 TOPIC
- 정의 : 여러 노드들 사이에 데이터가 오고가는 길
- pulisher(보내는 주체) <-> subscriber(받는 주체) : 노드 안에 존재
- 1 대 다수의 통신이 가능 
![image](https://user-images.githubusercontent.com/88695655/181877255-978d3d5d-f9d1-4e96-98f1-7f7d48c76a91.png)

# TOPIC MESSAGE
- 로봇 프로그래밍시 다양한 센서 데이터들이 다뤄진다
- 센서뿐 아니라 제어 데이터들도 주고받음

# TOPIC COMMAND
- 실행중인 topic의 리스트를 알고 싶을 때 : $ ros2 topic list
- 특정 topic의 정보를 알고 싶을 때 : $ ros2 topic info /skidbot(특정)/cmd_vel
- 특정 message를 알고자 할 때 : $ ros2 interface show geometry_msgs/msg/Twist (구글링을 통해서 하지 않아도 됨)
- 커맨드를 publish한 후 echo를 사용하여 잘 실행 되는지 확인 : $ ros2 topic echo /skidbot/cmd_vel
- rpt_graph를 통해 노드의 데이터가 잘 전달되는지 확인 ( 확인 안될 때 새로고침해보기 )
- 
