# Eﬃcient Large-Scale Multi-Drone Delivery using Transit Networks
##  Metadata
- ItemType: journalArticle
- Authors: [[Shushman Choudhury]]、 [[Kiril Solovey]]、 [[Mykel J Kochenderfer]]、 [[Marco Pavone]]
- Publication: [[Journal of Artificial Intelligence Research]]
- Date: 2021-02-17
- DOI: [https://doi.org/10.1613/jair.1.12450](https://doi.org/https://doi.org/10.1613/jair.1.12450)
- Collection: [[Transit]]
- PDF Attachments: [Choudhury et al. - Eﬃcient Large-Scale Multi-Drone Delivery using Tra.pdf](zotero://open-pdf/library/items/BTUN3K62)
- Tags: #reading #multiagent_systems #planning #robotics

👣➿👣

## Review
- Structure: 
	- Section 2: we present an overview of our two-layer approach. 
	- Section 3: we elaborate on the upper **task allocation layer**
	- Section 4: the lower **multi-agent pathfinding layer**
	- Section 5: we describe the surrogate cost estimate used to **couple** the two layers. 
	- Section 6 and 7: we present extensive experimental results on several aspects of our framework
- Core problems:
	- Which deliveries each drone should make?
	- For each drone, the deliveries are made in what order?
	- For each drone, which modes of transit (or transit line) to use, and for how long?
- Assumptions: 
	- Any package can be dispatched from any depot
	- We assume that a drone carries one package at a time, which is reasonable given state-of-the-art drone payloads (Sudbury & Hutchinson, 2016)
	- Drones are recharged in negligible time upon visiting a depot (e.g., a battery replacement)
	- Depots have unlimited drone capacity
	- The transit network is **deterministic** with respect to locations and vehicle travel times.
	- public transit vehicles are unaffected by drone actions
- Objective:
	- Minimize a cumulative objective over all drones, namely, the makespan, i.e., the maximum individual delivery time for any drone.
- Constraints:
	- plan over large time-dependent transit networks
	- accounting for flight range constraints
	- avoid inter-drone conflicts
	- exceeding the maximum carrying capacity of a vehicle
	- ...

## Extensions
- Additional features and extensions:
	- Time window
	- Drop and pick-up
	- En-route rendezvous instead of rendezvous at bus stops
	- Deterministic transit network w.r.t. locations and times
	- Depots given by data
	- the boarding conflicts constraints & capacity
	- Consider battery charging of drones on transit (TBD)
- Broader extensions:
	- Disruption recovery of transit vehicles via GAC: account for **delays and uncertainty** in the travel pattern of transit vehicles
	- Adjust the transit network to better accommodate delivery drones

## Figures
![[Pasted image 20221011141259.png|850]]
![[Pasted image 20221011141349.png|850]]
![[Pasted image 20221011141408.png|850]]
![[Pasted image 20221011141426.png|850]]



👣➿👣