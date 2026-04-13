# AWS VPC Network Lab

## Overview

This project demonstrates how to build a custom AWS Virtual Private Cloud (VPC) with public and private subnets, internet routing, and controlled traffic flow.

The setup was done from scratch to understand how networking components work together instead of relying on the default VPC.

---

## Project Goal

- Create a custom VPC
- Create public and private subnets
- Attach an Internet Gateway
- Configure route tables
- Control which subnet has internet access

---

## Tech Stack

- AWS VPC
- Subnets
- Internet Gateway
- Route Tables

---

## What Was Implemented

- Custom VPC (10.0.0.0/16)
- Public Subnet (10.0.1.0/24)
- Private Subnet (10.0.2.0/24)
- Internet Gateway attached to VPC
- Public route table with internet route
- Route table association for public subnet only

---

## Network Behavior

- Public subnet has internet access through Internet Gateway
- Private subnet has no internet route
- Internal communication within VPC is allowed

---

## Outcome

A working network structure where:
- Public resources can reach the internet
- Private resources remain isolated

---

## What I Learned

- How VPC defines network boundaries
- How subnets divide network space
- What makes a subnet public vs private
- How route tables control traffic flow
- Why isolation improves security
