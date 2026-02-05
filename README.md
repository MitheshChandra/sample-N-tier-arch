**AWS Three Tier Web Architecture**

**Description:**

Built a secure, scalable three‑tier architecture with network, security, application, and database layers.
Implemented both manual setup and Infrastructure as Code (IaC) options for flexibility and repeatability.
Ensured high availability and scalability through optimized configurations across all tiers.

**Architecture Overview**

<img width="941" height="640" alt="image" src="https://github.com/user-attachments/assets/7e1bdf97-7cb6-4289-aa56-cbea7fa94e3c" />


In this architecture, a public-facing Application Load Balancer forwards client traffic to our web tier EC2 instances. The web tier is running Nginx webservers that are configured to serve a React.js website and redirects our API calls to the application tier's internal facing load balancer. The internal facing load balancer then forwards that traffic to the application tier, which is written in Node.js. The application tier manipulates data in an Aurora MySQL multi-AZ database and returns it to our web tier. Load balancing, health checks and autoscaling groups are created at each layer to maintain the availability of this architecture.

