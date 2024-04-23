# Adpro - Tutorial 8

## Aliyah Faza Qinthara (2206024726)

### What is AMQP?

The Advanced Message Queuing Protocol (AMQP) is an open standard for passing business messages between applications or organizations. It connects systems, feeds business processes with the information they need, and reliably transmits onward the instructions that achieve their goals. AMQP is a binary application layer protocol, designed to efficiently support a wide variety of messaging applications and communication patterns.

### What does `guest:guest@localhost:5672` mean?

This is a connection string used to connect to a RabbitMQ server (or any other server that uses the AMQP protocol). The format is `username:password@hostname:port`.
- The first `guest` is the username for authentication.
- The second `guest` is the password for authentication.
- `localhost` is the hostname of the server. In this case, it's the local machine.
- `5672` is the port number on which the RabbitMQ server (or any other AMQP server) is listening.

### RabbitMQ

![Quick cargo runs](https://cdn.discordapp.com/attachments/1030834426126544907/1232341676081676358/image.png?ex=66291b1f&is=6627c99f&hm=a220f98f50e787a8b5df68b70b8860a6ba913e3b69dceb6634171aade7ef8344&)
The total number of queue is around 25. This happens because the subscriber needs more time to handle each event in the message queue, resulting in a buildup of messages. This is due to the publisher publishing messages faster than the subscriber can process them.

![Three subscribers](https://cdn.discordapp.com/attachments/1030834426126544907/1232345087523164373/image.png?ex=66291e4c&is=6627cccc&hm=6e790be6073eabf148ed677056de7d435666ba08e231d1002b38aba476e12464&)
![Three consoles](https://cdn.discordapp.com/attachments/1030834426126544907/1232345863083393055/image.png?ex=66291f05&is=6627cd85&hm=d9e03095f213aac9dfd5865483086fd2851769573ce455da1a3cdaf9e5416c38&)

The image shows that each subscriber gets unique data from the message queue when the publisher sends a large amount of data. Each subscriber is independent, so once a message is retrieved, it disappears from the queue. Also, making the subscriber application multithreaded could improve its ability to process multiple events simultaneously.
