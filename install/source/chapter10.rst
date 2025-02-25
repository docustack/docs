###################################################
Add additional CentreStack servers to the cluster
###################################################
Adding an additional CentreStack server is as simple as installing the first CentreStack server. Run the CentreStack server installation program on another server, specifying the same database as the first server in the cluster.

.. warning::
    Adding additional CentreStack servers to an existing cluster is optional. 

    If you only have a few hundred users, you don't need to have a 
    second node from a scalability perspective. The scalability
    point of adding a second CentreStack Server is at 1000 users. 
    For best practices, you will
    always scale vertically first such as making a 2-CPU machine into a
    4-CPU machine and add RAM to the CentreStack Server before
    scaling horizontally by adding more CentreStack Servers.
    
    However, from a high availability(HA) perspective, you may want to 
    have a second CentreStack Server.

.. warning::    
    An external database server should be deployed if you are scaling out the cluster to more than one CentreStack server. The "all-in-one" deployment with a local MySQL database is not intended to be used for scaling out or high availability.

.. warning::    
    A hardware or software load balancer will be required if more than one CentreStack server is deployed in a cluster.

.. warning::
    All CentreStack servers in the same cluster must use the same time zone.