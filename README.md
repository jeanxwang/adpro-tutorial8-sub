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
