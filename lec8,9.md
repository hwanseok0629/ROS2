# python
- import rclpy
- from rclpy.node import Node
- from geometry_msgs.msg import Twist : ros2에서 python 실행하기 위한 작업
- < 대문자 및 소문자 '. / \' 유의하기 >
- rclpy.spin(cmd_vel_publisher) : spin안에 while문이 있어 알아서 rclpy를 반복적으로 실행시킴
- rclpy.spin_once(cmd_vel_publisher) : 단 한번만 실행시키고 죽음 

# 중요 포인트
- ROS2의 모든 개발은 Class 형태로 개발을 추천하고 있습니다. 
- 더불어 모든 Class는 **Node**를 기본적으로 상속받아야 합니다.
- 이 Node안에 node 동작에 필수적인 기능들이 모두 구현되어 있습니다.
- 상속 : 상속이란, 마치 유산을 상속하듯이 상위 Class가 구현해 둔 것을 추가 개발 없이 동일하게 사용할 수 있다는 것과 더불어, 
상속받은 Class 자신만의 기능을 추가할 수 있다는 뜻입니다.
- super().__init__ ~ : 상위 class 불러오기 ...  ex) super().__init__("cmd_vel_pub_node")

# create_subscription
- LaserScan : 사용할 메세지 타입
- "skidbot/scan" : 데이터를 Subscribe받을 Topic의 이름을 지정
- self.sub_callback : callback 함수 ... *def sub_callback(self, msg): self 변수 말고도 꼭 또 하나의 변수를 받아야함 (msg : 메세지 변수) 
- queue_size : publisher때와 마찬가지로, "대기열의 크기" 

# LaserScan Message
- 실질적으로 Lidar의 데이터를 담고 있는 부분은 ranges이며 ranges는 길이 720의 list로, 다음과 같이 0.25도의 분해능으로 scan된 물체와의 거리를 저장
![image](https://user-images.githubusercontent.com/88695655/182029230-f9bcbbd7-7774-4fee-8d62-37c6b4751d92.png)
- 전방의 물체만 고려했을 때 : 	
  def sub_callback(self, msg):
  print(f'Distance from Front Object : {msg.ranges[360]}')
