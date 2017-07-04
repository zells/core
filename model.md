# zells Programming Model

This document describes the current programming model of *zells*. Please note that the programming platform and the model are under active development and likely to change.

## Zell

The programming model consisting of a single behavioural element, called `Zell`, with a single capability: to *receive* a `Signal`. Upon receiving a Signal, it is up to the Zell to decide how to react or whether to react at all.

	.-----------------.
	|       Zell      |
	|-----------------|
	|-----------------|
	| receive(Signal) |
	'-----------------'
	
## Signal

A `Signal` is a finite data stream of any content. The only requirement is that it can be interpreted correctly be the intended receiver.

	.-------------------.
	|       Signal      |
	|-------------------|
	|-------------------|
	| serialize():byte* |
	'-------------------'

## Dish

A `Dish` can be used to *transmit* a `Signal`. A copy of each transmitted `Signal` is received by every `Zell` of the `Dish`es culture simultaneously. A `Dish` that is connected to other `Dish`es transmits every `Signal` to all its *peers*.

	.------------------.
	|       Dish       |
	|------------------|
	| culture:Zell*    |
	| peers:Dish*      |
	|------------------|
	| transmit(Signal) |
	'------------------'
