# zells Protocol

**[work in progress]**

This document describes the *zells* protocol for delivering messages between nodes.

## Signals

- DELIVER <context:Path> <target:Path> <receiver:Path> <message:Path> <guid:String>
- RECEIVED
- FAILED <reason:String>
- JOIN <path:Path> <connection:String>
- LEAVE <path:Path> <connection:String>
- OK

## Syntax

- Path := <Name>[.<Name>]
- Name := Child|<Parent>|<Root>
- Parent := ^
- Root := *
- Child := any symbol, escaped with double quotes
