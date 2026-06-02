# KQL Detections

Microsoft Sentinel detection and hunting queries focused on threat detection, adversary tradecraft, and ATT&CK-aligned analytics.

## Purpose

This repository contains KQL detections developed for:

* Threat Detection
* Threat Hunting
* Detection Engineering
* Security Operations
* ATT&CK Coverage Mapping

The goal is to provide high-fidelity analytics suitable for Microsoft Sentinel environments.

---

## Detection Coverage

| Detection                  | ATT&CK Technique |
| -------------------------- | ---------------- |
| LSASS Memory Access        | T1003.001        |
| Defender Tampering         | T1562.001        |
| Office Spawn PowerShell    | T1204            |
| Certutil Payload Retrieval | T1105            |
| Regsvr32 Squiblydoo        | T1218.010        |

---

## Technologies

* Microsoft Sentinel
* Kusto Query Language (KQL)
* Sysmon
* Windows Event Logs
* MITRE ATT&CK

---

## Repository Structure

```text
detections/
hunts/
investigations/
```

---

## Disclaimer

These detections are created for research, lab validation, and portfolio purposes.
