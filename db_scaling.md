                                                   ┌───────────────────┐
                                                   │  Database Scaling │
                                                   └───────────────────┘
                                                           │
                             ┌─────────────────────────────┼─────────────────────────────┐
                             │                                                       │
                  ┌──────────▼───────────┐                                     ┌────────▼─────────┐
                  │  Vertical Scaling    │                                     │ Horizontal Scaling│
                  │  (Scale Up)          │                                     │  (Scale Out)      │
                  └──────────────────────┘                                     └───────────────────┘
                             │                                                       │
                             │                                                       │
            ┌────────────────┼────────────┐                           ┌──────────────┼───────────────┐
            │                                 │                           │                             │
┌───────────▼────────────┐       ┌────────────▼────────────┐    ┌────────▼──────────────┐    ┌────────▼────────────┐
│ Database Partitioning  │       │ Data Replication        │    │ Horizontal Partitioning│    │ Database Sharding   │
└────────────────────────┘       └─────────────────────────┘    └──────────────────────┘    └──────────────────────┘
            │                               │                                  │                       │
 ┌──────────┼─────────────┐        ┌────────┼───────────────┐         ┌────────┼───────────────┐       │
 │          │             │        │        │               │         │        │               │       │
 │   Vertical Partitioning│   Synchronous   │   Asynchronous│  Key-based  │ Range-based│ Hash-based │ Geographic│
 │   (Column-based)       │   Replication   │   Replication │Partitioning │Partitioning│Partitioning │ Sharding  │
 │                        │                  │               │             │             │            │           │
 │       ┌──────────────┐ │                  │               │             │             │            │           │
 │       │ Column Split │ │                  │               │             │             │            │           │
 │       └──────────────┘ │                  │               │             │             │            │           │
 │                        │                  │               │             │             │            │           │
 │                        │                  │               │             │             │            │           │
 └────────────────────────┘                  │               │             │             │            │           │
 ┌──────────────────────────────────────────────────────────────────────────────────────────────────────────────┐
 │ Explanation                                                                                                   │
 │                                                                                                               │
 │ Database scaling methods can be divided into two main categories: vertical scaling (scaling up) and           │
 │ horizontal scaling (scaling out).                                                                            │
 │                                                                                                               │
 │ Vertical Scaling (Scale-Up): This involves increasing the capacity of a single database instance              │
 │ by adding more resources (CPU, memory, storage).                                                              │
 │                                                                                                               │
 │ Horizontal Scaling (Scale-Out): This involves distributing the load across multiple instances.                │
 │ Horizontal scaling includes strategies like partitioning and sharding, which are detailed below.              │
 │                                                                                                               │
 │ Database Partitioning: Dividing data within a database to optimize performance and manageability.             │
 │                                                                                                               │
 │ - Vertical Partitioning (Column-based): Splits data by columns for better storage efficiency                  │
 │   or query performance.                                                                                       │
 │ - Horizontal Partitioning (Row-based): Divides data into rows to spread the load across                       │
 │   multiple partitions.                                                                                        │
 │                                                                                                               │
 │ Data Replication: Creating copies of data across different nodes to improve fault tolerance                   │
 │ and redundancy.                                                                                               │
 │                                                                                                               │
 │ Database Sharding: A form of horizontal partitioning where data is divided across multiple                    │
 │ databases or servers (shards) based on specific criteria like geographic region or hashing                    │
 │ of keys.                                                                                                      │
 └──────────────────────────────────────────────────────────────────────────────────────────────────────────────┘
