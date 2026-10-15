# Wazuh home lab: log analysis and threat detection

A security monitoring lab I built from scratch to practice what a security operations (SOC) analyst does day to day: collecting logs from multiple systems, detecting attacks, and checking that the detections work.

## What the project does

The lab collects logs and file-integrity events from a Linux server and a Windows machine into a central SIEM platform. It runs simulated attacks against those systems and checks that the custom detections raise the right alerts. Detections are mapped to MITRE ATT&CK techniques, so each alert can be traced back to a known attacker behavior. Alerts are also forwarded to a chat channel, and the same logs are analyzed in a second SIEM for comparison.

## Why it was challenging

Building this meant working across several layers at once: a containerized SIEM stack, Linux and Windows endpoint agents, kernel-level endpoint telemetry, detection logic written in the SIEM's rule language, and attack simulations to prove each detection works. Each layer has its own configuration and failure modes, so debugging often meant following logs across multiple machines. I also automated the multi-machine setup so the whole environment can be rebuilt from scratch.

## What it shows

- Log analysis and threat detection across Linux and Windows
- Detection engineering, including mapping detections to MITRE ATT&CK
- Testing detections with simulated attacks rather than assuming they work
- Infrastructure automation with reproducible, rebuildable environments
- Comparing SIEM platforms and the trade-offs between them

## Access

The code, configuration, detection content, and documentation are private. If you'd like to discuss the project or see more, get in touch.
