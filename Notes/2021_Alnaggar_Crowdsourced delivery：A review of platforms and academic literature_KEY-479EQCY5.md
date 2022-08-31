# Crowdsourced delivery: A review of platforms and academic literature
##  Metadata
- ItemType: journalArticle
- Authors: [[Aliaa Alnaggar]]、 [[Fatma Gzara]]、 [[James H. Bookbinder]]
- Publication: [[Omega]]
- Date: 2021-01-01
- DOI: [10.1016/j.omega.2019.102139](https://doi.org/10.1016/j.omega.2019.102139)
- Collection: [[Last-mile]]
- PDF Attachments: [Crowdsourced delivery_Alnaggar et al_2021.pdf](zotero://open-pdf/library/items/ZGDPUTK8)
- Tags: #Crowdsourcing #Last-mile_delivery #Optimization #Same-day_delivery #Survey #Transportation

👣➿👣

## Overview of available platforms
- Platform compensation scheme: According to the driver information on the official websites of those platforms, the value of such compensation is calculated by a formula, which may be city-specific, which considers factors like mileage, wait time, size of package and others. Drivers are notified of the earning amount before they accept a delivery task.
- **Dedicated or not:** All platforms, with the exception of Hitch and Roadie [13,14], assume that drivers are making dedicated trips just for the sake of fulfilling the delivery request, and are not necessarily heading in that direction. Contrarily, Hitch and Roadie [13,14] match delivery requests with a traveler’s already pre-planned trip. In other words, they collect information on when a driver is planning to go somewhere (the time and destination), and offer to drivers delivery requests that are already on their way.
- **Classification of the scheduling and matching mechanisms:**
	- Pure self-scheduling (like ride-hailing): 
		- different crowdsourced delivery systems use varying levels of such flexibility. 
		- Those platforms are very similar to how ride-hailing services such as Uber and Lyft operate. 
		- Once an order arrives, whose pickup is within a specified radius of where the driver is, the driver is notified through the app of the request, and may choose to accept or reject the offer.
	- Hybrid and centralized scheduling (booking and posting availability beforehand): 
		- a more centralized scheduling approach to better balance supply and demand at various times of the day. 
		- Those systems either require drivers to indicate their availability on the mobile app, then receive delivery offers when they become available, or pick shifts that work for their schedule on a first-come first-serve basis. 
		- Shifts are usually posted well in advance, up to a week ahead, and additional on-demand shifts may be posted on the app throughout the day.
		- Such scheduling and matching is closest to traditional delivery services with a company’s own fleet, since **supply and capacity are more predictable.**
		- Some systems, such as Amazon Flex and Deliv [9], provide minimum pay guarantees for drivers, which means that drivers are promised to be paid a given minimum amount, even if they are not matched. Such programs further reduce uncertainty in supply and make the system closer to classical scheduling, matching and routing problems.
	- En-route matching (like ridesharing, with minimum deviation regarding time and path):
		- For this type of matching, drivers are matched with delivery requests that are on their way of a pre-planned trip.
		- A traveler or commuter indicates on the system’s mobile app the date, time, origin, and destination of an upcoming trip.
		- Then the app matches the traveler with delivery requests on his/her way, such that a maximum distance or time deviation of the original travel route is observed.
		- Such matching closely resembles ridesharing problems, which aim to match drivers with riders on their way, with a small possible deviation.
	- Bulletin-board type matching (requests are posted and drivers match themselves):
		- This refers to systems that simply post delivery requests and a driver picks requests that match his/her schedule and preference.
		- In such systems, no algorithm is used to automatically match drivers to delivery requests, and the matching is done mainly through the sharing of information.
		- Walmart Spark Delivery follows such a system, where orders, with their associated destination and delivery time window, are posted on the app, and drivers pick orders that they can fulfill.

- **Three main categories of compensation schemes**
	- Hourly compensation：
		- Amazon Flex manages the supply of drivers through its minimum pay guarantee program and centralized scheduling discussed earlier.
		- The predictability in the compensation scheme is appealing to drivers, as drivers like to secure income during their scheduled hours.
		- Combining its attractive compensation scheme with the centralized scheduling mechanism, ensures the balance of supply and demand at various times of the day.
		- A major challenge faced by a delivery system with an hourly compensation scheme is forecasting delivery needs and the number of drivers required to fulfill those deliveries, ahead of time.
		- To offset such an obstacle, Amazon Flex offers realtime on-demand delivery blocks for drivers, in case scheduled drivers are not enough to meet current demand.
		- Disadvantage: However, those on-demand time blocks come with a higher level of risk, as the availability of drivers is not guaranteed. This may in turn reduce the service level through increasing the percentage of demands not met by the promised delivery time.
	- Per-delivery compensation:
		- All other systems, with the exception of some systems in the category of manual bulletin-board-type matching, compensate drivers per completed delivery.
		- Those formulas may depend on some or all of the following factors: mileage, wait time, size of package, traffic, and parking.
		- The majority of systems under this payment scheme provide no payment guarantee for drivers, i.e. if a driver is available but is not matched with a delivery task, then he/she does not receive any payment.
		- Features: In general, for a system with a per-delivery compensation scheme and no payment guarantee, the availability of drivers and the maintenance of their loyalty are major challenges.
		- In other words, drivers would prefer more predictability in their schedule and in their earning potential. That is, if they were to earn much less than the advertised earning potential, they may choose not to participate in this delivery system which may lead to a shortage of driver supply.
		- This is especially true for platforms that often have multiple packages on a route delivered by the same driver. If he/she expects to deliver multiple packages, but gets only one or two, and is paid based on the number of packages, the resulting earnings may be significantly less than anticipated.
		- So, to overcome the inconvenience of short-notice and unpredictability, drivers would choose these systems if, from their experience, they do get matched frequently during their available time, and are compensated well.
	- Shipper and driver determine the compensation:
		- In some systems, a shipper and a buyer agree on a delivery price and the platforms receives a commission for matching them.
		- This payment scheme is offered by some bulletinboard type matching systems where individuals are the target market.
		- Platforms with such a compensation arrangement are typically community-based casual networks that do not deal with large numbers of daily deliveries.
		- One major challenge for such a system is that matching is not guaranteed, which may deem the system unreliable.

assume that drivers are in-store customers who are willing to make stops on their way home. This setting is not currently applied in practice, as none of the crowdsourced delivery platforms reviewed in Section 2 employ drivers that way.

![[Pasted image 20220824161353.png]]

👣➿👣