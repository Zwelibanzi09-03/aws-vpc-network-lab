# VPC Network Lab Notes

## Overview

This project was focused on building a custom AWS VPC from scratch to understand how cloud networking works.

Instead of using the default VPC, everything was created manually to see how each component affects traffic flow.

---

## VPC Setup

- Created a VPC with CIDR block:
  10.0.0.0/16

This acts as the main private network for all resources.

---

## Subnets

Two subnets were created inside the VPC:

### Public Subnet
- CIDR: 10.0.1.0/24
- Intended for internet-facing resources

### Private Subnet
- CIDR: 10.0.2.0/24
- Intended for internal resources only

---

## Internet Gateway

- Created and attached an Internet Gateway to the VPC

This is what allows communication between the VPC and the internet.

Without this, nothing inside the VPC can access the internet.

---

## Route Table Configuration

Created a route table for public traffic:

- Default route:
  0.0.0.0/0 → Internet Gateway

This tells AWS that all internet-bound traffic should go through the Internet Gateway.

---

## Subnet Association

- Public subnet was associated with the public route table
- Private subnet was NOT associated

This is what makes the difference:

- Public subnet → has internet access  
- Private subnet → no internet access  

---

## Traffic Behavior Observed

- Resources in the public subnet can reach the internet
- Resources in the private subnet cannot reach the internet
- Internal traffic inside the VPC works through the local route

---

## Key Understanding

A subnet is NOT public because of its name.

It becomes public only if:
- it has a route to an Internet Gateway

---

## Why Private Subnet Matters

The private subnet is important for security.

It is used for:
- databases
- backend services
- internal systems

These should not be exposed to the internet.

---

## Lessons Learned

- VPC is the network boundary in AWS
- Subnets divide the network into smaller segments
- Route tables control where traffic goes
- Internet Gateway enables internet access
- Public vs private is controlled by routing, not naming

---

## Final Outcome

A working VPC setup where:
- Public subnet has internet access
- Private subnet remains isolated

This forms the base for building secure cloud architectures.
