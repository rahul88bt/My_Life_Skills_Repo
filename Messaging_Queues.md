# Messaging Queues

Messaging queues are a form of asynchronous communication between software systems or components. They act as intermediaries, allowing different applications to exchange messages without requiring them to be directly connected or synchronized. When a message is sent to a queue, it is stored until the receiving system or component is ready to process it.


## Messaging queues are used in various scenarios

    1.Decoupling: By separating the sender and receiver, queues let each one work independently and at its own pace. By allowing components to continue operating even when others are temporarily unavailable, this decoupling increases system reliability.

    2.Queues can balance the processing load across a number of users. Messages are automatically distributed across the subscribed instances of a service, allowing for scalable and effective processing, when many instances of a service join a queue.

    3.Fault tolerance: If a component malfunctions while processing a message, the message remains in the queue and may be retried at a later time. As a result, fault tolerance and message longevity are assured.

    4.Prioritization: A queue of messages can be arranged in order of importance or urgency. For improved timeliness, high-priority communications can be processed before low-priority ones.


## Popular tools for implementing messaging queues:

    1.RabbitMQ: An open-source message broker that supports multiple messaging protocols, including Advanced Message Queuing Protocol (AMQP) and Message Queuing Telemetry Transport (MQTT).

    2.Apache Kafka: A distributed event streaming platform that provides high-throughput, fault-tolerant messaging. Kafka is commonly used for real-time data streaming and processing.

    3.Amazon Simple Queue Service (SQS): A fully managed message queuing service offered by Amazon Web Services (AWS). It provides scalable and reliable messaging with pay-as-you-go pricing.

    An architectural design pattern called business Message Bus (EMB) offers a framework for linking different software components within a business. By utilizing a centralized communication network known as the message bus, it makes it easier for communication across various apps.


The message bus serves as a central node for connecting apps to route messages. Regardless of the underlying technology or platforms, it offers a standardized method for applications to communicate. The bus ensures flexible coupling between parts, enabling independent development.

Message queues are often used as the foundational communication method in EMB. Applications can now publish messages to the bus, which are then forwarded to subscribers who are interested in receiving them. This design pattern supports a variety of communication methods, including publish-subscribe, request-response, point-to-point messaging, and event-driven architectures.


## Some popular EMB implementations:

    1.Apache ActiveMQ: An open-source message broker that provides messaging capabilities for implementing an EMB.

    2.IBM MQ: A messaging middleware that supports EMB patterns and provides enterprise-grade messaging services.

    3.Microsoft BizTalk Server: A comprehensive integration platform that incorporates EMB principles, enabling seamless integration between diverse applications and systems.

    4.Enterprise Message Buses offer benefits such as decoupling, scalability, and extensibility, making them valuable for building complex, interconnected enterprise architectures.


Apache ActiveMQ, an open-source message broker that supports EMB implementations, is another well-liked messaging queue technology. Message persistence, message filtering, and support for numerous messaging protocols are just a few of the features that ActiveMQ has to offer. It supports both more sophisticated communications patterns like virtual destinations and message groups as well as more conventional ones like point-to-point and publish-subscribe. ActiveMQ may be integrated with several programming languages and frameworks thanks to its adaptable architecture, making it appropriate for a variety of applications.

When implementing messaging queues, it's essential to consider factors like message durability, message acknowledgment, and error handling. Messages can be persisted to disk to ensure durability, allowing them to survive system failures. Acknowledgments provide confirmation that a message has been received and processed, ensuring reliable message delivery. Error handling mechanisms, such as dead-letter queues, enable the handling of messages that couldn't be processed successfully.

Enterprise Message Buses and messaging queues have become fundamental components in modern distributed systems. They enable efficient and reliable communication between different parts of an enterprise architecture, facilitating scalability, fault tolerance, and flexibility. By leveraging these tools and patterns, organizations can build robust and loosely coupled systems that can adapt to changing requirements and seamlessly integrate various applications and services.


* RabbitMQ: https://www.rabbitmq.com/
* Apache ActiveMQ: http://activemq.apache.org/
* IBM MQ: https://www.ibm.com/products/mq
* Microsoft BizTalk Server: https://docs.microsoft.com/en-us/biztalk/core/biztalk-server-overview
