Content-Type: text/x-zim-wiki
Wiki-Format: zim 0.4
Creation-Date: 2016-10-19T08:45:41+01:00

###### Actor Pattern ######
Created Wednesday 19 October 2016

Wikipedia: "The actor model in computer science is a mathematical model of concurrent computation that treats \"actors\" as the universal primitives of concurrent computation"

Actors react to messages received
	make local decisions
	create more actors
	send more messages
	determine how to respond to the next message
	
Actors can modify private state but only affect each other through messages

#### Fundamental concepts ####

Philosopy that everything is an actor. (Similar to OOP where everything is an object)

An actor is a computational entity that, in response to a message it receives can concurrently:
	send a finite number of messages to other actors
	create a finite number of new actors
	designate the behaviour to be used for the next message it receives.
	
No assumed sequence to the above actions, and could be in parallel

Decouple sender from communications sent

Recipients addressed by address, "mailing address"
actor can only communicate with actors whos addresses it knows

