## Notes for week 2
1\. If we were to arrange various aspects of data storage as a hierarchy, what should be the correct order of this hierarchy from the bottom to the top?
+ Bottom layer: Raw storage ingredients
+ Middle layer: Storage systems
+ Top layer: Storage abstractions

Explanation: The bottom layer of the hierarchy consists of the raw storage ingredients since all storage solutions are built on top of the physical ingredients like SSD and magnetic disks, along with processes like networking, serialization, and compression. The middle layer consists of storage systems like databases and object storage that are built on top of the raw ingredients. Then the top layer consists of the these storage systems arranged into storage abstractions like data warehouses, data lakes, and data lakehouses.

2\. Availability, often referred to as uptime, is the percentage of time a service is expected to be in an operable state.

3\. What does the term "durability" refer to in the context of data systems?
+ Durability refers to the ability of a storage system to withstand data loss.

4\. RTO is the maximum acceptable time for a service outage, while RPO defines the acceptable state after recovery.

5\. Zero trust requires authentication for every action, while hardened perimeter security relies on a physical barrier.