# rabbitmq-queue-tutorials
This collection of .NET examples is prepared for learning RabbitMQ queue management and messaging patterns, based on the documentation available on the official RabbitMQ website.


## Hello World:
Send and receive messages from a named queue.
* Contains 2 console projects: Send and Receive.
* Clients can be run in any order, as both declares the queue.

```
cd Receive 
dotnet run
```

```
cd Send 
dotnet run
```

## Work Queues
Crated Work Queue that is used to distribute time-consuming tasks among multiple workers.
* Contains 2 console projects: Worker and NewTask.

```
# shell 1
cd Worker
dotnet run
# => Press [enter] to exit.
```

```
# shell 2
cd Worker
dotnet run
# => Press [enter] to exit.
```

```
# shell 3
cd NewTask
dotnet run "First message."
dotnet run "Second message.."
dotnet run "Third message..."
dotnet run "Fourth message...."
dotnet run "Fifth message....."
```
