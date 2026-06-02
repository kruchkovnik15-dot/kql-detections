# PowerShell Encoded Execution Detection Case Study

## Overview

This case study documents the detection and investigation of suspicious PowerShell execution using encoded command arguments.

Encoded PowerShell remains one of the most common execution techniques observed across malware delivery, post-exploitation frameworks, offensive security tooling, and adversary tradecraft.

## Detection Objective

Detect PowerShell executions that combine encoded command arguments with execution-evasion flags frequently associated with malicious activity.

## Data Sources

* Microsoft Defender for Endpoint
* DeviceProcessEvents
* Process Creation Telemetry
* Command Line Logging

## ATT&CK Mapping

| Technique | Description                     |
| --------- | ------------------------------- |
| T1059.001 | PowerShell                      |
| T1027     | Obfuscated Files or Information |

## Detection Logic

The detection identifies PowerShell processes containing encoded command arguments such as:

* -enc
* -encodedcommand

Combined with suspicious execution flags:

* -nop
* -w hidden
* -executionpolicy bypass
* -noninteractive

The combination of encoded payload delivery and execution-evasion parameters significantly increases detection fidelity compared to monitoring encoded commands alone.

## Example Activity

```powershell
powershell.exe -nop -w hidden -enc SQBFAFgA...
```

## Investigation Guidance

Analysts should review:

1. Parent process lineage.
2. Full command line arguments.
3. User context.
4. Network activity following execution.
5. Persistence artifacts.
6. Additional PowerShell executions on the host.

## Potential False Positives

* Administrative automation frameworks
* Enterprise software deployment tooling
* Security testing activities
* Internal IT scripting

## Detection Limitations

The detection does not identify:

* PowerShell payloads executed without encoded arguments
* AMSI bypass activity
* PowerShell execution through alternate hosts

Additional analytics should be deployed to improve coverage.

## Detection Outcome

Priority: High

The detection is intended to identify potentially malicious PowerShell execution requiring analyst triage and validation.
