# Introduction
The goal of this project is to achieve a collaboration between UAVs to extinguish fire outbreaks in forests and finding a balance between the number of UAV to be deployed and the on-board hardware communication range per UAV using CNP Protocol.

![image text](https://github.com/akob125/Autonomous-Drones-MAS-CNP/blob/master/Media/SimFast.gif)

# Multi Agent System
A multi-agent system (MAS) is a computerized system composed of multiple interacting intelligent agents. They can solve problems that are difficult or impossible for an individual agent. Intelligence may include methodic, functional, procedural approaches, algorithmic search or reinforcement learning.
Multi-agent systems consist of agents and their environment. Typically, multi-agent systems refer to software agents. However, the agents in a multi-agent system could equally well be robots, humans or human teams. A multi-agent system may contain combined human-agent teams.

# Contract Net Protocol
CNP is a task-sharing protocol in multi-agent systems, consisting of a collection of nodes or software agents that form the `contract net'. Each node on the network can, at different times or for different tasks, be a manager or a contractor.

When a node gets a `composite task' (or for any reason cannot solve the present task) it breaks the problem down into sub-tasks (if possible) and announces the sub-task to the contract net acting as a manager. Bids are then received from potential contractors and the winning contractor(s) are awarded the job(s).

# Logic of the Program:
CNP implements a task assignment which elects a manager in order to allocate tasks to nearest UAV. The manager allocates task to the neighboring UAV’s in the communication range of contractor by making sure that these UAV’s aren’t allocated with any task as of then.
The contractor sends out data about fire outbreaks to UAV’s in communication range. The UAV’s calculate distance from their position to the fire Centre as the proposal to contractor based on Proposal with a relation between number of cells on fire and the distance to reach the center of these fire cells. Based on the best Proposal, the contractor allocates task to the UAV’s until the fire is extinguished. The cells that are completely burned cannot be recovered and the contractor doesn’t assign any task for those cells to any of the UAV’s as these cells cannot be recovered.
The UAV’s that are not in communication range will do a random walk and checks if there is any fire.

# Data exchange between UAV’s:
The UAV’s share their position with the Contractor and all other UAV’s in the communication range. If anyone of them first see the fire, it will share the data with the others in the range. If one of them is lost from the range, it will use the data shared to it until then for executing the task or for coming back to the range. If all the fire in the area is extinguished then they share this data and move to another area in fire or the task will be terminated if no fire is existed in the forest.

# Requirements
The project was built using NetBeans 8.2 - Java setup on a MAC system.