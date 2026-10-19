# Cloud-Based Payment Processing Platform

An AWS SAA C03 learning experience designed to get hands-on experience in designing, configuring, and securing a minimum-viable-product cloud platform to support my studies.

## Problem Statement
A fictional payment technology company intends to develop a payment-processing platform that enables merchants to submit card transactions for authorisation.  
The platform must accept payment requests, communicate with a simulated acquiring or issuing bank interface, and return an authorisation response to the merchant.  
Develop a Python application applied to a subset of PCI DSS requirements to assess AWS configurations.  

## Mission Statement
Design and implement a small, demonstrable payment-processing proof of concept that:
1.	Accepts a payment request from a merchant-facing interface.
2.	Passes the request through a simplified payment-processing workflow.
3.	Obtains a simulated authorisation response from a bank service.
4.	Returns an approval or decline response to the merchant.
5.	Uses a Python-based assessor to inspect selected AWS configuration and report security findings.

## Scope and limitation
Payment processing, banking and authorisation will be simulated.  
No real funds, payment cards or cardholder data will be processed.  
Contactless, physical-card and online payments are represented by a single merchant-facing payment request in the MVP.  
The cloud architecture and security controls will be designed with relevant PCI DSS requirements in mind, without claiming PCI DSS compliance or certification.  
The security assessor will evaluate only explicitly supported checks and will document their evidence, limitations and requirement mappings.
