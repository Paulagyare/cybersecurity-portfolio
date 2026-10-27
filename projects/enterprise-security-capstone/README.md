# Enterprise Security Capstone: Network Defense and SOC Monitoring

## Overview

Over a 13-week capstone, I built and secured an enterprise network in four phases. The project brought together network segmentation, identity-based access, monitoring, and automated incident response.

## Objective

Create a segmented network that protects internal resources, makes services available through a DMZ, and gives a security operations team visibility into suspicious activity.

## Architecture and segmentation

I designed five network zones: outside, DMZ, inside, secure, and an interconnect between firewall tiers. I used private IPv4 addressing and VLANs to separate traffic. A Palo Alto firewall protected the internet-facing edge, while a FortiGate firewall provided another layer of control. I configured routing, NAT/PAT, and policies to manage traffic between zones.

## Secure access and infrastructure

I placed two web servers in the DMZ and configured load balancing and failover. I restricted Active Directory exposure and implemented access controls using SSL/TLS VPN, 802.1X, Duo MFA integrated with Active Directory, and a Guacamole gateway for browser-based access.

## Monitoring and detection

I deployed Security Onion to monitor DMZ traffic and wrote custom Suricata rules to detect an obfuscated string and outbound SYN requests from web servers. I used Zeek for network metadata and collected Sysmon endpoint telemetry using Elastic Agent.

I also deployed Splunk and brought together firewall syslog, IIS logs, and Security Onion alerts. I built dashboards and detections for brute-force attempts, scanning, suspicious URLs, and beaconing behavior.

## Automated response and validation

I built an n8n workflow, assisted by Claude Code, that takes a Splunk alert, extracts a source IP address, enriches it with GeoIP and threat intelligence, and can push a block to the Palo Alto firewall through its API.

I tested the environment with simulated scanning and web attacks against the DMZ. The detections fired and the automated workflow responded.

## Tools and skills

- **Network security:** Palo Alto, FortiGate, VLANs, routing, NAT/PAT, DMZ design
- **Identity and access:** Active Directory, Duo MFA, 802.1X, SSL/TLS VPN, Guacamole
- **Monitoring and detection:** Security Onion, Suricata, Zeek, Sysmon, Elastic Agent, Splunk
- **Response:** n8n, threat intelligence enrichment, Palo Alto API

## Project context

This write-up summarizes the capstone as described on [my portfolio website](https://paulagyare.github.io/web_page/). It is a project summary; configurations, screenshots, and detailed test evidence can be added as they become available.
