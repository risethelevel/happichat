# Chat design.
# Non functional requirements.
- Number of message per day supported initally? 1M messages, average size= 500kb, storage need = 1M * 500k.
- Low latency: Users should be able to receive messages with low latency.
- Strict ordering: message should be arrive to the user in order. 
- Availability: The system should be highly available. However, the availability can be compromised in the interest of consistency.
- Security: The system must be secure via end-to-end encryption.
- Scalability: The system should be highly scalable to support an ever-increasing number of users and messages per day.