# Namespace-synchronization-with-the-Common-Name-Library
Namespace synchronization with the Common Name Library

The hackathon code went into the following fork of the Common Name Library which was merged back into the main repository

https://github.com/4th-ndn-hackathon/PyCNL

## Use case

* A newspaper company at `/com/newspaper`
* Employees of the newspaper `/com/newspaper/USER/alice`, `/com/newspaper/USER/bob`
* Alice and Bob can announce new content for any department `/com/newspaper/sports`, `/com/newspaper/politics`
* A NameSync channel called `namesync/com/newspaper`.
* ChronoSync broadcast prefix: `/ndn/broadcast/namesync/com/newspaper` . ChronoSync sends `/ndn/broadcast/namesync/com/newspaper/<root hash>` .
* ChronoSync application prefixes: `/com/newspaper/USER/alice/<random>`, `/com/newspaper/USER/bob/<random>`

The namesync application message contains a JSON with a list of name URIs and a timestamp. Example: 

Data name: `/com/newspaper/USER/alice/11894/1`

Data content: 

    {'names': ["/com/newspaper/sports/superbowl2017.html/%FD1111/%00",
               "/com/newspaper/sports/superbowl2017overview.html/%FD3333/%00"], 
     'timestamp': 4553988853 }
    

