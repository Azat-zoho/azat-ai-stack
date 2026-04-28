# Legacy Architecture Diagram

```
+-----------------------------------------------------------+
|                    AWS (us-east-1)                        |
|                                                           |
|  +------------+  +------------+  +--------------------+  |
|  |   EC2 #1   |  |   EC2 #2   |  |   EC2 #3-#12       |  |
|  |  (App A)   |  |  (App B)   |  |  (App C + misc)    |  |
|  +-----+------+  +-----+------+  +----------+---------+  |
|        |               |                    |            |
|  +-----+---------------+--------------------+--------+   |
|  |              RDS PostgreSQL                        |   |
|  |          (single instance, no replicas)            |   |
|  +----------------------------------------------------+   |
|                                                           |
+-----------------------------------------------------------+
                        |
            +-----------+-----------+
            |  Chicago Co-Lo Rack   |
            |  4x Bare-metal servers|
            |  (MySQL + legacy APIs)|
            +-----------------------+
```

> Deployments: Engineer SSHs into each server, runs rsync, restarts service manually.
> No load balancer. No auto-scaling. No containers.
