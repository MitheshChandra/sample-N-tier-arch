**AWS Three Tier Web Architecture**

**Description:**

Built a secure, scalable three‑tier architecture with network, security, application, and database layers.
Implemented both manual setup and Infrastructure as Code (IaC) options for flexibility and repeatability.
Ensured high availability and scalability through optimized configurations across all tiers.

**Architecture Overview**

<img width="1032" height="694" alt="AWS Archi" src="https://github.com/user-attachments/assets/c1846372-839f-462e-aa39-6f1c3f866304" />

In this architecture, a public-facing Application Load Balancer forwards client traffic to our web tier EC2 instances. The web tier is running Nginx webservers that are configured to serve a React.js website and redirects our API calls to the application tier's internal facing load balancer. The internal facing load balancer then forwards that traffic to the application tier, which is written in Node.js. The application tier manipulates data in an Aurora MySQL multi-AZ database and returns it to our web tier. Load balancing, health checks and autoscaling groups are created at each layer to maintain the availability of this architecture.

