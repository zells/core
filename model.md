# zells Model

This document describes the structure and semantics of the *zells* programming model, named *qi*. Thoughts and motivation behind it can be found [here](http://blog.rtens.org/a-unified-computing-model.html).

The model consists of *composable*, *dynamic*, *concurrent*, *abstractable* and *distributed* objects, called *cells*. The semantics of the model are defined by these properties.


## Composable

A cell can contain any number of other cells as children. Each *child* has a name that is unique amongst its siblings. 

```text
Child := <symbol>+
```

This forms a tree where each cell is a node and can therefore be addressed by a *path* containing the *names* of each child cell.
   
```text
Path := Name+
Name := Child
```

To move up in the tree, a path can also contain a reference to the *parent* of a cell as well as the *root* of the tree.

```text
Name := Child|<parent>|<root>
```
   
### Example
    
Given the following tree structure

```text
      °
     / \
    A   B
    |   |
    C   D
```

The canonical path of `D` is `°.B.D` where `°` denotes the root and `.` separates two names. A path from `C` to `D` would be `^.^.B.D` where `^` denotes the parent.



## Dynamic

A cell may have dynamic behaviour in the form of a *reaction* which is executed every time the cell receives a *message*. The message is always a single cell, referenced by a path relative to the sender.

```text
Message := Path
```

A reaction can contain any kind of behaviour, including sending messages to other cells.

### Example

Given the following cell structure.

```text
       °
     / | \  
    A  B  C
```

If the reaction of `A` is to send `B` to `C` (written as `<receiver> <message>`),

```text
°.C °.B
```

then every time `A` receives any message, it will cause `°.B` to be sent to `°.C`.



## Concurrent

All messages are received *concurrently* without any specific order. Furthermore, each message is sent by a *messenger* which will keep trying to deliver the message until it is received or the messenger decides it's not deliverable. This way, data flow can be synchronized without requiring a fixed order of execution. Therefore messages may be sent to cells before they exist.

### Example

When calculating `2 * 3 + 4 * 5`, the summation has to wait for both factors to complete calculation. The following diagram illustrates the case where the calculation of `2*3` is delayed. 

```text
a = 2*3       ##
b = 4*5  ##
c = a+b  ~~~~~~~###
         ----------->t
```

The summation waits (denoted by `~`) until the calculation of both factors is completed.



## Abstractable

Every cell has a *stem* cell from which it inherits its reaction and all children. Each inherited child and the reaction can be replaced by the *specialized* cell.

### Example

Given a cell `A` with a child `C`. If a cell `B` has `A` as stem, it inherits `C` (denoted by lower-case `c`). 
        
```text
    A<--B
    |   ¦
    C   c
```
      
If a message is sent to `B.C`, the reaction of `A.C` is executed in the *context* of `B.C` which means all paths will be resolved relative to `B.C`. 

If `A.C` has a child `D`, it is inherited as well.
    
```text
    A<--B
    |   ¦
    C   c
    |   ¦
    D   d
```



## Distributed

A cell can be distributed over multiple processes and machines. It is connected to a *peer* by sending it a *join* signal with information about how the peer can be reached. If a cell can't deliver a message, it will forward it to each of its peers in turn by sending them a *deliver* signal. If a peer can't deliver the message either, it responds with *failed*, otherwise with *received*. A peer is disconnected from a cell by sending a *leave* signal.

To be able to avoid endlessly forwarding messages in circular peer connections, a *deliver* signal contains a globally unique identifier. Messages are guaranteed to be delivered at most once, but there are no guarantees regarding the order of messages.

### Example

Given a cell `A` in the process with the ID `111`.

```text
      111
    +-----+
    |     |
    |  A  |
    |     |
    +-----+
```

If a new process (with the ID `222`) is created that contains also cell `A`, the signal `join A 222` is sent to process `111`. This adds a unidirectional connection from the cell in `111` to its peer int `222`.

```text
      111        222
    +-----+    +-----+
    |     |    |     |
    |  A~~~~~~~~~>A  |
    |     |    |     |
    +-----+    +-----+
```