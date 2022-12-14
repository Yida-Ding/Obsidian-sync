#  Integrated Disruption Recovery of Drone-Truck Coordinated Delivery System
$\newline$
## Motivation
- Throughout the recent decade, various researchers have proposed to leverage the concept of urban air mobility for an effective construction of package delivery service. The major idea is to lift the typically ground-based delivery service to the third dimension, while addressing problems such as last-mile delivery and recurrent traffic jams in major metropolitan regions around the world. To resolve the relatively short travel range and limited capacity issues of drones, various researchers have proposed to further enhance the utility of drones by deploying them with ground vehicles (e.g., trucks) in tandem, referred as Drone-Truck Coordinated Operations (DTCO). 
- Such delivery services, however, are prone to the presence of *disruptions*, in which parts of the service network are affected, e.g., due to extreme weather condition, drone physical failure, drone network delay and etc. These disruptions have negative impact on the original drone-truck delivery schedule and even result in the failure of satisfying customer demand, leading to great economical loss and damage of reputation. It is presumed that the *operational uncertainty* due to unforeseeable disruptions hinders the actual deployment of drone-truck coordinated operations in current logistics industry.
- While an extensive number of studies have investigated on the efficiency improved by utilizing the drone-truck coordination, there is a gap in the literature considering *real-time disruption recovery* of the drone-truck coordinated system, which reroutes/reschedules the involved carriers in a systematic manner to cope with the emerging disruptions while maximizing efficiency. From the perspective of logistics practitioners, there is an urgent need to establish a decision recommendation framework which transits the operations from the *efficient* drone-dominated delivery mode to the *reliable* truck-dominated delivery mode in face of disruptions. We believe the construction of such reactive disruption recovery model is critical to the long-term development and deployment of drone-truck coordinated operations in the field of last-mile delivery.

## Modelling
- The *original DTCO schedule* is an ideal and efficient schedule under no disruption, which is generated by the exact method in the latest DTCO research (e.g., [1,2]), including multiple trucks, multiple drones and multiple depots.
- It is assumed that disruptions *only fall to drones*, since drones are much more vulnerable to disruptions as compared to the traditional trucks.
- Four types of disruptions and their external costs and mathematic modelling are listed as follows:

|      Disruption Type      |                          External Causes                           |                 Mathematic Modelling                 |
|:-------------------------:|:------------------------------------------------------------------:|:------------------------------------------------:|
| Severe weather conditions |  High winds, water/rain damage, cold temperatures, low visibility  | Drones resume operation in specific time windows (binary, fly/not fly) |
|  Drone technical failure  | Mechanical/telecommunication/sensor failure, cyber/physical attack | Reliability metrics e.g. the Mean Time Between Failures (MTBF), expressed in hours of activity|
|   Drone departure delay   |         Unscheduled maintanence, network delay propagation         | A probabilistic lag time over scheduled departure time |
|    Air exclusive zone     |        Air traffic management, urban air mobility regulations   | A zone defined by a center and radius which prohibits drone activity |
traffic congestion


- Drone Reliablity: 
	- The probability that a system, subsystem or part is able to perform its specific function in a pre-established time and under pre-established conditions
	- The commercial aviation failure rate is about $1/10^5$ flight hours, while for drones, it has been verified at about $1/10^3$ flight hours, so a higher magnitude of two orders. From a different point of view, sophisticated UAV systems have an overall failure rate of 25%. [3]
	- For a part or a single subsystem, the MTBF is often expressed as the reciprocal of reliability. For instance, the MTBF gives information about the level of unreliability, and it typically shows the number of failures of a piece of equipment over an established time, i.e., 10,000 h. [3]
	- The Failure In Time (FIT) rate of a device represents the number of expected failures in one billion device-hours of operation. This parameter is widely diffused in the semiconductor industry. [3]
- Model functionality:
	- Feature: real-time disruption \& real-time recovery.
	- Input: current states of the carriers + current customer demand situation + real-time disruptions.
	- Output: real-time recovery plan of carriers, including rerouting/rescheduling decisions.
- Modelling methodology:
	- Arc-based network flow model: typically applied in VRP and the majority of drone logistics literature.
	- Time-space network model: typically applied in air transportation management, for instance airline disruption recovery.

## Reference
[1] Murray, C.C., Raj, R., 2020. The multiple flying sidekicks traveling salesman problem: Parcel delivery with multiple drones. Transportation Research Part C: Emerging Technologies 110, 368???398. [https://doi.org/10.1016/j.trc.2019.11.003](https://doi.org/10.1016/j.trc.2019.11.003)
[2] Ham, A.M., 2018. Integrated scheduling of m-truck, m-drone, and m-depot constrained by time-window, drop-pickup, and m-visit using constraint programming. Transportation Research Part C: Emerging Technologies 91, 1???14. [https://doi.org/10.1016/j.trc.2018.03.025](https://doi.org/10.1016/j.trc.2018.03.025)
[3] Petritoli, E., Leccese, F., Ciani, L., 2018. Reliability and Maintenance Analysis of Unmanned Aerial Vehicles. Sensors 18, 3171. [https://doi.org/10.3390/s18093171](https://doi.org/10.3390/s18093171)

??????rare event???not severe consequence
????????????disruption??????????????????
md???mt???truck?????????????????????100??????????????????20??????urgent??????????????????similarity?????????reallocate???high frequency???not low consequence
drone ????????????disruption?????????
???????????????????????????
???????????????
?????????????????????local???????????????
1.???????????????replacing urban truck???????????????????????????
????????????????????????????????????????????????????????????
????????????????????????????????????????????????drones?????????????????????????????????????????????
- ??????????????????????????? - ?????????????????????
- ??????????????????????????? - ?????????????????????
?????????????????????????????????????????????
?????????????????????????????????disruption????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????
?????????????????????
?????????????????????????????????rare event
?????????????????????
??????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????????

1. Is severe weather condition a rare event?
2. How is the disruption on the ground?




