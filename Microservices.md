# **.NET Microservices**

>[1. Microservices](#microservices) 
> 
>[2. Benefits of Microservices](#benefits-of-microservices) 
> 
>[3. Synchronous Messaging](#synchronous-messaging) 
>
>[4. Asynchronous Messaging](#asynchronous-messaging) 
>
>[5. RabbitMQ](#rabbitmq) 
>
>[6. gRPC](#grpc) 
>
>[7. Some Commands](#some-commands) 
>

---

### **Microservices**

- Small (2 pizza team, 2 weeks to build);
- Responsible for doing one thing well;
- Organisationally aligned;
- Form part of the (distributed) whole;
- Self-contained / Autonomous.

---

### **Benefits of Microservices**

- Easier to change & deploy (small and decoupled);
- Can be build using different technologies;
- Increased organisational ownership & alignment;
- Resilient: 1 service can break the, others will continue to run;
- Scalable: ,you can scale out only the services you need to;
- Build to be highly replaceable / swappable.

---

### **Synchronous Messaging**

- Request / Response Cycle;
- Requester will "wait" response;
- Eternally facing services usually synchronous (e.g. http requests);
- Services usually need to "know" about each other;
- We are using two forms:
    - Http;
    - gRPC.

---

### **Asynchronous Messaging**

- No Request / Response Cycle;
- Requester does not wait;
- Event model, e.g. publish - subscribe;
- Typically used between services;
- Event bus is often used (we will be using RabbitMQ);
- Services don't need to know about each other, just the bus;
- Introduces ots own range of complexitites - not a magic bullet.

---

### **RabbitMQ**

- A Message Broker - it accepts and forwards messages;
- Messages are sent by Producers (or Publishers);
- Messages are received by Consumers (or Subscribers);
- Messages are stored on Queues (essentially a message buffer);
- Exchanges can be used to add "routing" functionality;
- Uses Advanced Message Queuing Protocol (AMQP) & others.

---

### **gRPC**

- "Google" Remote Procedure Call;
- Uses HTTP/2 protocol to transport binary messages (inc. TLS);
- Focused on high performance;
- Relies on "Protocol Buffers" (aka Protobuf) to defined the contract between end points;
- Multi-language support (C# client can call a Ruby service);
- Frequently used as a method of service to service communication.

---

### **Some commands**

- ```mkdir CommandsService```
- ```mkdir PlatformService```