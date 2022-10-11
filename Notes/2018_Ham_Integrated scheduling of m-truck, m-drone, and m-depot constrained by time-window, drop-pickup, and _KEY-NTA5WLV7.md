# Integrated scheduling of m-truck, m-drone, and m-depot constrained by time-window, drop-pickup, and m-visit using constraint programming
##  Metadata
- ItemType: journalArticle
- Authors: [[Andy M. Ham]]
- Publication: [[Transportation Research Part C：Emerging Technologies]]
- Date: 2018-06
- DOI: [10.1016/j.trc.2018.03.025](https://doi.org/10.1016/j.trc.2018.03.025)
- Collection: [[Select]]
- PDF Attachments: <ul><li><a href="zotero://open-pdf/library/items/7C25UNKK">Integrated scheduling of m-truck, m-drone, and m-depot constrained by_Ham_2018.pdf</a></li><li><a href="zotero://open-pdf/library/items/HC5IVB4K">ScienceDirect Full Text PDF</a></li></ul>
- Tags: #Traveling_salesman_problem #Unmanned_aerial_vehicle #Vehicle_routing_problem #Constraint_programming

👣➿👣

## Remained Challenges
- After a drone completes a drop, the drone actually has the capability to fly directly to another customer for pickup instead of flying back to the depot and starting a new tour.
- A customer might order multiple products with different shipping priorities (or time-windows).
- Multiple depots hosting a fleet of trucks and a fleet of drones can be collectively orchestrated to achieve the operational excellence.

## Methodology
#### PDSTSP with drop & pickup synchronization at single depot (CP1)
- • Objective: The time required to service all customers by either the truck or the drone and return both vehicles to the depot must be minimized. • C1: Each task must be processed by one vehicle. • C2: The different travel-time of truck and drone must be considered, when the vehicle travels between nodes. • C3: Both trucks and drones must start from the depot. • C4: Both trucks and drones must return to the depot upon completing all tasks. • C5: Each customer must be served during a time-window. • C6: Drones are subject to a maximum flight endurance.





👣➿👣