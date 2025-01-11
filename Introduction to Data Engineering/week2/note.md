## Notes for week 2
1. If we were to arrange various aspects of data storage as a hierarchy, what should be the correct order of this hierarchy from the bottom to the top?
+ Bottom layer: Raw storage ingredients
+ Middle layer: Storage systems
+ Top layer: Storage abstractions

Explanation: The bottom layer of the hierarchy consists of the raw storage ingredients since all storage solutions are built on top of the physical ingredients like SSD and magnetic disks, along with processes like networking, serialization, and compression. The middle layer consists of storage systems like databases and object storage that are built on top of the raw ingredients. Then the top layer consists of the these storage systems arranged into storage abstractions like data warehouses, data lakes, and data lakehouses.