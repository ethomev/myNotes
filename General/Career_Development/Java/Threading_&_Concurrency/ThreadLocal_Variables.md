Content-Type: text/x-zim-wiki
Wiki-Format: zim 0.4
Creation-Date: 2015-08-12T20:10:14+01:00

###### ThreadLocal Variables ######
Created Wednesday 12 August 2015

Each thread has it's own instance of a ThreadLocal variable
Typically private static fields in a class which associate state with a thread.
A thread local variable value is assigned the first time the .get method is invoked.
	Override the initialValue method when creating the instance of Thread local to do your own thing
