# Last-mile delivery concepts: a survey from an operational research perspective
##  Metadata
- ItemType: journalArticle
- Authors: [[Nils Boysen]]
- Publication: [[OR Spectrum]]
- Date: 2020-09-21
- DOI: [https://doi.org/10.1007/s00291-020-00607-8](https://doi.org/https://doi.org/10.1007/s00291-020-00607-8)
- Collection: [[Last-mile]]
- PDF Attachments: [Boysen - Last-mile delivery concepts a survey from an oper.pdf](zotero://open-pdf/library/items/6RKHJB85)
- Tags: #/reading #Transportation #City_logistics #Last-mile_delivery #Survey

👣➿👣
	
## Decision Problems:
- The compact chain notation is applied to denote the alternative last-mile delivery concepts and to briefly define the concept treated by each surveyed paper in the literature review.
- Given these basic elements, a specific last-mile delivery concept can now precisely be defined by a chain of storage and transport process steps, where each chain starts at the depot and ends with a handover element.
![[Pasted image 20220821123318.png|750]]

#### 1. Human‑driven delivery vans: **[depot>van>man>aHome]**
- Features:
	- Delivery vans depart from a central depot, each driven by a human delivery person. 
	- On a tour along customer homes, the delivery person stops the van at the roadside, approaches a customer home, and hands over a parcel directly to the customer via attended home delivery (aHome).
- Setup of infrastructure:
	- Traditional territory design: Service providers rather partition the territory serviced by a depot into smaller regions, which remain constant for a longer time. Each region is serviced by a repeated delivery pattern, e.g., once per day, by a tour of a single van.
	- Current problem: The price for fixed regions, and the simplification of the planning process coming along with this partitioning, is a loss of flexibility in the customer-to-tour assignment.
	- Challenge: Regions have to be determined without deterministic knowledge on the varying sets of customers that have to be serviced each day, in order to achieve higher flexibility in the customer-to-tour assignment.
- Staffing and fleet sizing:
	- Labor-related decision problem: the assignment of drivers to regions and their daily tours.
	- Challenge: The sizing of a stand-by workforce for these cases and decision support for driver-to-region assignments, e.g., including a (restricted) reassignment of shipments among regions to balance varying experience levels.
- Routing and scheduling:
	- Given a region serviced by a single vehicle whose capacity is not exceeded by the current set of customers to be serviced, the basic routing task to be solved is the asymmetric traveling salesman problem (aTSP).
	- Additional features: time windows specific to customers; time-dependent travel/service times; electric vehicles (limited ranges and the need for recharging, i.e., electric TSP with time windows); pedestrian subtours (additional walking to homes).
	- Main obstacle: Region-specific driver knowledge (e.g., with regard to suited parking spaces, timedependent congestion, and customer preferences) that cannot appropriately be modeled by commercial routing and scheduling software.
	- The wave (or delivery) dispatch problem: In other last-mile domains, e.g., express courier services or meal delivery, urgent deliveries rather arrive dynamically over time, so that as additional decision variables the departure times of all tours have to be determined; Has to consider a given set of fixed customers that have already arrived and potential customers which may arrive in the near future; Vehicle routing problem with release dates.

![[Pasted image 20220822130828.png|775]]

#### 2. Cargo bikes: [depot>van>micro>bike>aHome]
- Features: 
	- Vans to micro-depots and, from there, cargo bikes to customers. 
	- Micro-depots: Since capacities of cargo bikes are much smaller than those of delivery vans, they need to be replenished multiple times with additional shipments during the day. To avoid time-consuming returns to a central depot, cargo bikes are typically replenished via a network of decentralized micro- (also denoted as satellite) depots, e.g., a garage in a (multi-story) car park, the loading dock of a shop, or a trailer.
	- Cargo bikes are either manually powered and/or by an electric engine (sustainability); rather small capacities; hard for aging workforce.
- Setup of infrastructure:
	- Strategic decision problem: Whether to apply cargo bikes at all and how to integrate them into existing delivery networks.
	- Long-term decision when setting up this delivery concept: the locations and capacities of micro-depots.
	- Trade-off: Erecting more micro-depots increases facility costs, but reduces the transport costs toward customers and vice versa.
	- Multi-echelon location routing problems, which combine location planning with the routing decisions from the selected location.
	- Challenge: the customers to be delivered are yet uncertain and bound to daily change when selecting long-term locations for micro-depots.
- Staffing and fleet sizing:
	- Decisions on an appropriate number of bikedriver tandems to be applied and the truck fleet for supplying the micro-depots.
	- Trade-off: Larger fleets increase delivery services for customers, e.g., a higher rate of on-time deliveries, but increase wage and investment costs.
	- Three coupling decisions: the locations of the micro-depots, the interdependent routing of vans and cargo bikes, and fleet sizing.
- Routing and scheduling:
	- Given fixed locations of micro-depots, the remaining routing problem for a given fleet of cargo bikes resembles a multi-depot vehicle routing problem.
	- Peculiarities: limited capacities of micro-depots; time windows (customers are promised specific delivery times); recharging of electric cargo bikes; different travel speeds; timedependent travel times
	- The two-echelon location routing problems relevant for delivery concepts with cargo bikes are among the most challenging optimization problems of the transportation domain.
	- Extensions: uncertainties with regard to customers; limited capacities; time windows; fleet size and mix decisions; recharging of electric cargo bikes; speed-dependent energy consumption; time-dependent travel times.

![[Pasted image 20220822130854.png|775]]

#### 3. Self‑service: [depot>van>locker>self]
- Features: 
	- Set up and operate a self-service delivery concept and start with parcel lockers.
	- Decentralized facility can either be a parcel locker or a shop (i.e., an umbrella term for a decentral collection unit, where shipments for multiple customers are taken over and handled by a human service person)
- Setup of infrastructure:
	- Location planning of parcel lockers, the right layout of each parcel locker and the sizing of compartments.
	- Trade-off: The more parcel lockers are erected, the better their reach toward customers, but the higher one-time installation costs
	- Unifying both decisions: location planning of lockers and deciding on their individual layouts
- Staffing and fleet sizing:
	- Standard problem: The delivery process for a given network of parcel lockers with delivery vans launched from a central depot
- Routing and scheduling:
	- Given a network of parcel lockers, assign customer parcels to specific compartments of parcel lockers and to schedule their delivery toward the selected lockers, which is typically executed by delivery trucks.
	- The resulting routing and scheduling problems are rather of the pickup-and-delivery type where the limited capacity of a delivery truck may become a bottleneck, if some lockers have considerably more outgoing than incoming parcels.
	
![[Pasted image 20220822131114.png|775]]

#### 4. Drones: 
- Features: 
	- Electrically powered; comparatively fast; operate autonomously.
	- Achieving sustainability, lower costs, and the relief of an aging workforce.
	- Focusing on decision problems of drones, rather than technical and legislative restrictions.
- Concept **[depot>drone>uHome]**
	- Features: 
		- Drones are launched directly from the central depot and fly back and forth each leg toward a customer. 
		- Given the limited flight range of drones, which according to Agatz et  al. (2018) is currently restricted to about 20km, in large urban areas, this concept requires a dense and costly depot network.
		- The limited flight range of drones requires that either the single depot or the network of decentralized depots are erected directly in an urban area, where land is notoriously costly.
	- Setup of infrastructure:
		- Long-term planning: Where to locate the depots from where the drones are launched.
		- Trade-off: Given the limited flight-range of drones, opening more depots increases the reach toward customers and reduces travel distances, but leads to higher investment costs (and vice versa).
		- Two types of formulation: 
			1. (max coverage s.t. # depots) the coverage of drones for a given set of customer locations can be maximized given a limited budget for depots
			2. (min # depots s.t. enough coverage) the number of depots to be erected to cover a given set of customer locations can be minimized.
		- Extensions: To bridge a distance between depot and customer beyond a drone’s flight range, recharging stations can be inserted into the distribution network.
	- Staffing and fleet sizing:
		- Not only investigate the strategic depot location problem, but simultaneously integrate the tactical drone fleet sizing problem.
	- Routing and scheduling:
		- Decision problem: How to get a given set of parcels to customers given a depot network equipped with drones.
		- Since drones are typically restricted to carry a single shipment at a time, the routing problem in its most basic version reduces to a straightforward assignment of drones to customers. This setting resembles the well-researched parallel machine scheduling problem, where the machines represent drones and jobs their flights to customers.
		- Investigates that trucks and drones operate in parallel, so that a decision is required which kind of transportation device services each customer. The drones fly back and forth the depot and selected customers, and the truck services all remaining customers in a single TSP tour without capacity limitation.
		- Existing literature on drone routing often ignores recharging drone batteries.
- Concept **[depot>van>drone>uHome]**
	- Features: 
		- Applies delivery vans as mobile launching platforms for drones. Vans and their higher driving ranges allow to transport drones closer to customers. Drones are loaded en route each with a single shipment stored on the truck, depart to a customer, complete their unattended home delivery, and meet the truck either at the same or a later stop.
		- Avoid the costly network of urban depots required by delivery concept **[depot>drone>uHome]**
		- When customers have no suited landing space for a drone, e.g., living in a skyscraper without balcony or openable window, may rather extend the options of a given **[depot>van>man>aHome]** delivery chain.
	- Routing and scheduling:
		- Murray and Chu (2015) were the first to introduce concept **[depot>van>drone>uHome]** to the operations research community
		- Flying sidekick TSP, TSP-D, and etc. : Given a single depot and a truck equipped with a single drone, the task is to find a trip with minimum tour completion time (for both devices), so that each customer is served either by truck or drone. The drone is only allowed to depart from and return to the truck at a customer node.
		- Extensions: single-truck–multiple-drone setting; a drone is not forced to return to the same truck it is launched from; drone and truck with different travel costs; bi-objective (min-cost and min-time); no-fly zones; sustainability aspects; three options simultaneously (customers are either serviced by a given set of truck–drone tandems, by drones launched from the depot, or trucks without drones).
		- Both drone-based delivery concepts **[depot>drone>uHome]** and **[depot>van>drone>uHome]** have received considerable scientific attention.
- Alternative drone-based concepts:
	- Concept **[depot>van>micro>drone>uHome]** The shipments are loaded by a conventional van and delivered toward a drone station where drones can be loaded with shipments, recharge after delivery, and wait for the next truck.
	- Concept **[depot>drone>locker>self]** Drones could rather be applied to deliver shipments toward parcel lockers equipped with a suited landing platform and parcel retrieval mechanism on top. Addressing the problem that in urban areas, lack suited landing space for a fail-save, secure, and theft-protected unattended delivery.
	- Concept **[depot>drone>van>man>aHome]** Apply drones for resupplying trucks en route with urgent orders that have arrived at the depot after their departure. This adds to the flexibility and addresses the lack of suited landing space in urban areas
	- Concept **[depot>drone>micro>drone>uHome]** Larger drones, applying a specific layer of the airspace to avoid interference, transport multiple shipments toward microdepots, which they call supporting points also used for recharging. From there, small drones applying another layer, each transporting a single shipment, depart toward customers.
	
![[Pasted image 20220822131041.png|775]]


#### 5. Autonomous delivery robots:
- Main difference of drone- and bot-based delivery concepts:
	- Bots travel in pedestrian speed of about 6km/h on side-walks, which considerably slows down their delivery speed, but allows them to move slightly heavier shipments up to 10kg.
	- Bots face less security regulations, so that, in different field tests, one operator was allowed to supervise dozens of bots. A drone has to be supervised by a dedicated flight operator during all time and is not allowed in neuralgic areas.
	- Bots tied to the existing road network while drones can fly directly from A to B apart from no-fly zones (e.g., security areas) and obstacles (e.g., large buildings).
	- Bots can barely relieve the time pressure of last-mile distribution due to their slow delivery speeds.
	- Different handover option: Bots are only suited for attended home delivery (aHome), while drone delivery is unattended delivery (uHome) since parcels can be dropped of at the destination without the recipient being present.
- Related concept: **[depot>van>bot>aHome]**
- Most decision problems and solution approaches of the drone domain can also be applied to delivery bots. 
- Both autonomous delivery devices (i.e., drones and bots) are similar from a mathematical point of view, but mainly vary in specific parameters, such as payload, costs, and operating ranges.
- Thus, it would be interesting to investigate how customers with different characteristics and requirements should be partitioned among both kinds of autonomous delivery devices and their alternative launching options.
![[Pasted image 20220822132559.png|775]]

#### 6. Crowdshipping
- Features:
	- Instead of hiring fixedly employed delivery persons, these companies follow the idea of involving many people in the delivery process, professional and non-professional, who are already on the road, have spare capacity, and are willing to detour to consumer locations.
	- The existence of an online (digital) platform and a related smartphone app.
	- After a delivery request is posted on a platform, they are offered to registered crowdshippers (CS) who can choose one or multiple tasks, pick up the shipments, and deliver them to the recipient.
	- As a stand-alone delivery concept or as a support for traditional van delivery.
	- Since CS are not employees and only hired for one or multiple deliveries within a short time, the postal service provider has no expenses for long-term salaries, health insurance, gas, and vehicles, which saves costs.
	- If deliveries are performed by foot, bike, public, or public transit, emissions can be reduced.
	- Since CS are not fixedly employed, reliability and scalability are the main challenges for a logistics provider applying the crowd.
- Setup of infrastructure:
	- Key factor: A well-functioning platform that matches delivery requests and CS. The setup of such a system, however, is rather an IT challenge, but commonly not substance of operations research literature and therefore not in the scope of this review.
	- The main strategic decision to be taken is the design of a suited pricing scheme.
- Matching and routing **[depot>crowd>aHome]** :
	- The main service of a crowdshipping platform is the matching of supply and demand. A matching decides which shipping offers are executed by which CS.
	- Optimization-based matchings: collect shipping offers and CS over a specific time span and optimize their assignment according to some objective function.
	- An optimization-based matching cannot be determined in an isolated manner, It depends on the pricing scheme whether the shipping offers assigned to a CS meet her minimum wage expectations and the travel costs of each CS.
	- Constitute a challenging holistic optimization problem involving matching, routing, and pricing tasks.
	- Formulations: Combined matching, routing, and pricing; Leftover shipments; Leftover shipments; Combined with item sharing; Alternative handover locations; Workload sharing among multiple CS.
	- Future research should investigate how to apply these deterministic problems in a dynamic environment, e.g., by planning on rolling horizons, where CS arrive dynamically over time and are impatient to receive their assigned deliveries.

![[Pasted image 20220822135015.png|775]]

#### 7. Combined with people transportation
- Features:
	- The usage of free capacity of transport options originally dedicated to moving people.
	- Streetcars are applied to move shipment toward urban micro-depots.
	- Crowdshippers take shipments along on their own travel with the metro system and leave parcels in parcel lockers.
	- Reuse unused capacity of people transportation, adding to a sustainable last-mile distribution.
- Related concepts:
	- **[depot>public>aHome]** Taxi drivers are allowed to carry customers and shipments simultaneously. The introduced share-a-ride problem aims for efficient taxi routes and assignments of customers and parcels to taxis. The goal is to maximize the profit of the whole network, which consists of profit received for delivering customers and parcels minus the cost for additional travel distances and times.
	- **[depot>van>locker>public>locker>self]** Taxis pick up packages at parcel lockers and transport them to other ones, closer to final customers. With a given set of deliveries and dynamically incoming taxi requests, the objective is to minimize the total parcel delivery time.
	- **[depot>van>public>van>man>aHome]** Multi-modal transport chains, where traditional delivery vans and scheduled lines of public transport are combined. A delivery van starts from a depot, picks up parcels at different locations, and delivers them to a transfer point, called station-hub, where the shipments are transferred to a scheduled line. The line service then moves the packages to another station-hub on their fixed path, where, again, shipments are transferred to a van and, hereafter, delivered to the final customers. The objective is to minimize total costs, consisting of travel costs for the van and the use of the scheduled line service.
- Interesting extensions: Customers applying public transport by themselves can conveniently pick up their shipments on their way back from work, widely reuses existing infrastructure.

![[Pasted image 20220822140534.png|775]]

#### 8. Farther future
- Alternative mobile drone launching platforms:
	- Trains, vessels and airships
	- To avoid the high investment costs of a dense depot network for launching drones with restricted operating range
	- Do not add much peculiarities and the resulting decision models share a lot of similarities with those where drones are launched from trucks
	- Related concepts: **[depot>train>drone>uHome]**, **[depot>vessel>drone>uHome]**, **[depot>aircraft>drone>uHome]**
- Autonomous vehicles:
	- Autonomous driving will not only have a disruptive impact on people transportation, but it also has the potential to streamline last-mile deliveries.
	- Concept **[depot>aVan>man>aHome]**
		- The delivery person can quickly be released from the autonomous van directly next to a customer’s home, and the van can find a suited parking space while parcel handover.
		- On a pedestrian subtour, where the delivery person walks with more than a single shipment toward multiple nearby customers before returning to the van, the start and end of such a subtour need not be identical.
		- Future research should quantify the potential gains of autonomous delivery vans supporting a human delivery person and should provide routing problems addressing the resulting peculiarities.
	- Concept **[depot>mLocker>self]** 
		- Mobile parcel lockers are equipped with an autonomous drive, so that they can alter their location during the day.
		- The ability to change locations increases their reach toward customers, which may also move around in the city center during the day.
		- Mobile lockers have to wait for the pickups, once customers are informed on the arrival of a nearby mobile locker via a smartphone app.
	- Concept **[depot>aVan>locker>self]**
		- Autonomous delivery vans equipped with an automated handover mechanism could rather be applied to resupply self-service facilities such as parcel lockers.
	- Concept **[depot>loop>micro>bike>aHome]**
		- Apply automated guided vehicles (see Fig.  9, right) or rail-bound cargo vehicles to transport shipments from a central depot outside the city center via cargo tunnels toward inner-city microhubs.
		- The problems associated with congestion and emissions are reduced, but there are the huge digging and investment costs for the tunnel.

## Summary and future directions
- The impact of OR/Optimization: Critics may say that, first, future last-mile concepts such as drones or autonomous delivery bots should prove their capability, before operational decision tasks such as routing issues have to be resolved. Without sophisticated optimization approaches provided by operations research, however, simulation studies evaluating the economic viability of a novel delivery concepts can only be based on simple decisions rules. This, however, bears the risk of underestimating some novel last-mile concepts, so that R&D money is misdirected to the wrong concepts. Thus, already in an early phase of an innovative last-mile concept research of the operations research community seems highly welcome.
- Unified dataset for evaluation of various methods: For a systematic benchmark test, unique data set gained from real-world data is required, which is publicly available and contains all detailed information on street networks, parking spaces, footways, access restrictions, recharging opportunities, exact customer locations, etc. Once such a general data set is available each new delivery concept could be tested on the same data. In this way, a systematic benchmark of many alternative concepts with regard to KPIs could be gained. This would support the identification of the right delivery concepts for different customer segments, an efficient allocation of R&D money, and informed decisions on public legislation and rules related to city access and lastmile logistics.
- What is the right mix of delivery concepts? Each last-mile delivery mode has different strengths and weaknesses, so that the right choice will most likely be a combination of multiple concepts each focusing on different customer segments.For instance, delivery vans equipped with drones could rather be an option for rural areas where back yards provide appropriate landing space for drones, cargo bikes and autonomous delivery bots could be the right choice for urban areas, and especially non-urgent deliveries for price-sensitive customers could be candidates for self-service options. Investigating an appropriate customer segmentation and their assignment to the most suited delivery modes remains a valid task for future research.





👣➿👣