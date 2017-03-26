# Namespace-synchronization-with-the-Common-Name-Library
Namespace synchronization with the Common Name Library

## Use case

* A newspaper company at `/com/newspaper`
* Employees of the newspaper `/com/newspaper/USER/alice`, `/com/newspaper/USER/bob`
* Alice and Bob can announce new content for any department `/com/newspaper/sports`, `/com/newspaper/politics`
* A NameSync channel called `namesync/com/newspaper`.
* ChronoSync broadcast prefix: `/ndn/broadcast/namesync/com/newspaper` . ChronoSync sends `/ndn/broadcast/namesync/com/newspaper/<root hash>` .
* ChronoSync application prefixes: `/com/newspaper/USER/alice/namesync/com/newspaper/<random>`, `/com/newspaper/USER/bob/namesync/com/newspaper/<random>`

The namesync application message contains a JSON with a list of name URIs and a timestamp. Example: 

Data name: `/com/newspaper/USER/alice/namesync/com/newspaper/11894/1`

Data content: 

    {'names': ["/com/newspaper/sports/superbowl2017.html/%FD1111/%00",
               "/com/newspaper/sports/superbowl2017overview.html/%FD3333/%00"], 
     'timestamp': 4553988853 }
    

