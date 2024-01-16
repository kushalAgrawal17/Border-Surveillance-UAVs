Project Title: Intrusion Detection for Border Surveillance using Swarm Robotics
Submitted by -  Kushal Agrawal (2020CSB1096)
		Inayat Kaur (2020CSB1088)
		Pooja Goyal (2020CSB1108)

The code consists of the following classes:

Simulator - It controls the whole simulation process by calling the appropriate methods.
Basestation - It performs the tasks associated with base station like receiving data, flying a new drone, broadcasting priorities.
Environment - It performs detection of suspicious activities at various locations and drains battery of drones.
Trainer - handels the training aspect of the simulation. Interacts with DQNAgent for reinforcement learning, receive data from the environment and base station, and train drones to make informed decisions.
Drone - represents individual UAVs in the simulation. Each drone was equipped with Q-learning for algorithm decision-making, information about cell priorities, current position, last communication time, and battery levels. The drone class interacted with the environment, make decisions on movement.

For running any Algorithm the simulator is given the following parameters--
1. simulation time
2. warm-up time
3. number of UAVs
4. grid size

For runing DQN run all the cells as it is.
For running Hill Climbing Algorithm give warm-up time = 0 to simulator, and change the operate_drones function in Simulator class by commenting decide_and_move function call and uncommenting decide_and_move_hill_climbing.