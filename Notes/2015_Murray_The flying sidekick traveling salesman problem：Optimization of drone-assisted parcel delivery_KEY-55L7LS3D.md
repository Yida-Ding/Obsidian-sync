# The flying sidekick traveling salesman problem: Optimization of drone-assisted parcel delivery
##  Metadata
- ItemType: journalArticle
- Authors: [[Chase C. Murray]]、 [[Amanda G. Chu]]
- Publication: [[Transportation Research Part C：Emerging Technologies]]
- Date: 2015-05-01
- DOI: [10.1016/j.trc.2015.03.005](https://doi.org/10.1016/j.trc.2015.03.005)
- Collection: [[Select]]
- PDF Attachments: [The flying sidekick traveling salesman problem_Murray et al_2015.pdf](zotero://open-pdf/library/items/IZ9GLFNH)
- Tags: #Logistics #Heuristics #Integer_programming #Traveling_salesman_problem #Unmanned_aerial_vehicle #Vehicle_routing_problem

👣➿👣
### Major contribution
- The primary contribution of this paper is to introduce a new variant of the traditional traveling salesman problem (TSP) that addresses the challenge of determining optimal customer assignments for a UAV working in tandem with a delivery truck. We term this problem, as depicted in Fig. 3b, the flying sidekick traveling salesman problem (FSTSP).
- Secondarily, we also introduce the problem associated with devising optimal truck and UAV assignments in the case of a distribution center located in close proximity to customers. We term this the parallel drone scheduling TSP (PDSTSP). 

### TSP, VRP literature
- The myriad TSP and VRP variants (e.g., problems resulting from the incorporation of time windows, customer priorities, asymmetric travel distances, or heterogeneous vehicles)
- the FSTSP may be categorized under movement synchronization en route, whereby vehicles may join and separate multiple times along a route.
- Although the author notes that this particular category has received limited attention in the literature, one such paper considers the VRP with trailers and transshipments (VRPTT), as in Drexl (2007). The trailers, which may only be moved by trucks, can be decoupled from one truck and picked up by a different truck.

### The flying sidekick TSP
- Objective:
	- The objective of the FSTSP is to minimize the time required to service all customers and return both vehicles to the depot.
- UAV Sortie $<i,j,k>$: 
	- First node (The launch point i): may begin at either the depot (where the UAV is loaded with a parcel for a customer) or from a customer location (where it is loaded by the truck driver with a parcel); must not be the ending depot node
	- Second node (The delivery point, j): must be a customer that is serviced by the UAV; must be a UAV-eligible customer and must not be the same as the launch point, i
	- Final node (The rendezvous point, k): either the depot or the location of the truck. If a sortie ends at the truck, another service time may be required for the driver to recover the UAV; may be either a customer or the ending depot, it must not equal either i or j; and the UAV’s travel time from i ! j ! k must not exceed the endurance of the UAV
	- Service time: Prior to launch, a service time may be required for the driver to change the UAV’s battery and to load the parcel.
- Assumptions:
	- UAV may visit only one customer per sortie
	- the UAV cannot temporarily land while en route
	- if the UAV is launched from i, it may not return to the truck at node i.
	- If the final leg of a UAV sortie involves a rendezvous with the truck, this must take place at the location of a customer serviced by the truck; the UAV cannot reconnect with the truck at some intermediate location. Furthermore, the truck may not revisit any customer nodes to retrieve the UAV.
	- Neither the UAV nor the truck may visit any non-customer nodes (other than the depot, of course).
- Features:
	- A finite set of nodes: total c+1
	- Truck time and drone time: $\tau_{ij}$ and $\tau_{ij}'$
	- C12&13: force the truck and the UAV to arrive at node i at the same time.
	- Maybe for truck or drone, there is only one time associated with each node, so $t_i$ is both arrival time and departure time
- Decision variables:
	- $x_{ij}\in\{0,1\}$: flow variable for truck;
	- $y_{ijk}\in\{0,1\}$: flow variable for UAV sortie;
	- $t_j\geq0,t_j'\geq0$: the time truck/drone arrives at node j;
	- $p_{ij}\in\{0,1\}$: equals one if truck first visits i and then visits j;
	- $u_i\in[1,c+2]$: the position of node i in the truck's route;

-  Formulation:
	- Obj: $\text{min}~t_{c+1}$, with C14 and C15 to link the return time of truck and drone
	- Const.(2-6): C5?![[Pasted image 20220920105643.png|825]]
	- Const.(7-11):![[Pasted image 20220920105842.png|825]]
	- Const.(12-16): time coordination constraint![[Pasted image 20220920105916.png|800]]
	- Const.(17-21):![[Pasted image 20220920110103.png|800]]
	- Const.(22-24):![[Pasted image 20220920110217.png|800]]
	- Const. (25-32):![[Pasted image 20220920110312.png|800]]
	- Example:![[Pasted image 20220920151712.png]]
		





👣➿👣