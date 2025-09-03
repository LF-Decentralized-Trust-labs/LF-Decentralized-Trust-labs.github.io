---
layout: default
title: Payments Performance Test Harness
parent: Archived Labs
---
# Lab Name
Payments Performance Test Harness.

# Short Description
This is a test harness designed to measure the performance of payments
between peers on a blockchain network.
This performance is measured against the Emerald benchmark which is
specified here:

https://gitlab.com/emerald-platform/emerald/wikis/Emerald-Benchmark

# Scope of Lab

## Overview

The test harness should be able to measure the performance of a simple payments
network on a number of different blockchain platforms.

## Why Payments?

Choosing a payments use case enables to not only compare the performance of a
variety of blockchain plaforms but also compare against existing payment
platforms and networks.

## Definition of the payments network

The simple payment network consists of the following:

* A defined number of blockchain nodes/peers.
* Each node has a number of 'accounts' in which they can store tokens.
* Each node issues and sends tokens from its accounts to an account on a random peer/node other than itself.

## Use cases supported by the underlying blockchain platform

In order for the test harness to measure the performance of a blockchain
payents platform. The platform must support the following use cases:

* Create several accounts that can store tokens
* Issue tokens to specific accounts
* Transfer tokens from account to account between nodes.

The third use case is what is measured by this benchmark.

The overall scope is to have a ready made test harness which blockchain
developers can use to test and tune their own payment solutions.

## Integration with Hyperledger projects.

An example test harness has been written in javascript that currently
calls a Corda implementation of the payments network.
The goal of this lab is to generalise this code so that it will
work with all of the Hyperledger blockchain platforms in the Hyperledger
project and if appropriate plug into the Caliper test harness.

## What does the current test harness do to measure performance?

The performance benchmark test sends batches of payments to random nodes in the payments network.
The benchmark aims to find a stable latency between batches and constantly adjusts a target value to gradually find the optimum latency. This adjustment is 'smoothed' by a latency adjustment parameter so that we don't overload the nodes with too many payments too soon - think of it like turning up your central heating and waiting for the thermostat to click off at the target temperature.
The 'batching' is designed so that we can measure parallel throughput as well as latency.
For this reason we set up a number of test accounts and load each account with 1 million tokens. We then send a payment from each of the test accounts in each batch. We wait for the latency time to elapse before sending the next batch.
An instance of the test harness runs against each node in the network and measures the end to end latency by recording the submission time and listening to received payments - this makes it quite different from a jmeter test where there is only usually one instance of the test harness.

# Initial Committers
- https://github.com/Bartman250

# Lab Sponsor
Mark Wagner: chair of performance and scale WG & TSC member

