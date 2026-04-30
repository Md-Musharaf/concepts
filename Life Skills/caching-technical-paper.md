# Caching And Its Approaches

## Caching

Caching is a technique used to store frequently accessed data in a faster storage layer, allowing future requests to be served quickly without requiring recomputation or repeated database access. Due to repeated database queries and high request load, performance and scaling issues occur. Implementing caching reduces the need to fetch data from slower systems, such as databases, and improves response time while reducing server load.

#### There are multiple caching approaches that can be applied based on system requirements :-

### 1. In-Memory Caching
It is a caching technique where data is stored directly in a system’s RAM (main memory) instead of slower storage like disks or databases.
When an application frequently needs certain data (like user sessions, API responses, or database results), it keeps that data in memory so it can be accessed almost instantly instead of fetching it again from a slower source. Ex: Redis, Memcached etc.



### 2.  Distributed Caching
It is a technique that stores frequently accessed data across multiple servers (nodes) in a network, rather than confining it to a single machine. This architecture allows applications to scale horizontally, handle massive workloads, and maintain high availability by ensuring that the failure of one node does not result in data loss or service interruption. Ex: Redis Cluster.

### 3. Database Caching
It is a technique used to reduce the load on a database by storing frequently accessed data in a faster storage layer (like memory). Instead of querying the database every time, the application first checks the cache. If the data is found (cache hit), it is returned immediately; otherwise (cache miss), the data is fetched from the database and stored in the cache for future use. Ex: E-commerce App

### 4. Application-Level Caching
It means caching data inside the application itself (in code or app layer) instead of relying only on the database or external systems. The application decides what to cache, when to cache, and when to refresh it. The app keeps frequently used data in memory so it doesn’t need to repeatedly call the database or external APIs.

### 5. Content Delivery Network (CDN) Caching
It is a technique where static or semi-static content (like images, videos, CSS, JavaScript files) is stored on servers distributed across different geographic locations. These servers are called edge servers. Instead of fetching content from the main server every time, users get it from the nearest CDN server, which makes loading much faster. Ex: Cloudflare, Amazon Web Services etc.

### 6. Browser Caching
It is when a user’s web browser stores website resources locally (on their device), so it doesn’t need to download them again on every visit. The browser “remembers” parts of a website to make future loads much faster.

#### By adopting an appropriate caching strategy, the system can achieve better performance, reduced latency, and improved scalability under high traffic conditions.

## References
* https://medium.com/@yaroslavzhbankov/caching-essentials-types-strategies-and-best-practices-459493cc47d9
* https://redis.io/docs/
* https://memcached.org/
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Caching
* https://www.cloudflare.com/learning/cdn/what-is-caching/
* https://aws.amazon.com/caching/
* https://chatgpt.com/
