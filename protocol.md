# zells Protocol

**[work in progress]**

This document describes the *zells* protocol for delivering messages between nodes.

## Signals

- DELIVER: delivery (context, target, message, role)
- RECEIVED: path
- OK
- FAILED: reason
- JOIN: path, connection (e.g. host:port)
- LEAVE: path

## Syntax

- path
- escaping