# Distributed systems

## Rules of thumb

- Design for failure: Assume everything will fail, implement timeouts, retries, and circuit breakers
- Embrace eventual consistency: Do not expect immediate, global consistency
- Optimize data transfer: Reduce serialization costs and minimize bandwidth usage
- Secure everything: Assume the network is hostile

## Fallacies

### The network is reliable

- Networks fail, packets drop, and hardware breaks
- Implement strict timeouts so services don't stall indefinitely
- Use exponential backoff with jitter for retries to avoid overwhelming an already struggling network
- Monitor service health and temporarily stop sending requests to a failing service to prevent cascading failures across the system (circuit breaker)
- Use message queues (e.g., RabbitMQ, Kafka) to store messages temporarily until the receiving service is online
- Ensure that retrying a request (like a payment) multiple times results in only one actual operation (idempotency)

### Latency is zero

- Network distance and speed of light introduce unavoidable delays
- Store frequently accessed data in-memory (Redis) or closer to users via Content Delivery Networks (CDNs) to minimize round-trip times (caching)
- Instead of making multiple "chatty" calls to access individual properties, pack all necessary data into a single request to pay the latency penalty only once (data transfer objects \[DTOs\])
- Don't block the main application thread; acknowledge the request immediately and process the long-running task in the background (asynchronous processing)

### Bandwidth is infinite

- Data, especially in microservices, can overwhelm network capacity
- Use algorithms like GZIP or Brotli to reduce payload sizes before transmission (data compression)
- Replace verbose formats like XML with compact binary formats like Protocol Buffers (Protobuf) or Avro (effizient serialization)
- Control the flow of data to prevent any single service from hogging all available network capacity (throttling, rate limiting)

### The network is secure

- Assuming security without implementing it leads to vulnerabilities like broken access controls
- Assume no entity is automatically trusted; every request must be authenticated and authorized, even within the internal network (zero trust)
- Always encrypt data in transit to protect it from interception (TLS)
- Implement multiple security layers across the network, infrastructure, and application levels

### Topology doesn't change

- Network configurations and infrastructure change constantly
- Use tools like Consul, ZooKeeper, or Kubernetes services to dynamically locate resources instead of hardcoding IP addresses (service discovery)
- Regularly test system resilience by intentionally shutting down nodes (e.g., using Netflix's Chaos Monkey) to ensure the system can handle unexpected topology changes

### There is one administrator

- Multiple teams or organizations often manage different parts of a system
- Establish shared standards for logging, monitoring, and security across all teams (centralized governance)
- Use tools like Terraform or CloudFormation to ensure consistent configurations across environments managed by different people (infrastructure as code \[IaC\]

### Transport cost is zero

- Moving data incurs financial costs (e.g., cloud egress fees) and resource overhead (serialization)
- Deploy services and data in the same cloud region or availability zone to minimize egress fees and transfer overhead (data localization)
- Minimize CPU costs by choosing high-performance serialization libraries

### The network is homogeneous

- Networks consist of diverse hardware, protocols, and operating systems
- Use interoperable standards (e.g., REST, JSON, gRPC) to ensure different hardware and operating systems can communicate (standard protocols)
- Use Docker and Kubernetes to provide a consistent execution environment regardless of the underlying hardware (containerization)

### The system is monolithic

- Components fail independently
- Use Bulkheads to isolate resources (CPU, memory, threads) so a failure in one service doesn't starve others
- Implement loose coupling through asynchronous communication (queues/events) to ensure services can function independently when their peers are down

### The system is fully observable

- Debugging across many services is difficult
- Implement the _three pillars of observability_:
  - Distributed tracing: Use tools like OpenTelemetry to track a single request's path across multiple service boundaries
  - Centralized logging & metrics: Aggregate data into platforms like Grafana or the ELK stack to detect system-wide patterns

### The system is always on

- Maintenance and updates cause downtime

### There is one root cause

- In complex systems, failures are rarely caused by a single bug but rather by a "perfect storm" of overlapping minor issues
- Complex, cascading failures are common
- Adopt chaos engineering (e.g., Gremlin or Chaos Monkey) to proactively inject failures and find hidden dependencies
- Shift from "finding the culprit" to Post-Mortem Analysis focused on system-wide resilience improvements

### Versionings is easy

- Managing API changes across services is complex
- Assuming you can update one service without impacting others leads to "dependency hell" or broken integrations
- Follow semantic versioning and maintain backward compatibility for at least one version
- Use consumer-driven contract testing to ensure changes in a provider service don't break the specific expectations of its consumers

### Compensating updates always work

- Relying on "undo" operations (like in the Saga Pattern) to maintain data consistency assumes those cleanup tasks themselves won't fail
- Design for eventual consistency and use idempotent operations so that if a compensating update needs to be retried, it doesn't cause further data corruption

## Further reading

- [https://github.com/donnemartin/system-design-primer](https://github.com/donnemartin/system-design-primer)
- [https://news.ycombinator.com/item?id=17683844](https://news.ycombinator.com/item?id=17683844)
- [https://github.com/theanalyst/awesome-distributed-systems](https://github.com/theanalyst/awesome-distributed-systems)
- [https://github.com/Sairyss/system-design-patterns](https://github.com/Sairyss/system-design-patterns)
- [https://blog.bytebytego.com/p/scalability-patterns-for-modern-distributed](https://blog.bytebytego.com/p/scalability-patterns-for-modern-distributed)
- [https://github.com/papers-we-love/papers-we-love/blob/main/distributed_systems/README.md](https://github.com/papers-we-love/papers-we-love/blob/main/distributed_systems/README.md)
- [https://github.com/heidihoward/distributed-consensus-reading-list](https://github.com/heidihoward/distributed-consensus-reading-list)
- [https://dancres.github.io/Pages/](https://dancres.github.io/Pages/)
- [https://henryr.github.io/distributed-systems-readings/](https://henryr.github.io/distributed-systems-readings/)
- [https://gist.github.com/dominictarr/e804626e0bc4a75e9aa3](https://gist.github.com/dominictarr/e804626e0bc4a75e9aa3)

## Credits

- [https://learncloudnative.com/blog/2019-11-26-fallacies_of_distributed_systems](https://learncloudnative.com/blog/2019-11-26-fallacies_of_distributed_systems)
- [https://en.wikipedia.org/wiki/Fallacies_of_distributed_computing](https://en.wikipedia.org/wiki/Fallacies_of_distributed_computing)
- [https://blogs.oracle.com/developers/fallacies-of-distributed-systems](https://blogs.oracle.com/developers/fallacies-of-distributed-systems)
- [https://blog.bytebytego.com/p/top-strategies-to-improve-reliability](https://blog.bytebytego.com/p/top-strategies-to-improve-reliability)
- [https://betterengineers.substack.com/p/handling-failures-in-distributed](https://betterengineers.substack.com/p/handling-failures-in-distributed])
- [https://sookocheff.com/post/distributed-systems/unpacking-the-eight-fallacies-of-distributed-computing/](https://sookocheff.com/post/distributed-systems/unpacking-the-eight-fallacies-of-distributed-computing/)
- [https://www.thoughtworks.com/en-us/insights/podcasts/technology-podcasts/three-new-fallacies-distributed-computing](https://www.thoughtworks.com/en-us/insights/podcasts/technology-podcasts/three-new-fallacies-distributed-computing)
