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
