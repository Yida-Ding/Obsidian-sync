# Optimization for drone and drone-truck combined operations: A review of the state of the art and future directions
##  Metadata
- ItemType: journalArticle
- Authors: [[Sung Hoon Chung]]、 [[Bhawesh Sah]]、 [[Jinkun Lee]]
- Publication: [[Computers & Operations Research]]
- Date: 2020-11
- DOI: [10.1016/j.cor.2020.105004](https://doi.org/10.1016/j.cor.2020.105004)
- Collection: [[Survey]]
- PDF Attachments: [ScienceDirect Full Text PDF](zotero://open-pdf/library/items/VAHMNQZN)
- Tags: #Optimization #Unmanned_aerial_vehicle #Drone #Drone-truck_combined_operations #Survey_article #Transportation_planning

👣➿👣

### Overview
- Drone operations (DO): specify the case where only drones are used.
- Drone-truck combined operations (DTCO): 
	- Defined as a system in which a drone and a truck work together as a team to achieve tasks such as delivery/collection of items, reconnaissance, inspection, monitoring, etc.
	- The relatively short travel range and limited capacity issues could be resolved, and the utility of drones can be further enhanced if drones are used with ground vehicles (e.g., trucks) in tandem.
- Comparision of drones and trucks:![[Pasted image 20220915115153.png|1000]]
- Classification of models regarding DTCO: 
	- Traveling salesman problem with drone (TSPD), see, e.g., Agatz and Bouman (2018), Ha et al. (2018), Murray and Chu (2015), Seifried (2019)
	- Vehicle routing problem with drones (VRPD), see, e.g., Wang et al. (2017), Wang and Sheu (2019).
- Problem types of DO and DTCO:
	- A particular problem type, e.g., routing for a set of locations, can be used for multiple application areas, e.g., logistics, security, and entertainment.
	- Problem types: 1) routing for a set of locations, 2) area coverage, 3) search operations, 4) scheduling for DO and DTCO, 5) task assignment, and 6) other problems e.g. path planning
- Features and categories extracted from literature:![[Pasted image 20220915123301.png|1500]]

### DTCO Models
- Schematic representation of the basic component (sortie and operation):![[Pasted image 20220916023219.png|1100]]
- Typical DTCO models:
	- Single-drone-single-truck models
	- FSTSP formulation：Murray and Chu (2015)
	- TSP-D and the concept of operation：Agatz and Bouman (2018)
	- Min-cost TSP-D：Ha et al. (2018)
	- Multiple-drone-single-truck models：PDSTSP (Murray and Chu, 2015), mFSTSP (Murray and Raj, 2019), and MVDRP (Poikonen and Golden, 2020)
	- Multiple-drone-multiple-truck models：multiple drone PDSTSP (Ham, 2018), VRP with drones using service hubs (Wang and Sheu, 2019), and multiple FSTSP (mFSTSP) (Kitjacharoenchai et al., 2019)
	- ... see Page 20 for more variants
- Objective functions:
	- Minimization of the tour completion time or makespan.
	- Minimization of the total cost: maintenance cost, battery price, labor, etc; waiting time; parking fees for trucks, battery capacity of drones, physical or cyber attacks on drones while they are waiting; fixed truck cost and the travel cost of drones and trucks.
	- serving customers within time windows; minimizing the latency in serving the customers; maximizing the expected number of customers served the same day
- Technological issues:
	- Drone specifications such as the flight range, battery life, and carrying capacity limit the operational boundary of DO and DTCO
	- Current DTCO research seeks solutions with such technical limitations as constraints.
	- Research papers published on the DO- and DTCO-based delivery systems do not usually give enough attention to the obstacle avoidance technology because this may need to be addressed more in detail at the application level.
- Synchronization issue for truck and drone:
	- It is not an easy task for both vehicles to arrive at a rendezvous node at the same time.
	- A vehicle must wait for the other vehicle, and this will be a significant cost.
	- When synchronization is required, most papers consider the case where a drone or a truck waits for the other at the predetermined customer node.
	- A pseudo-node approach: the drone and the truck can meet to eliminate the waiting time (Chung and Sah, 2020).
	- Service hubs: (Wang and Sheu, 2019)
	- Rendezvous of a drone and a truck en route (Marinelli et al., 2017; Schermer and Moeini, 2019a), i.e., meeting at some point in a route, which is not a customer location.

### Solution Methodology
- Heuristic: 
	- Due to the NP-hard nature of DTCO problems, it is not practical to use off-the-shelf MILP solvers such as Gurobi or CPLEX for the larger instances of the problem. This leads to the popularity of heuristics in solving the DTCO problems.
	- Heuristics are problem-dependent techniques. As such, they usually are adapted to the problem at hand and they try to take full advantage of the particularities of this problem. However, because they are often too greedy, they usually get trapped in a local optimum and thus fail, in general, to obtain the global optimum solution.
- Metaheuristics: 
	- A metaheuristic, a higher-level procedure to find a good solution with few or no assumptions about the problem being optimized.
	- Meta-heuristics, on the other hand, are problem-independent techniques. As such, they do not take advantage of any specificity of the problem and, therefore, can be used as black boxes. In general, they are not greedy. In fact, they may even accept a temporary deterioration of the solution (see for example, the simulated-annealing technique), which allows them to explore more thoroughly the solution space and thus to get a hopefully better solution (that sometimes will coincide with the global optimum). Please note that although a meta-heuristic is a problem-independent technique, it is nonetheless necessary to do some fine-tuning of its intrinsic parameters in order to adapt the technique to the problem at hand.
- Exact methods:
	- Most DTCO problems are based on TSP and/or VRP, which are known to be NP-hard. Therefore, it is hard to solve the DTCO problems using exact methods, especially when the problem size is large.
	- Yurek and Ozmutlu (2018): decomposition-based iterative algorithm; 
	- Bouman and Agatz (2018): a three-pass approach (exact method) for TSP-D
- Continuous approximation:
	- Continuous approximation (CA) techniques replace the numerical methods by analytical techniques, and the detailed data is replaced by concise summaries
	- The problem can be reduced into a smaller set of parameters. Then, the impact of these parameters on the outcome of the problem can be determined.

### Future research directions
- Incorporating uncertainty:
	- There is always uncertainty in the air traffic and ground road networks. The uncertainty can be in the form of traffic conditions including accidents, natural disasters such as earthquakes and hurricanes, and man-made calamities such as riots, protests, political disturbances, etc.
	- In addition, drone travel may be affected by weather conditions such as extreme temperatures, precipitation, fog, humidity, and wind. In particular, the battery life, flying range, and drone speed may be impacted by these factors.
	- To address the uncertainty, data mining, machine learning and AI methods as well as stochastic optimization including robust optimization, stochastic programming, and dynamic programming should be explicitly used to plan DO and DTCO.
- Relaxing operational constraints/assumptions:
	- For example, a drone can depart from and rendezvous with a truck at some fixed locations. A drone can serve only one customer. A truck must wait for a drone to come back at the launch node. The customer demand is given and all the items are ready at the depot. These are only a few of many operational constraints and assumptions.
	- In addition, the relaxation of drone’s unit capacity assumption as well as enhanced solution algorithms would also be potential future works; the unit capacity of drones, because drones are becoming more capable at a fast rate.
	- Drone launch and recovery location assumption: Most of the reviewed DTCO papers that require drone launch and recovery assume that the launch and recovery can only be done at certain locations such as the customer node and/or the depot.
- Improving modeling techniques and solution methodologies:
	- Most DTCO problems are formulated as ILP or MILP, which are known to be NP-hard. For relatively larger problems, exact algorithms may not work and commercial solvers such as CPLEX and Gurobi will experience the curse of dimensionality.
	- Considering that the commercial application of DTCO is imminent, the development of effective and efficient heuristic algorithms is essential. As DTCO adds more complexity to already hard-to-solve TSP and VRP models, the state-of-the-art methods developed for TSP and VRP may not work well for DTCO problems.
	- As the number of trucks and drones increases, the DTCO problems will become increasingly difficult to solve with traditional approaches. Using simulation studies to find the optimal number of drone and truck combination for real life scenarios may be a practical research direction.



### Selected papers:
- [Murray. 2015. *The flying sidekick traveling salesman problem: Optimization of drone-assisted parcel delivery*](zotero://select/items/1_55L7LS3D)
	- present a MILP formulation for DTCO, which is called FSTSP. The problem describes the optimization of single drone and single truck scenario where the objective is to minimize the tour completion time. The paper uses the actual road distance metric to calculate the distances between nodes for the truck, while Euclidean distance is used to calculate the distance between nodes for the drone. The concept of drone sorties is ised in the paper, which we introduce in Section 3.1. Based on the typical TSP formulation, the paper adds one more variable for drone, and add DTCO constraints such as synchronization, drone endurance, launch and rendezvous, and flow conservation.
- [Agatz. 2018. *Optimization Approaches for the Traveling Salesman Problem with Drone*](zotero://select/items/1_M5WQ823F)
	- present an integer programming model for DTCO, which is called TSP-D. The nodes are divided into three categories: 1) drone node: a node visited by a drone only, 2) truck node: a node visited by a truck only, and 3) combined node: a node visited by a truck and a drone (mounted on the truck). A solution to TSP is the combination of a truck route (composed of the truck and combined nodes) and a drone route (composed of the drone and combined nodes). It is assumed that a drone’s speed is a times the speed of a truck. The advantage of this assumption is that the authors are able to provide bounds on the maximum savings produced by using the DTCO delivery as compared to truck only setting. For example, it is proved that the DTCO (TSP-D) optimal solution is at most 1 + a times better than that of the TSP (truck only). The properties of the TSP-D optimal solution are also shown in this paper. For example, in the TSP-D optimal solution, a combined node may be visited more than once, which is not allowed in the FSTSP formulation.
- [Murray. 2020. *The multiple flying sidekicks traveling salesman problem: Parcel delivery with multiple drones*](zotero://select/items/1_968M3TSL)
	- propose the multiple drone FSTSP (mFSTSP), which is an extension of Murray and Chu (2015). In this paper, a set of heterogeneous drones is introduced where each drone has its own flying time endurance and capacity while a single truck is used to work with the set of drones (synchronized working units). A truck can carry multiple drones and each drone can launch from the truck multiple times (but not from the same node). Each drone can carry one parcel at a time and is not allowed to come back to the node where it was launched from. The concept of operation is still used but the paper now considers a drone energy consumption rate when eligible sorties are to be identified. The objective is still the same: to minimize the make span, and the paper shows that increasing the number of drones results in diminishing benefits.
- [Ham. 2018. *Integrated scheduling of m-truck, m-drone, and m-depot constrained by time-window, drop-pickup, and m-visit using constraint programming*](zotero://select/items/1_NTA5WLV7)
	- extends PDSTSP proposed by Murray and Chu (2015) to incorporate multiple trucks in addition to multiple drones. In this paper, drones not only deliver items to customers but also are capable of picking up items from customers. A fleet of drones and a fleet of truck with multiple depots are considered in this paper for an operational excellence. A constraint programming approach is used to solve this problem (PDSTSP with drop off/pick up).
- [Wang. 2019. *Vehicle routing problem with drones*](zotero://select/items/1_ADLYTBLD)
	- propose the capacitated VRP (CVRP)based DTCO model, implying that the model becomes a traditional CVRP if drones are removed, where multiple trucks and multiple drones with limited flying range and capacity are considered. This model has some unique features and assumptions. First, drones cannot land on trucks at the customer locations. Instead, there are designated service hubs (docking nodes) where drones can land. Second, synchronization is not required because there are some backup drones at the service hubs. Third, drones can travel with another truck that is different than the ones they were launched from. Any truck can pick up any drone at the service hub as long as the flying range and capacity constraints are satisfied. The example of VRPD is illustrated in Fig. 4. The objective is to minimize the travel cost that is the combination of the fixed truck cost and the travel cost of drones and trucks. Because of these unique features and assumptions, the model does not require the concept of drone sortie nor operation.
- [Es Yurek. 2018. *A decomposition-based iterative optimization algorithm for traveling salesman problem with drone*](zotero://select/items/1_2T4BQ7N9)
	- develop a decompositionbased iterative algorithm that solves a single-drone-single-truck TSP-D problem up to 12 customers to optimality within 15 min. In contrast, the solution time of commercial solvers such as CPLEX and Gurobi for a 10 customer DTCO problem formulated using the state-of-the-art mathematical models can be several hours (Murray and Chu, 2015). However, when the size of the problem is increased beyond 12 customers, the solution time using their approach increases significantly.
- [Schermer. 2019. *A hybrid VNS/Tabu search algorithm for solving the vehicle routing problem with drones and en route operations*](zotero://select/items/1_98LREFQ6)
	- There are recent studies that allow the rendezvous of a drone and a truck at some locations in a route that are not customer locations. This type of problem is called Vehicle Routing Problem with Drones and En Route Operations (VRPDERO) (Marinelli et al., 2017; Schermer and Moeini, 2019a), which is formulated as MILP (Schermer and Moeini, 2019a). If we allow drones and trucks to meet each other at any point in the network, the synchronization issue may be completely resolved, which has potential to greatly enhance the economic aspect of DTCO.

One research problem, whether we need mobile launching platform? If the rendezvous of a drone and a truck is possible under specific conditions, how much is the saving and time and cost? What is the outcome at different speed limit and condition?
👣➿👣

