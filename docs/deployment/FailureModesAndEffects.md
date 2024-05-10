# Failure Modes and Effects Analysis

## Purpose

This analysis is intended to provide a detailed view of the possible failure modes and effects of the system with recommendations on how to mitigate them.  This document is intended to be used by product managers, architects, and engineering leaders to ensure that resiliency is built into the system.  Over time, root cause analysis of production incidents can be used to identify and mitigate new and additional failure modes.  The artifacts in the failure modes and effects analysis are at the `sea` level of abstraction.

**Note:** The calculation for the Risk Priority Number (RPN) is `RPN = Severity × Occurrence × Detection`.

## Electivity

This section is considered:  **Optional**

## Functional Failure Modes

| Failure Mode | Effects of Failure | Severity Rating | Occurrence Rating | Detection Rating | Risk Priority Number (RPN) |
|:---|:---|:---|:---|:---|:---|
| Transaction Processing Failure | <ul><li>Financial Loss for Customers</li><li>Legal and Regulatory Consequences</li><li>Customer Frustration and Discontent</li><li>Loss of Data Integrity</li><li>Operational Disruption</li></ul> | *8* | *5* | *7* | **280** |
| User Interface Error | <ul><li>Customer Frustration and Discontent</li><li>Loss of Data Integrity</li></ul> | *7* | *4* | *8* | **224** |
| Incorrect Account Balances | <ul><li>Financial Loss for Customers</li><li>Loss of Trust and Reputation</li><li>Legal and Regulatory Consequences</li><li>Customer Frustration and Discontent</li><li>Loss of Data Integrity</li><li>Operational Disruption</li><li>Negative Publicity</li></ul> | *8* | *5* | *6* | **240** |

## Non-Functional Failure Modes

| Failure Mode | Effects of Failure | Severity Rating | Occurrence Rating | Detection Rating | Risk Priority Number (RPN) |
|:---|:---|:---|:---|:---|:---|
| Server Downtime | <ul><li>Loss of Trust and Reputation</li><li>Customer Frustration and Discontent</li><li>Customer Frustration and Discontent</li><li>Loss of Data Integrity</li><li>Operational Disruption</li></ul> | *9* | *7* | *6* | **378** |
| Network Connectivity Issues | <ul><li>Loss of Trust and Reputation</li><li>Customer Frustration and Discontent</li><li>Operational Disruption</li></ul> | *7* | *6* | *5* | **210** |
| Payment Gateway Failure | <ul><li>Financial Loss for Customers</li><li>Loss of Trust and Reputation</li><li>Legal and Regulatory Consequences</li><li>Customer Frustration and Discontent</li><li>Operational Disruption</li></ul> | *9* | *7* | *6* | **378** |
| Software Bugs | <ul><li>Financial Loss for Customers</li><li>Customer Frustration and Discontent</li><li>Loss of Data Integrity</li></ul> | *8* | *5* | *7* | **280** |

## Security Failure Modes

| Failure Mode | Effects of Failure | Severity Rating | Occurrence Rating | Detection Rating | Risk Priority Number (RPN) |
|:---|:---|:---|:---|:---|:---|
| Data Breach | <ul><li>Financial Loss for Customers</li><li>Loss of Trust and Reputation</li><li>Legal and Regulatory Consequences</li><li>Customer Frustration and Discontent</li><li>Loss of Data Integrity</li><li>Operational Disruption</li><li>Negative Publicity</li></ul> | *10* | *6* | *5* | **300** |
| Unauthorized Access | <ul><li>Financial Loss for Customers</li><li>Loss of Trust and Reputation</li><li>Legal and Regulatory Consequences</li><li>Customer Frustration and Discontent</li><li>Loss of Data Integrity</li><li>Operational Disruption</li><li>Negative Publicity</li></ul> | *10* | *6* | *5*  | **300** |

## Prioritized Actions

Based on the RPN, these are the prioritized actions to mitigate the highest risks:

1. Implementing robust cybersecurity measures to prevent data breaches (e.g., encryption, multi-factor authentication).
2. Regularly testing and updating server infrastructure to minimize downtime.
3. Implementing intrusion detection systems and access controls to prevent unauthorized access.
4. Developing and implementing thorough testing procedures for transaction processing and software updates.
5. Improving user interface design and conducting usability testing to reduce errors.
6. Enhancing network redundancy and monitoring for connectivity issues.

## Implement Action Plans

Assign responsible teams or individuals to implement the action plans and establish timelines for completion.  Plans of record should be linked to the FMEA in this section.

## Date of Analysis

May 2024

**Note:** This analysis must be reviewed and updated annually.  It is recommended that you review and update the FMEA to account for changes in technology, regulations, and customer needs.
