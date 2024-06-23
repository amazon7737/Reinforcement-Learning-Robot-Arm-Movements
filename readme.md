## Unity Ml-Agent를 활용한 강화학습으로 팔동작에 대한 학습
> 로봇 팔은 정밀한 작업 수행과 위험환 환경에서의 작업 대체 등에서 광범위하게 활용되고 있습니다. 기존의 로봇 팔 조작 방식은 고정된 위치 값을 사용하여 목표물을 잡고 이동시키고 목적지에 놓는 동작을 개별적으로 스크립트화해야 하였지만, 유연성과 적응력이 부족하였습니다. 강화학습을 활용하여 로봇 팔이 인간의 동작을 유사하게 목표물과 목적지의 위치를 변경할 수 있도록 하고, 이동 동작의 다양성을 가질 수 있도록 합니다.

### Unity Robotics Hub
* [Unity Robotics Hub](https://github.com/Unity-Technologies/Unity-Robotics-Hub)

### 로봇 팔 모델
* Nityo One


### 동작 예시


#### A동작
![A동작](https://github.com/amazon7737/Reinforcement-Learning-Robot-Arm-Movements/blob/main/A%EB%8F%99%EC%9E%911.gif)

#### 위치가 바뀐 동작
![A동작2](https://github.com/amazon7737/Reinforcement-Learning-Robot-Arm-Movements/blob/main/A%EB%8F%99%EC%9E%912.gif)

#### B동작
![B동작](https://github.com/amazon7737/Reinforcement-Learning-Robot-Arm-Movements/blob/main/B%EB%8F%99%EC%9E%91.gif)

#### Ros Server Logging

![image](https://github.com/amazon7737/Reinforcement-Learning-Robot-Arm-Movements/assets/76634341/64b3662b-66a6-4bdf-81c3-e794948bae9d)


### 구현 내용
* Mesh Collider , Rigid Body 에서 중력, 물리적인 효과를 추가하였고, 로봇 팔에 대한 목적지에 다양성을 주기위해서 랜덤으로 위치를 변경하며 학습시켰습니다.
* 약 2,000번의 학습을 진행하였습니다. 매 보상마다 성공시 +2가 주어집니다.
* 그립에 대한 한계로 목표물 객체에 대한 다양성을 주지는 못하였지만, 목표물의 위치값이 변동되어도 Gripping이 가능합니다.
