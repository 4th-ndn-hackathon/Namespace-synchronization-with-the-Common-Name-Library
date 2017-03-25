# Namespace-synchronization-with-the-Common-Name-Library
Namespace synchronization with the Common Name Library

## Use case

* A newspaper company at /com/newspaper
* Employees of the newspaper /com/newspaper/USER/alice, /com/newspaper/USER/bob
* Alice and Bob can announce new content for any department /com/newspaper/sports, /com/newspaper/politics
* ChronoSync broadcast prefix: /ndn/broadcast/namesync/com/newspaper
* ChronoSync application prefixes: /com/newspaper/USER/alice/namesync, /com/newspaper/USER/bob/namesync

The namesync application message contains a newline-separated list of name URIs. Example: 

Data name: /com/newspaper/USER/alice/namesync/1
Data content: 

/com/newspaper/sports/superbowl2017.html/%FD1111
/com/newspaper/sports/superbowl2017overview.html/%FD3333

